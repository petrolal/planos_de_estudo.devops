# 📚 Plano de Estudos Completo – Terraform (Básico ao Avançado)

Este plano cobre desde os fundamentos de IaC (Infrastructure as Code) até a automação avançada com Terraform em nuvem (AWS/GCP/Azure).

---

## 🔹 Fase 1 – Fundamentos de IaC e Terraform
**Objetivos:** Entender o que é IaC e configurar ambiente.  
- **Teoria:**
  - O que é IaC (Infrastructure as Code).
  - Conceitos: Declarativo x Imperativo.
  - Terraform x Ansible x CloudFormation.
  - Instalação do Terraform.
- **Prática:**
  - `terraform -v`
  - Criar primeiro arquivo `main.tf` com provider `local`.
  - Executar ciclo: `terraform init`, `terraform plan`, `terraform apply`.

📌 **Tarefa prática:** Criar um `main.tf` que gera um arquivo local usando `local_file`.

---

## 🔹 Fase 2 – Providers, Resources e State
**Objetivos:** Trabalhar com recursos básicos e entender o state.  
- **Teoria:**
  - Providers (AWS, Azure, GCP, Docker, Kubernetes…).
  - Recursos (`resource`).
  - Arquivo `terraform.tfstate`.
  - Comandos: `plan`, `apply`, `destroy`.
- **Prática:**
  - Criar recurso no Docker (container Nginx).
  - Criar bucket S3 (AWS) ou storage no GCP.
  - Examinar `terraform.tfstate`.

📌 **Tarefa prática:** Subir um container Docker com Terraform.

---

## 🔹 Fase 3 – Variáveis e Outputs
**Objetivos:** Tornar a infraestrutura reutilizável.  
- **Teoria:**
  - `variables.tf` e `terraform.tfvars`.
  - Tipos de variáveis (string, number, bool, list, map, object).
  - Outputs (`output`).
- **Prática:**
  - Criar variáveis para nome e tamanho de instância EC2.
  - Exportar IP público como `output`.

📌 **Tarefa prática:** Subir EC2 na AWS parametrizada por variáveis.

---

## 🔹 Fase 4 – Módulos
**Objetivos:** Reutilizar infraestrutura em blocos.  
- **Teoria:**
  - Estrutura de módulos.
  - `module` local e remoto (Terraform Registry).
  - Boas práticas de organização.
- **Prática:**
  - Criar módulo para EC2.
  - Reutilizar o mesmo módulo para criar 2 instâncias.
  - Usar módulo pronto do Registry (ex: `vpc` da AWS).

📌 **Tarefa prática:** Criar VPC usando módulo oficial da AWS.

---

## 🔹 Fase 5 – Remote State e Workspaces
**Objetivos:** Gerenciar ambientes e múltiplos times.  
- **Teoria:**
  - Remote State (S3 + DynamoDB para locking).
  - Workspaces (dev, staging, prod).
- **Prática:**
  - Configurar backend remoto (AWS S3).
  - Criar 2 workspaces: `dev` e `prod`.

📌 **Tarefa prática:** Subir instâncias EC2 diferentes para cada workspace.

---

## 🔹 Fase 6 – Provisioners e Integrações
**Objetivos:** Personalizar recursos após criação.  
- **Teoria:**
  - Provisioners: `local-exec` e `remote-exec`.
  - Integração com Ansible e Docker.
- **Prática:**
  - Usar `remote-exec` para instalar pacotes via SSH.
  - Rodar playbook Ansible após criar VM.

📌 **Tarefa prática:** Criar EC2 e instalar Nginx automaticamente com `remote-exec`.

---

## 🔹 Fase 7 – Terraform Avançado
**Objetivos:** Dominar práticas de produção.  
- **Teoria:**
  - Estrutura de repositório (módulos + ambientes).
  - CICD com Terraform (GitHub Actions, Jenkins).
  - Boas práticas: `terraform fmt`, `validate`, `tflint`.
  - Testes de infraestrutura (Terratest).
- **Prática:**
  - Criar pipeline simples no GitHub Actions para rodar `terraform plan`.
  - Validar código com `terraform validate` e `tflint`.

📌 **Tarefa prática:** Criar pipeline de deploy automatizado.

---

## 🔹 Projeto Final
**Objetivos:** Consolidar tudo em um ambiente realista.  
- Criar infraestrutura completa em nuvem com Terraform:  
  - 1 VPC  
  - 2 Subnets (pública e privada)  
  - 1 EC2 web (com Nginx)  
  - 1 RDS (Postgres ou MySQL)  
  - Outputs (IP público, endpoint do banco)  
- Extras:  
  - State remoto (S3 + DynamoDB).  
  - Workspaces (dev/prod).  
  - Integração com Ansible para configurar servidores.  

📌 **Entrega:** Repositório Git com `main.tf`, módulos e documentação.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Providers (Fases 1 e 2).  
- **Semanas 3-4:** Variáveis + Módulos (Fases 3 e 4).  
- **Semanas 5-6:** Remote State + Workspaces (Fase 5).  
- **Semanas 7-8:** Provisioners + Integrações (Fase 6).  
- **Semanas 9-10:** Terraform Avançado (Fase 7).  
- **Semanas 11-12:** Projeto Final.  

---

