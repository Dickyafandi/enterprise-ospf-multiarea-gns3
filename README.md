English Version

Enterprise Multi-Router OSPF Routing & Redundancy (GNS3)
Documentation of a mid-scale enterprise network simulation project using GNS3, implementing OSPF (Open Shortest Path First) Area 0 on a multi-router topology with switch and end-host segmentation.

🛠️ Network Topology & Architecture
Routers: 3 Units (R1, R2, R3) configured using the OSPF Area 0 routing protocol.

Switches: 2 Units (Switch1, Switch2) acting as access layer interconnects.

End-Hosts: 3 Host Units (HostA, HostB, HostC) for end-to-end data traffic testing.

📂 Documentation Structure (Screenshots)
Below are the screenshots of the network configuration and verification results:

GNS3 Network Topology:
<img width="1170" height="693" alt="ospf-multi-router-topology" src="https://github.com/user-attachments/assets/7f02d818-e99a-440f-b9da-0cf9aba3ad88" />

(Layout structure of routers, switches, and hosts in GNS3)

OSPF Verification & Routing Table (Router R1):
<img width="877" height="485" alt="ospf-r1-verification-and-routing-table" src="https://github.com/user-attachments/assets/a3cba304-12c0-42a6-b0b4-8b77ff8e6460" />

(Output of show ip ospf neighbor showing FULL/DR status and show ip route displaying OSPF routes labeled with 'O')

End-to-End Ping Success Testing:
<img width="1915" height="416" alt="multi-router-ospf-ping-success" src="https://github.com/user-attachments/assets/63d63549-21d4-4c6d-ae90-024561527a95" />

(Two-way connectivity test successfully traversing subnets from HostA, HostB, and HostC)

⚙️ Core Configuration Summary
OSPF Area 0 Setup: All router interfaces are enabled within the OSPF autonomous system to ensure automated dynamic route exchange.

IP Addressing & Gateway:

Network A (HostA): 192.168.10.0/24 (Gateway R1: 192.168.10.1)

Inter-Router Link: 10.10.12.0/24 & 10.10.23.0/24

Network B (HostB & HostC): 192.168.20.0/24 (Gateway R3: 192.168.20.1)

Troubleshooting Highlights: Resolved R3 interface IP overlapping issues (FastEthernet 0/1 vs FastEthernet 1/0) until connections successfully replied with stability (ttl=61 to ttl=64).

🚀 Usage Instructions
Open the GNS3 application and import the project's topology file.

Start all devices (Routers and Hosts).

Verify OSPF neighbors using the show ip ospf neighbor command in the router CLI.

Versi Bahasa Indonesia

Enterprise Multi-Router OSPF Routing & Redundancy (GNS3)
Dokumentasi proyek simulasi jaringan enterprise skala menengah menggunakan GNS3, mengimplementasikan OSPF (Open Shortest Path First) Area 0 pada topologi multi-router dengan segmentasi switch dan end-host.

🛠️ Topologi & Arsitektur Jaringan
Router: 3 Unit (R1, R2, R3) yang dikonfigurasi menggunakan routing protokol OSPF Area 0.

Switch: 2 Unit (Switch1, Switch2) sebagai penghubung layer akses.

End-Host: 3 Unit Host (HostA, HostB, HostC) untuk pengujian lalu lintas data end-to-end.

📂 Struktur Dokumentasi (Screenshots)
Berikut adalah tangkapan layar hasil konfigurasi dan verifikasi jaringan:

Topologi Jaringan GNS3:
<img width="1170" height="693" alt="ospf-multi-router-topology" src="https://github.com/user-attachments/assets/1280cefc-6823-4a2f-bca3-bb0aba7e51a2" />
(Struktur penataan perangkat router, switch, dan host di GNS3)

Verifikasi OSPF & Routing Table (Router R1):
<img width="877" height="485" alt="ospf-r1-verification-and-routing-table" src="https://github.com/user-attachments/assets/bc02966f-9ed6-4117-8211-7606ee1bce0e" />

(Output show ip ospf neighbor menunjukkan status FULL/DR dan show ip route menampilkan rute OSPF berlabel 'O')

Pengujian End-to-End Ping Success:
<img width="1915" height="416" alt="multi-router-ospf-ping-success" src="https://github.com/user-attachments/assets/1287f5da-71e2-4bd0-9305-af09030cd088" />

(Uji coba konektivitas dua arah sukses melintasi antar-subnet dari HostA, HostB, dan HostC)

⚙️ Ringkasan Konfigurasi Utama
OSPF Area 0 Setup: Seluruh interface router diaktifkan ke dalam autonomous system OSPF untuk memastikan pertukaran rute dinamis berjalan otomatis.

IP Addressing & Gateway:

Network A (HostA): 192.168.10.0/24 (Gateway R1: 192.168.10.1)

Inter-Router Link: 10.10.12.0/24 & 10.10.23.0/24

Network B (HostB & HostC): 192.168.20.0/24 (Gateway R3: 192.168.20.1)

Troubleshooting Highlights: Mengatasi kendala port overlap IP pada interface R3 (FastEthernet 0/1 vs FastEthernet 1/0) hingga koneksi berhasil reply dengan stabil (ttl=61 s.d. ttl=64).

🚀 Cara Penggunaan
Buka aplikasi GNS3 dan impor file topologi proyek ini.

Jalankan seluruh perangkat (Router dan Host).

Lakukan verifikasi tetangga OSPF menggunakan perintah show ip ospf neighbor di CLI router.
