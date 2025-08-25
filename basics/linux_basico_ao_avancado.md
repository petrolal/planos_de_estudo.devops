# 📚 Plano de Estudos Completo – Linux (Básico ao Avançado)

Este guia cobre desde os fundamentos do sistema operacional até administração avançada de servidores em produção.

---

## 🔹 Fase 1 – Fundamentos do Linux
**Objetivos:** Aprender o básico do sistema e linha de comando.  
- **Teoria:**
  - O que é Linux e diferenças de distros (Debian, Ubuntu, RedHat, Arch).
  - Kernel, Shell e Filesystem.
  - Estrutura de diretórios (`/bin`, `/etc`, `/var`, `/home`...).
- **Prática:**
  - Navegar com `ls`, `cd`, `pwd`.
  - Criar arquivos e diretórios: `touch`, `mkdir`, `rm`, `cp`, `mv`.
  - Usar `man` e `--help`.

📌 **Tarefa prática:** Explorar `/etc`, `/var/log` e `/home`, criando e manipulando arquivos.

---

## 🔹 Fase 2 – Gerenciamento de Usuários e Permissões
**Objetivos:** Controlar acessos no sistema.  
- **Teoria:**
  - Usuários, grupos e UID/GID.
  - Permissões (`rwx`) e `chmod`, `chown`, `chgrp`.
  - Sudo e privilégios administrativos.
- **Prática:**
  - Criar usuário com `adduser`.
  - Alterar senha com `passwd`.
  - Configurar permissões em diretório compartilhado.

📌 **Tarefa prática:** Criar grupo `devs` e usuários com acesso restrito a `/srv/dev`.

---

## 🔹 Fase 3 – Processos e Serviços
**Objetivos:** Gerenciar execução de programas.  
- **Teoria:**
  - Conceito de processo e PID.
  - Estados de processos.
  - systemd e init.
- **Prática:**
  - Listar processos: `ps`, `top`, `htop`.
  - Matar processo: `kill`, `killall`.
  - Gerenciar serviços: `systemctl start|stop|status`.

📌 **Tarefa prática:** Criar serviço systemd simples que executa script a cada boot.

---

## 🔹 Fase 4 – Gerenciamento de Pacotes
**Objetivos:** Instalar e atualizar softwares.  
- **Teoria:**
  - Gerenciadores: `apt` (Debian/Ubuntu), `yum`/`dnf` (RedHat), `pacman` (Arch).
- **Prática:**
  - Instalar e remover pacotes.
  - Atualizar sistema.
  - Procurar pacotes no repositório.

📌 **Tarefa prática:** Instalar e configurar Nginx pelo gerenciador de pacotes.

---

## 🔹 Fase 5 – Redes no Linux
**Objetivos:** Configurar rede e diagnosticar conexões.  
- **Teoria:**
  - Interfaces de rede e IP.
  - DNS e resolv.conf.
  - Ferramentas de rede.
- **Prática:**
  - Configurar IP com `ip addr add`.
  - Testar conectividade com `ping`, `traceroute`, `curl`.
  - Ver conexões com `ss -tuln`.

📌 **Tarefa prática:** Configurar duas VMs Linux com IP estático e testar comunicação.

---

## 🔹 Fase 6 – Arquivos, Discos e Sistema de Arquivos
**Objetivos:** Gerenciar armazenamento.  
- **Teoria:**
  - Partições e sistemas de arquivos (ext4, xfs, btrfs).
  - Montagem e fstab.
  - LVM e RAID (conceitos).
- **Prática:**
  - Montar disco extra em `/mnt/data`.
  - Ver espaço com `df -h` e `du -sh`.
  - Criar e montar partição com `fdisk`.

📌 **Tarefa prática:** Adicionar disco a VM, particionar e montar automaticamente.

---

## 🔹 Fase 7 – Shell e Scripting
**Objetivos:** Automatizar tarefas.  
- **Teoria:**
  - Shells (bash, zsh, fish)

