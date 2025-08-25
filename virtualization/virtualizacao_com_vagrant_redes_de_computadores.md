# 📚 Plano de Estudos: Virtualização com Vagrant + Redes de Computadores no Linux

---

## 🔹 Fase 1 – Fundamentos de Virtualização e Linux
**Objetivos:** Entender os conceitos básicos e preparar o ambiente.  
- **Conceitos:**
  - O que é virtualização (Hypervisor tipo 1 x tipo 2).
  - Vagrant: propósito e arquitetura (Box, Provider, Provisioner).
  - Revisão de comandos Linux essenciais (bash, pacotes, systemctl, usuários).
- **Prática:**
  - Instalar VirtualBox ou Libvirt + Vagrant.
  - Criar a primeira VM com `vagrant init` + `vagrant up`.
  - SSH na VM com `vagrant ssh`.

📌 **Tarefa prática:** Criar uma VM Ubuntu mínima com Vagrant, atualizar pacotes e criar um usuário.

---

## 🔹 Fase 2 – Redes de Computadores (Teoria aplicada no Linux)
**Objetivos:** Dominar conceitos fundamentais de redes e aplicar em laboratório.  
- **Conceitos:**
  - Modelo OSI x TCP/IP.
  - Endereçamento IPv4 e IPv6.
  - Máscara de rede e sub-redes.
  - Protocolos essenciais: ARP, ICMP, DNS, HTTP, SSH.
- **Prática no Linux:**
  - Usar `ip a`, `ip r`, `ping`, `traceroute`, `dig`, `ss`, `tcpdump`.
  - Configurar IP manualmente (`/etc/netplan` ou `ip addr add`).
  - Criar alias de rede (`eth0:1`).
  - Levantar servidor simples: `python -m http.server`.

📌 **Tarefa prática:** Subir 2 VMs no Vagrant, configurar IPs estáticos e testar comunicação com ping/ssh.

---

## 🔹 Fase 3 – Avançando com Vagrant
**Objetivos:** Aprender a orquestrar múltiplas VMs com redes personalizadas.  
- **Conceitos:**
  - Tipos de rede no Vagrant:
    - NAT
    - Host-only
    - Bridged
  - Provisionamento (Shell, Ansible, Puppet).
- **Prática:**
  - Criar Vagrantfile com múltiplas VMs (ex: `web`, `db`).
  - Definir redes privadas e públicas.
  - Automatizar setup com script `provision.sh`.

📌 **Tarefa prática:** Criar um mini-lab: VM web + VM banco.  
A web se conecta ao DB via rede privada, mas só a web tem acesso à internet.

---

## 🔹 Fase 4 – Redes Linux Avançadas
**Objetivos:** Entender roteamento, firewall e serviços.  
- **Conceitos:**
  - Tabelas de roteamento.
  - NAT e masquerading.
  - iptables vs nftables.
  - DHCP, DNS e servidores básicos.
- **Prática:**
  - Configurar uma VM como **roteador** entre duas redes.
  - Criar firewall básico com `iptables -A INPUT -p tcp --dport 22 -j ACCEPT`.
  - Subir um servidor DHCP ou DNS simples.

📌 **Tarefa prática:** Ter 3 VMs:  
- Roteador (faz NAT).  
- Cliente (rede interna sem internet).  
- Servidor (web).  
O cliente acessa a web via roteador.

---

## 🔹 Fase 5 – Projeto Final
**Objetivos:** Integrar tudo em um ambiente prático.  
- Criar um **mini-lab corporativo** com Vagrant:  
  - 1 VM **router/firewall**.  
  - 1 VM **servidor web** (Nginx ou Apache).  
  - 1 VM **servidor banco** (Postgres/MySQL).  
  - 2 VMs **clientes**.  
- Configurar DNS interno.  
- Usar NAT para permitir que os clientes acessem a web externa **via roteador**.  
- Criar um script de provisionamento para automatizar todo o setup.  

---

# 📅 Sugestão de Cronograma
- **Semana 1:** Fase 1 – Fundamentos de Virtualização e Linux.  
- **Semana 2:** Fase 2 – Redes de Computadores básicas.  
- **Semana 3:** Fase 3 – Vagrant avançado (multi-VM, provisionamento).  
- **Semana 4:** Fase 4 – Redes Linux avançadas (roteador, firewall, serviços).  
- **Semana 5-6:** Projeto final integrando tudo.  

