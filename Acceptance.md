```text
SPDX-License-Identifier: Apache-2.0
Copyright © 2020 Intel Corporation
```
[ITP/NED/01/01: Acceptance Test ](#itpned35-Acceptance-Test)
ITP/NED/01/01: Deploy application in a multi node cluster with nodeSelector specified to feature one of edge node
Resource being detected for Pod deployment:](#itpned2500-Acceptance-installation)
 -[Test Summary](#test-summary)
  -[Prerequisites](#prerequisites)
  -[Test Steps](#test-steps)
  -
 - ITP/NED/01/01: Deploy K8s Master Using Converged Edge Experience Kits
 - TP/NED/01/02: Deploy K8s Worker Using Converged Edge Experience Kits
  [Test Summary](#test-summary)
  - [Prerequisites](#prerequisites)
  - [Test Steps](#test-steps)
 - Deploy 1 controller and 2 node cluster with node selector specified to feature one if edge node
 - ITP/NED/05/01: Deploy application on existing node
   
[ITP/NED/05/08: Acceptance Test ](#itpned35-Acceptance-Test)
   
[NF/STB/06: Acceptance Test ](#itpned35-Acceptance-Test)
Verify performance benchmark of CNIs with SR-IOV interface using 
[Test Summary](#test-summary)
 - [Prerequisites](#prerequisites)
 - [Test Steps](#test-steps)
Iperf network utility 
RFC2544 benchmark test for throughput and latency is executed 
NF/STB/06 : Verify that traffic flow across pod with SR-IOV VF interface and external host doesn’t interrupt on force reboot of controller 
NF/STB/06:  Perform a soak run on Network Edge K8s cluster with traffic for 48hrs( need to add for perform  reboot controller )

[NF/STB/06: Acceptance Test ](#itpned35-Acceptance-Test)
[Test Summary](#test-summary)
  - [Prerequisites](#prerequisites)
  - [Test Steps](#test-steps)
-Verify the throughput and latency of network pod by deploying it on same NUMA node where Intel® SR-IOV network card and CPU memory is allocated
-ITP/NED/05/08: NIC SRIOV with Multus

[ITP/NED/35: Acceptance Test](#itpned35-Acceptance-Test)
-Verify performance benchmark of CNIs with two pods each having SR-IOV VF interface from same PF using 
-Scalability with more than one pod using VFs from same PF 
-perf network utility 
-RFC2544 benchmark test for throughput and latency 
-Deploy minimal with 2 host while deploying add sriov VF interfaces from the same Pf's 
-Bring up 2 pods each having the SRIOV interface with the different PF
-Start iperf server from one pod and client from other pod verify the traffic 

[ITP/NED/05/13: Acceptance Test ](#itpned35-Acceptance-Test)
-[Test Summary](#test-summary)
 - [Prerequisites](#prerequisites)
 - [Test Steps](#test-steps)
-ITP/NED/05/13 : Verify create and delete of multi interface pod for specified cycles 
-Deploy pod with multiple interfaces , repeat the test case for 10 times

[ITP/NED/35: Acceptance Test](#itpned35-Acceptance-Test)
Verify deployment of multiple pods (atleast 3) with multi-interfaces each from different CNI 
ITP/NED/35 : Verify deployment of multiple pods (atleast 3) with multi-interfaces each from different CNI 
[Test Summary](#test-summary)
 - [Prerequisites](#prerequisites)
 - [Test Steps](#test-steps)
 - Deploy 2 host cluster with multiple cni's where calico as main ,flannel and sriov are secondary 
kubernetes_cnis:
- calico
- flannel
- sriov

- Add some node’s SR-IOV capable network interfaces to the node config file 
sriov:
  network_interfaces: {ens787f0: 3}
- Deploy 3 pods with 3 interfaces from each cni (calico,flannel,sriov) (ITP/NED/06/02: SR-IOV VF attachment verification)
- allowed all the ingress 
- for pod A flannel interface to pod B flannel interface 
- Now sent traffic by using iperf from pod A sriov interface to pod B  sriov  interface 

[ITP/NED/35: Acceptance Test](#itpned35-Acceptance-Test)
Verify deployment of pod with 3 Interfaces –  
-Default,  
-	SR-IOV1  to use Net/kernel Interface and 
-	SR-IOV 2 to use DPDK. 
-	Test Steps

 -Deploy minimal deployment with 2 host cluster 
 - Add some node’s SR-IOV capable network interfaces to the node config file 
sriov:
  -network_interfaces: {ens787f0: 3}
   -On the node bind the SRIOV VF port to dpdk vfio driver.
   -Bind the SRIOV VF interface created during the deploy
  -[root@node01]# /opt/openness/dpdk-19.11.1/usertools/dpdk-devbind.py -b vfio-pci af:0a.0 af:0a.1
   -verify interfaces are binded properly 
  
  output looks like
  - Network devices using DPDK-compatible driver
   ============================================
   -0000:af:0a.0 'Ethernet Virtual Function 700 Series 154c' drv=vfio-pci unused=i40evf,igb_uio
   -0000:af:0a.1 'Ethernet Virtual Function 700 Series 154c' drv=vfio-pci unused=i40evf,igb_uio
   -6) Restarting the sriov-device-plugin Pod on Edge Node(s)
   -Perform the following steps on controller node to enable the intel_sriov_dpdk network interface needed for the VPP.




