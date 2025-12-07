🟩 NGINX Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение

1.1 What is NGINX
•	HTTP сервер
•	Reverse proxy
•	TCP/UDP load balancer
•	Static CDN server
•	API Gateway (частично)

1.2 Use Cases
•	Балансировка нагрузки
•	SSL termination
•	Reverse Proxy
•	Caching
•	Web acceleration

⸻

⭐ 2. Installation & Setup
•	apt/yum install
•	nginx.conf структура
•	sites-available/sites-enabled

⸻

⭐ 3. Core Concepts
•	worker_processes
•	worker_connections
•	event loop
•	master/worker model

⸻

⭐ 4. HTTP Configuration
•	server {}
•	listen
•	location {}
•	root / alias
•	return
•	rewrite

⸻

⭐ 5. Reverse Proxy
•	proxy_pass
•	upstream {}
•	load balancing algorithms:
•	round-robin
•	least_conn
•	ip_hash

⸻

⭐ 6. SSL/TLS
•	ssl_certificate
•	ssl_protocols
•	LetsEncrypt staging
•	SSL termination

⸻

⭐ 7. Caching
•	proxy_cache
•	cache levels
•	cache keys
•	purge

⸻

⭐ 8. Performance
•	sendfile
•	keepalive
•	gzip
•	rate limiting

⸻

⭐ 9. Security
•	IP Access Rules
•	Basic Auth
•	limit_req / limit_conn
•	WAF (ModSecurity)

⸻

⭐ 10. Observability
•	access_log
•	error_log
•	stub_status
•	prometheus exporters

⸻

⭐ 11. NGINX in Kubernetes
•	Ingress Controller
•	Annotations
•	Nginx Plus features

⸻

⭐ 12. Best Practices
•	Keep config minimal
•	Use includes
•	Enable caching
•	Rate limit abusive clients
