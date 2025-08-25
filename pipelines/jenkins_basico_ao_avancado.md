# 📘 Plano de Estudos: Jenkins (CI/CD)

## 🎯 Objetivo
Aprender Jenkins do zero até o uso avançado em **CI/CD pipelines**, com foco em automação de builds, testes, deploys e integração com ferramentas de DevOps (Docker, Kubernetes, GitLab, SonarQube, etc).

---

## 📍 Pré-requisitos
- Conceitos básicos de **DevOps e CI/CD**.
- Noções de **Git** (branches, hooks, workflows).
- Conhecimento de **Docker** e **Linux**.
- Noções de **Groovy** (para pipelines mais avançados).

---

## 🟢 Nível Básico

### 1) Introdução
- O que é **Jenkins** e papel no CI/CD.  
- Diferença entre Jenkins, GitHub Actions, GitLab CI.  
- Conceito de **Master/Controller** e **Agents**.  

### 2) Instalação
- Instalação em Linux (war, docker, pacotes).  
- Primeira configuração (plugins, admin user).  
- Estrutura de jobs e pipelines.  

### 3) Jobs e Builds
- Criando **Freestyle Jobs**.  
- Integração com Git (Git plugin).  
- Build automático em push.  
- Introdução a **Webhooks** (GitHub/GitLab/Bitbucket).  

---

## 🟡 Nível Intermediário

### 4) Pipelines
- Conceito de Pipeline como código.  
- Diferença **Declarative Pipeline** vs **Scripted Pipeline**.  
- Sintaxe básica (`pipeline { ... }`).  
- Stages e Steps (`stage('Build')`, `steps { ... }`).  

### 5) Integração com Docker
- Rodando builds dentro de containers.  
- Build e publish de imagens Docker.  
- Docker agents (`agent { docker { ... } }`).  

### 6) Integrações Essenciais
- Integração com Maven/Gradle (Java builds).  
- Integração com SonarQube (análise estática).  
- Integração com JUnit (test reports).  
- Integração com Slack/Teams (notificações).  

### 7) Credenciais
- **Jenkins Credentials Store**.  
- `withCredentials` e variáveis de ambiente.  
- Boas práticas para senhas, tokens e SSH keys.  

---

## 🔴 Nível Avançado

### 8) Jenkinsfile Avançado
- Parallel stages.  
- `post` actions (always, success, failure).  
- Uso de `when` e condições (branches, env vars).  
- Reutilização com funções e scripts.  

### 9) Shared Libraries
- Estrutura de reuso (vars/, src/).  
- Chamando steps customizados.  
- Testando libraries com **Pipeline Unit**.  

### 10) Escalabilidade
- Configuração de **agents/nodes** distribuídos.  
- Labels e restrições (`agent { label 'docker' }`).  
- Executores e filas de builds.  

### 11) Segurança
- Permissões e RBAC.  
- Sandboxing de Groovy.  
- Hardening e backup de configuração.  

### 12) Observabilidade
- Logs de build e stages.  
- Integração com **Prometheus + Grafana**.  
- Alertas e métricas de performance.  

---

## 🛠️ Projeto Final
1. Instalar Jenkins em um servidor ou container.  
2. Criar **Pipeline Declarativo** para um microserviço Java com:  
   - build com Maven,  
   - testes JUnit,  
   - análise com SonarQube,  
   - build e push de imagem Docker,  
   - deploy em **Docker Swarm ou Kubernetes**.  
3. Adicionar **notificação no Slack** no final.  
4. Migrar para **Shared Library** para steps comuns.  

---

## 📅 Cronograma de Estudo
- **Semana 1**: Introdução + instalação + Freestyle jobs.  
- **Semana 2**: Pipelines declarativos + integrações (Git, Maven, Docker).  
- **Semana 3**: Jenkinsfile avançado + credenciais + notificações.  
- **Semana 4**: Shared Libraries, escalabilidade, segurança e projeto final.  

---

## 📚 Referências Curadas
- [Jenkins Official Docs](https://www.jenkins.io/doc/)  
- [Jenkins Pipeline Syntax](https://www.jenkins.io/doc/book/pipeline/syntax/)  
- [Jenkins Shared Libraries](https://www.jenkins.io/doc/book/pipeline/shared-libraries/)  
- Livro: *Jenkins 2: Up and Running* (O'Reilly)  

---

## ✅ Checklist de Domínio
- [ ] Instalar e configurar Jenkins.  
- [ ] Criar jobs freestyle e pipelines básicos.  
- [ ] Escrever Jenkinsfiles declarativos.  
- [ ] Usar credenciais de forma segura.  
- [ ] Integrar com Docker, Maven, SonarQube e Slack.  
- [ ] Criar e usar Shared Libraries.  
- [ ] Escalar com múltiplos agents.  
- [ ] Monitorar e aplicar boas práticas de segurança.  

