# 📊 Monitoring

Monitoring helps us keep an eye on our systems to ensure they are working properly.

### 🎯 Purpose
Maintaining the **health**, **performance**, and **security** of IT environments. It enables early detection of issues, ensuring they can be addressed before causing downtime or data loss.

---

## ✅ Why Do We Use Monitoring?

- **Detect Problems Early**
- **Measure Performance**
- **Ensure Availability**

---

## 🔭 Does Observability Cover Monitoring?

Yes! **Monitoring is a subset of Observability.**

- Observability is a broader concept that includes monitoring as one of its components.
- Monitoring focuses on tracking specific metrics and alerting on predefined conditions.
- Observability provides a **comprehensive understanding** of the system by collecting and analyzing **metrics, logs, and traces**.

---

# Monitoring

## Metrics vs Monitoring

Metrics are measurements or data points that tell you what is happening. For example, the number of steps you walk each day, your heart rate, or the temperature outside—these are all metrics.

Monitoring is the process of keeping an eye on these metrics over time to understand what’s normal, identify changes, and detect problems. It's like watching your step count daily to see if you're meeting your fitness goal or checking your heart rate to make sure it's in a healthy range.

---

## 📦 Categories of Monitoring (with Prometheus Metric Examples)

| Category                  | What’s Monitored                                      | Prometheus Metric Examples                     | Exporter/Tool              |
|---------------------------|-------------------------------------------------------|------------------------------------------------|----------------------------|
| **Infrastructure Monitoring** | CPU, memory, disk, network on nodes                   | `node_cpu_seconds_total`, `node_memory_MemAvailable_bytes`, `node_disk_read_bytes_total`, `node_network_receive_bytes_total` | `node_exporter` |
| **Application Monitoring (APM)** | Response times, error rates, request throughput     | `http_requests_total`, `http_request_duration_seconds`, `process_cpu_seconds_total` | Instrumented via OpenTelemetry or Prometheus client libs |
| **Database Monitoring**   | Query latency, active connections, cache hits         | `pg_stat_activity`, `pg_stat_database_blks_hit`, `pg_locks`, `pg_up` | `postgres_exporter` |
| **Network Monitoring**    | Latency, packet loss, DNS, HTTP/ICMP uptime           | `probe_success`, `probe_duration_seconds`, `probe_dns_lookup_time_seconds` | `blackbox_exporter` |
| **Security Monitoring**   | Auth failures, suspicious activity (numeric counters) | Custom metrics or logs via tools like `wazuh_alerts_total`, `auditd_syscalls_total` | SIEM, AuditD, Wazuh, Falco |

## 👀 What Can Be Observed?

- **Logs**: Detailed records of events and transactions within the system  
- **Metrics**: Quantitative data points like CPU load, memory consumption, request counts  
- **Traces**: Data that shows the flow of requests through various services and components  

---

## 🚀 Why Observability Is Important?

Suppose you're hosting an application in your VPC on a Kubernetes cluster in AWS.  
If you want to bring in new potential customers, what do you show them?

You present your **Service Level Agreement (SLA)** and define your **objectives**:

- ✅ 99.9% availability  
- ✅ Out of 10,000 API requests, 9,995 return HTTP 200 (success), with only 5 failing

If you dont meet then it could be a problem for the company who took the contract.
---

## 👨‍💻 Who Is Responsible for Observability?

**Both Developers and DevOps/SRE Engineers share the responsibility.**

- **Developers**: Instrument the application with metrics, logs, and traces using tools like **OpenTelemetry**
- **DevOps/SRE**: Set up and maintain observability tools like:
  - **Prometheus** (metrics)
  - **ELK/EFK Stack** (logs)
  - **Jaeger** (traces)

---

## ⚒️ What Are the Tools Available?

### 🔧 Monitoring Tools:
- **Prometheus**
- **Grafana**
- **Nagios**
- **Zabbix**
- **PRTG**
- **Fluent Bit**

## 📦 Monitoring Tool References

---

### 📡 Prometheus

Learn what Prometheus is, understand its architecture, and see how to install and configure it on an EKS cluster.  
This reference covers:

- Prometheus architecture & components
- Metric types (Counter, Gauge, Histogram, Summary)
- Exporters (e.g., Node Exporter, Kube-State-Metrics)
- Setting up Prometheus on EKS via Helm
- Scraping application and infrastructure metrics

- 🔗 [Prometheues Reference)](docs/prometheus.md)
---

### 📊 Grafana

Learn about Grafana, how it connects with Prometheus and other data sources, and how to visualize metrics in dashboards.  
This reference includes:

- Grafana architecture
- Installing Grafana on EKS
- Accessing Grafana UI and setting up data sources
- Creating, importing, and customizing dashboards
- Configuring alerts and role-based access control

- 🔗 [Grafana Reference)](docs/grafana.md)
---

