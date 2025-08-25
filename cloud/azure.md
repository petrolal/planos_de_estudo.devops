# 📚 Plano de Estudos – Azure (Básico ao Avançado)

Este guia cobre desde os fundamentos do Microsoft Azure até automação, segurança e DevOps.

---

## 🔹 Fase 1 – Fundamentos do Azure (2 semanas)
**Objetivos:** Conhecer a plataforma e seus conceitos básicos.  
- **Teoria:**
  - O que é Cloud Computing (IaaS, PaaS, SaaS).
  - Estrutura do Azure: Regiões, Resource Groups e Subscriptions.
  - Ferramentas de acesso: Azure Portal, CLI, PowerShell.
- **Prática:**
  - Criar conta gratuita do Azure.
  - Explorar o **Azure Portal**.
  - Instalar e configurar **Azure CLI**.
  - Rodar comandos simples (`az group create`, `az vm list`).

📌 **Tarefa prática:** Criar Resource Group e VM simples via Azure CLI.

---

## 🔹 Fase 2 – Identidade e Acesso (1 semana)
**Objetivos:** Aprender controle de acesso.  
- **Teoria:**
  - Azure Active Directory (AAD).
  - RBAC (Role-Based Access Control).
  - Service Principals e Managed Identities.
- **Prática:**
  - Criar usuário AAD.
  - Configurar RBAC para dar acesso somente a um Resource Group.
  - Criar Service Principal para uso em automação.

📌 **Tarefa prática:** Criar usuário com permissões limitadas a Storage Accounts.

---

## 🔹 Fase 3 – Computação (3 semanas)
**Objetivos:** Provisionar workloads no Azure.  
- **Teoria:**
  - Azure Virtual Machines.
  - Escalabilidade: Scale Sets e Load Balancers.
  - App Services (Web Apps).
  - Serverless: Azure Functions.
- **Prática:**
  - Criar VM Linux no Azure.
  - Configurar Load Balancer com 2 VMs.
  - Subir aplicação em **Azure App Service**.
  - Criar Azure Function simples.

📌 **Tarefa prática:** Webserver em App Service com banco no Azure SQL.

---

## 🔹 Fase 4 – Armazenamento e Bancos de Dados (2-3 semanas)
**Objetivos:** Gerenciar dados no Azure.  
- **Teoria:**
  - Azure Storage: Blob, File, Queue, Table.
  - Azure SQL Database.
  - CosmosDB (NoSQL).
- **Prática:**
  - Criar Storage Account com container de Blobs.
  - Subir arquivos com CLI.
  - Criar Azure SQL e conectar via VM.
  - Testar CosmosDB com API MongoDB.

📌 **Tarefa prática:** Aplicação que salva arquivos no Blob Storage e consulta dados no SQL Database.

---

## 🔹 Fase 5 – Redes e Segurança (3 semanas)
**Objetivos:** Entender VNet e segurança de rede.  
- **Teoria:**
  - Virtual Network (VNet).
  - Subnets, NSG (Network Security Group) e Firewalls.
  - Azure VPN Gateway e ExpressRoute.
- **Prática:**
  - Criar VNet com 2 subnets.
  - Configurar NSG permitindo apenas HTTP e SSH.
  - Deploy de app com frontend público e banco privado.

📌 **Tarefa prática:** Infra com VNet + App Service público + SQL Database privado.

---

## 🔹 Fase 6 – Automação (ARM, Bicep, Terraform) (2-3 semanas)
**Objetivos:** Infra as Code no Azure.  
- **Teoria:**
  - Azure Resource Manager (ARM).
  - Bicep (linguagem declarativa nativa).
  - Terraform com Provider Azure.
- **Prática:**
  - Criar VM com template ARM.
  - Reescrever template em Bicep.
  - Subir VNet + VM + Storage com Terraform.

📌 **Tarefa prática:** Subir stack completa (VM + Storage + SQL) com Terraform.

---

## 🔹 Fase 7 – Observabilidade e Logging (2 semanas)
**Objetivos:** Monitorar recursos no Azure.  
- **Teoria:**
  - Azure Monitor.
  - Log Analytics.
  - Application Insights.
- **Prática:**
  - Monitorar métricas de CPU e memória de VM.
  - Criar alertas no Azure Monitor.
  - Configurar Application Insights em App Service.

📌 **Tarefa prática:** Dashboard de métricas de App Service + alertas de performance.

---

## 🔹 Fase 8 – DevOps no Azure (3 semanas)
**Objetivos:** Integrar pipelines e Kubernetes.  
- **Teoria:**
  - Azure DevOps (Repos, Pipelines, Boards).
  - AKS (Azure Kubernetes Service).
  - ACR (Azure Container Registry).
- **Prática:**
  - Criar pipeline no **Azure Pipelines** para app Node.js.
  - Fazer build e push de imagem no ACR.
  - Deploy automático no AKS via pipeline.

📌 **Tarefa prática:** Pipeline CI/CD com build + deploy em AKS.

---

## 🔹 Fase 9 – Segurança Avançada (2 semanas)
**Objetivos:** Garantir segurança corporativa.  
- **Teoria:**
  - Azure Key Vault (segredos e chaves).
  - Azure Security Center.
  - Azure Defender.
- **Prática:**
  - Armazenar senha no Key Vault e injetar no App Service.
  - Ativar recomendações do Security Center.
  - Testar vulnerabilidades com Defender.

📌 **Tarefa prática:** App protegido com segredos no Key Vault.

---

## 🔹 Projeto Final – Arquitetura Azure Completa (4 semanas)
**Objetivos:** Montar uma infra realista de produção.  
- Infra:
  - VNet com subnets públicas e privadas.
  - App Service (frontend).
  - Azure SQL (banco).
  - Blob Storage (arquivos).
  - ACR + AKS (containers).
- Extras:
  - Pipeline CI/CD no Azure DevOps.
  - Observabilidade no Azure Monitor.
  - Segredos no Key Vault.

📌 **Entrega:** Repositório Git com Bicep/Terraform + documentação.

---

# 📅 Cronograma Sugerido
- **Meses 1-2:** Fundamentos + IAM + Computação.  
- **Mês 3:** Armazenamento + Redes.  
- **Mês 4:** Automação (ARM/Bicep/Terraform).  
- **Mês 5:** Observabilidade + Azure DevOps.  
- **Mês 6:** Segurança + Projeto Final.  

---

