#### Linux boot process is going to have 6 steps
- we will be knowing what exatly happens behind the scenes from the time when we press the power button of a server to the screen appearing for us to work
- Lets us see the 6 steps,
- 1. BIOS
  2. MBR
  3. GRUB
  4. KERNEL
  5. init
  6. RUNLEVEL
 - - BIOS - As operating system is the low level software and as soon as we hit the power button all the attached peripherals of the servers are initialized and they wil be cheked for any errors, and it will run a POST called as power on self test and if there is any error it will be displayed on the screen and futher initiasing the Basic inputoutput system BIOS will lookfor the MBR and loads into the Memory
   - and BIOS will look for Boot loader and once it finds the boot loader BIOS gives control to MBR
   - MBR - Master boot record it is present int he first sector of the drive /dev/sda or dev/hda and it is of 512 bytes size and it contains the information about the GRUB, will detects the boot loader Which is LILO or GRUB and loads in to the kernel, LILO Linux loader is used in the older OS's but newer version is using GURB or GRUB2, so in simple terms MBR loads and executes GRUB boot loader.
   - GRUB - GRUB stands for grand unified boot loader, we have mutilple kernel version installed on the server you can choose one which has to be executed. GUUB displays the splash sreen waits for few seconds, if you dont enter anything it iwll take the defaylt kernel image and specified int he grub configuration file. GRUB has the knowledge of the file syste where as older boot loader LILO has no idea. GRUB configuration file is /boot/grub/grub.conf it is linked to /etc/grub.conf, whcih has the the Kernel and initrd image, in simple terms GRUB will loads and executes kernel and initrd images
   - Kernel - Kernel is the core of the Opertating system, which mounts the root file system as specified int eh grub.conf and executes the /sbin/init program, initrd stand intital ram disk, the first process executed in the Kernel is init it has the process id 1. initrd uses the kernel as the temporary root file system untill kernel is booted and the real root filessytem is mounted. it also 
   - 
 - 
