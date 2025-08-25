# 📚 Plano de Estudos Completo – Ansible (Básico ao Avançado)

Este plano guia do zero até automações complexas com **Ansible** em ambientes Linux.  
O foco será prática com **laboratórios usando Vagrant**.

---

## 🔹 Fase 1 – Fundamentos
**Objetivos:** Entender o que é o Ansible e configurar o ambiente.  
- **Teoria:**
  - O que é Ansible e para que serve.
  - Arquitetura: Control Node vs Managed Nodes.
  - Conceitos: Ad-hoc, Playbook, Inventory, Modules.
  - Instalação do Ansible (`pip install ansible` ou `apt/yum install ansible`).
- **Prática:**
  - Configurar 2 VMs com Vagrant (controlador + alvo).
  - Configurar acesso via SSH sem senha (chaves).
  - Testar comunicação: `ansible all -m ping`.

📌 **Tarefa prática:** Criar primeiro inventário (`hosts.ini`) e rodar `ansible all -m ping`.

---

## 🔹 Fase 2 – Inventários e Ad-hoc Commands
**Objetivos:** Aprender a gerenciar máquinas com inventários e módulos.  
- **Teoria:**
  - Inventário estático (`ini`/`yaml`).
  - Grupos de hosts.
  - Inventário dinâmico (conceito).
- **Prática:**
  - Listar pacotes instalados com `ansible -m shell -a "dpkg -l"`.
  - Criar grupos de hosts (web, db).
  - Usar módulos básicos: `ping`, `copy`, `file`, `service`, `yum/apt`.

📌 **Tarefa prática:** Criar inventário com 3 grupos (`web`, `db`, `infra`) e executar comandos diferentes em cada.

---

## 🔹 Fase 3 – Playbooks
**Objetivos:** Automação básica com Playbooks.  
- **Teoria:**
  - Estrutura de um playbook YAML.
  - Tasks, Modules e Handlers.
  - Variáveis (`vars`, `vars_files`).
  - Templates com Jinja2.
- **Prática:**
  - Criar playbook para instalar Nginx.
  - Criar playbook para copiar arquivos de configuração.
  - Usar `notify` e `handlers` para reiniciar serviço.
  - Usar `when` para condicionais.

📌 **Tarefa prática:** Playbook que instala Nginx, copia um `index.html` e reinicia o serviço.

---

## 🔹 Fase 4 – Estruturação e Roles
**Objetivos:** Organizar projetos grandes com Roles.  
- **Teoria:**
  - Estrutura padrão de roles.
  - Pastas: `tasks`, `handlers`, `templates`, `files`, `vars`, `defaults`.
  - Boas práticas de organização.
- **Prática:**
  - Criar role `webserver` para instalar Nginx.
  - Criar role `database` para instalar MySQL/Postgres.
  - Usar múltiplas roles em um playbook.

📌 **Tarefa prática:** Criar um site com stack `web + db` usando roles separadas.

---

## 🔹 Fase 5 – Inventário Dinâmico e Variáveis Avançadas
**Objetivos:** Trabalhar com ambientes mais flexíveis.  
- **Teoria:**
  - Inventários dinâmicos (AWS, GCP, Docker, etc.).
  - Group vars e host vars.
  - Fatos (`ansible_facts`).
  - Criptografia com Ansible Vault.
- **Prática:**
  - Usar variáveis específicas para cada grupo.
  - Consultar `ansible_facts` para escolher pacotes conforme SO.
  - Criptografar senhas com `ansible-vault`.

📌 **Tarefa prática:** Criar playbook que instala pacotes diferentes em Ubuntu e CentOS.

---

## 🔹 Fase 6 – Collections, Galaxy e Integrações
**Objetivos:** Usar a comunidade e extender o Ansible.  
- **Teoria:**
  - O que são Collections.
  - Ansible Galaxy.
  - Integração com Docker, Kubernetes, AWS.
- **Prática:**
  - Instalar collection do Docker: `ansible-galaxy collection install community.docker`.
  - Criar playbook para subir container Nginx.
  - Usar roles da Galaxy (ex: `geerlingguy.nginx`).

📌 **Tarefa prática:** Subir containers via Ansible em múltiplas VMs.

---

## 🔹 Fase 7 – Ansible Avançado
**Objetivos:** Automação de alto nível e boas práticas.  
- **Teoria:**
  - CI/CD com Ansible.
  - Testes de Playbooks (Molecule).
  - Estrutura de projetos grandes.
  - Performance (forks, async, delegate_to).
- **Prática:**
  - Usar `delegate_to` para rodar tarefas apenas no controlador.
  - Criar playbook com `serial` para deploy gradual.
  - Criar pipeline Jenkins que roda playbooks automaticamente.

📌 **Tarefa prática:** Pipeline de deploy com Ansible + Jenkins em um ambiente simulado.

---

## 🔹 Projeto Final
**Objetivos:** Consolidar tudo em um ambiente realista.  
- Criar um **lab corporativo automatizado** com Vagrant + Ansible:  
  - 1 VM **load balancer** (HAProxy ou Nginx).  
  - 2 VMs **webservers** (Nginx/Apache).  
  - 1 VM **banco** (Postgres).  
  - 1 VM **ansible-control**.  
- Features:  
  - Playbooks organizados em roles.  
  - Configuração automatizada de firewall.  
  - Deploy de aplicação exemplo.  
  - Vault para senhas do banco.  

📌 **Entrega:** Repositório Git com `Vagrantfile`, playbooks e roles.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Inventário (Fases 1 e 2).  
- **Semanas 3-4:** Playbooks + Roles (Fases 3 e 4).  
- **Semanas 5-6:** Variáveis avançadas + Vault (Fase 5).  
- **Semanas 7-8:** Collections e Galaxy (Fase 6).  
- **Semanas 9-10:** Ansible Avançado (Fase 7).  
- **Semanas 11-12:** Projeto Final.  

---

