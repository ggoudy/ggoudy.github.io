---
layout: post
title: Microsegmentation... What is it and where you can get started!
---

#### Adversaries must be asking themselves what's up with all these walls!

One of the latest trends in network security that everyone is talking about (or at the very least should be) is Microsegmentation. Now for those unfamiliar you might be asking yourself, just what is Microsegmentation and why should I care? Well let's take a look shall we.

Microsegmentation is a big part of the Zero Trust Architecture (ZTA) paradigm. With cloud and hybrid computing models, the need for a security everywhere approach has become more relevant. Microsegmentaton is a security approach that allows administrators to create policies which define zones. These zones are then applied to workloads to isolate them from one another. To break it down further let's take a look at an example:

APPSRV1, APPSRV2 and APPSRV3 are all on the same VLAN. APPSRV1 and APPSRV2 are in a cluster and therefore by default these devices should be able to communicate with each other. APPSRV3 is for a completely different project, but it's on the same VLAN, so unless the administrator(s) of APPSRV3 configured firewall rules allowing and disallowing traffic from certain hosts, then APPSRV1 and APPSRV2 can communicate with APPSRV3 and vice versa. These systems are susceptible to what security professionals call lateral movement which is a method attackers will use to make their way around your network. 

Here's where Microsegmentation comes in. Using your Microsegmentation product of choice, you apply a policy to APPSRV1 and APPSRV2, while applying a seperate policy to APPSRV3. These policies limit network traffic to and from the servers and this all happens from a centralized location. The policy set on APPSRV3 could disallow network traffic to and from APPSRV1 and APPSRV2 even though all three machines are on the same VLAN. This has the benefit of scaling very well since it's policy driven. Another benefit of this is that because workloads can be anywhere (cloud or on-premise) these policies will follow that server anywhere it goes thanks to the integration features most (if not all) Microsegmentation products have with cloud providers.

If you're looking to get started, there are multiple vendors available like:
* [VMware NSX](https://www.vmware.com/products/nsx.html)
* [Cisco Secure Workload](https://www.cisco.com/c/en/us/products/security/tetration/index.html)
* [Palo Alto Networks Virtual NGFW](https://www.paloaltonetworks.com/prisma/vm-series)
