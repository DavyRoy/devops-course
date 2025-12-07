🌐 Networking Roadmap — Дорожная карта по изучению сетей
⭐ 1. Networking Fundamentals — Основы сетей
1.1 What is a Network — Что такое сеть
Определение компьютерной сети
Локальные (LAN), глобальные (WAN), домашние и корпоративные сети
Клиент-сервер и peer-to-peer модели
1.2 OSI Model — Модель OSI
7 слоёв:
Physical
Data Link
Network
Transport
Session
Presentation
Application
Зачем нужна модель OSI
1.3 TCP/IP Model — Модель TCP/IP
4 слоя:
Link
Internet
Transport
Application
Сопоставление с OSI
1.4 Network Devices — Сетевые устройства
Модем
Сетевые платы (NIC)
Коммутатор (Switch)
Маршрутизатор (Router)
Точка доступа (Access Point)
Межсетевой экран (Firewall)
⭐ 2. Physical & Data Link Layer — Физический и канальный уровень
2.1 Ethernet
MAC-адрес
ARP
Фреймы Ethernet
VLAN (802.1Q)
2.2 Wi-Fi
Стандарты Wi-Fi (802.11a/b/g/n/ac/ax)
SSID, BSSID
WPA2/WPA3
2.3 ARP / RARP
ARP-запросы и ответы
ARP-кэш
ARP spoofing (как атака)
2.4 Switch Features
STP
VLAN
Trunk vs Access режимы
Port Security
⭐ 3. Network Layer — Сетевой уровень
3.1 IP Addressing — IP-адресация
IPv4
IPv6
Частные и публичные IP
3.2 Subnetting — Подсети
Маска подсети
Подсчёт подсетей
CIDR (Classless Inter-Domain Routing)
3.3 Routing — Маршрутизация
Static Routing — статическая
Dynamic Routing — динамическая
Default gateway
Routing tables
3.4 ICMP
ping
traceroute
ICMP-пакеты
⭐ 4. Transport Layer — Транспортный уровень
4.1 TCP — надёжный протокол
Three-way handshake (SYN, SYN/ACK, ACK)
Принцип надёжности (ACK, окна)
Порты TCP
4.2 UDP — ненадёжный протокол
Минимальная задержка
Использование в VoIP, стримах
4.3 Differences TCP vs UDP
Надёжность
Скорость
Области применения
⭐ 5. Application Layer — Прикладные протоколы
5.1 DNS — Domain Name System
A-записи
AAAA
CNAME
MX
PTR
Tools:
dig
nslookup
5.2 HTTP/HTTPS
Get/Post
HTTPS — TLS/SSL
Headers / Cookies
5.3 DHCP
Получение IP
Лизы
DHCP Discover/Offer/Request/Ack
5.4 Email Protocols
SMTP
IMAP
POP3
⭐ 6. Network Security — Сетевая безопасность
6.1 Firewalls — Брандмауэры
iptables
nftables
Windows Firewall
6.2 VPN — Виртуальные частные сети
IPSec
OpenVPN
WireGuard
6.3 IDS/IPS
Intrusion Detection System
Snort / Suricata
6.4 Common attacks
DDoS
MITM
ARP spoofing
DNS poisoning
⭐ 7. Tools & Commands — Утилиты и команды
7.1 Diagnostic Tools — Диагностика
ping
traceroute / tracepath
mtr
netstat / ss
ip addr
ip route
ifconfig (legacy)
7.2 Packet Inspection — Просмотр трафика
tcpdump
wireshark
7.3 Performance & Monitoring
nmap
iperf
Netcat (nc)
⭐ 8. Local Networking — Локальные сети
8.1 DHCP server/client
8.2 Local DNS
dnsmasq
bind
8.3 NAT — Network Address Translation
SNAT
DNAT
PAT (маскарадинг)
8.4 Port Forwarding — проброс портов
⭐ 9. Enterprise Networking — Корпоративные сети
9.1 Routing Protocols — Протоколы маршрутизации
RIP
OSPF
BGP
9.2 VLAN & Trunking
Интер-влан маршрутизация
802.1Q
9.3 QoS — Quality of Service
Полосы пропускания
Приоритет пакетов
⭐ 10. Cloud Networking — Сети облаков
10.1 VPC — виртуальные сети
Subnets
Route tables
Security groups
10.2 Load Balancers
TCP LB
HTTP LB
Reverse proxy (NGINX, HAProxy)
10.3 Peering & Gateways
NAT Gateway
VPC Peering
⭐ 11. Network Automation — Автоматизация сетей
11.1 Infrastructure as Code
Terraform
Ansible
11.2 Network Config Automation
Netmiko
Nornir
⭐ 12. Advanced Topics — Продвинутые темы
12.1 IPv6 Advanced
SLAAC
Link-Local
Tunneling
12.2 SDN — Software Defined Networking
OpenFlow
управления сетями через API
12.3 MPLS — Multiprotocol Label Switching
LSR
LER
LSP
12.4 Zero Trust Networks
Identity-based access
⭐ 13. Best Practices — Лучшие практики
Правильное документирование схем
Использование VLAN для сегментации
Мониторинг и логирование
Минимизация поверхностей атаки
Резервирование важных сервисов
⭐ 14. Practice — Практика
14.1 Build home lab — Лаборатория дома
Router + Switch
VirtualBox / Proxmox
14.2 Configure network services
DHCP
DNS
NAT
14.3 Analyze real traffic
Wireshark
tcpdump
14.4 Simulate networks
Cisco Packet Tracer
GNS3
EVE-NG