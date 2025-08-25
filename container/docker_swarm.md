# 📘 Plano de Estudos: Docker Swarm

## 🎯 Objetivo
Aprender a usar o Docker Swarm como ferramenta de **orquestração nativa do Docker**, dominando desde os conceitos básicos até a operação de clusters em produção.

---

## 📍 Pré-requisitos
- Conhecimentos básicos de **Docker** (imagens, containers, volumes, networks).
- Noções de **redes** (TCP/IP, DNS, portas, overlay networks).
- Familiaridade com **Linux** (linha de comando, systemd, permissões).

---

## 🟢 Nível Básico

### 1. Introdução
- O que é **Docker Swarm** e por que usar em vez de rodar containers avulsos.  
- Conceito de **Cluster**: manager e workers.  
- Diferença entre **Swarm vs Kubernetes**.  

📚 Estudo sugerido:
- Documentação oficial: [Swarm mode overview](https://docs.docker.com/engine/swarm/).

---

### 2. Conceitos Fundamentais
- Inicializando um cluster (`docker swarm init`).  
- Adicionando nodes (`docker swarm join`).  
- Criando **services** (`docker service create`).  
- Escalando serviços (`docker service scale`).  

---

### 3. Deploy Básico
- Criar seu primeiro serviço **replicado** (ex: Nginx).  
- Testar escalabilidade aumentando e reduzindo réplicas.  
- Ver status dos nós: `docker node ls`.  
- Ver status dos serviços: `docker service ls`.

---

## 🟡 Nível Intermediário

### 4. Redes no Swarm
- **Overlay networks** e comunicação entre containers em diferentes hosts.  
- **Ingress network** e balanceamento de carga automático.  
- Configuração de portas publicadas (`-p`).  

---

### 5. Stacks e Compose
- Deploy de aplicações com **Docker Stack** (`docker stack deploy`).  
- Diferença entre `docker-compose.yml` e `stack.yml`.  
- Escalando múltiplos serviços em conjunto.  

---

### 6. Persistência de Dados
- Volumes no Swarm.  
- Estratégias para storage distribuído (NFS, GlusterFS, Portworx).  
- Bind mounts vs named volumes.  

---

### 7. Configs e Secrets
- Gerenciamento de **Docker secrets** (senhas, chaves, tokens).  
- **Docker configs** para arquivos de configuração.  
- Usando secrets e configs em serviços.  

---

## 🔴 Nível Avançado

### 8. Estratégias de Deploy
- Rolling updates (`--update-parallelism`, `--update-delay`).  
- Rollback de serviços (`docker service rollback`).  
- Políticas de restart (`--restart-condition`).  

---

### 9. Monitoramento e Logs
- Logs de serviços (`docker service logs`).  
- Monitoramento com **Docker Swarm Visualizer**.  
- Integração com **Prometheus + Grafana**.  
- Alertas e métricas de cluster.  

---

### 10. Segurança
- Comunicação segura com **TLS automático** no Swarm.  
- Controle de acesso aos nodes.  
- Práticas de hardening em produção.  

---

### 11. Alta Disponibilidade
- Múltiplos managers (RAFT consensus).  
- Failover automático.  
- Estratégias de resiliência.  

---

### 12. Casos de Uso Avançados
- Deploy de aplicações reais (WordPress + MySQL, microservices).  
- Blue/Green Deployment em Swarm.  
- Comparação prática com Kubernetes para migração futura.  

---

## 🛠️ Projeto Final
1. Montar um **cluster Swarm com 3 nós** (1 manager + 2 workers).  
2. Deploy de uma aplicação multi-serviço com **Docker Stack** (ex: frontend, backend, banco de dados).  
3. Configurar **rede overlay** + **secret** para senhas.  
4. Fazer **rolling update** do backend sem downtime.  
5. Monitorar com **Prometheus + Grafana**.  

---

## 📅 Sugestão de Cronograma
- **Semana 1**: Conceitos e cluster básico.  
- **Semana 2**: Redes, volumes e stacks.  
- **Semana 3**: Secrets, updates e monitoramento.  
- **Semana 4**: Segurança, alta disponibilidade e projeto final.  

