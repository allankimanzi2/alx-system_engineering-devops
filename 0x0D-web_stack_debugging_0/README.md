Docker, 
an open-source technology, isn't just the darling of Linux powers such as Red Hat and Canonical. Proprietary software companies such as Oracle and Microsoft have also embraced Docker. Today, almost all IT and cloud companies have adopted Docker. 

Why companies embrace Docker containers
So why does everyone love containers and Docker? James Bottomley, formerly Parallels' CTO of server virtualization and a leading Linux kernel developer, explained VM hypervisors, such as Hyper-V, KVM, and Xen, all are "based on emulating virtual hardware. That means they're fat in terms of system requirements."
Containers, however, use shared operating systems. This means they are much more efficient than hypervisors in system resource terms. Instead of virtualizing hardware, containers rest on top of a single Linux instance. This means you can "leave behind the useless 99.9 percent VM junk, leaving you with a small, neat capsule containing your application," said Bottomley.

Therefore, according to Bottomley, with a perfectly tuned container system, you can have as many as four-to-six times the number of server application instances as you can using Xen or KVM VMs on the same hardware.

Another reason why containers are popular is they lend themselves to Continuous Integration/Continuous Deployment (CI/CD). This a DevOps methodology designed to encourage developers to integrate their code into a shared repository early and often, and then to deploy the code quickly and efficiently. 
Docker enables developers to easily pack, ship, and run any application as a lightweight, portable, self-sufficient container, which can run virtually anywhere. As Bottomley told me, "Containers gives you instant application portability."

Containers do this by enabling developers to isolate code into a single container. This makes it easier to modify and update the program. It also lends itself, as Docker points out, for enterprises to break up big development projects among multiple smaller, Agile teams using Jenkins, an open-source CI/CD program, to automate the delivery of new software in containers.

Jay Lyman, senior analyst at 451 Research, added: "Enterprise organizations are seeking and sometimes struggling to make applications and workloads more portable and distributed in an effective, standardized, and repeatable way. Just as GitHub stimulated collaboration and innovation by making source code shareable, Docker Hub, Official Repos, and commercial support are helping enterprises answer this challenge by improving the way they package, deploy, and manage applications."

In addition, Docker containers are easy to deploy in a cloud. As Ben Lloyd Pearson wrote in Opensource.com: "Docker has been designed in a way that it can be incorporated into most DevOps applications, including Puppet, Chef, Vagrant, and Ansible, or it can be used on its own to manage development environments."
Specifically, for CI/CD Docker makes it possible to set up local development environments that are exactly like a live server; run multiple development environments from the same host with unique software, operating systems, and configurations; test projects on new or different servers; and allow anyone to work on the same project with the exact same settings, regardless of the local host environment. This enables developers to run the test suites, which are vital to CI/CD, to quickly see if a newly made change works properly.

By using CI/CD, according to a 2016 Puppet survey of 4,600 IT professionals, IT departments with a strong DevOps workflow deployed software 200 times more frequently than low-performing IT departments. Moreover, they recovered 24 times faster, and had three times lower rates of change failure. Simultaneously, these businesses are spending 50 percent less time overall addressing security issues, and 22 percent less time on unplanned work.

All this comes as no surprise that the most popular way to deliver applications via CI/CD are containers.

What's not to like? You get a lot more application bang for your server buck and you improve and deploy your software quicker than ever before. So, why hasn't anyone done it before? Well, actually they have. Containers are an old idea
Docker, however, is built on top of LXC. Like with any container technology, as far as the program is concerned, it has its own file system, storage, CPU, RAM, and so on. The key difference between containers and VMs is while the hypervisor abstracts an entire device, containers just abstract the operating system kernel.

This, in turn, means one thing VM hypervisors can do that containers can't is to use different operating systems or kernels. So, for example, you can use Microsoft Azure to run both instances of Windows Server 2012 and SUSE Linux Enterprise Server, at the same time. With Docker, all containers must use the same operating system and kernel.

On the other hand, if all you want to do is get the most server application instances running on the least amount of hardware, you couldn't care less about running multiple operating system VMs. If multiple copies of the same application are what you want, then you'll love containers.
This move can save a data center or cloud provider tens of millions of dollars annually in power and hardware costs. It's no wonder they're rushing to adopt Docker as fast as possible.

Container standardization

Docker brings several new things to the table that the earlier technologies didn't. The first is it's made containers easier and safer to deploy and use than previous approaches. In addition, because Docker's partnering with the other container powers, including Canonical, Google, Red Hat, and Parallels, on its key open-source component libcontainer, it's brought much-needed standardization to containers.

Since then Docker donated "its software container format and its runtime, as well as the associated specifications," to The Linux Foundation's Open Container Project. Specifically, "Docker has taken the entire contents of the libcontainer project, including nsinit, and all modifications needed to make it run independently of Docker, and donated it to this effort."

Docker has continued to work on other container standardization efforts. For example, Docker's containerd, the container open-source runtime, is now hosted by the Cloud Native Computing Foundation (CNCF).

So, today Docker doesn't have any rivals per se. True, there are other LXC-based container implementations as CoreOS, now Red Hat's, Rkt, or Canonical's LXD, but they aren't so much competitors as they are LXC refinements. That said, you can run Docker containers on essentially any operating system or cloud. This gives it an advantage over the others.

In the level above containers, container orchestration, Docker does has a serious competitor: Kubernetes.

Container orchestration

Like any other element of your IT infrastructure, containers need to be monitored and controlled. Otherwise, you literally have no idea what's running on your servers.

You can use DevOps programs to deploy and monitor Docker containers but they're not optimized for containers. As DataDog, a cloud-monitoring company, points out in its report on real-world Docker adoption, "Containers' short lifetimes and increased density have significant implications for infrastructure monitoring. They represent an order-of-magnitude increase in the number of things that need to be individually monitored."

The answer is cloud orchestration tools. These monitor and manage container clustering and scheduling. In May 2017, there were three major cloud container orchestration programs: Docker Swarm, Kubernetes, and Mesosphere. Today, these are all still around, but Kubernetes is by far the most dominant cloud-orchestration program.

Indeed, in early October, Mesosphere jumped on the Kubernetes bandwagon. Docker announced it will integrate Kubernetes into the Docker platform. Users can choose to use Kubernetes and/or Docker Swarm for orchestration.

Why? As Adrian Chifor, senior DevOps engineer at English background checking company Onfido, blogged earlier this year, "Kubernetes has the largest community and is the most popular by a big margin."

Docker knew this was coming. Hykes said at DockerCon EU in Copenhagen that the company added Kubernetes to its offerings because it gave "our users and customers the ability to make an orchestration choice with the added security, management, and end-to-end Docker experience that they've come to expect from Docker since the very beginning."

Still, while Kubernetes may be the container orchestration winner, the containers themselves remain largely Docker's design and run on containerd. Docker's technology will be with us for years to come.

Container conclusions

In a nutshell, here's what Docker can do for you: It can get more applications running on the same hardware than other technologies; it makes it easy for developers to quickly create ready-to-run containered applications; and it makes managing and deploying applications much easier. Put it all together and I can see why Docker rode the hype cycle as fast as I can recall ever seeing an enterprise technology go.

Moreover, for once the reality is living up to the hype. Frankly, I can't think of a single company of any size that's not at least looking into moving their server applications to containers in general and Docker in specific.

