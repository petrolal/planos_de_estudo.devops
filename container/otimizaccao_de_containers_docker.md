# 📦 Plano de Estudos – Otimização de Containers (Docker)

Este guia cobre práticas de **performance, segurança e redução de custos** em containers.

---

## 🔹 Fase 1 – Fundamentos de Containers (1 semana)
**Objetivos:** Reforçar conceitos básicos antes da otimização.  
- **Teoria:**
  - Diferença entre containers e VMs.
  - Como funcionam camadas de imagens (UnionFS).
  - Relação entre kernel, cgroups e namespaces.
- **Prática:**
  - Analisar camadas de imagem (`docker history`).
  - Medir tamanho de imagens (`docker images`).
  - Usar `docker stats` para consumo de recursos.

📌 **Tarefa prática:** Subir imagem oficial (nginx) e medir consumo de CPU/memória.

---

## 🔹 Fase 2 – Imagens Otimizadas (2 semanas)
**Objetivos:** Reduzir tamanho e vulnerabilidades de imagens.  
- **Teoria:**
  - Escolha de base images (alpine, distroless, scratch).
  - Multi-stage builds.
  - Remoção de pacotes desnecessários.
  - Rebuild vs cache.
- **Prática:**
  - Converter Dockerfile para **multi-stage**.
  - Usar `alpine` e `distroless`.
  - Comparar tamanho das imagens.

📌 **Tarefa prática:** Criar imagem Node.js multi-stage 70% menor.

---

## 🔹 Fase 3 – Performance em Containers (2 semanas)
**Objetivos:** Melhorar performance e consumo de recursos.  
- **Teoria:**
  - Limites de recursos (`--cpus`, `--memory`).
  - Uso de **read-only containers**.
  - Estratégias de caching (buildkit, mounts).
- **Prática:**
  - Configurar `docker run` com limites de CPU/RAM.
  - Testar containers `read-only` com volumes separados.
  - Usar **Docker BuildKit** para builds rápidos.

📌 **Tarefa prática:** Subir app com limite de 512MB RAM e 1 CPU.

---

## 🔹 Fase 4 – Segurança de Containers (2 semanas)
**Objetivos:** Minimizar riscos e vulnerabilidades.  
- **Teoria:**
  - Princípio do least privilege.
  - Evitar rodar containers como root.
  - Scan de vulnerabilidades (Trivy, Clair).
  - Capabilities do Linux.
- **Prática:**
  - Ajustar `USER` no Dockerfile.
  - Rodar scan com `trivy image`.
  - Remover capabilities extras (`--cap-drop`).

📌 **Tarefa prática:** Container Node.js rodando como usuário sem privilégios.

---

## 🔹 Fase 5 – Redes e Volumes (1 semana)
**Objetivos:** Otimizar conectividade e persistência.  
- **Teoria:**
  - Redes Docker (bridge, host, overlay).
  - Overhead de NAT.
  - Otimização de volumes (tmpfs, drivers nativos).
- **Prática:**
  - Criar rede `bridge` customizada.
  - Usar volume `tmpfs` para cache.
  - Testar performance entre `bridge` vs `host`.

📌 **Tarefa prática:** Lab comparando latência de rede entre containers.

---

## 🔹 Fase 6 – Observabilidade e Troubleshooting (2 semanas)
**Objetivos:** Monitorar e ajustar containers em produção.  
- **Teoria:**
  - Logs (`docker logs`, drivers de log).
  - Métricas (`docker stats`, cAdvisor).
  - Ferramentas: sysdig, dive.
- **Prática:**
  - Analisar imagem com `dive`.
  - Monitorar métricas com cAdvisor + Grafana.
  - Usar `docker events` para debugging.

📌 **Tarefa prática:** Criar dashboard Grafana para métricas de containers.

---

## 🔹 Fase 7 – Orquestração e Escalabilidade (2 semanas)
**Objetivos:** Aplicar otimização em clusters.  
- **Teoria:**
  - Estratégias de escalabilidade no Docker Swarm e Kubernetes.
  - Pod autoscaling (HPA).
  - Requests vs Limits no Kubernetes.
- **Prática:**
  - Deploy de app no K8s com `resources.requests` e `resources.limits`.
  - Medir impacto em autoscaling.
  - Ajustar tuning de pods.

📌 **Tarefa prática:** App em K8s com autoscaling baseado em CPU.

---

## 🔹 Projeto Final – Container Otimizado (2-3 semanas)
**Objetivos:** Construir aplicação containerizada otimizada e segura.  
- Imagem:
  - Multi-stage build (mínima e sem root).  
  - Scan de vulnerabilidades automatizado.  
- Runtime:
  - Recursos limitados (CPU/RAM).  
  - Containers read-only.  
  - Volumes otimizados.  
- Observabilidade:
  - Logs centralizados.  
  - Métricas de consumo no Grafana.  
- Deploy:
  - App rodando em Kubernetes com autoscaling.  

📌 **Entrega:** Repositório Git com Dockerfile + manifests + dashboards.

---

# 📅 Cronograma Sugerido
- **Semana 1:** Fundamentos de containers.  
- **Semanas 2-3:** Imagens otimizadas.  
- **Semanas 4-5:** Performance + segurança.  
- **Semana 6:** Redes e volumes.  
- **Semanas 7-8:** Observabilidade + troubleshooting.  
- **Semanas 9-10:** Orquestração + Projeto Final.  

---

