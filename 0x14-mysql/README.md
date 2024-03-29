What is a database?

A database is information that is set up for easy access, management and updating. Computer databases typically store aggregations of data records or files that contain information, such as sales transactions, customer data, financials and product information.

Databases are used for storing, maintaining and accessing any sort of data. They collect information on people, places or things. That information is gathered in one place so that it can be observed and analyzed. Databases can be thought of as an organized collection of information.
What are databases used for?

Businesses use data stored in databases to make informed business decisions. Some of the ways organizations use databases include the following:

    Improve business processes. Companies collect data about business processes, such sales, order processing and customer service. They analyze that data to improve these processes, expand their business and grow revenue.
    Keep track of customers. Databases often store information about people, such as customers or users. For example, social media platforms use databases to store user information, such as names, email addresses and user behavior. The data is used to recommend content to users and improve the user experience.
    Secure personal health information. Healthcare providers use databases to securely store personal health data to inform and improve patient care.
    Store personal data. Databases can also be used to store personal information. For example, personal cloud storage is available for individual users to store media, such as photos, in a managed cloud.

This article will explore the idea of redundancy. Redundant data is not a backup, but can give you a failover in case your primary method of accessing data becomes unavailable.

How you choose to implement replication on your system mostly depends on how you are using your data, what failures you would like to guard against, and what how your visitors are interacting with your server instances.
RAID Redundancy

Perhaps the most common type of replication is RAID. RAID stands for redundant array of independent disks. This means that in most configurations, disks mirror each other in one way or another.

The most basic redundant RAID implementation is a RAID 1 array. This type of array mirrors one disk on another disk. This means that if one disk fails, the other is still available to serve and write data. This type of array speeds up reads due to the fact that the system can read from either of the data locations.

This example is also a great example of why RAID, and redundant setups in general, are not appropriate backups. If you delete a file, it is gone for good. Every change is applied to both disks immediately.

RAID replication is implemented on a low level, so you will not have control over the RAID implementation on a DigitalOcean VPS.
Block-Level Redundancy

Another method of providing redundancy is to mirror entire block structures. DRBD, or distributed replicated block device, is a way to achieve redundancy across block devices.

This might seem similar to a mirrored RAID array, and in some ways, it is. The difference lies in where the replication takes place. With RAID, the redundancy takes place below the application level. The RAID card or RAID software manages the physical storage devices and presents the application with a single apparent device.

DRBD, on the other hand, is configured in a completely different way. In a DRBD set up, each hardware stack is completely mirrored. The application interface is also mirrored. This means that an application failure can be dealt with because there is a completely separate machine with a copy of the data to work with. If your first server has a power supply failure, the second server will still operate effectively.
SQL Replication

If your important data is stored in an SQL database (MySQL, MariaDB, PostgreSQL, etc.), you can take advantage of some built-in replication features. These can be used to provide a failover system in case the main server goes down.
Master-Slave Replication

The most basic kind of SQL replication is a Master-Slave configuration. In this scenario, you have a main database server, which is referred to as the “master” server. This server is responsible for performing all writes and updates. The data from this server is copied continuously to a “slave” server. This server can be be read from, but not written to.

This setup allows you to distribute the reads across multiple machines, which can dramatically improve your application’s performance.

While this performance increase is an advantage, one of the main reasons you may set up master-slave replication is for handling failover. If your master server becomes unavailable, you can still read from your slave server. Furthermore, it is possible to convert the slave into a master server in the event that your master is offline for an extended period of time.

Master-slave replication is, in fact, one area where we begin to see how redundancy and backups can complement each other. In a master-slave configuration, you can replicate data from the master to the slave. You can then temporarily disable replication to maintain a consistent state of information on the slave. From here, you can back up the database using whatever backup mechanism is appropriate.

To learn more about how to configure MySQL master-slave replication, click here. To learn about how to accomplish master-slave replication with PostgreSQL, follow this link.
Master-Master Replication

A second form of replication is called Master-Master replication. This configuration allows both servers to have “master” abilities. This means that each server can accept writes and updates and will transfer the changes to the opposite server. This configuration inherits the advantages of the master-slave setup, but also benefits from increased write performance if the writes are properly distributed by a load balancing mechanism.

This also means that, in the event that one server goes down, the other is still up and ready to accept requests. While the configuration is more complicated, the failover in the event of a problem is less complicated than the master-slave redundancy, because the slave database does not need to transform into the master.

This configuration can also be combined with a backup mechanism if you take one of the master servers offline. You must maintain a static database for backups to function correctly, so you have to ensure that no data is being modified or written to until after the backup is complete.

For more information about how to configure master-master replication, click here.
Distribution as a Redundancy Alternative

Distributed systems offer many of the advantages of traditional redundant setups.

You already looked at mirrored RAID levels above (RAID 1). Another common RAID level is RAID 5. This RAID distributes data across a number of drives and also writes the parity of the data across each drive. This means that any kind of transaction can be “rebuilt” from combining the parity information on the other drives if a single drive dies.

This provides a different way of distributing data across disks, and can handle a single disk failure as well.

Distributed systems do not have to be hardware based. There are also quite a few databases and other software solutions designed with distributed data as a key feature.

An example of this is Riak, a distributed database. Riak nodes are all the same. There is no master-slave relationship between the different pieces. Objects stored in the database are replicated, so there is traditional redundancy in that respect.

However, each node does not each hold the entire database. Instead the data is distributed among the nodes in an even manner. The objects that are replicated are placed on different nodes to allow for availability in case of hardware failures.

Another great example of this concept implemented in a database is Cassandra. It is based on the same principles as Riak, but is implemented in a different way.
Conclusion

As you can see, there are many options for redundancy, each with their advantages and faults. It mainly depends on what problems you are trying to anticipate and which parts of your system you consider a failure unacceptable. As you can imagine, a combination of some of these techniques will always yield a more comprehensive safety net.

You should also be able to see by this point that redundant setups are not a substitute for backups. The need for redundant systems to be always operational and always mirroring changes can easily allow data to be destroyed from all points of your configuration.

For applications where data integrity and access are essential, both redundancy and backups are invaluable. Proper implementation will ensure that your product is always available to your users and that important data will never be lost.
