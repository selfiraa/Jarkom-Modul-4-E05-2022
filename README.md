# Jarkom-Modul-4-E05-2022 
Kelompok E05

Anggota:  
* Maula Izza Azizi - 5025201104
* Selfira Ayu Sheehan - 5025201174
* Brian Akbar Wicaksana - 5025201207

# VLSM
- Langkah pertama yang dilakukan adalah me-label setiap subnet yang ada di topologi:
![Subnet](https://user-images.githubusercontent.com/94432967/204087617-f955ab6f-afc4-459a-bed9-cb9d15b12923.png)

Lalu, pada setiap subnet dihitung berapa jumlah ip yang dibutuhkan. Dari jumlah ip tersebut tentukan subnet mask paling ideal yang dapat menampung semua ip tersebut kemudian jumlahkan address yang terdapat pada semua subnet mask.
| **Subnet** | **Jumlah IP** | **Netmask** | **Address yg dibutuhkan** |
| :--------: | :-----------: | :---------: | :-----------------------: |
| A1         | 1001          | /22         | 1024                      |
| A2         | 2             | /30         | 4                         |
| A3         | 51            | /26         | 64                        |
| A4         | 2             | /30         | 4                         |
| A5         | 2             | /30         | 4                         |
| A6         | 2             | /30         | 4                         |
| A7         | 271           | /23         | 512                       |
| A8         | 2             | /30         | 4                         |
| A9         | 251           | /24         | 256                       |
| A10        | 2             | /30         | 4                         |
| A11        | 121           | /25         | 128                       |
| A12        | 2             | /30         | 4                         |
| A13        | 212           | /24         | 256                       |
| A14        | 2             | /30         | 4                         |
| A15        | 501           | /23         | 512                       |
| A16        | 2             | /30         | 4                         |
| A17        | 121           | /25         | 128                       |
| A18        | 71            | /25         | 128                       |
| **Total**  |               | **/20**     | **3044**                  |

- Langkah kedua yang dilakukan adalah pembagian subnet dengan menggunakan tree:
![Tree](https://user-images.githubusercontent.com/94432967/204087639-35df1137-566b-4db7-8e26-807391f86822.png)

Untuk gambar yang lebih jelas bisa dilihat [disini](https://miro.com/app/board/uXjVPBQwOeU=/?share_link_id=525325568234)

- Langkah ketiga yang dilakukan adalah konfigurasi subnet dalam CPT yang telah ditentukan dalam tree.

- Langkah keempat yang dilakukan adalah routing.

**The Resonance**
```
10.24.0.64/26 via 10.24.0.5
10.24.8.0/22 via 10.24.0.5
10.24.0.0/30 via 10.24.0.5
10.24.0.16/30 via 10.24.0.5
10.24.2.0/24 via 10.24.0.5
10.24.4.0/23 via 10.24.0.14
10.24.0.128/25 via 10.24.0.22
10.24.0.24/30 via 10.24.0.22
10.24.3.0/24 via 10.24.0.22
10.24.0.28/30 via 10.24.0.22
10.24.6.0/23 via 10.24.0.22
10.24.0.32/30 via 10.24.0.22
10.24.1.0/25 via 10.24.0.22
10.24.1.128/25 via 10.24.0.22
```
**The Order**
```
0.0.0.0/0 via 10.24.0.6
10.24.8.0/22 via 10.24.0.1
10.24.0.16/30 via 10.24.0.1
10.24.2.0/24 via 10.24.0.1
```
**The Minister**
```
0.0.0.0/0 via 10.24.0.2
10.24.2.0/24 via 10.24.0.18
```
**The Dauntless**
```
0.0.0.0/0 via 10.24.0.17
```
**The Magical**
```
0.0.0.0/0 via 10.24.0.13
```
**The Instrument**
```
0.0.0.0/0 via 10.24.0.21
10.24.1.0/25 via 10.24.0.34
10.24.1.128/25 via 10.24.0.34
10.24.3.0/24 via 10.24.0.26
10.24.0.28/30 via 10.24.0.26
10.24.6.0/23 via 10.24.0.26
```
**The Profound**
```
0.0.0.0/0 via 10.24.0.33
```
**The Firefist**
```
0.0.0.0/0 via 10.24.0.25
10.24.0.28/30 via 10.24.3.2
```
**The Queen**
```
0.0.0.0/0 via 10.24.3.1
```

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

### Routing 
- The Order 
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.64.1
route add -net 10.24.0.0 netmask 255.255.248.0 gw 10.24.8.1
```
- The Resonance 
```
route add -net 10.24.0.0 netmask 255.255.224.0 gw 10.24.64.2
route add -net 10.24.136.0 netmask 255.255.254.0 gw 10.24.132.2
route add -net 10.24.32.0 netmask 255.255.240.0 gw 10.24.130.2
route add -net 10.24.128.0 netmask 255.255.254.0 gw 10.24.130.2
```
- The Minister
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.8.2
route add -net 10.24.4.0 netmask 255.255.255.0 gw 10.24.5.2
```
- The Dauntless
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.5.1
```
- The Queen
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.32.1
```
- The Fire First
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.36.1
route add -net 10.24.33.0 netmask 255.255.255.252 gw 10.24.32.2
```
- The Instrument 
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.130.1
route add -net 10.24.32.0 netmask 255.255.252.0 gw 10.24.36.2
route add -net 10.24.128.0 netmask 255.255.255.0 gw 10.24.129.2
```

- The Magical
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.132.1
```

- The Profound 
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.24.129.1
```
