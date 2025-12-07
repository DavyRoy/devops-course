🟩 Linkerd Roadmap — Полное структурированное описание всех тем

Linkerd — лёгкий и быстрый service mesh, ориентированный на простоту и безопасность. Более лёгкий, чем Istio.

⸻

⭐ 1. Introduction — Введение в Linkerd

1.1 What is Linkerd?
•	Ультра-лёгкий service mesh
•	Быстрее и проще Istio
•	Архитектура без Envoy (использует Rust-proxy — linkerd2-proxy)

1.2 Why Linkerd?
•	Простота
•	Высокая производительность
•	Малый overhead
•	Built-in mTLS
•	Kubernetes-first

1.3 Key Features
•	Zero-config mTLS
•	Golden metrics
•	Retry policies
•	Traffic splits
•	Multicluster

⸻

⭐ 2. Architecture — Архитектура

2.1 Control Plane
•	controller
•	destination
•	identity
•	proxy-injector
•	tap

2.2 Data Plane
•	linkerd2-proxy sidecar (на Rust)

2.3 No Envoy
•	Быстрее, легче, безопаснее

⸻

⭐ 3. Installation & Setup

3.1 Installation
•	linkerd CLI
•	linkerd install → kubectl apply
•	Helm charts

3.2 Sidecar Injection
•	automatic
•	manual

3.3 Check Tools
•	linkerd check
•	linkerd viz

⸻

⭐ 4. Security

4.1 Automatic mTLS
•	Mutual TLS включен по умолчанию
•	Без ручной настройки сертификатов

4.2 Identity Service
•	SPIFFE identities
•	Cert rotation

4.3 Authorization Policies
•	ServerAuthorization
•	Authz rules

⸻

⭐ 5. Traffic Management

5.1 TrafficSplit
•	Canary
•	Blue-Green
•	Percentage-based routing

5.2 Retries & Timeouts
•	RetryBudget
•	Per-route policies

5.3 Load Balancing
•	EWMA алгоритм (Latency-aware)

5.4 Failover
•	Multi-service failover

⸻

⭐ 6. Observability

6.1 Linkerd Viz
•	Dashboards
•	Service dependency graphs
•	Success rate
•	Latency histograms

6.2 Metrics
•	Prometheus
•	Grafana
•	Golden Metrics (success rate / RPS / latency)

6.3 Tap
•	Реальное время трафика между Pod

⸻

⭐ 7. Linkerd in Kubernetes

7.1 CRDs
•	TrafficSplit
•	Server
•	ServerAuthorization

7.2 Multi-Cluster
•	Gateway
•	Service mirroring

7.3 Sidecar Resource Tuning
•	CPU/memory limits
•	Proxy init containers

⸻

⭐ 8. Multicluster Mesh

8.1 Multi-Cluster Gateway
•	TLS between clusters

8.2 Service Mirror
•	Cross-cluster service discovery

⸻

⭐ 9. Performance Tuning

9.1 Proxy
•	Lightweight Rust proxy
•	Minimal latency overhead

9.2 Control Plane
•	Scale horizontally
•	Tune Prometheus retention

9.3 Cluster Autoscaling
•	Multiple replicas
•	Pod disruption budgets

⸻

⭐ 10. Troubleshooting

10.1 Tools
•	linkerd check
•	linkerd viz
•	tap
•	dashboard

10.2 Common Issues
•	Missing sidecar
•	No identity
•	Expired certificates
•	Misconfigured TrafficSplits

⸻

⭐ 11. Best Practices — Linkerd
•	Использовать TrafficSplit для canary
•	Включить viz + Prometheus
•	Наблюдать golden metrics
•	Следить за certificate TTL
•	Использовать multi-cluster gateway при необходимости
•	Предпочитать Linkerd для простых mesh сценариев