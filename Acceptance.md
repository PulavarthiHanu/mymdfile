```text
SPDX-License-Identifier: Apache-2.0
Copyright © 2020 Intel Corporation
```
[ITP/NED/01/01: Acceptance Test ](#itpned35-Acceptance-Test)
ITP/NED/01/01: Deploy application in a multi node cluster with nodeSelector specified to feature one of edge node
Resource being detected for Pod deployment:](#itpned2500-opc-package-installation)
 -[Test Summary](#test-summary)
  - [Prerequisites](#prerequisites)
  - [Test Steps](#test-steps)
  -
 - ITP/NED/01/01: Deploy K8s Master Using Converged Edge Experience Kits
 - TP/NED/01/02: Deploy K8s Worker Using Converged Edge Experience Kits
 - [Test Summary](#test-summary)
  - [Prerequisites](#prerequisites)
  - [Test Steps](#test-steps)
 - Deploy 1 controller and 2 node cluster with node selector specified to feature one if edge node
 - ITP/NED/05/01: Deploy application on existing node
   
[ITP/NED/05/08: Acceptance Test ](#itpned35-Acceptance-Test)
   
[NF/STB/06: Acceptance Test ](#itpned35-Acceptance-Test)
Verify performance benchmark of CNIs with SR-IOV interface using 
Iperf network utility 
RFC2544 benchmark test for throughput and latency is executed 
NF/STB/06 : Verify that traffic flow across pod with SR-IOV VF interface and external host doesn’t interrupt on force reboot of controller 
NF/STB/06:  Perform a soak run on Network Edge K8s cluster with traffic for 48hrs( need to add for perform  reboot controller )

[NF/STB/06: Acceptance Test ](#itpned35-Acceptance-Test)
Verify the throughput and latency of network pod by deploying it on same NUMA node where Intel® SR-IOV network card and CPU memory is allocated
ITP/NED/05/08: NIC SRIOV with Multus

Verify performance benchmark of CNIs with two pods each having SR-IOV VF interface from same PF using 
Scalability with more than one pod using VFs from same PF 
perf network utility 
RFC2544 benchmark test for throughput and latency 
Deploy minimal with 2 host while deploying add sriov VF interfaces from the same Pf's 
Bring up 2 pods each having the SRIOV interface with the different PF
Start iperf server from one pod and client from other pod verify the traffic 

[ITP/NED/05/13: Acceptance Test ](#itpned35-Acceptance-Test)
ITP/NED/05/13 : Verify create and delete of multi interface pod for specified cycles 
ITP/NED/05/13:  Deploy pod with multiple interfaces , repeat the test case for 10 times




