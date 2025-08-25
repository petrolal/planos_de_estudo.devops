# 📚 Plano de Estudos – GitLab CI/CD (Básico ao Avançado)

Este guia cobre desde os fundamentos do GitLab CI/CD até pipelines avançados com deploy em Kubernetes e integrações DevSecOps.

---

## 🔹 Fase 1 – Fundamentos de CI/CD no GitLab (1 semana)
**Objetivos:** Entender a base do GitLab CI.  
- **Teoria:**
  - O que é CI/CD e porque usar.
  - Estrutura do `.gitlab-ci.yml`.
  - Conceitos: Jobs, Stages, Runners.
  - Shared runners vs. self-hosted runners.
- **Prática:**
  - Criar repositório no GitLab.
  - Adicionar `.gitlab-ci.yml` com job `echo "Hello GitLab"`.
  - Executar pipeline e entender logs.

📌 **Tarefa prática:** Pipeline inicial com estágio `build` imprimindo mensagem.

---

## 🔹 Fase 2 – Pipelines Básicos (1-2 semanas)
**Objetivos:** Criar pipelines multi-stage.  
- **Teoria:**
  - Variáveis (`variables`, `.gitlab-ci.yml`).
  - Artefatos e cache (`artifacts`, `cache`).
  - Estratégias de dependência (`needs`).
- **Prática:**
  - Criar pipeline com stages: `build`, `test`, `deploy`.
  - Salvar artefatos de build.
  - Usar cache para acelerar builds.

📌 **Tarefa prática:** Pipeline Node.js com `npm install`, `npm test` e `npm run build`.

---

## 🔹 Fase 3 – Runners (1 semana)
**Objetivos:** Configurar e entender GitLab Runners.  
- **Teoria:**
  - Tipos de executores (Shell, Docker, Kubernetes).
  - Tags para runners.
  - Segurança de runners.
- **Prática:**
  - Instalar GitLab Runner local com Docker executor.
  - Vincular runner ao projeto.
  - Rodar pipeline customizado no runner local.

📌 **Tarefa prática:** Pipeline rodando em runner Docker próprio.

---

## 🔹 Fase 4 – Integração com Docker (2 semanas)
**Objetivos:** Usar containers dentro do pipeline.  
- **Teoria:**
  - Uso de `image:` e `services:` no `.gitlab-ci.yml`.
  - Build e push de imagens Docker.
  - GitLab Container Registry.
- **Prática:**
  - Criar pipeline que builda imagem Docker.
  - Fazer push da imagem para o GitLab Registry.
  - Usar imagem no job de deploy.

📌 **Tarefa prática:** Pipeline que builda imagem de app e publica no GitLab Registry.

---

## 🔹 Fase 5 – Deploy Automatizado (2-3 semanas)
**Objetivos:** Automatizar deploy em servidores e Kubernetes.  
- **Teoria:**
  - Deploy SSH remoto.
  - Deploy em Kubernetes.
  - GitOps com GitLab CI.
- **Prática:**
  - Pipeline que faz deploy em servidor via SSH.
  - Pipeline que aplica manifests no Kubernetes (`kubectl apply`).
  - Usar Helm charts no deploy.

📌 **Tarefa prática:** Deploy de aplicação web no Kubernetes via GitLab CI.

---

## 🔹 Fase 6 – CI/CD Avançado (2 semanas)
**Objetivos:** Dominar boas práticas e recursos avançados.  
- **Teoria:**
  - Estratégias: `manual`, `only`, `except`, `rules`.
  - Environments e Review Apps.
  - Pipelines Dinâmicos e Include (`include:`).
- **Prática:**
  - Criar pipeline com aprovação manual antes de `prod`.
  - Usar `rules:` para rodar jobs apenas em `main`.
  - Criar Review Apps no Kubernetes.

📌 **Tarefa prática:** Pipeline com ambientes: `dev → staging → prod`.

---

## 🔹 Fase 7 – DevSecOps e Observabilidade (2 semanas)
**Objetivos:** Integrar segurança e monitoramento ao pipeline.  
- **Teoria:**
  - Scans de vulnerabilidade (SAST, DAST, Dependency Scanning).
  - Container Scanning (Trivy).
  - Monitoramento de pipelines no GitLab.
- **Prática:**
  - Adicionar job de SAST no pipeline.
  - Adicionar job de scan de imagens com Trivy.
  - Configurar relatórios no GitLab.

📌 **Tarefa prática:** Pipeline com build/test/deploy + scan de segurança.

---

## 🔹 Projeto Final – Pipeline Completo (2-3 semanas)
**Objetivos:** Construir um pipeline realista estilo empresa.  
- Criar pipeline multi-stage com:
  - `build`: build de app e imagem Docker.
  - `test`: testes unitários e lint.
  - `security`: scan de código e imagem.
  - `deploy`: deploy em Kubernetes (staging e prod).
- Features:
  - Aprovação manual para produção.
  - Review Apps.
  - Push automático para GitLab Container Registry.
  - Relatórios de segurança.

📌 **Entrega:** `.gitlab-ci.yml` pronto para rodar app em produção.

---

# 📅 Cronograma Sugerido
- **Semana 1:** Fundamentos + Pipelines Básicos (Fases 1 e 2).  
- **Semana 2:** Runners (Fase 3).  
- **Semanas 3-4:** Docker + Registry (Fase 4).  
- **Semanas 5-6:** Deploy Automatizado (Fase 5).  
- **Semana 7:** CI/CD Avançado (Fase 6).  
- **Semana 8:** DevSecOps (Fase 7).  
- **Semanas 9-10:** Projeto Final.  

---

