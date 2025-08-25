# 📚 Plano de Estudos Completo – Kubernetes (Básico ao Avançado)

Este plano cobre desde os conceitos fundamentais até tópicos avançados de Kubernetes para orquestração de containers em ambientes reais.

---

## 🔹 Fase 1 – Fundamentos
**Objetivos:** Entender o que é Kubernetes e como funciona.  
- **Teoria:**
  - Problema que o Kubernetes resolve.
  - Conceitos: Cluster, Master, Node, Pod, Container Runtime.
  - Componentes principais:
    - API Server
    - etcd
    - Controller Manager
    - Scheduler
    - Kubelet
    - Kube-proxy
  - Instalações possíveis: Minikube, kind, k3s, cluster gerenciado (EKS, GKE, AKS).
- **Prática:**
  - Instalar **Minikube**.
  - Rodar primeiro pod: `kubectl run nginx --image=nginx`.
  - Ver pods: `kubectl get pods`.

📌 **Tarefa prática:** Subir um pod Nginx e acessar logs.

---

## 🔹 Fase 2 – Objetos Básicos
**Objetivos:** Manipular recursos fundamentais.  
- **Teoria:**
  - Pods
  - ReplicaSets
  - Deployments
  - Namespaces
- **Prática:**
  - Criar `deployment.yaml` para rodar Nginx.
  - Escalar réplicas: `kubectl scale deployment nginx-deploy --replicas=3`.
  - Usar `kubectl describe` para inspecionar objetos.
  - Criar namespace `dev` e rodar app lá.

📌 **Tarefa prática:** Deployment com 3 réplicas do Nginx em namespace `dev`.

---

## 🔹 Fase 3 – Serviços e Configurações
**Objetivos:** Aprender a expor aplicações e gerenciar configs.  
- **Teoria:**
  - Services: ClusterIP, NodePort, LoadBalancer.
  - ConfigMaps e Secrets.
  - Volumes básicos (emptyDir, hostPath).
- **Prática:**
  - Criar `service.yaml` para expor Nginx via NodePort.
  - Usar ConfigMap para configurar app.
  - Criar Secret com senha e injetar em container.
  - Montar volume simples.

📌 **Tarefa prática:** App com variáveis de ambiente vindas de ConfigMap + Secret.

---

## 🔹 Fase 4 – Armazenamento Persistente
**Objetivos:** Lidar com dados persistentes.  
- **Teoria:**
  - Persistent Volumes (PV).
  - Persistent Volume Claims (PVC).
  - StorageClass.
- **Prática:**
  - Criar PVC ligado a PV local.
  - Subir container MySQL com PVC.
  - Testar persistência após recriar o pod.

📌 **Tarefa prática:** Banco MySQL persistente com PVC.

---

## 🔹 Fase 5 – Escalabilidade e Alta Disponibilidade
**Objetivos:** Escalar e tornar aplicações resilientes.  
- **Teoria:**
  - Horizontal Pod Autoscaler (HPA).
  - Liveness e Readiness Probes.
  - Estratégias de atualização (RollingUpdate, Recreate).
- **Prática:**
  - Criar HPA baseado em CPU.
  - Configurar probes de saúde no Nginx.
  - Fazer update de imagem com zero-downtime.

📌 **Tarefa prática:** Deployment com HPA e probes configurados.

---

## 🔹 Fase 6 – Networking e Ingress
**Objetivos:** Trabalhar com tráfego interno e externo.  
- **Teoria:**
  - DNS interno do cluster.
  - Network Policies.
  - Ingress Controller (Nginx Ingress, Traefik).
- **Prática:**
  - Criar Ingress para expor aplicação com domínio fake.
  - Criar Network Policy restringindo acesso ao DB.
  - Testar acesso externo.

📌 **Tarefa prática:** Subir Ingress para app web acessível via `http://meuapp.local`.

---

## 🔹 Fase 7 – Segurança
**Objetivos:** Gerenciar acesso e proteger cluster.  
- **Teoria:**
  - Service Accounts.
  - RBAC (Role-Based Access Control).
  - Secrets e criptografia.
  - Pod Security Standards (ex-PodSecurityPolicy).
- **Prática:**
  - Criar usuário com permissão só para `get pods`.
  - Configurar pod rodando como usuário não-root.
  - Usar Secret para credenciais de banco.

📌 **Tarefa prática:** RBAC para limitar acesso de usuário `dev`.

---

## 🔹 Fase 8 – Observabilidade e Monitoramento
**Objetivos:** Monitorar e diagnosticar aplicações.  
- **Teoria:**
  - Logs e métricas.
  - Ferramentas: Prometheus, Grafana, ELK, Jaeger.
- **Prática:**
  - Usar `kubectl logs` e `kubectl exec`.
  - Instalar Prometheus + Grafana via Helm.
  - Visualizar métricas de pods.

📌 **Tarefa prática:** Dashboard Grafana com métricas do cluster.

---

## 🔹 Fase 9 – Kubernetes Avançado
**Objetivos:** Explorar práticas de produção.  
- **Teoria:**
  - Helm Charts.
  - Operators.
  - CI/CD com Kubernetes.
  - Service Mesh (Istio, Linkerd).
- **Prática:**
  - Deploy app via Helm Chart.
  - Criar pipeline CI/CD (GitHub Actions/Jenkins) com `kubectl apply`.
  - Instalar Istio e criar canary release.

📌 **Tarefa prática:** Fazer deploy de app via Helm com pipeline CI/CD.

---

## 🔹 Projeto Final
**Objetivos:** Integrar tudo em um cluster realista.  
- Criar aplicação completa em Kubernetes:  
  - **Frontend (Nginx ou React)**  
  - **Backend (Node.js/Java/Python)**  
  - **Banco (Postgres/MySQL com PVC)**  
  - **Ingress com domínio fake**  
  - **HPA + probes de saúde**  
  - **RBAC com ServiceAccounts**  
  - **Dashboard com Prometheus + Grafana**  
- Extras:  
  - Deploy via Helm.  
  - Canary release com Istio.  

📌 **Entrega:** Repositório Git com manifests + Helm Charts.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Objetos básicos (Fases 1 e 2).  
- **Semanas 3-4:** Serviços + Configurações (Fase 3).  
- **Semanas 5-6:** Armazenamento + Escalabilidade (Fases 4 e 5).  
- **Semanas 7-8:** Networking + Ingress (Fase 6).  
- **Semanas 9-10:** Segurança + Observabilidade (Fases 7 e 8).  
- **Semanas 11-12:** Kubernetes Avançado + Projeto Final (Fases 9).  

---

