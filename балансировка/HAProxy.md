🟧 HAProxy Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction
•	Высокопроизводительный TCP/HTTP load balancer
•	Работает на L4 и L7
•	Часто используется в High Availability

⸻

⭐ 2. Architecture
•	frontends
•	backends
•	listeners
•	stick-tables

⸻

⭐ 3. Installation
•	Binary packages
•	HAProxy Enterprise
•	Docker

⸻

⭐ 4. Configuration Basics
•	global
•	defaults
•	frontend
•	backend
•	ACL
•	use_backend rules

⸻

⭐ 5. Load Balancing Algorithms
•	roundrobin
•	leastconn
•	source
•	first
•	random

⸻

⭐ 6. Health Checks
•	http-check
•	tcp-check
•	rise/fall parameters

⸻

⭐ 7. SSL/TLS
•	bind :443 ssl crt /path
•	modern ciphers
•	SNI routing

⸻

⭐ 8. Stick Tables
•	rate limiting
•	DDoS mitigation
•	session persistence

⸻

⭐ 9. Observability
•	stats page
•	Prometheus exporter
•	Logging (Syslog)

⸻

⭐ 10. Performance
•	tune.bufsize
•	tune.maxaccept
•	multi-process mode

⸻

⭐ 11. HA / Fault Tolerance
•	VRRP (Keepalived)
•	Active/passive LB
•	Multi-datacenter LB

⸻

⭐ 12. Best Practices
•	Always use ACLs
•	Use health checks
•	Tune connection limits