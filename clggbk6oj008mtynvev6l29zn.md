---
title: "An Introduction to Linux OS"
seoTitle: "An Introduction to Linux"
seoDescription: "An Introductory post to Linux OS, plus installation guides!"
datePublished: Fri Apr 14 2023 09:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clggbk6oj008mtynvev6l29zn
slug: an-introduction-to-linux-os
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/NLSXFjl_nhc/upload/430ddce79b1d53b1a090b039ca4f6bc0.jpeg
tags: linux, linux-for-beginners, linux-kernel, linux-commands

---

# What is Linux?

Linux is a type of Operating System (OS) that is Free and Open Source, running on the GNU General Public License.

It was created by Linus Torvalds in 1991 and is based on UNIX. Now, it has evolved to run on a variety of devices including phones and supercomputers.

# Who uses it?

Up to now, Linux OS is being used by developers on their workstations and servers as it is supported by every major platform, including x86-64, x86, ARM, RISC, and DEC Alph. It is known to be the largest open sources project in the world, as professional and hobbyist programmers provide their contributions for the continuous improvement of the Linux Kernel.

On a personal note, my first introduction to Linux was in college, when I started to learn about Programming!

Fun fact: Most of the world's supercomputers are running on Linux!

# The Different Flavors

Linux has several distributions or "Flavors". Among the most popular ones are the following:

