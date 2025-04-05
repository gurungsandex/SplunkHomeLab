# Splunk Home Lab for Learning and Practice 
This lab helps in simple & easy-to-understand home lab setup for Splunk. 

Splunk is a powerful platform for searching, monitoring, and analyzing machine-generated data. Setting up a Splunk home lab is a great way to get hands-on experience with log collection and analysis. 
In this guide, I’ll walk through installing Splunk Enterprise on a host machine and configuring a Splunk Universal Forwarder on a client computer to send logs to the Splunk server.

# My Splunk home lab setup
I re-purposed my old MacBook Air by installing Windows 11 on it. Within a VirtualBox on this system, I have set up Windows Server 2022 which I use for practicing Active Directory and other stuff. For this lab, I installed Splunk Enterprise on the Windows Server OS.

For client computers that send logs to the server using the Splunk Universal Forwarder, I am using my new MacBook Air, which is my primary laptop, running UTM. Within UTM, I have installed Windows 11 and Kali Linux. For this lab, I will install the Splunk Universal Forwarder on my Windows 11 machine within UTM.
I sometimes find it challenging to distinguish between the operating systems on my two laptops, especially with the virtual machines running on them.

I aim to create a simple, instructional guide that’s easy to use, reflecting my own learning experience. I want to highlight the challenges I faced during my foundational learning phase and the difficulties I had in finding straightforward, easy-to-follow resources online, without overwhelming people with complexity.


# Prerequisites
- A host computer (Windows/Linux) for installing Splunk Enterprise
- Client computers (Windows/Linux) for installing Splunk Universal Forwarder

# Step 1: Install Splunk Enterprise on the Host Server
- Download Splunk Enterprise from Splunk's official website.
- Install Splunk Enterprise and create a username and password.
  <img width="1093" alt="sp1" src="https://github.com/user-attachments/assets/9b2a1253-3c51-4316-ab29-2e79a3554f1d" />

- Access the Splunk Web interface by navigating to the default URL: http://127.0.0.1:8000
<img width="756" alt="sp2" src="https://github.com/user-attachments/assets/b69b2e59-2904-4dfc-abb6-655cd3df2973" />

# Step 2: Set up the receiving port in Splunk Enterprise
- Go to Settings, then select Forwarding and Receiving. 
- Add a new receiving port (9997) under "Receive Data" and ensure it is enabled.

# Step 3: Install Splunk Universal Forwarder on the Client Machines
- Install the Forwarder on the client machines, using the local system as of this lab. 
- Enter the host IP address when prompted.

# Step 4: Forwarder Management 
- Make sure to navigate to Settings and then to Forwarder Management, where you'll see your forwarder listed.
- To collect logs and establish a connection between the server and client, go to Settings and select the "Add Data" option.
- Choose the client/forwarder, add the event logs types, create a new index name, and submit.

# Step 5: Monitor & Analyze logs 
- Now, go to the Search & Reporting section to view the logs from your client machine.
- Search using the index you created, filter the search mode, and monitor and analyze the logs.

This is a simple and straightforward method to set up a Splunk home lab. I struggled to figure the setup, but I managed to get it working in a simple way. I hope you find this an easy way to set up your own SIEM lab. 
Stay tuned for more interesting articles on log analysis in the future. 
Until then, happy learning and see ya! 


