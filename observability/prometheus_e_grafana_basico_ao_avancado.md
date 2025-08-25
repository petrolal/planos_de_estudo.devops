# 📚 Plano de Estudos Completo – Prometheus & Grafana (Básico ao Avançado)

Este guia cobre desde a instalação do Prometheus e Grafana até dashboards avançados e monitoramento de clusters Kubernetes.

---

## 🔹 Fase 1 – Fundamentos de Monitoramento
**Objetivos:** Entender o que são métricas e por que usar Prometheus + Grafana.  
- **Teoria:**
  - O que são métricas (time series).
  - Diferença entre métricas, logs e traces.
  - Arquitetura do Prometheus:
    - Prometheus Server
    - Exporters
    - Alertmanager
    - Pushgateway
  - Conceito de *pull-based metrics*.
  - Grafana: dashboards e datasources.
- **Prática:**
  - Instalar Prometheus (Docker ou binário).
  - Acessar web UI (`http://localhost:9090`).
  - Consultar métricas básicas (`up`, `node_cpu_seconds_total`).

📌 **Tarefa prática:** Subir Prometheus em Docker e verificar métricas com queries simples.

---

## 🔹 Fase 2 – Prometheus Básico
**Objetivos:** Trabalhar com targets e exporters.  
- **Teoria:**
  - Prometheus scrape jobs.
  - Node Exporter (métricas de sistema).
  - Blackbox Exporter (checagem de endpoints).
- **Prática:**
  - Configurar `prometheus.yml` com job para `node_exporter`.
  - Subir Node Exporter em uma VM.
  - Monitorar CPU, memória e disco.
  - Adicionar Blackbox Exporter para monitorar HTTP/ICMP.

📌 **Tarefa prática:** Monitorar uma VM Linux com Node Exporter.

---

## 🔹 Fase 3 – Grafana Básico
**Objetivos:** Visualizar métricas em dashboards.  
- **Teoria:**
  - Datasources no Grafana.
  - Painéis, queries e variáveis.
  - Reutilização de dashboards da comunidade.
- **Prática:**
  - Instalar Grafana (Docker).
  - Conectar Prometheus como datasource.
  - Criar primeiro dashboard com métricas de CPU e RAM.
  - Importar dashboard pronto da Grafana Labs.

📌 **Tarefa prática:** Criar dashboard customizado mostrando uso de CPU por máquina.

---

## 🔹 Fase 4 – Alertas
**Objetivos:** Configurar alertas com Prometheus e Grafana.  
- **Teoria:**
  - Alertmanager.
  - Regras de alerta (`alert.rules`).
  - Integrações: Slack, Email, PagerDuty.
  - Alertas no Grafana (Alerting v2).
- **Prática:**
  - Configurar Alertmanager.
  - Criar regra de alerta para CPU > 80%.
  - Enviar alerta para Slack/Email.
  - Criar alerta simples no Grafana.

📌 **Tarefa prática:** Receber alerta quando um serviço estiver fora do ar.

---

## 🔹 Fase 5 – Monitorando Aplicações
**Objetivos:** Instrumentar aplicações.  
- **Teoria:**
  - Instrumentação com client libraries (Go, Java, Python, Node.js).
  - Exposição de métricas em `/metrics`.
  - Pushgateway (casos batch jobs).
- **Prática:**
  - Criar app Node.js com biblioteca `prom-client`.
  - Expor métricas em `/metrics`.
  - Configurar Prometheus para coletar.
  - Criar dashboard Grafana com métricas customizadas.

📌 **Tarefa prática:** App Node.js expondo métricas de requisições HTTP.

---

## 🔹 Fase 6 – Prometheus + Grafana no Kubernetes
**Objetivos:** Monitorar clusters.  
- **Teoria:**
  - kube-state-metrics.
  - cAdvisor.
  - Prometheus Operator.
  - Grafana Operator.
- **Prática:**
  - Instalar kube-prometheus-stack via Helm.
  - Monitorar pods, deployments, nodes.
  - Criar dashboards com métricas de cluster.

📌 **Tarefa prática:** Monitorar Kubernetes local (Minikube/Kind) com kube-prometheus-stack.

---

## 🔹 Fase 7 – Observabilidade Avançada
**Objetivos:** Integrar Prometheus + Grafana em produção.  
- **Teoria:**
  - High availability com Prometheus.
  - Long-term storage (Thanos, Cortex, Mimir).
  - Logs + métricas + traces → stack completa (Loki, Tempo, Jaeger).
- **Prática:**
  - Configurar Grafana Loki para logs.
  - Configurar Jaeger/Tempo para traces.
  - Criar dashboard unificado com logs + métricas.

📌 **Tarefa prática:** Dashboard unificado (logs + métricas + traces).

---

## 🔹 Projeto Final
**Objetivos:** Integrar tudo em ambiente realista.  
- Subir stack completa:  
  - Prometheus (com exporters)  
  - Alertmanager (alertas)  
  - Grafana (dashboards)  
  - Loki (logs)  
  - Tempo/Jaeger (traces)  
- Funcionalidades:  
  - Monitoramento de VMs e apps.  
  - Dashboards para CPU/RAM/Disco + app HTTP.  
  - Alertas para Slack.  
  - Dashboard unificado de observabilidade.  

📌 **Entrega:** Repositório Git com `docker-compose.yml` ou manifests Kubernetes para a stack.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Prometheus básico (Fases 1 e 2).  
- **Semanas 3-4:** Grafana básico + alertas (Fases 3 e 4).  
- **Semanas 5-6:** Monitoramento de apps (Fase 5).  
- **Semanas 7-8:** Kubernetes (Fase 6).  
- **Semanas 9-10:** Observabilidade avançada (Fase 7).  
- **Semanas 11-12:** Projeto final.  

---

