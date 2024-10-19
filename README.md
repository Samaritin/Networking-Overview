# Networking Overview

**Overview:** This lab focused on configuring and analyzing network connections using IP address configuration, subnetting, and NAT (Network Address Translation).

**Skills Developed:** IP analysis, subnetting, connectivity testing, troubleshooting using ping commands.

**Tools Used:** Windows Command Prompt, ipconfig, ping.

---
**Lab Details**
---

Introduction
This lab will help the individual understand how networks work and gain an overview of where to look in the command prompt in a Windows Operating System for any network configuration information. Networks are the communication tool between computers and to the internet. 
Objective
The objective of this week’s lab is to gain a better insight of how networks work within a computer environment. Additionally, this lab will help the user understand how the user’s network talks to the internet and find information about the users own network and configuration.


Results and Analysis
To begin the lab, the user must verify the setup. This lab will assume the user will be running the lab on a Windows operating system. Although, the user can run the lab on other types of systems such as MacOS and Linux distributions. The user will open the command prompt but hitting the windows or ‘start’ button at the bottom of the screen and typing run then clicking the command prompt. Once the command prompt window is available, the user will execute the ‘netsat -a’ command to show all protocols and IPs(Internet Protocols). In the figure below is what the user will see and could be quite long depending on what the user has running. 
Figure 1: Setup
 
![image](https://github.com/user-attachments/assets/237a257d-b84c-44b3-8779-25e83e824e9f)


Figure 2: Setup continued
 ![image](https://github.com/user-attachments/assets/c842206e-a5b6-43d5-af97-6aaed22f02fa)


Next the user will examine the network settings of the running host by running the ‘ipconfig -all’ This will display all of the network configuration settings on the host computer. In this lab, the figure below will only display some of the information that the command executed. Following the next figure will be the Graphical User Interface (GUI) of the IP settings. This only provides some of the information compared to the information provided in the command prompt. 

Figure 3: ipconfig command
 
![image](https://github.com/user-attachments/assets/7d93a56a-7650-41ee-9df8-45bc052591e8)



Figure 4: GUI IP settings
 
![image](https://github.com/user-attachments/assets/c903f40d-a412-4bc6-b683-edd38b004863)


When going to the site IPchicken.com, the site displayed a different IP address than the one displayed in the ipconfig command. This is due to the NAT(Network Address Translation). The NAT takes the private address that is on the home network and translates it to a public address for the internet and other websites to find. The NAT chooses a public IP address for the local/private address to talk to other servers. The NAT can assign a static IP for a local address, however, it is mostly dynamic. This means it is always changing whenever the user attempts to use the internet. This is due to the conversion to IPv6 and the increasing number of IoT(Internet of Things) that are connected to the internet. In the 1970s when IPv4 was created it allowed for approximately 7 billion pieces of technology to be connected to the internet. Now with the increase in technology there needs to be more availability for IP addresses and launched IPv6. Below is figure 5 of the external IP address. 
Figure 5: External IP address
 
![image](https://github.com/user-attachments/assets/3999424b-a122-4bc0-b93f-3003318b3da9)

Next testing connectivity, the user will use the ping command in the command prompt by pinging three host names or IP addresses. In this example, for clarity the host names were used. Interestingly, when pinging fbijobs.gov the request timed out. However, when pinging fbi.gov there was a connection. This could be due to the website or because it’s a subsite within the fbi.gov. Additionally, in this example a ‘.com’, ‘.org’ and a ‘.gov’ were all used for testing connectivity. 


Figure 6: Testing Connectivity
 
![image](https://github.com/user-attachments/assets/9d207d00-2460-4418-83b0-51aa50732b98)



In the next task, the user should run the command prompt as administrator. If the user runs the command prompt as normal. The user will get an error message stating, “the requested operation requires elevation” This means the command the user is attempting to run needs to be run as the administrator. Therefore, when the user goes to open the command prompt instead of left clicking to normally open the command prompt. The user will right click on the command prompt application then left click on ‘run as administrator’ this tab should be at the top of the list. The administrator command prompt should appear and the first line the user should see is ‘C:\WINDOWS\system32>’. It will also state at the very top of the window ‘Administrator: Command Prompt’. Now that the user is in the correct command prompt, executing the ‘netstat -ab’ command will show all of the task running. The user will let this run for some time. While this is running the user will then go into the start windows and search for the task manager. This will show all the task running as well in a more simplistic user friendly way. Although, the command prompt shows more detailed information about what is running on the host machine. The figure below shows the two compared. 
Figure 7: netstat command with task manager

![image](https://github.com/user-attachments/assets/c2315a32-5740-4e98-bb7c-39eac3357114)

 
The next command the user will use is the ‘nslookup’ command. This command will allow the user to find IP addresses for any websites. This command can help users when setting permissions for users at the corporate level and setting up web proxies as well. This command is also useful for professionals to verify if IP addresses are real or not during phishing attacks as well. Below in Figure 8 is an example of the same three websites used during the command. 
Figure 8: nslookup command
 
![image](https://github.com/user-attachments/assets/c361c786-fc49-4ad0-9557-e34bd479e55e)


Next the user will set up a web proxy using IPchicken.com to verify if the proxy is in good use. Finding a free proxy to use from the internet. A proxy server is an intermediary server that helps act as additional data security protecting users from malicious activity on the internet. Depending on the configuration they can be used in many ways. Typically, the user will send a request to the internet or website. At this point the IP address is exposed, once the website responds back the website appears at the computer or originating IP address. A web proxy receives the originating IP address then forwards it to the users request such as a website. Then the website responds and send the data back to the proxy server and then back to the host computer. The proxy server is a different IP address and takes the public address and changes it allowing more privacy of the information the individual is requesting over the internet.
The user will go into settings then network and internet. After the user will click on the proxy tab. In this section the user will manually setup the proxy by clicking on the edit button on the right side of the window. A new window will appear at this time, the user will then click the on button allowing the computer to use the proxy. After the user will enter in the proxy found from the internet and also enter the port the proxy has come with. It is optional to allow the proxy to work for local addresses or not. By clicking the box at the bottom of the window the proxy will not be used for local addresses. In the examples below are shown of IPchicken.com of the public address before and after the use of the proxy. 
Figure 9: before web proxy
 
![image](https://github.com/user-attachments/assets/22774f87-2283-4886-98aa-71c75197683e)



Figure 10: After web proxy
 
![image](https://github.com/user-attachments/assets/873fffe1-a78d-4f7d-8409-773e2e945ff7)










Conclusion
Network protocols and information is essential to any cyber professional. Any individual is going to use the internet and for any cyber professional it is necessary to be able to find where the information is containing the network protocols to diagnose and troubleshoot problems. It is also a fundamental skill to be able to set up proxies as a cyber professional working in the private and government sector due to the need for privacy of data when using the internet. This is just a basic overview or network commands, information, and proxies. However, these are essential skills for any cyber professional whether a penetration tester or blue team member. 
