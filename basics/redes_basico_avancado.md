# 📚 Plano de Estudos Completo – Redes de Computadores (Básico ao Avançado)

Este plano vai do **nível iniciante ao avançado**, com teoria e práticas aplicadas no **Linux**.  
A ideia é progredir em camadas, como a própria pilha de redes.

---

## 🔹 Fase 1 – Fundamentos de Redes
**Objetivos:** Compreender os conceitos básicos.  
- **Teoria:**
  - O que é rede de computadores.
  - Tipos de redes: LAN, WAN, MAN, WLAN.
  - Topologias (estrela, barramento, anel, mesh).
  - Dispositivos: hub, switch, roteador, firewall.
  - Modelo OSI (7 camadas).
  - Modelo TCP/IP (4 camadas).
- **Prática no Linux:**
  - Comandos básicos: `ip a`, `ip r`, `ping`, `traceroute`.
  - Analisar tabela de roteamento: `ip route`.
  - Observar conexões abertas: `ss -tuln`.

📌 **Tarefa prática:** Montar 2 VMs no Vagrant, configurar IP estático e testar ping entre elas.

---

## 🔹 Fase 2 – Endereçamento e Protocolos
**Objetivos:** Entender endereçamento e protocolos essenciais.  
- **Teoria:**
  - Endereçamento IPv4: classes A, B, C, D, E.
  - Máscara de rede e sub-rede.
  - Endereços privados e públicos (RFC 1918).
  - Introdução ao IPv6.
  - Protocolos:
    - ARP
    - ICMP
    - TCP vs UDP
    - DNS
    - DHCP
- **Prática no Linux:**
  - Configurar IP estático: `ip addr add`.
  - Configurar rota: `ip route add`.
  - Analisar tráfego com `tcpdump -i eth0`.
  - Resolver nomes com `dig` e `nslookup`.

📌 **Tarefa prática:** Criar servidor DHCP em uma VM e cliente em outra para pegar IP dinâmico.

---

## 🔹 Fase 3 – Camada de Transporte e Aplicação
**Objetivos:** Trabalhar com portas, serviços e protocolos de aplicação.  
- **Teoria:**
  - Portas TCP e UDP (0–65535).
  - Serviços comuns:
    - 22 (SSH)
    - 53 (DNS)
    - 80/443 (HTTP/HTTPS)
    - 25/587 (SMTP)
    - 3306 (MySQL)
  - Conceito de sockets.
- **Prática no Linux:**
  - Ver portas abertas: `ss -tulnp`.
  - Instalar e configurar servidor web (Apache ou Nginx).
  - Testar com `curl` e `wget`.
  - Instalar servidor DNS simples (`bind9`).
  - Subir servidor simples em Python: `python -m http.server 8080`.

📌 **Tarefa prática:** Criar VM com Nginx e VM cliente que acessa o site interno via curl.

---

## 🔹 Fase 4 – Redes Virtuais e Roteamento
**Objetivos:** Configurar redes privadas e roteamento em Linux.  
- **Teoria:**
  - Redes NAT, Host-only e Bridged.
  - Roteamento estático vs dinâmico.
  - NAT e masquerading.
- **Prática:**
  - Configurar 3 VMs:
    - Router
    - Cliente
    - Servidor
  - Usar `iptables` ou `nftables` para NAT.
  - Habilitar IP forwarding (`sysctl -w net.ipv4.ip_forward=1`).
  - Cliente acessa servidor via roteador.

📌 **Tarefa prática:** Criar um roteador Linux que conecta duas redes privadas.

---

## 🔹 Fase 5 – Segurança e Firewalls
**Objetivos:** Aprender controle de tráfego e proteção de rede.  
- **Teoria:**
  - Conceitos de firewall.
  - Stateful vs Stateless.
  - IDS e IPS.
  - VPNs (conceito e aplicações).
- **Prática no Linux:**
  - Configurar regras com `iptables` ou `nftables`.
  - Permitir apenas tráfego SSH (porta 22).
  - Bloquear pings (ICMP).
  - Criar NAT para saída de internet.

📌 **Tarefa prática:** Criar firewall básico que bloqueia tudo, exceto HTTP e SSH.

---

## 🔹 Fase 6 – Redes Avançadas
**Objetivos:** Entrar em protocolos e cenários corporativos.  
- **Teoria:**
  - VLANs e trunking.
  - Roteamento dinâmico (OSPF, BGP – conceitos).
  - QoS e Traffic Shaping.
  - Balanceamento de carga.
- **Prática com Linux:**
  - Criar VLAN virtual (`ip link add link eth0 name eth0.10 type vlan id 10`).
  - Testar bridge (`brctl addbr br0`).
  - Configurar `tc` (traffic control) para limitar largura de banda.

📌 **Tarefa prática:** Simular 2 VLANs e criar um roteador Linux que interliga ambas.

---

## 🔹 Fase 7 – Projeto Final
**Objetivos:** Integrar todo o aprendizado em um ambiente completo.  
- Criar um **mini-lab corporativo** com Vagrant:  
  - 1 VM **router/firewall**.  
  - 1 VM **servidor web** (Nginx).  
  - 1 VM **servidor banco** (MySQL/Postgres).  
  - 2 VMs **clientes**.  
- Configurações:  
  - DNS interno.  
  - Firewall com regras específicas.  
  - NAT para acesso à internet.  
  - VLANs simuladas.  
- Extras:  
  - Monitorar tráfego com `tcpdump` e `wireshark`.  
  - Testar estresse de rede com `iperf3`.  

📌 **Entrega:** Um documento + Vagrantfile com toda a infra automatizada.

---

# 📅 Cronograma Sugerido
- **Semanas 1-2:** Fundamentos + Endereçamento (Fases 1 e 2).  
- **Semanas 3-4:** Transporte + Aplicação (Fase 3).  
- **Semanas 5-6:** Roteamento + Redes Virtuais (Fase 4).  
- **Semanas 7-8:** Segurança e Firewalls (Fase 5).  
- **Semanas 9-10:** Redes Avançadas (Fase 6).  
- **Semanas 11-12:** Projeto Final (Fase 7).  

---