* [Ubuntu](https://ubuntu.com/desktop#download)
    
* [Fedora](https://getfedora.org)
    
* [Red Hat](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux)
    
* [Debian](https://www.debian.org)
    

# Advantages

* Open Source - The source code for Linux is available online, where a lot of enthusiasts help test and maintain the code for free. Since it is open-sourced, it is also completely customizable.
    
* FREE - You can download most (if not all) flavors of Linux systems online without having to pay for Licensing fees! Of course, there's the exception of Enterprise versions, but generally, you can download the OS and access all of its features for free!
    
* Robust
    
* Scalable - New modules can be added to the system without affecting its other parts.
    
* Flexible - It can adapt to all types of workloads.
    

# Disadvantages

* No official support - as it is free and maintained by the open-source community, there is a lack of official support for Linux. However, the community is composed of many bright and helpful people who are willing to help you with troubleshooting your Linux woes away!
    
* It is not completely user-friendly, especially for people with a Non-Tech background
    

# Installation Guides

Here are some quick installation guides to help you get started with your Linux journey!

## UBUNTU OS INSTALLATION

1. Install [Rufus](https://rufus.ie/en/) on your system to create a bootable USB drive
    
2. Get the official .iso image from the Official Ubuntu page
    
3. Insert a USB drive into a Windows System and launch the Rufus application
    
4. From the Rufus application, select the name of the USB device (this is usually automatically selected) and select the .iso image that needs to be flashed
    
5. Start the process and wait for it to finish.
    
6. Insert the bootable USB drive into the Device where Ubuntu is going to be installed
    

<mark>Note: The Ubuntu Device must be turned off before the USB drive is inserted into the USB port</mark>

1. On boot, proceed to the OS selection page by pressing F12
    
2. Select "USB HDD: "
    
3. Proceed with the setup
    

<mark>Note: Ensure that the Ubuntu Device is plugged into a charger before proceeding with the installation process</mark>

## FEDORA OS INSTALLATION

1. Download the [Fedora Media Writer](https://getfedora.org/en/workstation/download/) from the Official Fedora Downloads Page
    
2. Download the .iso file for x86\_64 from the Official Fedora Downloads Page if you need a specific image. If not, you can directly create an installer using the Fedora Media Writer application.
    
3. Insert a USB drive into a Windows System and launch the Fedora Media Writer application.
    
4. On the "Select Image Source", select "Select .iso file" if you need a specific image. Else, to download the latest version, select the following:
    
    1. `Select Image source: Download Automatically`
        
    2. `Select From: Official Editions`
        
    3. `Fedora Workstation`
        
    4. `Version:`
        
    5. `Hardware Architecture: Intel/AMD 64bit`
        
5. Select "Write" to start the process and wait for it to finish.
    
6. Insert the bootable USB drive into the Device where Fedora is going to be installed.
    
    <mark>Note: The Fedora Device must be turned off before the USB drive is inserted into the USB port</mark>
    
7. On boot, proceed to the OS selection page by pressing F12
    
8. Select "USB HDD: "
    
9. Proceed with the setup
    

## KERNEL INSTALLATION

1. Connect to the WiFi network.
    
2. Edit the `sources.list` file and uncomment all lines with `deb-src`
    

```bash
$ sudo gedit /etc/apt/sources.list
```

1. Save the changes and reboot the DUT
    
2. Run the following command on the terminal:
    

```bash
$ sudo apt-get update && sudo apt install && sudo apt dist-upgrade && sudo apt autoremove && reboot
```

1. Reopen the terminal and install the dependencies
    

```bash
$ sudo apt-get install git build-essential libncurses-dev fakeroot dpkg-dev ncurses-dev xz-utils libssl-dev bc flex libelf-dev bison zstd
```

1. Download the tarball link of the kernel version you wish to install from [kernel.org](https://www.kernel.org). At the time of writing this, the latest kernel version is 6.2.10.
    
2. From Menu on the Device, search for "File Manager".
    
3. Open the Downloads folder. The downloaded kernel should be located in this folder.
    
4. Right-click the downloaded &lt;linux-kernel-version&gt; and select "Open Terminal Here".
    
5. Run the following command on the terminal to extract the Kernel folder:
    

```bash
$ sudo tar -xf linux-5.4.145.tar.xz
```

1. Copy and configure the `.config` file from the extracted folder of the downloaded firmware
    

```bash
$ sudo cp /boot/config-$(uname -r) .config
```

1. Edit the `.config` file and include the changes/patches you want to implement.
    

```bash
$ sudo gedit .config
```

```bash
CONFIG_SYSTEM_TRUSTED_KEYS=""
CONFIG_MODULE_SIG=n
CONFIG_DEBUG_INFO=n
CONFIG_PSI=y
CONFIG_CPUSETS=n
CONFIG_PROC_PID_CPUSET=n
CONFIG_SYSTEM_REVOCATION_KEYS=""
```

1. Please make sure that this command is run inside the extracted folder of the downloaded Kernel.
    

```plaintext
$ sudo make nconfig
```

1. A User interface will appear, do NOT change anything just proceed to exit and save.
    
2. Press the "F9" key to Exit then Select "Save" &gt; "Ok"
    
3. Run the following commands on the terminal
    

```bash
$ sudo make oldconfig
$ sudo nice make -j 6 bindeb-pkg
```

1. This compilation could take a while (around 1-2 hours). After this is done (i.e. no errors were encountered), the `linux.deb` files will be generated outside of the extracted folder of the downloaded Kernel.
    
2. Install the generated `.deb` files.
    

```bash
$ sudo dpkg -i linux-*.deb
```

1. After the installation is done, reboot the device.
    
2. On boot to OS, you should be able to select the version of the kernel file that you just installed.
    

# References

* [https://www.techopedia.com/definition/3512/linux](https://www.techopedia.com/definition/3512/linux)
    
* [Ubuntu Desktop Guide](https://help.ubuntu.com/lts/ubuntu-help/index.html)
    
* [Fedora Documentation :: Fedora Docs (](https://docs.fedoraproject.org/en-US/docs/)[fedoraproject.org](http://fedoraproject.org)[)](https://docs.fedoraproject.org/en-US/docs/)
    
* [https://linux-tips.com/about](https://linux-tips.com/about)
    
* [https://www.linuxfromscratch.org/blfs/view/svn/index.html](https://www.linuxfromscratch.org/blfs/view/svn/index.html)
    
* [https://www.stackscale.com/blog/most-powerful-supercomputers-linux/#Linux\_more\_than\_20\_years\_in\_the\_supercomputing\_world](https://www.stackscale.com/blog/most-powerful-supercomputers-linux/#Linux_more_than_20_years_in_the_supercomputing_world)
    
* [https://www.redhat.com/en/topics/linux/what-is-linux](https://www.redhat.com/en/topics/linux/what-is-linux)