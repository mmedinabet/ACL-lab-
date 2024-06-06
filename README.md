<h1> Access Control List Lab  </h1>

![Screenshot 2024-06-06 135641](https://github.com/mmedinabet/ACL-lab-/assets/142737434/79c1925a-358f-4b9b-999b-dd591f4276a9)

The initial setup does not have rules, and the laptop, PC, and Server “computers” can all ping and reach each 
other.  Note: The router and switches do not have passwords, this is intentional.  

Test communications:
1. Double click on each computer, then click on “Command Prompt” then use the ping utility to ping each computer.  You may perform this on each of the computers to test initial connectivity
   
![Screenshot 2024-06-06 135722](https://github.com/mmedinabet/ACL-lab-/assets/142737434/f334174c-b30a-47e7-93b2-18144dadaca8)

Test the Laptop connectivitity with both PC and server: 

<img width="296" alt="Screenshot 2024-06-06 140212" src="https://github.com/mmedinabet/ACL-lab-/assets/142737434/86c79658-31d7-4a4a-b624-1794283bf14c">

Test the PC connectivity with laptop and server:

![Screenshot 2024-06-06 140646](https://github.com/mmedinabet/ACL-lab-/assets/142737434/b3a85a95-b0a8-45d1-8f24-0a2a538a4fdc)

Lets test the server connectevity with both laptop and PC:

![Screenshot 2024-06-06 140959](https://github.com/mmedinabet/ACL-lab-/assets/142737434/bfdd217f-bafc-4464-a34e-f20bf160e88d)

TASK 2:  Double-click on the router and use the ping utility to ping each of the computers from each of the routers.

test router 1 : 
![Screenshot 2024-06-06 142155](https://github.com/mmedinabet/ACL-lab-/assets/142737434/9f4414cf-f4a3-4caf-b1f0-8124318eff3d)

test router 2: 
![Screenshot 2024-06-06 142440](https://github.com/mmedinabet/ACL-lab-/assets/142737434/4ebd0b1e-0c62-469c-b12d-aed7bf78c2f1)

<h1> Setup ACLs</h1>
 Task 1: 
1. On Router2 - create a standard ACL and deny Laptop1 from accessing Server1, create a standard ACL and apply it on interface: Gigabit Ethernet 0/2 “in” - Inbound direction on the interface.

![Screenshot 2024-06-06 143435](https://github.com/mmedinabet/ACL-lab-/assets/142737434/5f36f0fc-a1b3-4321-b8ad-38aa6b7e36b7)

now test the laptop by using ping to check connectivity with server
![Screenshot 2024-06-06 143654](https://github.com/mmedinabet/ACL-lab-/assets/142737434/8b3b3694-7a69-4d5f-b438-3d1615809855)

