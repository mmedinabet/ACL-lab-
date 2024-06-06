<h1> Inbound Access Control List Lab  </h1>

In this lab, we will explore the configuration and testing of Inbound Access Control Lists (ACLs) using Cisco's Packet Tracer 8.0.1. ACLs are a crucial component in network security, providing the ability to control traffic and restrict unauthorized access to network resources. The lab environment is pre-configured with basic connectivity allowing communication between all devices, including switches, routers, and computers. Our objective is to implement standard ACLs to manage and filter network traffic based on specific rules.
 
 Environment information for the Packet Tracer architecture: 

![Screenshot 2024-06-06 135641](https://github.com/mmedinabet/ACL-lab-/assets/142737434/79c1925a-358f-4b9b-999b-dd591f4276a9)


![Screenshot 2024-06-06 154849](https://github.com/mmedinabet/ACL-lab-/assets/142737434/17ec0288-6ec0-42a7-affe-087a36ef6de9)

Lab Environment Overview

The initial setup includes:

- Pre-configured switches, routers, and computers.
- Unrestricted communication among all devices (laptops, PCs, and servers).
- No passwords set on routers and switches to facilitate easy access for configuration. 

<h1>Test Initial Connectivity</h1>

Task 1: Verify Connectivity
1. Double-click each computer.
2. Open the Command Prompt.
3. Use the ping utility to check connectivity between:
   - Laptop and PC
   - Laptop and Server
   - PC and Server
   
![Screenshot 2024-06-06 135722](https://github.com/mmedinabet/ACL-lab-/assets/142737434/f334174c-b30a-47e7-93b2-18144dadaca8)

Test the Laptop connectivitity with both PC and server: 

<img width="296" alt="Screenshot 2024-06-06 140212" src="https://github.com/mmedinabet/ACL-lab-/assets/142737434/86c79658-31d7-4a4a-b624-1794283bf14c">

Test the PC connectivity with laptop and server:

![Screenshot 2024-06-06 140646](https://github.com/mmedinabet/ACL-lab-/assets/142737434/b3a85a95-b0a8-45d1-8f24-0a2a538a4fdc)

Lets test the server connectevity with both laptop and PC:

![Screenshot 2024-06-06 140959](https://github.com/mmedinabet/ACL-lab-/assets/142737434/bfdd217f-bafc-4464-a34e-f20bf160e88d)

TASK 2: Use the ping utility to check connectivity between each of the computers from each of the routers.

Test router 1 : 

![Screenshot 2024-06-06 142155](https://github.com/mmedinabet/ACL-lab-/assets/142737434/9f4414cf-f4a3-4caf-b1f0-8124318eff3d)

Test router 2: 

![Screenshot 2024-06-06 142440](https://github.com/mmedinabet/ACL-lab-/assets/142737434/4ebd0b1e-0c62-469c-b12d-aed7bf78c2f1)

<h1> Setup ACLs</h1>

1. Create a Standard ACL:
   - Deny Laptop1 from accessing Server1.
   - Apply the ACL on the Gigabit Ethernet 0/2 interface in the inbound direction.
   - Include the "permit any" statement to allow other traffic.

![Screenshot 2024-06-06 143435](https://github.com/mmedinabet/ACL-lab-/assets/142737434/5f36f0fc-a1b3-4321-b8ad-38aa6b7e36b7)


2. Test the ACL:
   - Use ping to test connectivity from Laptop1 to Server1 (ping should fail).
  
![Screenshot 2024-06-06 143654](https://github.com/mmedinabet/ACL-lab-/assets/142737434/8b3b3694-7a69-4d5f-b438-3d1615809855)

   - Use ping to test connectivity from PC1 to Server1 (ping should succeed).

![Screenshot 2024-06-06 144731](https://github.com/mmedinabet/ACL-lab-/assets/142737434/8453818d-8bf2-48ad-a1db-431ee6549ead)

   - Use ping to test connectivity from Server to both Laptop (ping should fail) and PC1 (ping should suceed) 
![Screenshot 2024-06-06 145047](https://github.com/mmedinabet/ACL-lab-/assets/142737434/62ee8152-f2d8-4deb-9dd2-c43bdf1c5499)

 
<h1> Modify ACLs </h1>

1. Adjust ACL Rules
   - Remove Existing ACL:Use the "no" command to remove the current ACL rule and the ip access-group on Gigabit Ethernet 0/2.
 
![Screenshot 2024-06-06 152105](https://github.com/mmedinabet/ACL-lab-/assets/142737434/b3aaf035-ca24-4dd6-abbc-fd0e0fedd7f0)

![Screenshot 2024-06-06 152240](https://github.com/mmedinabet/ACL-lab-/assets/142737434/5a41ba3e-f1d3-4c82-be0c-10d17a8156cd)

![Screenshot 2024-06-06 152623](https://github.com/mmedinabet/ACL-lab-/assets/142737434/f73a1026-ee43-4b64-8246-8714c6e6dea0)

2. Create a New ACL:
   - Deny PC1 from accessing Server1.
   - Apply the ACL on the Gigabit Ethernet 0/2 interface.
   - Include the "permit any" statement to allow other traffic.
   - 
![Screenshot 2024-06-06 153244](https://github.com/mmedinabet/ACL-lab-/assets/142737434/cdff13dd-f7c9-46cd-87fe-447e7f415101)


3. Test the New ACL:
   - Use ping to check connectivity from Laptop1 to Server1 (ping should succeed).
   - Use ping to check connectivity from PC1 to Server1 (ping should fail).
   
![Screenshot 2024-06-06 153411](https://github.com/mmedinabet/ACL-lab-/assets/142737434/a3fd8a82-73f7-4f77-a787-8d86c607f087)

![Screenshot 2024-06-06 153411](https://github.com/mmedinabet/ACL-lab-/assets/142737434/7281c4b6-6d05-4f7c-93e1-285d85c6a26c)

<h1>Conclusion</h1>
This lab demonstrated the process of configuring and testing standard ACLs to manage network traffic. By successfully implementing ACLs, we restricted specific devices from accessing network resources while allowing other communications to proceed. The exercises reinforced the importance of ACLs in enhancing network security and controlling access within a trusted network environment. By systematically applying, testing, and modifying ACLs, we gained practical experience in network traffic management and security configuration.
