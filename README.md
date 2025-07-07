# BRG-27-labs

28/06/2025 AM Session - 

Setting Up and Exploring Linux
Linux installation 
-download VMware (https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)
-download Ubuntu Desktop.iso (https://ubuntu.com/download/desktop)

Start to install VMware and Ubuntu.iso
![image](https://github.com/user-attachments/assets/2f021cee-f27f-4956-b268-af23db41a205)

Create a GitHub account and document progress.
Created a GitHub account.
 ![image](https://github.com/user-attachments/assets/e6138d1e-9ba1-4dad-b1a4-f79b2cf7f181)

Create a new repository 
 ![image](https://github.com/user-attachments/assets/3064bb3b-eb5a-400d-92d8-b227bf198bf8)

Clone the repository to my local machine.
![image](https://github.com/user-attachments/assets/f00e1008-ed42-4623-94ee-3e44b2953b57)

1a-1:VirtualBox Installed 

Reusable_Learning_Objects/obtaining_a_linux_environment.md


Step 1: Install Ubuntu using VMware
Step 2: Download Ubuntu.iso file
![image](https://github.com/user-attachments/assets/40b477d5-fde3-45c6-a185-281c00cb597a)
Download VMware 17 Pro
![image](https://github.com/user-attachments/assets/ce30cad5-e653-4aa6-b438-593ed6330242)

Step 3: Install Ubuntu 
![image](https://github.com/user-attachments/assets/d3635652-ef20-4b93-b266-50ef09f6daa3)

Key in the username and password

![image](https://github.com/user-attachments/assets/17028ce2-301e-4fa6-96a8-fd8a097eb5d6)

Configure the VM 20GB storage 4GB RAM.
![image](https://github.com/user-attachments/assets/7e1911e3-358f-4532-b6d9-b66768175494)

Step 4: A New Ubuntu VM was created.
Step 5: Networking Mode Configured (NAT)
![image](https://github.com/user-attachments/assets/4429cb70-b85e-4a8a-8217-ded26a01d32a)

Step 6: Ubuntu Running with GUI or CLI Access
![image](https://github.com/user-attachments/assets/af0fb998-4f8c-4f59-979b-476cddceab4e)

Step 7: Install VirtualBox Guest Additons : sudo apt update
![image](https://github.com/user-attachments/assets/88cdf273-1d2e-4b12-ad98-cc8cd3376a9a)

sudo apt install virtualbox-guest-utils virtualbox-guest-x11
![image](https://github.com/user-attachments/assets/3bc2a723-62ff-4c25-9b57-5d7a4e27758f)
sudo reboot

Step 8: SSH Enabled
![image](https://github.com/user-attachments/assets/87c62e10-e7b4-4a8e-a4e7-e367e886c21b)

Test from host OS
![image](https://github.com/user-attachments/assets/6f732482-93f5-4ae8-9a18-70093be2945b)

Step 9: WSL installed
![image](https://github.com/user-attachments/assets/72fa3052-6cd0-41d8-bc38-f3b33b330db1)

Step 10: Different Distro Explored
Installed Kali
![image](https://github.com/user-attachments/assets/c34e0e94-e9ed-4120-bb0f-fab7d682b934)

------------------------------------------------------------------------------------------------

Lab 1a-2: Ubuntu Desktop and Command Line Familiarisation

[Server_Environments_and_Architectures/ubuntu_desktop_familiarisation.md]
(https://github.com/SCH-IT-MurdochUni/NetworkingLabs/blob/e0a4d12bb05b3a4bf0654b9c427c8eaecbee065a/Server_Environments_and_Architectures/ubuntu_desktop_familiarisation.md)

Step 1: Open Firefox
![image](https://github.com/user-attachments/assets/4e95a122-e20f-4a9e-b244-cef2cb2dbbfa)

Open the File and the App Store.
![image](https://github.com/user-attachments/assets/09383411-e85d-45d2-8265-7d4641170dad)

------------------------------------------------------------------------------------------------

Step 2: Terminal Command Outpu
Familiarity with Ubuntu Linux 
try command: ps -e
![image](https://github.com/user-attachments/assets/b7375bf0-0a47-4440-9a45-6962e90bfe94)

Command: top
![image](https://github.com/user-attachments/assets/56bff7b8-bb23-47c8-984d-0c6c1fede3f1)

Command: q to quit the top command
Command: ls
![image](https://github.com/user-attachments/assets/d8c77900-d16a-4912-87a3-0e02a3607d96)

Command: ls -la
![image](https://github.com/user-attachments/assets/cc3106f2-818a-4b90-8525-e103a04040e3)

The difference between ls and ls -la
ls
•	Lists files and directories in the current directory.
•	Shows only names (no hidden files, no detailed info).

ls -la (or ls -l -a)
•	-l → Long format (detailed listing).
•	-a → Show all files (including hidden files starting with .).


Command: ls -alt
![image](https://github.com/user-attachments/assets/12943b87-7268-454d-824d-cc88e4fb5c4b)

Try command: touch testfile (to create a file)
Command: gedit testfile (edit the file)
Command: featherpad testfile( to view the file)

![image](https://github.com/user-attachments/assets/35bcb304-5d0a-47ee-98e4-258a07703c83)

Command: nano testfile
![image](https://github.com/user-attachments/assets/a91a516f-5be4-42f8-b189-2c693a24ec08)

![image](https://github.com/user-attachments/assets/d770d468-6098-4cef-a776-467510d50f1c)

Can You Use gedit Over a Remote Terminal?
No, not easily—unless you have X11 forwarding enabled. Here's why:
1.	gedit Requires a GUI
o	It’s a graphical application (part of GNOME) and needs a desktop environment.
o	If you’re connected via SSH (just a terminal), there’s no GUI to display gedit.

2.	Possible Workaround (X11 Forwarding)
o	If your SSH connection supports X11 forwarding (ssh -X user@remote), you might be able to run gedit, but:
	It will be slow (graphics are sent over the network).
	Many servers don’t have GUI libraries installed.
	Not practical for most remote admin tasks.

3.	Better Alternative: nano (or vim/emacs)
o	Since nano is terminal-based, it works seamlessly over SSH.
o	No extra setup needed—just run it.

When to Use Which?
•	Use nano (or vim/emacs) for remote work → Fast, reliable, no GUI needed.
•	Use gedit only locally → Better for GUI environments with mouse support.

Command: cat testfile
![image](https://github.com/user-attachments/assets/0aa5c0b5-d814-4c37-95bb-50f2802d974e)

Command: less testfile
![image](https://github.com/user-attachments/assets/9855c5f7-532d-4742-bea0-d13df5a71aaa)

------------------------------------------------------------------------------------------------

Step 3: File Operations Practiced
Command: cp testfile testfile2
Run: ls
command cp testfile2 testfile3
rerun: ls
![image](https://github.com/user-attachments/assets/221e02c1-4f8b-4c41-bc5b-fe18d3642904)

Key Differences
1.	Original File Preservation
o	cp → Keeps the original file.
o	mv → Removes the original (unless renaming in the same directory).

2.	Storage Impact
o	cp → Uses additional disk space (since it makes a copy).
o	mv → Just changes the file's path, no extra space used.

3.	Common Use Cases
o	Use cp when:
	You need a backup (cp important.txt important_backup.txt).
	You want to duplicate a file to another directory (cp file.txt ~/Documents/).
o	Use mv when:
	You want to rename a file (mv oldname.txt newname.txt).
	You want to move a file to another location (mv file.txt /tmp/).

Run command: ls -lah
![image](https://github.com/user-attachments/assets/2aac7dac-4123-4a22-952b-bc941feffcf6)

•	Command: ls
•	Action: Lists files and directories in the current folder.
•	Details:
o	Shows only visible files (no hidden files).
o	No extra details (just names).
Command: ls -la (or ls -l -a)
Action: Lists all files (including hidden) in long format.
Details:
-l → Long format (shows permissions, owner, size, timestamp).
-a → Shows all files (including hidden ones starting with .).
File sizes are shown in bytes. 

------------------------------------------------------------------------------------------------

Step 4- System Information Commands 
Command: uname -a
Command: lsb_release -a
![image](https://github.com/user-attachments/assets/9a5454c3-0983-40e5-a986-68451a5c51e0)

Command: hostnamectl
![image](https://github.com/user-attachments/assets/2b36719c-544a-4976-b92e-f3bc2223ce30)

Command: ls -alt
![image](https://github.com/user-attachments/assets/0a645168-f936-4f4a-a47f-61c52a064531)

------------------------------------------------------------------------------------------------

Step 5: User Privilege Experiment
Super User
Command: whoami, adduser abcd1234, sudo whoami, sudo adduser abcd1234

![image](https://github.com/user-attachments/assets/f443eeee-18fe-4270-a448-80588220b299)

------------------------------------------------------------------------------------------------

Step 6- Network Configuration
Command: ip a
![image](https://github.com/user-attachments/assets/b66e1602-e188-4b84-98dd-24ebca8a148c)

Can’t ping [neighborsipaddress] because I didn’t connect their network.
Can ping 8.8.8.8 because is the Google default public IP

------------------------------------------------------------------------------------------------

Step 7: 
Hosts
Command: less /etc/hosts
![image](https://github.com/user-attachments/assets/99125d82-25c7-40a2-89c1-4ac71e6f3ad7)

Command: sudo nano /etc/hosts
Add 8.8.8.8 GoogleEpicDNS
![image](https://github.com/user-attachments/assets/ca116028-f4bc-4216-b5ba-3cc3c60b8a36)

Ping GoogleEpicDNS
![image](https://github.com/user-attachments/assets/15b4fd0c-f88a-4f9c-94c9-c82c93928da7)

------------------------------------------------------------------------------------------------

Step 8: DNS Lookup Performed
Command: nslookup google.com
![image](https://github.com/user-attachments/assets/1643e4b6-b385-4d87-9e9c-a33654e73038)

Command: sudo apt install whois, whois google.com
![image](https://github.com/user-attachments/assets/f6d7ef18-09ed-4372-a693-7ac01c8ccab9)

------------------------------------------------------------------------------------------------

Step 9: Public and Private IP Reflection
Command: ip a

![image](https://github.com/user-attachments/assets/4b838264-2367-40d6-9141-b42fdd815ad1)

IP from whatismyipaddress.com

![image](https://github.com/user-attachments/assets/95f44cfe-b3f7-4571-bddf-109f4e232f89)

The IP address shown by ip a is my private IP used within my local network, while the IP shown on whatismyipaddress.com is my public IP assigned by my ISP for internet access—these are different because my system is behind a router using NAT (Network Address Translation).

------------------------------------------------------------------------------------------------

Step 10: Hardware Info Commands 
Command: lsusb, lspci
![image](https://github.com/user-attachments/assets/2200d107-ca24-4ae7-8ab5-b042b1680e0b)

Less /proc/cpuinfo and settings > About this computer
![image](https://github.com/user-attachments/assets/19debcf2-7ac3-4de7-8cd9-7b699cb86ee8)

------------------------------------------------------------------------------------------------

Step 11: Output Redirection Practiced
Command: lsusb > output_of_lsusb

![image](https://github.com/user-attachments/assets/72ee1508-21c9-4fa8-9cd2-1fa7738d1129)

Try:
less output_of_lsusb

![image](https://github.com/user-attachments/assets/9831a5a1-bdf4-41d1-9e5b-1fc0705ea5cc)

cat output_of_lsusb
![image](https://github.com/user-attachments/assets/f67be065-1c91-4a63-ba9d-e97d004434c6)

•	cat output_of_lsusb Behavior:
o	Dumps the entire content of the file to the terminal at once.
o	No interactivity – you can't scroll or search.
o	Best for short outputs or when you want to quickly see content.

•	less output_of_lsusb Behavior:
o	Opens the file in an interactive pager.
o	Allows scrolling (↑/↓, Page Up/Down).
o	Supports search (/ + type query, then Enter).
o	Press q to quit.
o	Best for long outputs or when you need to analyze details.


Command: ls -la output_of_lsusb, rm output_of_lsusb (to remove file)
![image](https://github.com/user-attachments/assets/f2ee9e47-2c54-47cb-a598-fef9217bf7b6)

------------------------------------------------------------------------------------------------

Step 12: Software installed
1. Using Google Docs
-Create a new document and type Test ICT171 assignment.

![image](https://github.com/user-attachments/assets/4aab03c7-3d32-4558-bdea-6002e7db41b2)

2. Binary Download
Download a .deb file (e.g., Chrome or Opera) from the official website.
![image](https://github.com/user-attachments/assets/ce53422c-8a0f-4906-8c30-114fa8ad6da1)

And run: sudo dpkg -i opera.deb
 ![image](https://github.com/user-attachments/assets/5c14b54f-e724-470f-b2d8-3caf1718368c)

Opera installed
![image](https://github.com/user-attachments/assets/04b75bf4-afb8-4884-b8b8-6a1617616128)

3. Repository install via Ubuntu Software Centre 
![image](https://github.com/user-attachments/assets/9505f6a3-b73c-424a-803a-b2c0a0b97912)

------------------------------------------------------------------------------------------------

Step 13: Installing Software
Downloading and installing a binary a trusted repository
Command: less /etc/apt/sources.list, sudo apt update, sudo apt upgrade

![image](https://github.com/user-attachments/assets/d3103b1f-6ba9-4792-9169-d266561a328f)

![image](https://github.com/user-attachments/assets/f5bb4075-0c38-4ffd-ba2d-f604bf5a883e)

sudo apt install vlc
![image](https://github.com/user-attachments/assets/9abfd16f-6299-417b-9831-8ab23965200d)

Installing from source code
sudo apt install build-essential
![image](https://github.com/user-attachments/assets/4cb58e68-920b-4a42-83b5-1704a50cc571)

------------------------------------------------------------------------------------------------

Step 14: Source Code Compilation
Save a file to hello_world.c

![image](https://github.com/user-attachments/assets/17a893e4-4941-45f5-af0f-045434e61b0e)

Compile it with: gcc hello_world.c -o hello_world_executable
Execute: ./hello_world_executable
Set permission: chmod 777 hello_world_executable
Run: less hello_world.c , less hello_world_executable
![image](https://github.com/user-attachments/assets/011f83ea-c69b-4661-b017-cfb6adbbbf03)

![image](https://github.com/user-attachments/assets/e9bcaac8-f4b8-4263-98c0-56f11bcaa6c6)

------------------------------------------------------------------------------------------------

Step 15: Reflection Summary
I looked at both the GUI and the CLI in Ubuntu during this lab. The GUI was easy to use and made sense, especially when it came to things like browsing the web or installing apps through the applications center. The CLI, on the other hand, gave you more power and speed when it comes to scripting and system-level tasks. 
I looked into a variety of different ways to install software, such as SaaS options like Google Docs, repository-based installs with apt, manual .deb file installations, and making source code. There are pros and cons to each choice. You don't have to install SaaS on your computer, and it's easy to use. 
It is safe and simple to install from a repository. You can choose how to do things with manual installs, and you can control the full build process using source compilation. For everyday tasks, I appreciate using the GUI, but for development and troubleshooting, I really like how strong the CLI is. I want to be a software engineer, so I know that I need to be able to use both interfaces properly so that I can work in a variety of places.

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Day 2 – AM
Total Cost of Ownership (TCO) Report: Cloud Storage vs External Hard Drive

1. Introduction
This report presents a Total Cost of Ownership (TCO) comparison between a budget inkjet printer and a high-capacity laser printer over a 5-year period. The objective is to determine which printer offers better value based on fixed and variable costs, including consumables, electricity, and paper usage. This analysis is useful for both personal and business decision-making, similar to evaluating cloud vs on-premises infrastructure or choosing between buying and renting assets.

2. Assumptions
The following assumptions are used for the TCO calculations:
- Time period: 5 years
- Printing volume: 750 pages per week
- Power usage: 40 hours per week
- Electricity cost: $0.30 per kWh
- Paper cost: $6 per 500 pages
- Ink yield: 500 pages per cartridge
- Inkjet cartridge cost: $25
- Laser toner yield: 5000 pages
- Laser toner cost: $120
- Inkjet printer cost: $120
- Laser printer cost: $250
- Power consumption: Inkjet 30W, Laser 75W

3. Cost Breakdown

![image](https://github.com/user-attachments/assets/f1830d81-2735-407e-a154-1b5d99abe8d4)

4. Analysis
Over a 5-year period, the inkjet printer has a total cost of $12303.60, while the laser printer costs $7504.00. Although the laser printer has a higher upfront cost, its lower toner cost and higher yield make it more suitable for high-volume printing. The inkjet printer is more cost-effective in this scenario due to lower consumable costs and electricity usage.


5. Reflection Questions
- Based on the TCO, the inkjet printer is the most cost-effective over 5 years.
- For a home user printing only 5 pages per week, the inkjet printer remains more cost-effective due to lower usage and consumable needs.
- Other factors to consider include print quality, speed, noise level, and environmental impact.
- For a large workgroup printer, high yield toner, low maintenance, and network capabilities are important cost factors.
- The break-even point occurs when the cumulative cost of both printers is equal. In this scenario, the inkjet remains more cost-effective throughout the 5-year period.

6. Conclusion
This TCO analysis demonstrates that while both printers serve different needs, the inkjet printer offers better value for high-volume printing over a 5-year period. Understanding TCO helps make informed decisions by quantifying long-term costs and aligning them with usage patterns and preferences.

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Day 2-PM
2b-1 Lab - Cloud Computing 
Step 1: Lauch EC2 Instance
To create an AWS EC2 account, login to the dashboard

![image](https://github.com/user-attachments/assets/c11830d9-e7c1-4d49-a2e8-dc825327b364)
![image](https://github.com/user-attachments/assets/18b4a779-62bb-4807-971d-ab434fb19b66)

------------------------------------------------------------------------------------------------

Step 2. Configure Security Group
Add inbound rules:
![image](https://github.com/user-attachments/assets/983cf896-5866-4ff7-b319-8cea995d4cbc)

------------------------------------------------------------------------------------------------

Step 3. SSH Access
![image](https://github.com/user-attachments/assets/f1b121d6-55fd-4fa2-9384-b6156847a8fe)

Step 4. Install Apache
sudo apt update
sudo apt install apache2

![image](https://github.com/user-attachments/assets/0accc27e-c34c-4fa3-9d13-4a20014cac54)
![image](https://github.com/user-attachments/assets/dfad0ac4-68d3-4191-bc65-20ed419a4461)

------------------------------------------------------------------------------------------------

Step 5.  Edit index.heml
![image](https://github.com/user-attachments/assets/ac3632e7-c7d0-4264-9333-1f9653da89f1)

------------------------------------------------------------------------------------------------

Step 6. Download file with wget command: wget https://code.jquery.com/jquery-3.6.0.min.js
![image](https://github.com/user-attachments/assets/172cdac3-643e-49db-a0ba-fda1213cd8df)

------------------------------------------------------------------------------------------------

Step 7: Copy file to Web Root
![image](https://github.com/user-attachments/assets/37b85acc-8905-4ef8-b526-56bbf57818d3)

------------------------------------------------------------------------------------------------

Step 8: Access the file via browser
![image](https://github.com/user-attachments/assets/af778fb8-5d7f-47a8-95a8-0f69f99bfcae)

------------------------------------------------------------------------------------------------

Step 9: Insert Link in HTML

http://15.152.31.28
![image](https://github.com/user-attachments/assets/f708b64f-8150-48f1-a546-7d2c916c5255)

------------------------------------------------------------------------------------------------


Step 10: Budget Monitoring Enabled
![image](https://github.com/user-attachments/assets/7a90bb35-cf42-468a-91c0-85e5d1a0d460)

------------------------------------------------------------------------------------------------

Step 11: Terminate Instance
![image](https://github.com/user-attachments/assets/447ffa2a-9002-4d61-b9d9-0a41f9cbe629)

------------------------------------------------------------------------------------------------

Challenge Deliverables:
C1: Ping International Servers: ping google.com; ping Baidu.com; ping aws.amazon.com
![image](https://github.com/user-attachments/assets/b6ce4c26-e145-4d90-9ce0-122c2e16fb98)


C2: Upload File via SCP
![image](https://github.com/user-attachments/assets/d300731a-8393-4c47-9ea0-f390cd63abcb)


C3: create a .html file
![image](https://github.com/user-attachments/assets/b2414a29-d44c-4421-a830-547da4d3044b)

Save as index.html, double click it
![image](https://github.com/user-attachments/assets/edc975da-7e0c-40d4-90bb-bf00acb0b728)

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

2b-2 Lab - Bash Coding 
Familiarize the commands
![image](https://github.com/user-attachments/assets/9c56bdac-e153-4a9b-9b22-6ecd04350d95)

------------------------------------------------------------------------------------------------

Step 1: Create a new Directory Command: 
mkdir LabFiles 
cd LabFiles
![image](https://github.com/user-attachments/assets/2c916d29-a5a5-48df-91cc-2f754593777c)

1.	Create a New File Command: touch notes.txt

![image](https://github.com/user-attachments/assets/169c997b-5564-41e6-9926-01cb5c94bcf4)

2.	Write Content to the File Command: echo "This is a Bash scripting lab." > notes.txt
3.	Display File Content Command: cat notes.txt

![image](https://github.com/user-attachments/assets/bf451dfe-cf88-410c-bcb9-3e7328008e68)

4.	Copy the file Command: cp notes.txt backup_notes.txt

![image](https://github.com/user-attachments/assets/66aa37c7-8ddc-43dd-af0a-3c5769e1c0f3)

5.	Rename the file Command: mv backup_notes.txt old_notes.txt

![image](https://github.com/user-attachments/assets/16d219b0-0a76-4c9b-b2aa-a762254e20b0)

6.	Remove a file Command: rm old_notes.txt
   
![image](https://github.com/user-attachments/assets/3a878f4c-4c7e-4cff-8992-8e37997f6a23)

------------------------------------------------------------------------------------------------

Step 2: What command did you use to create a new directory?
o	mkdir LabFiles 
•	How can you view the contents of a file without opening it in a GUI besed text editor?
o	cat [filename].txt
•	What is the difference between cp and mv commands?
o	cp is to copy the file, mv is to rename the file.

------------------------------------------------------------------------------------------------

Step 3: Basic Bash Script Created and Run 
Creating and Executing Basic Bash Scripts
-	Command: cd ~/LabFiles
-	Create a new script file Command: nano hello_world.sh

![image](https://github.com/user-attachments/assets/727f2f21-f889-44c4-b9a2-bddd6916b30b)

-	Add content to the script:
![image](https://github.com/user-attachments/assets/56181c7a-70d7-4ec8-a819-ab44ed667529)

-	Press CTRL + X, then Y, and ENTER to save the file. Make the Script Executable command: chmod 777 hello_world.sh
![image](https://github.com/user-attachments/assets/032fb100-eabc-45fb-a2da-8249073dc124)

-	Execute the Script: ./hello_world.sh 
  nano hello_world.sh
 	![image](https://github.com/user-attachments/assets/de26115e-811c-4a7b-bb9e-fb09fd51bfd5)

-	Modify the echo command: echo "Welcome to the Bash scripting lab!"
![image](https://github.com/user-attachments/assets/c6f5f866-dc6f-494d-ab57-619897522aee)

-	Save and execute command: ./hello_world.sh

------------------------------------------------------------------------------------------------

Step 4: Reflection Questions
•	What is the purpose of the chmod +x command?
  o	Is to add execute permission to the script file.
•	Why do we use the shebang (#!/bin/bash) at the beginning of scripts?
  o	Is to tell the system which interpreter to use to run the script.
•	How can you modify the script to display a personalized message?
  o	Use echo “[message]”

------------------------------------------------------------------------------------------------

Step 5: Loop and Conditional Script
Implementing Loops and Conditionals
-	Create a new script command: BASH nano system_info.sh, and add the content.

![image](https://github.com/user-attachments/assets/b55bb44a-096f-4636-8c04-439e951223c0)

Save and Make Executable command: chmod 777 system_info.sh

![image](https://github.com/user-attachments/assets/a4282620-5929-4189-b2d7-8aa4834a773e)

Run the script command: ./system_info.sh

![image](https://github.com/user-attachments/assets/fbee2f0f-51da-4246-96ab-44381d726484)

------------------------------------------------------------------------------------------------

Step 6: Reflection Questions(Loops and Conditionals) 
•	How does the for loop in the script operate?
  #!/bin/bash
  for i in {1..5}
  do
   echo "Number: $i"
done
•	What happens if a user enters a number greater than 10?
  o	It shows number out of range
•	How can you modify the script to handle invalid inputs gracefully?
Accepts a number from the user. 
Validates that it’s a number between 1 and 10. 
Uses that number as the upper limit in the loop.

![image](https://github.com/user-attachments/assets/b064db4a-5382-415d-b13d-4e170f4c9cfd)

------------------------------------------------------------------------------------------------

Step 7: System Monitoring Script Created and Run
Generate a resource_monitor.sh script, and run

![image](https://github.com/user-attachments/assets/eacca78d-f38a-4251-95bc-1cfd050f5dfd)

Make the script executable: chmod +x resource_monitor.sh

![image](https://github.com/user-attachments/assets/7c62832f-b820-44a1-a1c2-a64db06e1ea3)

Run the script: ./resource_monitor.sh

![image](https://github.com/user-attachments/assets/9a67f472-ad1d-46a8-8994-0d5f95ef7bc7)

------------------------------------------------------------------------------------------------

Step 8: Reflection: Monitoring Automation
• What does free -h show?
free -h displays the system's memory usage, including total, used, free, shared, buffer/cache, and available memory in a human-readable format (e.g., MB or GB).

![image](https://github.com/user-attachments/assets/d9e94022-04ba-4fd9-9f02-236026d8cff3)

How can this script be modified to monitor network usage?
 - can add a command like ip -s link to monitor network traffic.

![image](https://github.com/user-attachments/assets/3e95af4c-47ad-47b6-9db4-1f561cc87409)

Why is automation important for admins?
- Automation helps system administrators save time, reduce human error, and ensure consistent monitoring. It allows for proactive issue detection and improves system reliability and performance.

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Lab 3 AM
Activity 1: DNS Lab Objectives
Understand DNS Concepts
-	Learn how DNS translates domain names (e.g., example.com) into IP addresses.
-	Understand the role of forward and reverse DNS lookups.
-	
------------------------------------------------------------------------------------------------

Step 1: Setup a DNS Server

![image](https://github.com/user-attachments/assets/0fa1ceec-bffa-4d8a-a2fc-347c6ff0de65)

Check public IP
![image](https://github.com/user-attachments/assets/65125ee6-ebb6-4380-94e0-cd763ea69e6d)

------------------------------------------------------------------------------------------------

Step 3: install Apache on Ubuntu VM
![image](https://github.com/user-attachments/assets/b70bffcb-9232-490e-9793-e9b967d3141c)

Check Apache if running: 
![image](https://github.com/user-attachments/assets/ee6cb687-507d-45ee-b274-d983452802bf)

------------------------------------------------------------------------------------------------

Step 4: Verify DNS Mapping
![image](https://github.com/user-attachments/assets/a964e6cd-f008-4fb2-93cc-fc8cea95eadc)

![image](https://github.com/user-attachments/assets/3f45324b-a304-4b32-a2d3-f80e574bfb9f)

------------------------------------------------------------------------------------------------

Step 5: Screenshot Apache Welcome Page
![image](https://github.com/user-attachments/assets/c9e815a4-8063-4269-a1b5-5ab2c140d2de)

------------------------------------------------------------------------------------------------

Step 6: Screenshot DNS Test Output

![image](https://github.com/user-attachments/assets/d823f2e8-9fee-454e-b5fb-e78852c11929)


Use Linux VM (Ubuntu VM)
Install BIND9

![image](https://github.com/user-attachments/assets/25e6367b-c8e5-49e6-a3b1-9f2b1da6d75d)

Configure Zone File
•	Create a forward zone file (e.g., db.example.com) to map domain names to IPs.
•	Create a reverse zone file (e.g., db.192) to map IPs back to domain names.
•	Define these zones in named.conf.local.

------------------------------------------------------------------------------------------------

Activity 2: Encrypt TLS Certificate Setup
Step 1: Install Certbot and Apache Plugin

![image](https://github.com/user-attachments/assets/1b655323-3bc4-4333-a142-c5ffcf51b1e6)

Then install Apache plugin:

![image](https://github.com/user-attachments/assets/8ae12157-1721-42c3-a5fa-e7f6ffe091b1)

------------------------------------------------------------------------------------------------

Step 2: Install Snapd

-sudo apt install snapd
![image](https://github.com/user-attachments/assets/03a8dc71-fdc7-4224-93e0-994729b3e065)

-Ensure Snap’s path is available: 
sudo ln -s /var/lib/snapd/snap /snap

![image](https://github.com/user-attachments/assets/14587570-4e30-4e97-a3f0-cdb44b9ee95b)

-Install Certbot using Snap:
![image](https://github.com/user-attachments/assets/9f870081-1b24-4570-a0cc-0db184f5730c)

-Create a symlink for Certbot

------------------------------------------------------------------------------------------------

Step 3: Issue TLS Certificate

![image](https://github.com/user-attachments/assets/7fa5d2ce-3a0f-4dd4-a90c-321afd0eb5b4)

------------------------------------------------------------------------------------------------



Step 5: Certbot Success Message

![image](https://github.com/user-attachments/assets/9e3ee2a9-4445-45b9-ab2e-92483ad56fd1)

------------------------------------------------------------------------------------------------

Step 4: Enable HTTPS on Apache
Certbot automatically updates Apache config.
You can verify: 
sudo apachectl configtest
sudo systemctl restart apache2
 
------------------------------------------------------------------------------------------------
Step 5: Verify HTTPS with Lock Icon

![image](https://github.com/user-attachments/assets/36398f01-95a3-4d5b-b7ea-c72114d2137a)


------------------------------------------------------------------------------------------------

Step 6: Test Auto-Renewal

![image](https://github.com/user-attachments/assets/3aeddedb-d56a-4f52-987e-086d41a32159)

------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------

Lab 3 PM
Step 1: Practice Bash Commands Executed
Step 2: Test files and directories created

![image](https://github.com/user-attachments/assets/23c5717b-5491-4729-acb3-68e4e5f4bb37)

------------------------------------------------------------------------------------------------

Step 3: Some Bash basics
Save the code in text editor, and provide privileges

![image](https://github.com/user-attachments/assets/6d414996-6b2f-48b1-a918-0bec42f5c7b6)

![image](https://github.com/user-attachments/assets/92cdb6af-ff78-48a1-96fc-a2c45b70bf4c)

------------------------------------------------------------------------------------------------

Variables

![image](https://github.com/user-attachments/assets/3c7b1599-fec8-4a56-b8c5-c4f685ff4012)

Modify the code 1
![image](https://github.com/user-attachments/assets/5ebd8cc7-eba2-4b0f-ace0-9cb218560628)

Create files and folders in /home/ubuntu/Documents:
![image](https://github.com/user-attachments/assets/265846cd-5690-47f8-b837-79ecfd427a58)

Results:
![image](https://github.com/user-attachments/assets/8bd06590-8f6d-4083-923a-a59d56da6992)

------------------------------------------------------------------------------------------------

Creating a basic script: mkdir backup

![image](https://github.com/user-attachments/assets/7d2593e8-d468-41a7-88c8-ff69a35e7019)

![image](https://github.com/user-attachments/assets/de51fd0e-7c5c-494f-af28-2e5c7e08bfdd)

------------------------------------------------------------------------------------------------

Give the file execute permissions for testscript.sh
![image](https://github.com/user-attachments/assets/63af8a4c-2ab1-4dfd-9233-1d619741be18)

------------------------------------------------------------------------------------------------

tep 4: Script Moved to /usr/bin and Tested
Making the script available system wide
Move the testscript file to user bin command: sudo mv /home/ubuntu/testscript /usr/bin/testscript

![image](https://github.com/user-attachments/assets/ce67ef70-c076-4224-9a0e-610bde99d4f4)

Run change the owner command: sudo chown ubuntu /usr/bin/testscript

![image](https://github.com/user-attachments/assets/747c23b8-2ae8-4575-8e63-b557e2b8ef20)

Test the file is available to be executed system wide and display the system variable $PATH

![image](https://github.com/user-attachments/assets/76219b31-29fd-406a-a44c-a5858b38b2a6)

------------------------------------------------------------------------------------------------

Step 5: ZIP Archive with Date Filename
Creating an archive
Zipping command: zip zippedfile * (tested in backup folder)

![image](https://github.com/user-attachments/assets/80214ef3-8b9a-413a-82d0-e762ece683b8)

------------------------------------------------------------------------------------------------

Adding the date
Create a script call currentfile and copy the command: now=$(date +"%d_%m_%y")
![image](https://github.com/user-attachments/assets/a6f149e9-e333-43a7-9564-b57e476539be)

------------------------------------------------------------------------------------------------

Save the script
Make it executable and run it.
The result show below:

![image](https://github.com/user-attachments/assets/d2fb8ac2-4447-4c7b-9ac9-0d20e80a7e1c)

Command for zip –help
![image](https://github.com/user-attachments/assets/82257a09-9d6f-4d45-951c-18d991913bd8)

------------------------------------------------------------------------------------------------

Cron
Edit cron with command: sudo nano /etc/crontab

![image](https://github.com/user-attachments/assets/b4772595-64f0-48f4-9ded-3191c65e2496)

Edit the crontab:
crontab -e, 
add the line 9 * * * * /usr/bin/bash /home/sohjie/testscript.sh (Add this line (runs at 9 mins past every hour))

![image](https://github.com/user-attachments/assets/7e9fa61f-da32-4d37-a547-146250c3f34a)

------------------------------------------------------------------------------------------------

Step 6: Creating the backup script
Create the backup script: nano /home/ubuntu/testscript.sh

![image](https://github.com/user-attachments/assets/0cd3b608-8907-4fe5-8c78-f84adf9563eb)

Make it executable

![image](https://github.com/user-attachments/assets/f9a331ff-22b7-4115-b689-ec13b1322020)

Let the cron run for an hours or trigger manually:

![image](https://github.com/user-attachments/assets/6442d979-4fa6-4f91-9c8d-fbdd7e31120f)

------------------------------------------------------------------------------------------------

Step 7: Successful Cron Execution Verified
Verify: ls -lh /home/ubuntu/backup_*

![image](https://github.com/user-attachments/assets/855bd515-6ae8-4f8c-84b7-62d4641650f5)

Result:
![image](https://github.com/user-attachments/assets/a12f1854-6db6-4f98-9393-0bd0cf6f52d1)

------------------------------------------------------------------------------------------------

Step 8: SCP to Cloud Working
Check if Backup File Exists

![image](https://github.com/user-attachments/assets/695a891e-8f38-4893-a6ba-f45d28b8e495)

Manually Run SCP: ssh -i /home/sohjie/key.pem sohjie@192.168.91.129

![image](https://github.com/user-attachments/assets/87788b2d-f8f9-4223-9fb5-a7ca0daac3cc)

Verify Transfer:
ls -lh ~/backup_2025-07-05_11-09.zip

![image](https://github.com/user-attachments/assets/c4d2c208-d575-4571-97a8-945dcaf6d2fa)

------------------------------------------------------------------------------------------------

Step 9: SSH Certificate Accepted by Root
ssh -i /home/sohjie/key.pem sohjie@192.168.91.129

![image](https://github.com/user-attachments/assets/17968e06-ffdf-4f9f-98cc-fadfef4cce51)

------------------------------------------------------------------------------------------------

Step 10: Final Script Submitted

![image](https://github.com/user-attachments/assets/0e2a4826-4a0c-4150-bab2-50942e3f449d)

And ensure it executable:
chmod +x /home/sohjie/tscript.sh

![image](https://github.com/user-attachments/assets/0b093c46-df36-46e7-ba37-6a5533bddb28)

------------------------------------------------------------------------------------------------

Step 11: Run Script automatically on boot
Create a systemed service: sudo nano /etc/systemd/system/backupboot.service

![image](https://github.com/user-attachments/assets/50fb3cc9-eebe-4b54-a601-db3cb117fd83)


Enable and start the service:
sudo systemctl daemon-reexec
sudo systemctl enable backupboot

![image](https://github.com/user-attachments/assets/36a2d8d7-5e6b-4205-8b77-b2e9c8dbfad8)

Reboot to test: sudo reboot
After reboot run: ls -lh /home/sohjie/backup_*.zip

![image](https://github.com/user-attachments/assets/859e947d-e962-48ad-a38a-c904b3deb1ed)

------------------------------------------------------------------------------------------------

Step 12: Customized MOTD with neofetch & figlet
Install figlet and neofetch
sudo apt update
sudo apt install figlet neofetch -y

![image](https://github.com/user-attachments/assets/d5ba851b-40a7-4a34-9a9e-15f481a0514d)

Create a Custom MOTD script: sudo nano /etc/update-motd.d/99-custom
Save and exit.

![image](https://github.com/user-attachments/assets/418d1188-fcd1-45ea-80d7-e333d63ad53b)

Make it executable: sudo chmod +x /etc/update-motd.d/99-custom

![image](https://github.com/user-attachments/assets/e94b91b7-06ce-450b-bb2e-1486e245d61d)

Test run:

![image](https://github.com/user-attachments/assets/f2243b41-bdec-438c-815d-72416ce7a7c1)

![image](https://github.com/user-attachments/assets/9f1f24f0-4753-468e-9c3e-9944833a2027)

Test figlet with color: sudo apt install ruby -y, sudo gem install lolcat
Figlet “ICT171 is the BEST” | lolcat

![image](https://github.com/user-attachments/assets/a3a4e48b-84d8-43ca-9765-1f906496184f)







Ubuntu CLI exploration




https://github.com/SCH-IT-MurdochUni/NetworkingLabs/blob/e0a4d12bb05b3a4bf0654b9c427c8eaecbee065a/Server_Environments_and_Architectures/linux_services.md

