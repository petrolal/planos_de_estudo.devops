# 📚 Plano de Estudos Completo – Proxmox VE (Básico ao Avançado)

Este guia cobre desde a instalação e fundamentos até cenários avançados de cluster, alta disponibilidade (HA) e integração com ferramentas de automação.

---

## 🔹 Fase 1 – Fundamentos de Virtualização com Proxmox
**Objetivos:** Entender o que é Proxmox VE e preparar ambiente.  
- **Teoria:**
  - O que é Proxmox VE.
  - Diferença entre KVM (máquinas virtuais) e LXC (containers).
  - Requisitos de hardware (CPU com VT-x/AMD-V, memória, storage).
  - Instalação do Proxmox (ISO oficial).
  - Acesso via web UI.
- **Prática:**
  - Instalar Proxmox em máquina física ou VM nested.
  - Explorar interface web.
  - Criar primeira VM Linux (Ubuntu/Debian).

📌 **Tarefa prática:** Instalar Proxmox e rodar primeira VM com Ubuntu.

---

## 🔹 Fase 2 – Gerenciamento Básico de VMs e Containers
**Objetivos:** Aprender a administrar workloads no Proxmox.  
- **Teoria:**
  - Gerenciamento de VMs (KVM).
  - Containers LXC.
  - Snapshots e backups.
  - Templates.
- **Prática:**
  - Criar container LXC Debian.
  - Criar snapshot de VM antes de update.
  - Clonar VM a partir de template.

📌 **Tarefa prática:** Criar um template de Ubuntu Server e clonar várias VMs a partir dele.

---

## 🔹 Fase 3 – Redes no Proxmox
**Objetivos:** Configurar redes virtuais no cluster.  
- **Teoria:**
  - Linux Bridges.
  - VLANs e tagging.
  - NAT e roteamento.
- **Prática:**
  - Criar bridge `vmbr0` conectada à interface física.
  - Configurar VLAN em VM.
  - Criar rede interna isolada para testes.

📌 **Tarefa prática:** Configurar duas VMs se comunicando em rede privada (sem acesso externo).

---

## 🔹 Fase 4 – Armazenamento
**Objetivos:** Entender e configurar opções de storage.  
- **Teoria:**
  - Tipos de storage no Proxmox:
    - Local
    - NFS
    - iSCSI
    - Ceph
  - Thin provisioning.
- **Prática:**
  - Adicionar storage NFS remoto.
  - Criar disco extra em VM.
  - Migrar VM entre storages.

📌 **Tarefa prática:** Configurar storage NFS externo e rodar VM nele.

---

## 🔹 Fase 5 – Cluster Proxmox
**Objetivos:** Criar e gerenciar cluster de Proxmox.  
- **Teoria:**
  - O que é cluster PVE.
  - Quorum e Corosync.
  - Migração de VMs entre nodes.
- **Prática:**
  - Subir 2 ou mais nós Proxmox.
  - Criar cluster.
  - Migrar VM online entre nós.

📌 **Tarefa prática:** Criar cluster com 2 nós e testar migração de VM.

---

## 🔹 Fase 6 – Alta Disponibilidade (HA)
**Objetivos:** Garantir continuidade dos serviços.  
- **Teoria:**
  - HA Manager do Proxmox.
  - Regras de failover.
  - Monitoramento de nodes.
- **Prática:**
  - Configurar grupo HA.
  - Definir prioridade de failover.
  - Testar desligando um nó e observar realocação da VM.

📌 **Tarefa prática:** VM web sempre disponível em cluster com HA.

---

## 🔹 Fase 7 – Backup e Recuperação
**Objetivos:** Proteger workloads com backup e restore.  
- **Teoria:**
  - Proxmox Backup Server (PBS).
  - Tipos de backup (full, incremental, differential).
  - Agendamento de backups.
- **Prática:**
  - Instalar Proxmox Backup Server.
  - Fazer backup full de VM.
  - Restaurar VM a partir do backup.

📌 **Tarefa prática:** Criar política de backup diário para VMs críticas.

---

## 🔹 Fase 8 – Automação e Integrações
**Objetivos:** Automatizar operações no Proxmox.  
- **Teoria:**
  - API do Proxmox.
  - CLI (`pvesh`, `qm`, `pct`).
  - Integração com Ansible e Terraform.
- **Prática:**
  - Usar `qm create` para criar VM via CLI.
  - Configurar Terraform Provider do Proxmox.
  - Criar playbook Ansible para gerenciar VMs.

📌 **Tarefa prática:** Provisionar VM no Proxmox via Terraform + Ansible.

---

## 🔹 Fase 9 – Proxmox Avançado
**Objetivos:** Usar recursos empresariais e avançados.  
- **Teoria:**
  - Ceph (storage distribuído).
  - SDN (Software Defined Network).
  - Hookscripts para automação customizada.
- **Prática:**
  - Criar Ceph storage distribuído entre 3 nós.
  - Configurar rede definida por software.
  - Criar script para rodar sempre que VM iniciar.

📌 **Tarefa prática:** Subir cluster Ceph com 3 nós e rodar VM nele.

---

## 🔹 Projeto Final
**Objetivos:** Montar lab completo de virtualização corporativa.  
- Criar **cluster Proxmox de 3 nós** com:
  - Storage distribuído (Ceph).
  - Rede com VLANs para isolar ambientes.
  - Grupo HA para VMs críticas.
  - Backup em Proxmox Backup Server.
  - Automação via Terraform + Ansible.
- Rodar aplicações de exemplo:
  - 2 VMs web em HA.
  - 1 VM banco de dados com storage persistente.
  - Monitoramento via Grafana/Prometheus.

📌 **Entrega:** Documentação + repositório com configs do Terraform/Ansible.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + VMs/Containers (Fases 1 e 2).  
- **Semanas 3-4:** Redes + Storage (Fases 3 e 4).  
- **Semanas 5-6:** Cluster + HA (Fases 5 e 6).  
- **Semanas 7-8:** Backup + Automação (Fases 7 e 8).  
- **Semanas 9-10:** Proxmox avançado (Fase 9).  
- **Semanas 11-12:** Projeto Final.  

---

