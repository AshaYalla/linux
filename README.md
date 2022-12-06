# Assignment 2

>> By Asha Yalla(016006250) and Mounica Reddy Kandi(016021902)




### Asha's Contribution:


### Mounica's Contribution:

### Steps followed:

Step 1: Forked the https://github.com/torvalds/linux repository and cloned it into the Cascade Lake Architecture n2-standard-2 instance in GCP.

Step 2: Enter this command to check the virtualization capability of the cpu

![WhatsApp Image 2022-12-05 at 10 07 47 PM](https://user-images.githubusercontent.com/99624135/205836536-f1eba314-f08a-4e3f-afb9-676268f0ba3f.jpeg)

Step 3: Install gcc by `sudo apt-get install gcc`

Step 4: Run `make -j 8 modules`

<img width="455" alt="image" src="https://user-images.githubusercontent.com/99624135/205842792-5410724b-bdc0-4337-98b8-89306292e37c.png">

Step 5: Run `sudo make INSTALL_MOD_STRIP=1 modules_install && make install`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842893-24ee8786-2fc7-40f1-92e5-76f5219c893d.png">

Step 4: Install make by `sudo make install`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205838433-e109d11b-71ca-48fc-a0b8-baf8a1bb7e9f.png">

Step 5: Run this command to know the version of the kernal `uname -a`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842067-956d867f-449a-4992-b386-311d6b5848ca.png">

Step 6: Reboot to update the kernal version

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205842510-8a234ba8-08c8-4e0c-931a-da8c8ad632e0.png">

Step 7: Run `uname -a` again the check the kernal version

![WhatsApp Image 2022-12-05 at 10 15 50 PM](https://user-images.githubusercontent.com/99624135/205839084-5aa3954a-f3af-4e3f-beb3-412b05aa9aa6.jpeg)

Step 6: Run `make`

![image](https://user-images.githubusercontent.com/99624135/205839150-57d2c4d5-236e-41a6-ad65-2f105aa4f4f8.png)

Step 7: Install ncurses by running `sudo apt install libncurses-dev`

Step 8: Install flex by running `sudo apt install flex`

Step 9: Install bison by running `sudo apt-get install bison`

Step 10: Install `sudo apt-get install libssl-dev`

Step 11: Install `sudo apt install libelf-dev`

Step 12: Install `sudo apt install dwarves`

Step 13: Install `apt-get install zstd`

Step 14: In linux folder copy oldconfig file and run `make oldconfig`

![image](https://user-images.githubusercontent.com/99624135/205839665-4be4bdd4-1609-4f7f-902e-cb12960a815d.png)

Step 15: Modify the code in the cpuid.c file and vmx.c file

Step 16: Run `make -j 8 modules`

Step 17: Run `sudo make INSTALL_MOD_STRIP=1 modules_install && make install’

Step 18: Run `lsmod | grep kvm’

Step 19: Run `rmmod kvm`

Step 20: Run `rmmod kvm_intel`

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205846273-9efc9fcd-b0e8-4aeb-9e50-2476ceb74204.png">

Step 21: Run `modprobe kvm`

Step 22: Run `modprobe kvm_intel`

Step 17: Run `lsmod | grep kvm` again

<img width="468" alt="image" src="https://user-images.githubusercontent.com/99624135/205846237-fba1ca48-0a37-40d2-9899-d25fb4193ab4.png">



