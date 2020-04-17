# Enable Supervisor Cluster

![](../../././images/enablesupervisor.png)

Menu > Workload Management > Enable

![](../.././images/enable.png)

![](../.././images/enable2.png)

![](../.././images/enable3.png)

``Below configurations should be according to your enviornment``

``Network: Management Network``

``Subnet Mask: 255.255.255.0``

``Starting IP: 10.###.###.45``

``Gateway: 10.###.###.1``

``DNS Server: 10.192.2.10``

``NTP: 10.192.2.5``

``DNS Search Domain: pplab.io``

``vSphere Distributed Switch: choose default (UUID)``

``Edge Cluster: Edge-Cluster-01``

``Ingress CIDR: 10.###.###.64/26``

``Egress CIDR: 10.###.###.128/26``


![](../.././images/enable4.png)

![](../.././images/enable5.png)

![](../.././images/enable6.png)

![](../.././images/enable7.png)

THIS STEP TAKES ABOUT 20-30min. IT DOES FAIL AT TIMES AND YOU MAY NEED TO REMOVE WORKLOAD MANAGEMENT, AND DO THIS STEP OVER.
