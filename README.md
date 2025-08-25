# 🚀 Roadmap DevOps – Do Zero ao Avançado

Este roadmap foi criado para organizar um **plano completo de estudos para se tornar DevOps Engineer**, baseado em práticas reais do mercado e nas exigências mais comuns em **vagas de emprego**.  

A trilha vai desde **fundamentos de Linux e Redes** até **Kubernetes, Cloud, Observabilidade, DevSecOps e SRE**.  
O foco é **mão na massa**: cada módulo tem teoria + prática + projeto.

---

## 📌 Pré-requisitos
Antes de iniciar, é importante ter:
- Noções de **programação** (Python, JavaScript ou Shell Script).  
- Familiaridade com **Git** e controle de versão.  
- Vontade de aprender **linha de comando**.  

---

## 🧭 Estrutura do Roadmap

### 🔹 1. Mentalidade DevOps
- Cultura e princípios DevOps (CALMS).  
- Quebra de silos → Dev + Ops + Sec juntos.  
- Infra como Código, Automação e Feedback Contínuo.  
- Leitura: *The Phoenix Project* e *The DevOps Handbook*.  

📄 [Plano Mentalidade DevOps](#)

---

### 🔹 2. Linux (4 semanas)
- Fundamentos do sistema, usuários, permissões.  
- Processos, pacotes, discos, redes.  
- Shell Script e automação.  
- **Projeto:** Servidor Linux com usuários, firewall e serviço web.  

📄 [Plano Linux](#)

---

### 🔹 3. Redes de Computadores (4 semanas)
- Modelo OSI/TCP-IP, IPv4/IPv6.  
- Roteamento, NAT, firewall.  
- Testes com ping, traceroute, tcpdump.  
- **Projeto:** Lab com roteador Linux + firewall + cliente/servidor.  

📄 [Plano Redes](#)

---

### 🔹 4. Virtualização com Vagrant (2 semanas)
- Conceitos de VM vs Containers.  
- Criação de múltiplas VMs com provisionamento.  
- Redes privadas e públicas.  
- **Projeto:** VM web + VM banco conectadas em rede interna.  

📄 [Plano Vagrant](#)

---

### 🔹 5. Contêineres – Docker (4 semanas)
- Fundamentos de imagens e containers.  
- Volumes, redes, Docker Compose.  
- Multi-stage builds e segurança.  
- **Projeto:** Stack web + banco + proxy reverso com Compose.  

📄 [Plano Docker](#)

---

### 🔹 6. Automação – Ansible (4 semanas)
- Inventários, playbooks e roles.  
- Variáveis, templates, handlers.  
- Integrações com Docker, Terraform, K8s.  
- **Projeto:** Infra automatizada com web + banco + load balancer.  

📄 [Plano Ansible](#)

---

### 🔹 7. Infraestrutura como Código – Terraform (4 semanas)
- Providers, resources e state.  
- Variáveis, outputs e módulos.  
- Remote State + Workspaces.  
- **Projeto:** Subir app completo (VPC + EC2 + RDS) em nuvem.  

📄 [Plano Terraform](#)

---

### 🔹 8. Cloud Computing (AWS, Azure, GCP) (6-8 semanas)
- Fundamentos: Regiões, IAM, Redes, Storage, Compute.  
- AWS: EC2, S3, RDS, VPC, IAM.  
- Azure: Resource Groups, VMs, VNets, Key Vault, AKS.  
- GCP: Compute Engine, Cloud Storage, Pub/Sub, GKE.  
- **Projeto:** Deploy de aplicação multi-tier em cloud (EC2/App Service/Compute Engine).  

📄 [Plano AWS](#) | [Plano Azure](#) | *(GCP opcional)*  

---

### 🔹 9. Orquestração – Kubernetes (6 semanas)
- Pods, Deployments, Services, ConfigMaps, Secrets.  
- Persistência (PVC, StorageClass).  
- HPA, Probes e Updates.  
- Ingress e RBAC.  
- **Projeto:** App full-stack (frontend + backend + DB) em K8s.  

📄 [Plano Kubernetes](#)

---

### 🔹 10. CI/CD (GitLabCI, Jenkins, GitHub Actions, ArgoCD) (6 semanas)
- Pipelines multi-stage: build, test, deploy.  
- Runners, artefatos e cache.  
- Deploy automatizado em Docker/K8s.  
- GitOps com ArgoCD.  
- **Projeto:** Pipeline completo (build → test → security → deploy em K8s).  

📄 [Plano GitLabCI](#)

---

### 🔹 11. Observabilidade (4-6 semanas)
- Métricas com Prometheus.  
- Dashboards com Grafana.  
- Logs: ELK/EFK, Loki.  
- Tracing: Jaeger, Tempo.  
- **Projeto:** Stack observability monitorando aplicação + cluster.  

📄 [Plano Prometheus + Grafana](#)

---

### 🔹 12. DevSecOps (4-6 semanas)
- SAST, DAST e Dependency Scanning.  
- Scan de imagens Docker (Trivy).  
- Gestão de segredos (Vault, Key Vault, Sealed Secrets).  
- Policies de segurança em K8s (RBAC, Kyverno).  
- **Projeto:** Pipeline CI/CD com segurança integrada em todas as fases.  

📄 [Plano DevSecOps](#)

---

### 🔹 13. Virtualização Avançada – Proxmox (opcional, 6 semanas)
- KVM, LXC, redes, storage.  
- Cluster + HA + Ceph.  
- Integração com Ansible e Terraform.  
- **Projeto:** Cluster Proxmox com HA + automação IaC.  

📄 [Plano Proxmox](#)

---

### 🔹 14. Complementos Importantes
- **Mensageria**: Kafka, RabbitMQ, SQS.  
- **Service Mesh**: Istio, Linkerd.  
- **CI/CD alternativos**: GitHub Actions, Jenkins, ArgoCD.  
- **Multi-cloud**: AWS + Azure + GCP.  

---

### 🔹 15. SRE – Site Reliability Engineering (4 semanas)
- Conceitos de SLO, SLI e Error Budgets.  
- Automação de incidentes.  
- Postmortems sem culpa (*blameless*).  
- Monitoramento focado em confiabilidade.  
- **Projeto:** Definir SLIs e SLOs para aplicação e configurar alertas.  

---

## 📅 Linha do Tempo (12 meses sugeridos)
- **Mês 1-2:** Linux + Redes.  
- **Mês 3:** Vagrant + Docker.  
- **Mês 4:** Ansible.  
- **Mês 5:** Terraform.  
- **Mês 6-7:** Cloud (AWS/Azure/GCP).  
- **Mês 8-9:** Kubernetes.  
- **Mês 10:** CI/CD (GitLabCI/Jenkins).  
- **Mês 11:** Observabilidade + DevSecOps.  
- **Mês 12:** Projeto Final + SRE.  

---

## 🏁 Projeto Final – DevOps Lab Completo
- **Infra**: Provisionada com Terraform em Cloud (AWS/Azure/GCP).  
- **Configuração**: Ansible para setup de VMs e serviços.  
- **Containers**: Docker + Kubernetes (EKS/AKS/GKE).  
- **CI/CD**: Pipeline GitLabCI/Jenkins com testes e deploy automatizado.  
- **Segurança**: Scans de código, containers e policies de segurança.  
- **Observabilidade**: Prometheus + Grafana + ELK/EFK + Falco.  
- **SRE**: Definição de SLIs/SLOs + alertas + postmortems.  

📌 **Entrega final:** Repositório GitHub documentado com todos os labs, IaC, pipelines e diagramas.

---

## 🔑 Dicas de Estudo
- Estude **todo dia** (mesmo 30min já ajuda).  
- Documente tudo no seu **GitHub** → serve como portfólio.  
- Monte **mini-projetos semanais** aplicando o conteúdo.  
- Leia sempre as **documentações oficiais**.  
- Participe de comunidades DevOps (Slack, Discord, Fóruns).  

---

