🟫 Envoy Proxy Roadmap — Полное структурированное описание всех тем

⸻

⭐ 1. Introduction
•	L4/L7 proxy, создатель service mesh архитектуры
•	Используется в Istio, Consul Connect, AWS AppMesh

⸻

⭐ 2. Architecture
•	Listeners
•	Filters
•	Clusters
•	Endpoints
•	xDS API (dynamic config)

⸻

⭐ 3. Envoy Configuration
•	Static config
•	Dynamic xDS config
•	Layers: Listener → Filter → Router → Cluster

⸻

⭐ 4. Protocol Support
•	HTTP/1.1
•	HTTP/2
•	gRPC
•	HTTP/3/QUIC

⸻

⭐ 5. Filters
•	HTTP Connection Manager
•	Rate Limiter
•	gRPC-Web filter
•	Buffer filter
•	Lua filter
•	WASM filter

⸻

⭐ 6. Load Balancing
•	round robin
•	least request
•	maglev hash
•	ring hash

⸻

⭐ 7. Resilience
•	Retries
•	Timeouts
•	Circuit breakers
•	Outlier detection

⸻

⭐ 8. Security
•	mTLS
•	JWT auth
•	RBAC filter

⸻

⭐ 9. Observability
•	Access Logs
•	OpenTelemetry
•	Stats sinks
•	Admin interface

⸻

⭐ 10. Service Mesh
•	Istio uses Envoy sidecars
•	Consul Connect
•	Kuma / Kong Mesh

⸻

⭐ 11. Best Practices
•	Use xDS dynamic config
•	Enable retries carefully
•	Enforce mTLS