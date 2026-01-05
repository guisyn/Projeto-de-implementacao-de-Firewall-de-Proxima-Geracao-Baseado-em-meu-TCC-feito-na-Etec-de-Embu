# 📂 Relatório 0: Setup do Ambiente e Conectividade Base

Este relatório documenta a infraestrutura inicial do projeto, detalhando a topologia de rede virtualizada e o acesso administrativo ao firewall.

## 🖥️ Topologia das Máquinas Virtuais
Para este projeto, foram utilizadas duas máquinas virtuais principais:
* **OPNsense 25.7:** Atuando como gateway de segurança e firewall de borda.
* **Ubuntu 18.04 LTS:** Atuando como estação de trabalho (Host) na rede interna (CLIENTES).

## 🌐 Configuração de Interfaces (Networking)
O firewall foi configurado com três interfaces lógicas para isolamento de tráfego:

| Interface | Configuração (VMware) | Endereço IP | Função |
| :--- | :--- | :--- | :--- |
| **WAN** | NAT | 192.168.192.136/24 | Saída para Internet e recebimento de VPN |
| **GERENCIAMENTO** | Host-Only | 192.168.1.1/24 | Acesso exclusivo à WebGUI pelo Host físico |
| **CLIENTES** | LAN/Internal | 192.168.10.1/24 | Rede protegida para os dispositivos internos |

## 🛠️ Acesso Administrativo (WebGUI)
O acesso à interface de gerenciamento foi estabelecido através do navegador na máquina física, apontando para o IP da interface de Gerenciamento.

![Dashboard OPNsense](dashboard_opnsense.jpg)
*Dashboard principal exibindo o status operacional das interfaces e serviços.*

## 🛡️ Planejamento de Regras de Firewall
As regras iniciais foram estabelecidas na interface **CLIENTES** para garantir a conectividade básica e preparar os bloqueios de segurança posteriores:
* **DNS:** Permissão para consultas ao servidor DNS interno.
* **HTTP/S:** Controle de navegação web.
* **SSH:** Preparação para gerência remota.

![Regras Iniciais](firewall_rules.PNG)
*Visualização das regras de firewall aplicadas à rede de clientes.*
