# 🛡️ Implementação de Firewall de Próxima Geração (NGFW) com OPNsense

Este repositório contém a documentação técnica e as evidências da implementação de uma infraestrutura de rede segura em um ambiente virtualizado utilizando o firewall **OPNsense**. Todo o projeto foi baseado no TCC que realizei em grupo na Etec de Embu, onde a idéia era reutilizar PCs velhos e transformar-los em um firewall eficáz. Agora com meu curso concluído, resolvi refazer este projeto em ambiente virtual para usar como material de estudo e portfólio. O projeto foi dividido em 6 relatórios que cobrem desde a base de redes até a segurança avançada e integridade de dados.

## 🚀 Visão Geral do Projeto
O objetivo principal foi criar um ambiente controlado e seguro para uma pequena infraestrutura corporativa simulada, utilizando virtualização através do VMware e sistemas open-source.

---

## 📂 Sumário dos Relatórios Técnicos

Clique nos links abaixo para acessar o detalhamento de cada etapa:

### 📑 [Relatório 0: Setup e Conectividade Base](Relatório_0.md)
* Configuração das 3 interfaces (WAN, Gerenciamento e Clientes).
* Topologia lógica e acesso à WebGUI.

### 📑 [Relatório I: Conectividade, DHCP e DNS](Relatório_1.md)
* Validação do host Ubuntu na rede interna.
* Atribuição dinâmica de IPs (DHCP) e resolução de nomes (DNS).

### 📑 [Relatório II: Segurança de Perímetro e Filtros](Relatório_2.md)
* Bloqueios de portas lógicas e sites (Aliases).
* Análise de logs em tempo real (Live View) comprovando os bloqueios.

### 📑 [Relatório III: Administração Remota via SSH](Relatório_3.md)
* Configuração de gerência CLI via SSH.
* Demonstração de controle de acesso por interface (Bloqueio na rede Clientes).

### 📑 [Relatório IV: Acesso Remoto via OpenVPN](Relatório_4.md)
* Implementação de túnel criptografado com certificados digitais.
* Liberação de tráfego na interface WAN e teste de latência (<1ms).

### 📑 [Relatório V: Backup e Integridade dos Dados](Relatório_5.md)
* Estratégia de Disaster Recovery com backup criptografado.
* Exportação e proteção do arquivo de configuração XML.

---

## 🛠️ Tecnologias Utilizadas
* **Firewall:** OPNsense 25.7
* **Virtualização:** VMware Workstation 17 Player
* **Sistemas Operacionais:** Windows 10 (Host/Gerência) e Ubuntu 18.04 (Cliente)
* **VPN:** OpenVPN (Criptografia AES-256)

---
**Projeto desenvolvido por Guilherme Rodrigues para fins acadêmicos e portfólio técnico.**
