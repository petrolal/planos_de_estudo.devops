# 📚 Plano de Estudos – AWS (Básico ao Avançado)

Este guia cobre desde os fundamentos da AWS até arquiteturas avançadas, com foco em **DevOps e infraestrutura como código**.

---

## 🔹 Fase 1 – Fundamentos de Cloud e AWS (2 semanas)
**Objetivos:** Entender o básico da nuvem e da AWS.  
- **Teoria:**
  - Conceitos de **IaaS, PaaS, SaaS**.
  - Regiões e zonas de disponibilidade.
  - Console AWS, CLI e SDKs.
  - Free Tier da AWS.
- **Prática:**
  - Criar conta AWS (Free Tier).
  - Explorar o console.
  - Configurar **AWS CLI**.
  - Rodar comandos simples (`aws s3 ls`, `aws ec2 describe-instances`).

📌 **Tarefa prática:** Criar bucket S3 e enviar arquivos via CLI.

---

## 🔹 Fase 2 – Identidade e Acesso (IAM) (1 semana)
**Objetivos:** Aprender controle de acesso.  
- **Teoria:**
  - IAM Users, Groups e Roles.
  - Policies e JSON.
  - Princípio do menor privilégio.
- **Prática:**
  - Criar usuário IAM com permissões específicas.
  - Gerar Access Keys.
  - Testar permissões com CLI.

📌 **Tarefa prática:** Usuário IAM com permissão só para S3.

---

## 🔹 Fase 3 – Computação (EC2, Lambda) (3 semanas)
**Objetivos:** Criar workloads na nuvem.  
- **Teoria:**
  - EC2 (tipos de instância, AMIs, EBS).
  - Auto Scaling e Load Balancer.
  - Lambda e Serverless.
- **Prática:**
  - Subir instância EC2 Ubuntu.
  - Conectar via SSH.
  - Instalar e rodar Nginx.
  - Criar função Lambda simples (Hello World).

📌 **Tarefa prática:** Webserver em EC2 atrás de Load Balancer.

---

## 🔹 Fase 4 – Armazenamento e Banco de Dados (2-3 semanas)
**Objetivos:** Gerenciar dados na nuvem.  
- **Teoria:**
  - S3 (armazenamento de objetos).
  - EBS (blocos).
  - EFS (arquivos).
  - RDS (bancos gerenciados).
  - DynamoDB (NoSQL).
- **Prática:**
  - Criar bucket S3 para armazenar imagens.
  - Criar RDS MySQL.
  - Testar queries a partir de EC2.
  - Criar tabela DynamoDB.

📌 **Tarefa prática:** App que salva arquivos no S3 e consulta dados no RDS.

---

## 🔹 Fase 5 – Redes e Segurança (3 semanas)
**Objetivos:** Configurar redes privadas e segurança.  
- **Teoria:**
  - VPC, Subnets, Route Tables, Internet Gateway, NAT Gateway.
  - Security Groups e NACLs.
  - VPN e Direct Connect.
- **Prática:**
  - Criar VPC com subnets públicas e privadas.
  - Configurar instância em subnet privada com acesso via NAT.
  - Testar regras de Security Groups.

📌 **Tarefa prática:** Infra de 2 camadas (web pública + banco privado).

---

## 🔹 Fase 6 – Automação (CloudFormation e Terraform) (2-3 semanas)
**Objetivos:** Infra as Code na AWS.  
- **Teoria:**
  - CloudFormation basics.
  - Terraform provider AWS.
  - Infra modular.
- **Prática:**
  - Subir EC2 via CloudFormation.
  - Criar VPC com Terraform.
  - Integrar Ansible para configurar servidores.

📌 **Tarefa prática:** Subir app web (EC2 + RDS) com Terraform.

---

## 🔹 Fase 7 – Observabilidade e Logging (2 semanas)
**Objetivos:** Monitorar e auditar recursos.  
- **Teoria:**
  - CloudWatch Metrics, Logs e Alarms.
  - CloudTrail (auditoria).
  - X-Ray (tracing).
- **Prática:**
  - Criar alarmes de CPU em EC2.
  - Coletar logs de aplicação no CloudWatch.
  - Auditar eventos com CloudTrail.

📌 **Tarefa prática:** Monitorar instância EC2 e gerar alarme de CPU > 70%.

---

## 🔹 Fase 8 – Serviços DevOps na AWS (3 semanas)
**Objetivos:** Usar serviços nativos de DevOps.  
- **Teoria:**
  - CodeCommit, CodeBuild, CodeDeploy, CodePipeline.
  - EKS (Kubernetes gerenciado).
  - ECS + Fargate.
- **Prática:**
  - Criar pipeline CodePipeline para app containerizado.
  - Deploy em ECS Fargate.
  - Deploy em EKS com Terraform.

📌 **Tarefa prática:** Pipeline CI/CD rodando build → deploy em ECS.

---

## 🔹 Fase 9 – Segurança Avançada (2 semanas)
**Objetivos:** Garantir compliance e boas práticas.  
- **Teoria:**
  - AWS WAF e Shield.
  - KMS (Key Management Service).
  - Secrets Manager e Parameter Store.
  - GuardDuty.
- **Prática:**
  - Criar secret no Secrets Manager.
  - Ativar GuardDuty no ambiente.
  - Proteger app com WAF.

📌 **Tarefa prática:** App protegido com WAF + secrets no Parameter Store.

---

## 🔹 Projeto Final – Arquitetura AWS Completa (4 semanas)
**Objetivos:** Montar uma infra realista de produção.  
- Infra:
  - VPC com subnets públicas e privadas.
  - EC2 para web.
  - RDS para banco.
  - S3 para arquivos.
  - CloudFront como CDN.
  - ELB para balanceamento.
- Extras:
  - Pipeline CodePipeline para CI/CD.
  - Monitoramento no CloudWatch.
  - Secrets no Secrets Manager.

📌 **Entrega:** Repositório Git com Terraform/CloudFormation + documentação.

---

# 📅 Cronograma Sugerido
- **Meses 1-2:** Fundamentos + IAM + EC2 + Armazenamento.  
- **Mês 3:** Redes + Segurança.  
- **Mês 4:** Automação (Terraform/CloudFormation).  
- **Mês 5:** Observabilidade + Serviços DevOps.  
- **Mês 6:** Segurança avançada + Projeto final.  

---

