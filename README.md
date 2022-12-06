# Assignment 2

>> By Asha Yalla(016006250) and Mounica Reddy Kandi(016021902)


### Asha's Contribution:
I have examined the kernal source code and built the kernal. To run the expected functionality we need to set-up the environment. I tried to understand and study about the leaf Function.  I added a leaf function under kvm_emulate_cpuid for calculating the total number of exits and storing it in eax register(0x4FFFFFFC). When I was trying to build the kernel for the nested Virtual Machine by running make modules, I faced multiple errors. Once that was successful, I then installed Virtual Machine Manager, built a nested VM with 4 cores of CPU, 4GB of memory and 20GB of disk space with debian OS on it. This was followed by creating a test .c file for printing register values in nested VM and successfully running it. 


### Mounica's Contribution:
Along with Asha I have examined the kernal source code and built the kernal.  I've tried to understand the function and added the required code for 0x4FFFFFFD in the cpuid.c under kvm_emulate_cpuid for calculating the total time spent processing all the  exits in ebx and ecx and also added required code in vmx.c file. I've tried to setup the nested VM and building the linux kernal which failed multiple times. After the final setup, I have created a test file in c for testing the code.


## Steps followed:

Step 1: Forked the https://github.com/torvalds/linux repository and cloned it into the Cascade Lake Architecture n2-standard-2 instance in GCP.

Step 2: Enter this command to check the virtualization capability of the cpu

![WhatsApp Image 2022-12-05 at 10 07 47 PM](https://user-images.githubusercontent.com/99624135/205836536-f1eba314-f08a-4e3f-afb9-676268f0ba3f.jpeg)

Step 3: Install gcc by `sudo apt-get install gcc`

Step 4: Install make by `sudo apt install make`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205838433-e109d11b-71ca-48fc-a0b8-baf8a1bb7e9f.png">

Step 5: Install make by `sudo apt install linux-headers-$(uname -r)`

Step 6: Install ncurses by running `sudo apt install libncurses-dev`

Step 7: Install flex by running `sudo apt install flex`

Step 8: Install bison by running `sudo apt-get install bison`

Step 9: Install `sudo apt-get install libssl-dev`

Step 10: Install `sudo apt install libelf-dev`

Step 11: Install `sudo apt install dwarves`

Step 12: Install `apt-get install zstd`

Step 13: Run `make -j 8 modules`

<img width="455" alt="image" src="https://user-images.githubusercontent.com/99624135/205842792-5410724b-bdc0-4337-98b8-89306292e37c.png">


Errors faced and rectified while running make -j 8 modules:

<img width="468" alt="image" src="https://user-images.githubusercontent.com/12370049/205850599-e779bea4-9b02-434a-8e6b-4b547e46a81d.png">

<img width="468" alt="image" src="https://user-images.githubusercontent.com/12370049/205850618-b8ddd825-ad8c-4c0e-ba42-41714d06862f.png">

<img width="468" alt="image" src="https://user-images.githubusercontent.com/12370049/205850637-155284f4-1388-4c91-93fd-8fe4a99870e8.png">

<img width="468" alt="image" src="https://user-images.githubusercontent.com/12370049/205850681-0ccb7d2e-c3e1-4e9f-8bf6-7ef7d5726b10.png">

<img width="455" alt="image" src="https://user-images.githubusercontent.com/12370049/205850703-396bca5c-def5-4963-a353-2a1d8fab8cb2.png">

Step 14: Run `sudo make install`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/12370049/205850808-68800bce-3c92-4e71-a04b-e7a6423ab754.png">


Step 15: Run `make -j 8`

Step 16: Run `sudo make INSTALL_MOD_STRIP=1 modules_install && make install`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842893-24ee8786-2fc7-40f1-92e5-76f5219c893d.png">


Step 17: Run this command to know the version of the kernal `uname -a`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842067-956d867f-449a-4992-b386-311d6b5848ca.png">

Step 18: Reboot to update the kernal version

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842510-8a234ba8-08c8-4e0c-931a-da8c8ad632e0.png">

Step 19: Run `uname -a` again the check the kernal version

![WhatsApp Image 2022-12-05 at 10 15 50 PM](https://user-images.githubusercontent.com/99624135/205839084-5aa3954a-f3af-4e3f-beb3-412b05aa9aa6.jpeg)


Step 20: In linux folder copy oldconfig file and run `make oldconfig`

![image](https://user-images.githubusercontent.com/99624135/205839665-4be4bdd4-1609-4f7f-902e-cb12960a815d.png)

Step 21: Modify the code in the cpuid.c file and vmx.c file

Step 22: Run `make -j 8 modules`

Step 23: Run `make -j 8`

![image](https://user-images.githubusercontent.com/99624135/205839150-57d2c4d5-236e-41a6-ad65-2f105aa4f4f8.png)

Step 24: Run `sudo make INSTALL_MOD_STRIP=1 modules_install && make install’

Step 25: Run `lsmod | grep kvm’

<img width="583" alt="image" src="https://user-images.githubusercontent.com/12370049/205849583-622305dc-7eaa-4a71-84df-5576317da9ca.png">

Step 26: Run `rmmod kvm`

Step 27: Run `rmmod kvm_intel`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205846273-9efc9fcd-b0e8-4aeb-9e50-2476ceb74204.png">

Step 28: Run `modprobe kvm`
 Run `modprobe kvm_intel`
 Run `lsmod | grep kvm` again

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205846237-fba1ca48-0a37-40d2-9899-d25fb4193ab4.png">

Step 29: Followed these steps Set up Chrome Remote Desktop for Linux Instance GCP 

https://cloud.google.com/architecture/chrome-desktop-remote-on-compute-engine#cinnamon

Step 30: Downloaded the iso image. 

<img width="700" alt="image" src="https://user-images.githubusercontent.com/12370049/205852383-c325fe65-e3a6-4799-b3c4-b39b324e3e62.png">


Step 31: Followed these steps to install an inner Virtual Machine: 

https://www.tecmint.com/install-kvm-on-ubuntu/

<img width="1198" alt="image" src="https://user-images.githubusercontent.com/12370049/205852286-b1e01fca-8226-4e71-a97f-f507907cbc2c.png">


Step 32: Ran the test.c file and got this as output:

![image](https://user-images.githubusercontent.com/12370049/205851905-755b0133-323b-4196-8885-ed992c837715.png)




