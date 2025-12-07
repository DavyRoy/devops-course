🟦 Ingress Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction — Введение в Ingress

1.1 What is Ingress
•	Механизм маршрутизации HTTP/HTTPS трафика в Kubernetes

1.2 Why Ingress is Needed
•	Одноточечный вход
•	Управление доменами
•	TLS termination

1.3 Ingress vs LoadBalancer vs NodePort
•	NodePort — порт на ноде
•	LoadBalancer — внешний LB
•	Ingress — маршрутизация уровня L7

⸻

⭐ 2. Ingress Controller — Контроллер Ingress

2.1 What is an Ingress Controller
•	Приложение, управляющее Ingress правилами

2.2 Popular Ingress Controllers
•	NGINX Ingress Controller
•	Traefik
•	HAProxy
•	Istio Ingress Gateway (service mesh)

2.3 Installing Ingress Controller
•	Helm
•	manifest install
•	operator install

⸻

⭐ 3. Ingress Resources — Ресурсы Ingress

3.1 Basic Ingress Manifest
•	apiVersion
•	kind: Ingress
•	metadata
•	rules

3.2 HTTP Routing
•	host
•	path
•	backend service

3.3 Path Types
•	Prefix
•	Exact

3.4 Multiple Services
•	Один Ingress → несколько сервисов

⸻

⭐ 4. TLS / HTTPS — SSL для Ingress

4.1 TLS Certificate
•	secretName
•	сертификаты PEM

4.2 Automatic Certificates
•	cert-manager
•	Let’s Encrypt

4.3 Termination Modes
•	edge
•	passthrough

⸻

⭐ 5. Annotations — Аннотации Ingress

5.1 NGINX Annotations
•	rewrite-target
•	rate limiting
•	timeouts
•	sticky sessions

5.2 Traefik Annotations
•	middleware
•	rate limits
•	auth

5.3 Global vs Local Annotations
•	приоритеты настроек

⸻

⭐ 6. Load Balancing — Балансировка через Ingress

6.1 Algorithms
•	round robin
•	weighted
•	least connections

6.2 Health Checks
•	readiness/liveness
•	custom checks

⸻

⭐ 7. Middleware & Plugins

7.1 NGINX Modules
•	auth
•	headers
•	rate-limit

7.2 Traefik Middleware
•	redirectScheme
•	stripPrefix
•	circuitBreaker

7.3 Custom Filters
•	Lua scripts (NGINX)

⸻

⭐ 8. Advanced Ingress Configurations

8.1 Canary Releases
•	weight-based routing
•	header-based routing

8.2 Blue–Green via Ingress
•	два backend’а

8.3 Multi-domain / Multi-tenant
•	different hostnames

8.4 Regex Routing
•	регулярные выражения для path

⸻

⭐ 9. Ingress & Service Mesh

9.1 Istio Gateway
•	ingressgateway pod
•	VirtualService
•	DestinationRule

9.2 Linkerd
•	ingress integration

⸻

⭐ 10. Troubleshooting Ingress

10.1 Debugging
•	describe Ingress
•	logs controller

10.2 Common Problems
•	TLS mismatch
•	wrong annotations
•	controller not installed

10.3 Tools
•	kubectl describe
•	kubectl logs
•	ingress-nginx debug logs