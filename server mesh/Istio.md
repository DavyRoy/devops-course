🟦 Istio Roadmap — Полное структурированное описание всех тем

Istio — самый популярный service mesh, основанный на Envoy Proxy, предоставляет: mTLS, RBAC, Observability, Routing, Policies.

⸻

⭐ 1. Introduction — Введение в Istio

1.1 What is Istio?
•	Service Mesh для Kubernetes
•	Управляет сервис-к-сервис коммуникацией
•	Использует Envoy sidecars
•	Обеспечивает безопасность, наблюдаемость, маршрутизацию

1.2 Why Istio?
•	Полный контроль сетевого уровня
•	Автоматический mTLS
•	A/B testing
•	Canary / Blue-Green
•	Tracing + Metrics
•	Circuit Breaking

1.3 Istio Components
•	Pilot (конфигурация для Envoy)
•	Citadel (security / certificates)
•	Galley (validation, legacy)
•	IngressGateway / EgressGateway
•	Envoy sidecar

⸻

⭐ 2. Architecture — Архитектура Istio

2.1 Control Plane
•	Istiod
•	Service Registry
•	Configuration Distribution

2.2 Data Plane
•	Envoy sidecars
•	Ingress Gateway
•	Egress Gateway

2.3 xDS API
•	Pilot конфигурирует Envoy через xDS

⸻

⭐ 3. Installation & Setup

3.1 Installation Options
•	Istioctl
•	Helm
•	Istio Operator

3.2 Profiles
•	minimal
•	default
•	demo
•	production

3.3 Sidecar Injection
•	automatic injection
•	manual injection

⸻

⭐ 4. Networking in Istio

4.1 VirtualService
•	HTTP routing
•	Match rules
•	Traffic splitting
•	Retries
•	Timeouts

4.2 DestinationRule
•	Subsets
•	Load balancing
•	Circuit breaking
•	Outlier detection

4.3 Gateways
•	Ingress Gateway
•	Egress Gateway

4.4 ServiceEntry
•	External services declaration

4.5 Envoy Filters
•	WASM filters
•	Custom logic

⸻

⭐ 5. Security

5.1 mTLS
•	Automatic encryption
•	Strict mode
•	Permissive mode

5.2 Authentication Policies
•	PeerAuthentication
•	RequestAuthentication (JWT)

5.3 Authorization Policies (RBAC)
•	Allow/Deny rules
•	Conditions (paths, methods, principals)

5.4 Certificates
•	Rotations
•	SPIFFE identities

⸻

⭐ 6. Traffic Management

6.1 Routing
•	Path-based
•	Header-based
•	Regex-based routing

6.2 Load Balancing Modes
•	ROUND_ROBIN
•	LEAST_CONN
•	RANDOM
•	PASSTHROUGH

6.3 Fault Injection
•	Delay
•	Abort
•	Chaos testing

6.4 Canary / A/B Testing
•	Traffic percent splits
•	Subset routing

6.5 Circuit Breaking
•	max_connections
•	outlier detection

⸻

⭐ 7. Telemetry & Observability

7.1 Metrics
•	Prometheus
•	Grafana dashboards

7.2 Logging
•	Access logs from Envoy
•	Gateway logs

7.3 Tracing
•	Jaeger
•	Zipkin
•	OpenTelemetry

7.4 Kiali
•	Service graph
•	Traffic visualization
•	Error maps

⸻

⭐ 8. Istio in Production

8.1 Multi-cluster
•	Same network
•	Cross-network mesh
•	Primary/remote pattern

8.2 Performance Tuning
•	Sidecar resource tuning
•	Envoy filter tuning
•	Proxy config

8.3 Security Best Practices
•	Strict mTLS
•	Minimal authorization policies
•	Strong JWT validation

⸻

⭐ 9. Troubleshooting

9.1 Common Issues
•	Sidecar injection issues
•	mTLS mismatch
•	Missing VirtualService routes
•	Outlier ejections

9.2 Tools
•	istioctl analyze
•	Envoy admin console
•	Kiali service map

⸻

⭐ 10. Best Practices — Istio
•	Включать strict mTLS
•	Использовать DestinationRule subsets
•	Canary deployments через VirtualService
•	Минимализм в полисах
•	Контролировать Envoy ресурсы
•	Использовать Kiali для мониторинга