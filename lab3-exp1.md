# steps to download virtual box, ubuntu and vs code

## Part 1: Install VirtualBox
Go to VirtualBox download page:
https://www.virtualbox.org/wiki/Downloads

Download for your OS:

Windows → “Windows hosts”

macOS → “OS X hosts”

Linux → choose your distro

Install VirtualBox:

Run the installer you downloaded

Follow the installation prompts

Accept default settings unless you need something specific

## 🐧 Part 2: Download Ubuntu ISO
Go to Ubuntu download page:
https://ubuntu.com/download/desktop

Click “Download” for the latest LTS version (e.g., Ubuntu 24.04 LTS)

Save the ISO file — this will be used to install Ubuntu in VirtualBox.

## Part 3: Set Up Ubuntu in VirtualBox
Open VirtualBox and click "New"

Fill out:

Name: e.g., "Ubuntu"

Type: Linux

Version: Ubuntu (64-bit)

Click Next

Memory size: At least 2048 MB (2 GB), ideally 4096 MB (4 GB) or more

Create a virtual hard disk now → VDI → Dynamically allocated → at least 20 GB

Start the VM and select the Ubuntu ISO you downloaded

Install Ubuntu inside the VM:

Choose your language and install options

Use default installation settings

Create a username and password

Let the installation complete and reboot

## Part 4: Install VS Code
Go to the VS Code download page:
https://code.visualstudio.com/Download

Download for your host OS (Windows/macOS/Linux)

Install VS Code like any regular app

## Part 5: Optional – Use VS Code with Ubuntu VM
If you want to code inside the Ubuntu VM and use VS Code from your host system, do the following:

Option 1: Use VS Code inside the VM
Open Firefox in Ubuntu VM → Download VS Code for Linux

Install using .deb file

Use VS Code directly inside Ubuntu VM

Option 2: Use VS Code on host with VM via SSH (advanced)
Install OpenSSH server on Ubuntu:

bash
Copy
Edit
sudo apt install openssh-server
Use VS Code Remote - SSH extension on your host system

Connect to the VM’s IP via SSH from VS Code

![alt text](<Screenshot (2).png>)