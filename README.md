# Apache Cloudstack (Zone Creation)
This particular repository consists of creation of zones, pods, cluster, primary &amp; secondary storage after successful installation of Apache Cloudstack.

Note : Perform these steps only after installing KVM in your system otherwise "Host" creation will not be done except adding Host all things will get add.

<h2>Steps for Zone Creation </h2>
-> Go to Infrastructure Tab after successfull installation of Apache Cloudstack

-> Go to Zones

<h2>Add Zone</h2>

<h4>Zone Type</h4>
-> Select Core as a type

<h4>Core zone type</h4>
-> Select Advanced as a Core zone type

<h4>Zone Details</h4>

-> Name : Zone-1

-> IPv4 DNS1 : 8.8.8.8

-> Internal DNS1 : 8.8.8.8

-> Hypervisor : KVM

<h4>Network</h4>
<h5>Physical Network</h5>

-> Network name : Physical Network-1

-> Isolation Method : VLAN

-> Traffic Types : Select Guest, Management, Public

<h5>Public Network</h5>

-> Gateway : 192.168.79.2 (for Linux cmd is - ip r)

-> Netmask : 255.255.255.0

-> VLAN/VNI : Keep it default

-> Start IP : 192.168.79.20 (If your IP Address is 192.168.45.131 then replace 20 with 131, you can make it as much as you can ) 

-> End IP : 192.168.79.50 (Same as Start IP)

<h5>Pod</h5>

-> Pod Name : Pod-1

-> Reserved System Gateway : Write your systems default gateway

-> Reserved System Netmask : 255.255.255.0

-> Start Reserved System IP : 192.168.79.51 (Initially End IP was 192.168.45.50, Now start with .51)

-> End Reserved System IP : 192.168.79.80 (Take as many you need)

<h5>Guest Traffic</h5>

-> VLAN/VNI range : 150 to 200 (Take as many you need)

<h4>Add Resources</h4>
<h5>Cluster</h5>

-> Cluster Name : Cluster-1

<h5>IP Address</h5>

-> Host Name : 192.168.79.131 (Your systems IP Address)

-> Username : anish (Your systems username)

-> Authentication Method : Select Password

-> Password : **** (Your systems password)

<h5>Primary Storage</h5>

-> Name : Primary-1

-> Protocal : nfs

-> Server : 192.168.79.131 (Your systems IP Address)

-> Path : /export/primary

-> Provider : DefaultPrimary

<h5></h5>

-> Provider : NFS

-> Name : Secondary-1

-> Server : 192.168.79.131 (Your systems IP Address)

-> Path : /export/secondary

<h4> Click On Launch Zone</h4>

