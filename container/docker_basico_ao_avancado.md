# 📚 Plano de Estudos Completo – Docker (Básico ao Avançado)

Este plano cobre desde fundamentos de containers até arquiteturas avançadas com Docker Compose, redes, volumes e boas práticas de produção.

---

## 🔹 Fase 1 – Fundamentos de Containers e Docker
**Objetivos:** Entender o que é Docker e configurar ambiente.  
- **Teoria:**
  - Diferença entre VM e container.
  - Conceito de imagens e containers.
  - Docker Engine, Docker CLI e Docker Hub.
  - Instalação do Docker.
- **Prática:**
  - `docker run hello-world`
  - Executar container interativo: `docker run -it ubuntu bash`
  - Listar containers: `docker ps -a`
  - Remover containers e imagens: `docker rm`, `docker rmi`.

📌 **Tarefa prática:** Rodar container Ubuntu, instalar pacotes dentro dele e salvar como imagem.

---

## 🔹 Fase 2 – Imagens e Dockerfile
**Objetivos:** Aprender a criar e personalizar imagens.  
- **Teoria:**
  - Estrutura de um Dockerfile.
  - Comandos principais: `FROM`, `RUN`, `COPY`, `ADD`, `CMD`, `ENTRYPOINT`, `EXPOSE`, `ENV`, `WORKDIR`.
  - Camadas de imagem (layers).
- **Prática:**
  - Criar Dockerfile para rodar Nginx.
  - Usar `docker build -t meu-nginx .`
  - Rodar com porta mapeada: `docker run -d -p 8080:80 meu-nginx`
  - Usar `.dockerignore`.

📌 **Tarefa prática:** Criar imagem customizada do Nginx que exibe uma página HTML própria.

---

## 🔹 Fase 3 – Volumes e Persistência
**Objetivos:** Gerenciar dados persistentes.  
- **Teoria:**
  - Tipos de volumes: Named, Bind Mounts, tmpfs.
  - Volumes x camadas de imagem.
- **Prática:**
  - Criar volume: `docker volume create dados`
  - Usar volume em container MySQL.
  - Usar bind mount para mapear diretório local.

📌 **Tarefa prática:** Subir MySQL com volume persistente para os dados.

---

## 🔹 Fase 4 – Redes no Docker
**Objetivos:** Conectar containers entre si.  
- **Teoria:**
  - Tipos de rede: bridge, host, none, overlay.
  - DNS interno do Docker.
- **Prática:**
  - Criar rede bridge personalizada.
  - Conectar containers (Nginx → app → banco).
  - Testar comunicação com `ping` e `curl`.

📌 **Tarefa prática:** Criar rede onde um container web se conecta a um container DB via nome DNS.

---

## 🔹 Fase 5 – Docker Compose
**Objetivos:** Orquestrar múltiplos containers.  
- **Teoria:**
  - Estrutura do `docker-compose.yml`.
  - Serviços, volumes, redes.
  - Escalabilidade com `docker-compose up --scale`.
- **Prática:**
  - Criar ambiente com:
    - `app` (Node.js ou Python)
    - `db` (Postgres)
    - `nginx` (reverse proxy)
  - Usar variáveis de ambiente (`.env`).
  - Subir stack com `docker-compose up -d`.

📌 **Tarefa prática:** Criar `docker-compose.yml` para rodar Nginx + app + banco.

---

## 🔹 Fase 6 – Boas Práticas e Produção
**Objetivos:** Aprender a otimizar imagens e ambientes.  
- **Teoria:**
  - Multi-stage builds.
  - Reduzir tamanho de imagens.
  - Segurança: usuários não-root.
  - Gerenciamento de logs.
- **Prática:**
  - Criar Dockerfile multi-stage para Node.js.
  - Analisar tamanho da imagem com `docker images`.
  - Usar `docker exec` e `docker logs`.

📌 **Tarefa prática:** Criar imagem Node.js otimizada em multi-stage build.

---

## 🔹 Fase 7 – Docker Avançado
**Objetivos:** Entrar em redes e clusters mais complexos.  
- **Teoria:**
  - Overlay networks.
  - Docker Swarm (conceito e uso básico).
  - Registro privado (`docker registry`).
  - CI/CD com Docker.
- **Prática:**
  - Criar cluster Swarm local com `docker swarm init`.
  - Fazer deploy stack com `docker stack deploy`.
  - Configurar registry local.

📌 **Tarefa prática:** Deploy de aplicação simples em Swarm com 2 nós.

---

## 🔹 Projeto Final
**Objetivos:** Integrar tudo em um ambiente realista.  
- Criar um **lab completo** com Docker Compose:
  - **Nginx (load balancer)**  
  - **2 containers web (Node.js/Python)**  
  - **1 container banco (Postgres/MySQL)**  
  - **1 container monitoramento (Portainer ou Grafana/Prometheus)**  
- Extras:
  - Multi-stage build para otimização.
  - Volumes para persistência do banco.
  - Redes isoladas para separar frontend, backend e db.

📌 **Entrega:** Um `docker-compose.yml` + Dockerfiles otimizados.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Imagens (Fases 1 e 2).  
- **Semanas 3-4:** Volumes + Redes (Fases 3 e 4).  
- **Semanas 5-6:** Docker Compose (Fase 5).  
- **Semanas 7-8:** Boas práticas (Fase 6).  
- **Semanas 9-10:** Docker Avançado (Fase 7).  
- **Semanas 11-12:** Projeto Final.  

---

