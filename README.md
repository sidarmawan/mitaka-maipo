# mitaka-trusty

This repo contains commands and configurations for manually install services of OpenStack Mitaka by using packages on RHEL/CentOS 7 through the RDO repository. The services in this installation include Keystone Identity, Glance Image, Nova Compute, Neutron Networking, Horizon Dashboard, Heat Orchestration, Ceilometer Telemetry, Cinder Block Storage and Swift Object Storage. The architecture in this installation intended to assist new users of OpenStack to understand basic installation, configuration and operation of OpenStack core services. The architecture is not recommended for production environment. The architecture is using 5 VirtualBox nodes for controller, compute, block, object1 and object2.

__Main Reference:__
- OpenStack Installation Guide for Red Hat Enterprise Linux and CentOS Through the RDO Repository (http://docs.openstack.org/mitaka/install-guide-rdo/)

__Minimum requirements:__
- Desktop/laptop with 2 cores 64bit processor and 8 GB RAM.
- 5 VirtualBox guests of RHEL/CentOS 7 minimal installation. Node controller: 2 core CPU, 4 GB RAM, 20 GB HDD. Node compute: 2 core CPU, 2 GB RAM, 20 GB HDD. Node block/object0/object1: 1 core CPU, 512 MB RAM, 3 x 10 GB HDD.

__Topology:__
![alt tag](https://github.com/utianayuba/mitaka-maipo/raw/master/topology/topology.png)

__Installation:__

1. Create new virtual RHEL/CentOS 7 minimal installation. No network adapter, disable firewall and enable SSH service.
2. Clone the virtual into 5 nodes. Add network adapter(s) to each of node and arrange the topology as shown above.
3. Copy directory of node commands and configurations to each node into /root directory.
4. SSH to each node as root and change the shell working directory to the node config directory.
5. Copy commands from trusty_*_commands.txt file and paste it into the SSH terminal of each node. Do the copy and paste command(s) per line or per section so you can see the command(s) executed successfully or not.
