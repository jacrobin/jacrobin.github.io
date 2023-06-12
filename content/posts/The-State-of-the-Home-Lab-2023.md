---
title: "The State of the Home Lab 2023"
date: 2023-06-12T13:28:50-07:00
draft: false
---

# Upgrading My Workflow

For those who don't know me, I love tinkering with hardware and software. I am also the type of person who will do something a hundred times before deciding on the best strategy for dealing with a given problem. I only just finished my undergraduate studies for cybersecurity, so for the last year or so my home lab was the last thing I was allocating time to. However, with all my new found free-time, I wanted something to work on in the midst of frantically applying for jobs. First, though I wanted a platform in place before working on projects, hence Home Lab 3.0.

![a](/images/TOPO.svg#center)

Before talking about what I added, or what I want to add, for all the gear heads out there here is a breakdown of what drives my home lab.

# Hardware

### NAS (aka Mr.NAS) 

- Made up of remnants of my first gaming PC, this server acts as my personal NAS (but more like DAS). While in the middle of being decommissioned it still serves as a suitable space to store photos, ISOs, and my music collection. Making my distro hopping less of a nightmare.
- Technical Specifications
	- Asus M5A99X EVO R2.0 Desktop Motherboard
	- AMD FX- 6350
	- 16 GB of Corsair 3000hz Memory
	- 2 x 4 TB Ironwolf 3.5" HDDs
	- ~~1 x 2 TB Western Digital Blue 3.5" HDD~~
	- Random HP network card from eBay

### Hypervisor (aka Mrs.Server)

- One big issue with the NAS was just the amount of resources. Because of the required amount of resources for TruNAS, I had little headroom. I knew too that I ultimately wanted a server that could run Proxmox. This server was my first big home lab purchase. When I had my internship I had a large amount of disposable income and I wanted to invest in my home lab in a way that could not only allow me to expand my skills but also make my life easier. At first, I wanted to do a rack setup not only because of the coolness factor but also because some of my other gear is rack mountable. But given the associated costs, and more importantly noise, of a rack set up I decided against it. After some deliberation, I decided to pick up a "refurbished" Dell T7000:
-  Technical Specifications:
	- 2 x Xeon 16-Core 2.70GHz E5-2680
	- 64 GB of EEC Memory
	- No label 1 TB HDD
	- 2 x 1 TB ADATA SU750 2.5" SSDs

- I think this machine was originally designed for graphical, modeling, or video editing work. However, the parts and design make it not only compact and quiet, but the drives and power supply are hot-swappable. Much of the hardware and design seems to mirror Dell's rack mount series too, making parts easily obtainable.  

### Networking Gear

- Dell Optiplex 3020 (Upgraded to a i5-4590s)
- TP-Link TL-SG1024S
- NETGEAR AP WAX610

# Software

### NAS (aka Mr.NAS) 
- The host OS is TruNAS scale. At the time I was just getting into the home lab community and it seemed like the best option given the needs I had, which was mainly storage. However, the fact it could run VMs was a bonus. But I always had Raspberry Pis floating around so any VM work on it was limited.

### Hypervisor (aka Mrs.Server)
- As mentioned previously this machine was always intended to run Proxmox. Currently, there are a handful of VMs that run 24/7.
	- A Ubuntu server instance running Pi-Hole
	- A Ubuntu server instance running Docker
		- Currently, it is only running my private GitLab instance
	- A Fedora server instance, which acts almost as a bastion host to code when I am working from my Windows machine.
	- A TruNAS instance, which is meant to eventually fully replace the NAS machine.
- There are some other VMs such as an instance of Parrot OS, a popular distro for cyber security operations.

### Router: Dell Optiplex 3020
- For my router, I just run OPNsense. While I have explored the plugin market for it, I have yet to use any of them.

# Whats New?

- The newest addition was the TruNAS instance and GitLab on the server. So far a personal GitLab has been great and exactly what I was looking for. I have three machines that I work on. So having a single place to store my code that I have control over is perfect. 

# Whats Next?
- I still want to do a rack setup eventually. While my current server has plenty of headroom, I would still like the free space in my room back. Though the single desktop layout will have to do for now. I also found some options for expanding storage on the server machine, and any expansions should be able to be easily relocated to a server setup. 
- The next big thing is personal development with CI/CD and DevOps. 
	- My formal education did not address much of anything regarding DevOps. Additionally, my previous internship was not an engineering-focused one, and I only started to start learning the systems in place when my time was up, and none of the interns were hired (they hired George Clooney to talk at their key note instead.)
	- Also a wanted addition is making a script that can automatically sync my GitLab with my GitHub. I'm still debating on the process I want for this, but it should be easy to implement regardless.
- VPN access is a big want. It should be painless to implement and is going to be one of the top priorities on my list of things to do once I get a job that requires me to move around a lot. However, with my current arrangement, it's just not mission-critical right now.
- A place to work on static and dynamic malware analysis is also going to be a big want in the future. However, because of some hardware I have laying around I might make a separate network for this that has no relation to the home lab.
