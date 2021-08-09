# Tp-Link_Tp-WN722N Adapter To Monitor_Mode
trouble shoot the new version of the tp-link wn722n model to enable the monitor_mode and packet_injection
older version of the tp-link wireless adapters are adaptable for kali_linux and parrot_os
the new version of the wirlesss adapter comes with realteck chipset which does not work with kali_linux and parrot_os 
so this are the commands used to change the old driver and set the new version drivers with kali compatable

--> this commands are used for the installation of the new drivers that support kali linux , and other linux operating systems 
--> make sure to type command one after other to decrease your problems at middle of the installation

1.sudo apt update<br>
2.sudo apt install bc<br>
3.sudo rmmod r8188eu.ko<br>
4. git clone https://github.com/aircrack-ng/rtl8188eus<br>
5.cd rtl8188eus<br>
6.sudo -i<br>
7.echo "blacklist r8188eu" > "/etc/modprobe.d/realtek.conf"<br>
8.exit<br>
9.make<br>
10.sudo make install<br>
11.sudo modprobe 8188e<br>

This are the commands that allow your your tp-link wirlsess adapter to monitor mode, packet injection 
