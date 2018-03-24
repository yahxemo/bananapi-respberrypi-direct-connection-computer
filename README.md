# bananapi,respberrypi(kali linux)direct connection computer
for some error:

when I direct connection bananapi to computer,somtime haven't nothing wrong

on computer(windows) for cmd execute the order:
arp -a

can find bananapi's ip address.

but some moment later,can't find.

so you must edit ip address for youself.
find /etc/network/interfaces
or order:

vi /etc/network/interfaces
{
auto lo

iface lo inet loopback

auto eth0

iface eth0 inet static //no DHCP

address 192.168.xxx.??? //write the ip address you want

netmask 255.255.255.0 

gateway 192.168.xxx.1 //you computer address  **and 'xxx' must consistency**
}
ok
