🟪 Kong Gateway Roadmap — Полное структурированное описание всех тем

(API Gateway на базе NGINX + Lua)

⸻

⭐ 1. Introduction
•	Enterprise API Gateway
•	Построен на NGINX + Lua
•	Поддерживает Plugins, mTLS, Rate limiting

⸻

⭐ 2. Installation
•	Docker
•	Kubernetes (Ingress Controller mode)
•	DB-backed / DB-less mode

⸻

⭐ 3. Core Concepts
•	Services
•	Routes
•	Plugins
•	Consumers
•	Upstreams

⸻

⭐ 4. Routing
•	Path-based
•	Host-based
•	Headers-based
•	Regex routes

⸻

⭐ 5. Plugins

Security:
•	KeyAuth
•	JWT
•	OAuth2
•	mTLS

Traffic:
•	Rate Limiting
•	Request Transformer
•	Response Transformer
•	IP Restriction

Observability:
•	Prometheus
•	Zipkin
•	OpenTelemetry

Enterprise:
•	RBAC
•	Dev Portal

⸻

⭐ 6. Load Balancing (Upstreams)
•	Health checks
•	Active / Passive checks
•	Circuit breakers

⸻

⭐ 7. Kong in Kubernetes
•	Kong Ingress Controller
•	Gateway API support
•	CRDs:
•	KongIngress
•	KongPlugin
•	KongConsumer

⸻

⭐ 8. Security
•	ACL
•	CIAM (Enterprise)
•	Vault integration
•	mTLS everywhere

⸻

⭐ 9. Observability
•	Prometheus metrics
•	Distributed tracing
•	Audit logs

⸻

⭐ 10. Best Practices
•	DB-less mode для простоты
•	Centralized API policies
•	Use enterprise plugins for security
•	Keep plugins minimal
