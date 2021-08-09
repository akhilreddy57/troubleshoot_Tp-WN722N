# troubleshoot_Tp-WN722N
trouble shoot the new version of the tp-link wn722n model to enable the monitor_mode and packet_injection
older version of the tp-link wireless adapters are adaptable for kali_linux and parrot_os
the new version of the wirlesss adapter comes with realteck chipset which does not work with kali_linux and parrot_os 
so this are the commands used to change the old driver and set the new version drivers with kali compatable

--> this commands are used for the installation of the new drivers that support kali linux , and other linux operating systems 
--> make sure to type command one after other to decrease your problems at middle of the installation

1.sudo apt update
2.sudo apt install bc
3.sudo rmmod r8188eu.ko
4. git clone https://github.com/aircrack-ng/rtl8188eus
5.cd rtl8188eus
6.sudo -i
7.echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"
8.exit
9.make
10.sudo make install
11.sudo modprobe 8188e

This are the commands that allow your your tp-link wirlsess adapter to monitor mode, packet injection 
