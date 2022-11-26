# Jarkom-Modul-4-E05-2022 
Kelompok E05

Anggota:  
* Maula Izza Azizi - 5025201104
* Selfira Ayu Sheehan - 5025201174
* Brian Akbar Wicaksana - 5025201207

# VLSM

# CIDR
Langkah pertama, dilakukan pengelompokkan subnet-subnet hingga menjadi satu, dengan step:  
![A](https://user-images.githubusercontent.com/80016547/204078901-cce1ec89-5f54-4113-b6d6-48b6a2bb6bda.png)  
![B](https://user-images.githubusercontent.com/80016547/204078913-00087abb-c2a3-4a93-8268-54cfe6469fec.png)  
![C](https://user-images.githubusercontent.com/80016547/204078918-6df65422-3b9f-4269-b533-e713e02ce0f4.png)  
![D](https://user-images.githubusercontent.com/80016547/204078923-87e9c0ce-fefb-4f84-bcb0-957a3e3ad42a.png)  
![E](https://user-images.githubusercontent.com/80016547/204078926-5d708190-f65c-44a9-a806-786f55874ff4.png)  
![F](https://user-images.githubusercontent.com/80016547/204078927-344479e8-4f3e-4961-adf5-8a329797c5a9.png)  
![G](https://user-images.githubusercontent.com/80016547/204078930-494b4fcd-0aca-4535-b4f1-f307a6075b83.png)  
![H](https://user-images.githubusercontent.com/80016547/204078938-f4d0a321-71d4-4ca3-a81f-51b02dc5b33c.png)  
Atau dengan rincian:  
![image](https://user-images.githubusercontent.com/80016547/204079108-7f4da4d3-10f4-46d5-9165-2eb510de5569.png)  
Dengan pengelompokkan yang telah dilakukan, maka dapat dibuat pohon IP CIDR dengan hasil sebagai berikut:  
![Untitled - Frame 3](https://user-images.githubusercontent.com/80016547/204079156-d7791620-d3b3-4702-8c32-20ae575af1ec.jpg)
Dengan rincian:  
![image](https://user-images.githubusercontent.com/80016547/204079245-e7238bfb-fbf7-4649-8562-17cc5bd875f6.png)
  
Pada GNS3, lakukan konfigurasi pada tiap node.  
**The Resonance**
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 10.24.64.1
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 10.24.130.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.24.132.1
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 10.24.144.1
	netmask 255.255.255.252
```  
**The Order**
```
auto eth0
iface eth0 inet static
	address 10.24.64.2
	netmask 255.255.255.252
	gateway 10.24.64.1

auto eth1
iface eth1 inet static
	address 10.24.16.1
	netmask 255.255.255.192

auto eth2
iface eth2 inet static
	address 10.24.8.1
	netmask 255.255.255.252
```  
**The Minister**
```
auto eth0
iface eth0 inet static
	address 10.24.8.2
	netmask 255.255.255.252
	gateway 10.24.8.1

auto eth1
iface eth1 inet static
	address 10.24.0.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 10.24.5.1
	netmask 255.255.255.252
```
**The Dauntless**
```
auto eth0
iface eth0 inet static
	address 10.24.5.2
	netmask 255.255.255.252
	gateway 10.24.5.1

auto eth1
iface eth1 inet static
	address 10.24.4.1
	netmask 255.255.255.0
```
**The Queen**
```
auto eth0
iface eth0 inet static
	address 10.24.32.2
	netmask 255.255.255.0
	gateway 10.24.32.1

auto eth1
iface eth1 inet static
	address 10.24.33.1
	netmask 255.255.255.252
```
**The Firefirst**
```
auto eth0
iface eth0 inet static
	address 10.24.36.2
	netmask 255.255.255.252
	gateway 10.24.36.1

auto eth1
iface eth1 inet static
	address 10.24.32.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 10.24.34.1
	netmask 255.255.254.0
```
**The Instrument**
```
auto eth0
iface eth0 inet static
	address 10.24.130.2
	netmask 255.255.255.252
	gateway 10.24.130.1

auto eth1
iface eth1 inet static
	address 10.24.40.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.24.36.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 10.24.129.1
	netmask 255.255.255.252
```
**The Magical**
```
auto eth0
iface eth0 inet static
	address 10.24.132.2
	netmask 255.255.255.252
	gateway 10.24.132.1

auto eth1
iface eth1 inet static
	address 10.24.136.1
	netmask 255.255.254.0
```
**The Profound**
```
auto eth0
iface eth0 inet static
	address 10.24.129.2
	netmask 255.255.255.252
	gateway 10.24.129.1

auto eth1
iface eth1 inet static
	address 10.24.128.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 10.24.128.129
	netmask 255.255.255.128
```
**Ashaf**
```
auto eth0
iface eth0 inet static
	address 10.24.16.2
	netmask 255.255.255.192
	gateway 10.24.16.1
```
**Guideau**
```
auto eth0
iface eth0 inet static
	address 10.24.0.2
	netmask 255.255.252.0
	gateway 10.24.0.1
```
**Phanora**
```
auto eth0
iface eth0 inet static
	address 10.24.4.2
	netmask 255.255.255.0
	gateway 10.24.4.1
```
**Johan**
```
auto eth0
iface eth0 inet static
	address 10.24.4.3
	netmask 255.255.255.0
	gateway 10.24.4.1
```
**Keith**
```
auto eth0
iface eth0 inet static
	address 10.24.32.2
	netmask 255.255.255.0
	gateway 10.24.32.1
```
**Matt Cugat**
```
auto eth0
iface eth0 inet static
	address 10.24.40.2
	netmask 255.255.255.128
	gateway 10.24.40.1
```
**Oakleave**
```
auto eth0
iface eth0 inet static
	address 10.24.34.2
	netmask 255.255.254.0
	gateway 10.24.34.1
```
**Corvekt**
```
auto eth0
iface eth0 inet static
	address 10.24.136.3
	netmask 255.255.254.0
	gateway 10.24.136.1
```
**Haines**
```
auto eth0
iface eth0 inet static
	address 10.24.136.2
	netmask 255.255.254.0
	gateway 10.24.136.1
```
**Heiga**
```
auto eth0
iface eth0 inet static
	address 10.24.128.130
	netmask 255.255.255.128
	gateway 10.24.128.129
```
**Spendrow**
```
auto eth0
iface eth0 inet static
	address 10.24.128.2
	netmask 255.255.255.128
	gateway 10.24.128.1
```
**The Beast**
```
auto eth0
iface eth0 inet static
	address 10.24.144.2
	netmask 255.255.255.252
	gateway 10.24.144.1
```
**The Witch**
```
auto eth0
iface eth0 inet static
	address 10.24.33.2
	netmask 255.255.255.252
	gateway 10.24.33.1
```
