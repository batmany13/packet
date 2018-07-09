### General Terms

[ipxe](https://ipxe.org/) - iPXE is the leading open source network boot firmware
[ocp](https://www.opencompute.org/) - The Open Compute Project (OCP) is reimagining hardware, making it more efficient, flexible, and scalable. Join our global community of technology leaders working together to break open the black box of proprietary IT infrastructure to achieve greater choice, customization, and cost savings.
[Sledgehammer](http://provision.readthedocs.io/en/tip/doc/arch/sledgehammer.html) [repo](https://github.com/digitalrebar/sledgehammer) - Digital Rebar's system discovery/inventory/configuration in-memory OS image
[BGP](https://en.wikipedia.org/wiki/Border_Gateway_Protocol) - Border Gateway Protocol,  is a standardized exterior gateway protocol designed to exchange routing and reachability information among autonomous systems (AS) on the Internet

## Packet Micro-services (provisioning)

[Blog](https://www.packet.net/blog/our-journey-to-zero-failed-installs/)

PBNJ - Reboots machines, sets boot order, and performs BMC/BIOS related tasks.
Tinkerbell - Handles DHCP requests, hands out IPs, serves up iPXE.
OSIE - Installs all of our operating systems and handles deprovisioning.
Narwhal - Configures all switches with proper ACLs, DHCP groups, BGP, Layer 2/3.
Pensieve - Sets up reverse DNS for all instances.
Soren - Bandwidth billing.
Doorman - Provides VPN to customers.
Kant - Our EC2-style metadata service.
SOS - Provides out-of-band access to instances, if public connectivity is down.
Magnum IP - Acts as our authoritative IPAM, hands out IP reservations and assignments.
PacketBot - Our version of chaos monkey, which provisions all OSes, in all facilities, all day, every day. 

### RackN

https://www.packet.net/developers/guides/ditch-cobbler-for-rackn/
https://github.com/digitalrebar/provision
https://www.rackn.com/

Digital Rebar How To

[Part 1](https://www.rackn.com/2018/03/14/deploy-and-test-digital-rebar-provision-in-less-than-10-minutes-how-to-guide/)
[Part 2](https://www.rackn.com/2018/03/21/rackn-portal-management-connection-to-the-10-minute-demo/)
[Part 3](https://www.rackn.com/2018/04/05/create-your-first-centos-7-machine-on-rackn-portal-with-digital-rebar-provision/)

[Slack Channel](http://www.rackn.com/support/slack/)

### OpenStack

Packet Blog about [how we failed at openstack](https://www.packet.net/blog/how-we-failed-at-openstack/)

[OpenStack](http://www.openstack.org/) - innovations in infrastructure plumbing as building blocks for our services: network automation, IP management, installation routines, hardware lifecycle, and (of course!) installations.
[Ironic](https://github.com/openstack/ironic) - OpenStack for managing and provisioning bare metal servers, [RackSpace's blog](https://developer.rackspace.com/blog/how-we-run-ironic-and-you-can-too/)
[Neutron](https://docs.openstack.org/neutron/pike/) - network connectivity as a service
[Nova](https://docs.openstack.org/nova/latest/) - Provision compute instances
IPAM - IP address manager 


Interesting comment from poster

Raja Srinivasan • 3 years ago
This is fascinating. I was a big proponent of OpenStack but over the years, the glimmer is going out. OpenStack is still pre-mature for industrial strength deployments -- industrial strengths means easy to deploy, scale, manage, and upgrade. It appears that every deployment is a custom deployment that is purpose built and is not easily replica-table, kind of a Franken-stack. Your blog confirms what I had always suspected to be the truth around OpenStack. It has a lot of momentum and it will take some time to get right. By taking on Amazon and VMs they are ignoring the vast majority of the managed service providers who are asking for a "Software-Defined-Data-Center" that works with individual servers.