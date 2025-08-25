# 📘 Plano de Estudos: SonarQube

## 🎯 Objetivo

Aprender a utilizar o **SonarQube** para análise estática de código, integrando-o em pipelines de CI/CD e aplicando boas práticas de qualidade de software.

---

## 📍 Pré-requisitos

- Conhecimento básico de **Git** e **CI/CD**.  
- Experiência com alguma linguagem de programação (Java, JS, Python, etc.).  
- Docker (para rodar SonarQube local).  
- Jenkins/GitLab/GitHub Actions (para integração).  

---

## 🟢 Nível Básico

### 1) Fundamentos de Qualidade de Código

- O que é análise estática.  
- Conceitos: **Code Smells, Bugs, Vulnerabilities, Debt, Coverage**.  
- Métricas principais:  
  - **Coverage**: % de código coberto por testes.  
  - **Duplication**: código duplicado.  
  - **Complexity**: complexidade ciclomática.  
  - **Maintainability Index**.  

### 2) Instalação do SonarQube

- Instalação via **Docker Compose**.  
- Interface Web do SonarQube.  
- Estrutura: Server + Database + (opcional) Agents.  

### 3) Primeiro Projeto

- Criar **token de autenticação**.  
- Rodar análise com **SonarScanner CLI**.  
- Integrar em projeto Java/Maven (`mvn sonar:sonar`).  
- Explorar o dashboard: issues, hotspots, métricas.  

---

## 🟡 Nível Intermediário

### 4) Linguagens Suportadas

- Java, JS/TS, Python, Go, C#, C/C++, PHP etc.  
- Plugins e suporte estendido.  
- Configuração de `sonar-project.properties`.  

### 5) Integração com CI/CD

- **Jenkins**: plugin SonarQube Scanner + stage no Jenkinsfile.  
- **GitLab CI**: integração com `sonar-scanner` ou Maven/Gradle.  
- **GitHub Actions**: action oficial do SonarSource.  

### 6) Qualidade como Gate

- **Quality Gates**: aprovar/reprovar builds.  
- Definir políticas mínimas (ex.: 80% cobertura de testes).  
- Configurar para "break the build" em caso de falha.  

### 7) Test Coverage

- Integração com ferramentas de testes:  
  - Java: JaCoCo.  
  - JS/TS: Jest + lcov.  
  - Python: pytest-cov.  
- Publicar relatórios de cobertura no SonarQube.  

---

## 🔴 Nível Avançado

### 8) Administração e Segurança

- Criar usuários, grupos e permissões.  
- Tokens de API para integração.  
- LDAP/SAML para autenticação corporativa.  

### 9) SonarQube vs SonarCloud

- Diferenças (self-hosted vs SaaS).  
- Casos de uso e custos.  

### 10) Customização

- Criar **Quality Profiles** customizados.  
- Criar **Rules** específicas da empresa.  
- Ajustar severidade e thresholds.  

### 11) Monitoramento e Escalabilidade

- Rodar em cluster (Enterprise).  
- Integração com **Postgres** para persistência.  
- Monitoramento de logs e métricas (Prometheus/Grafana).  

---

## 🛠️ Projeto Final

1. Subir SonarQube com Docker.  
2. Configurar um projeto Java com Maven + JaCoCo.  
3. Integrar no Jenkinsfile:  
   - Build → Testes → SonarQube analysis.  
4. Criar Quality Gate (ex.: 80% coverage).  
5. Configurar notificação no Slack/GitHub PR.  

---

## 📅 Cronograma de Estudo

- **Semana 1**: Conceitos de qualidade + instalação + primeiro projeto.  
- **Semana 2**: CI/CD + Quality Gates + coverage.  
- **Semana 3**: Administração + SonarCloud + customização.  
- **Semana 4**: Projeto final e boas práticas.  

---

## 📚 Referências

- [SonarQube Docs](https://docs.sonarsource.com/sonarqube/latest/)  
- [SonarScanner CLI](https://docs.sonarsource.com/sonarqube/latest/analyzing-source-code/scanners/sonarscanner/)  
- [SonarCloud](https://sonarcloud.io)  
- Livro: *Continuous Code Quality with SonarQube* (Packt)  

---

## ✅ Checklist de Domínio

- [ ] Instalar e rodar SonarQube local.  
- [ ] Rodar análise com SonarScanner.  
- [ ] Integrar em Jenkins/GitLab/GitHub Actions.  
- [ ] Configurar Quality Gates.  
- [ ] Publicar cobertura de testes.  
- [ ] Criar perfis e regras customizadas.  
- [ ] Monitorar e administrar em produção.  
