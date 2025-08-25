# 📚 Plano de Estudos – DevSecOps (Básico ao Avançado)

Este guia cobre desde os fundamentos de segurança em DevOps até pipelines completos com **CI/CD seguro**, **scan de vulnerabilidades** e **gestão de segredos**.

---

## 🔹 Fase 1 – Fundamentos de DevSecOps (1 semana)
**Objetivos:** Entender o conceito e importância.  
- **Teoria:**
  - O que é DevSecOps.
  - Diferença DevOps x DevSecOps.
  - O conceito de *Shift Left Security*.
  - Segurança em cada estágio: **Code → Build → Test → Release → Deploy → Monitor**.
- **Prática:**
  - Analisar ciclo de vida seguro de software (SDLC).
  - Estudar exemplos de ataques comuns (OWASP Top 10).

📌 **Tarefa prática:** Criar diagrama do ciclo DevSecOps com pontos de segurança.

---

## 🔹 Fase 2 – Segurança em Código e Dependências (2 semanas)
**Objetivos:** Detectar falhas cedo no ciclo.  
- **Teoria:**
  - SAST (Static Application Security Testing).
  - Dependency Scanning.
  - Licenças e vulnerabilidades em libs.
- **Prática:**
  - Usar **SonarQube** para análise estática de código.
  - Usar **OWASP Dependency-Check** ou `npm audit` / `pip-audit`.
  - Configurar **pre-commit hooks** para scans automáticos.

📌 **Tarefa prática:** Pipeline CI com SAST + scan de dependências.

---

## 🔹 Fase 3 – Segurança em Containers (2 semanas)
**Objetivos:** Garantir que imagens Docker estejam seguras.  
- **Teoria:**
  - Imagens oficiais vs customizadas.
  - Scanners de imagens (Trivy, Clair, Anchore).
  - Princípio do **least privilege** em containers.
- **Prática:**
  - Rodar `trivy image nginx:latest`.
  - Criar Dockerfile seguro (usuário não-root, multi-stage build).
  - Adicionar scan automático no CI/CD.

📌 **Tarefa prática:** Pipeline que builda imagem + scan automático (Trivy).

---

## 🔹 Fase 4 – Gestão de Segredos (1-2 semanas)
**Objetivos:** Proteger credenciais e variáveis sensíveis.  
- **Teoria:**
  - Problema de segredos hardcoded.
  - Vaults (HashiCorp Vault, AWS Secrets Manager, Sealed Secrets no K8s).
  - Encrypt/Decrypt com Ansible Vault.
- **Prática:**
  - Criar secret no Kubernetes (Sealed Secrets).
  - Usar HashiCorp Vault para armazenar senhas de banco.
  - Configurar CI/CD para puxar segredos dinâmicos.

📌 **Tarefa prática:** Pipeline que busca senha de banco no Vault e injeta no container.

---

## 🔹 Fase 5 – Testes Dinâmicos e Pentest Automatizado (2 semanas)
**Objetivos:** Validar aplicações rodando.  
- **Teoria:**
  - DAST (Dynamic Application Security Testing).
  - Ferramentas: OWASP ZAP, Nikto.
  - Testes de API.
- **Prática:**
  - Rodar scan com OWASP ZAP em aplicação web.
  - Automatizar DAST no pipeline (rodar em ambiente de staging).
  - Gerar relatório de vulnerabilidades.

📌 **Tarefa prática:** Pipeline com DAST rodando antes de deploy em produção.

---

## 🔹 Fase 6 – Segurança em Infraestrutura e Kubernetes (3 semanas)
**Objetivos:** Garantir segurança no ambiente.  
- **Teoria:**
  - Hardening de servidores Linux.
  - RBAC no Kubernetes.
  - Policies: PodSecurityStandards, OPA/Gatekeeper, Kyverno.
- **Prática:**
  - Criar regra RBAC para restringir usuário em namespace.
  - Usar `kube-bench` e `kube-hunter` para checar cluster.
  - Aplicar policies com Kyverno (ex: containers só podem rodar como non-root).

📌 **Tarefa prática:** Cluster K8s com RBAC + policies de segurança aplicadas.

---

## 🔹 Fase 7 – Observabilidade e Resposta a Incidentes (2 semanas)
**Objetivos:** Detectar e responder a ameaças.  
- **Teoria:**
  - SIEM (Security Information and Event Management).
  - Logs de segurança.
  - Monitoramento com Prometheus/Grafana + Loki + Falco.
- **Prática:**
  - Configurar Falco para monitorar eventos suspeitos no K8s.
  - Criar dashboard Grafana com alertas de segurança.
  - Gerar alertas para Slack/Email.

📌 **Tarefa prática:** Alertas quando container tenta rodar como root.

---

## 🔹 Projeto Final – Pipeline DevSecOps Completo (3-4 semanas)
**Objetivos:** Integrar tudo em um **pipeline seguro**.  
- Pipeline `.gitlab-ci.yml` ou GitHub Actions com:  
  - **SAST** → scan de código (SonarQube).  
  - **Dependency Scanning** → libs seguras.  
  - **Container Scan** → imagens Docker com Trivy.  
  - **DAST** → OWASP ZAP em staging.  
  - **Secrets** → via Vault/Sealed Secrets.  
  - **Deploy** → em Kubernetes com RBAC e policies.  
  - **Monitoramento** → Falco + Grafana.  

📌 **Entrega:** Repositório Git com CI/CD seguro, aplicação exemplo e relatórios.

---

# 📅 Cronograma Sugerido
- **Semana 1:** Fundamentos DevSecOps.  
- **Semanas 2-3:** Segurança em código e dependências.  
- **Semanas 4-5:** Containers + segredos.  
- **Semanas 6-7:** DAST + segurança em K8s.  
- **Semanas 8-9:** Observabilidade e incidentes.  
- **Semanas 10-12:** Projeto Final.  

---

