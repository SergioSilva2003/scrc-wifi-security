# scrc-wifi-security
# Segurança em Redes Wi-Fi e Mitigação de Ataques 🛡️📶

Repositório dedicado ao projeto prático e teórico da unidade curricular SCRC do Mestrado em Engenharia de Telecomunicações e Informática (ISCTE-IUL).

**Autores:** Sérgio Silva e Tiago Inácio
**Data:** Abril, 2026

## 📌 Sobre o Projeto
Este projeto tem como objetivo analisar as vulnerabilidades dos protocolos de segurança de redes Wi-Fi (com foco no WPA2-Personal) e demonstrar técnicas eficazes de mitigação através da implementação de uma arquitetura WPA2-Enterprise. 

O projeto está dividido em duas vertentes principais:
1. **Teórica:** Análise da evolução dos protocolos (WEP ao WPA3), vulnerabilidades inerentes (como o KRACK attack) e metodologias de pentesting.
2. **Prática (Laboratório CP3):** Simulação de um ciberataque e posterior fortificação (hardening) da infraestrutura.

## 🔬 Laboratório (CP3)

### Cenário 1: Teste de Penetração (WPA2-Personal)
Demonstração das vulnerabilidades inerentes à utilização de uma Chave Pré-Partilhada (PSK).
* **Objetivo:** Captura do 4-way handshake e quebra da palavra-passe.
* **Ferramentas utilizadas:** Kali Linux, Aircrack-ng suite (`airodump-ng`, `aireplay-ng`).
* **Metodologia:** Foram executados ataques de desautenticação forçada para capturar as credenciais, seguidos de um ataque de dicionário offline.

### Cenário 2: Hardening e Mitigação (WPA2-Enterprise)
Implementação de uma solução de nível corporativo para suprimir os riscos associados às chaves partilhadas.
* **Objetivo:** Configuração de um servidor RADIUS e autenticação via 802.1X.
* **Ferramentas utilizadas:** FreeRADIUS.
* **Metodologia:** Transição para o modo Enterprise com configuração do protocolo EAP (PEAP/MSCHAPv2 ou EAP-TLS), garantindo que cada cliente possui um canal criptográfico isolado e dinâmico.

## 📂 Estrutura do Repositório
* `/docs` - Contém o relatório final do projeto detalhando toda a investigação teórica.
* `/lab_ataque` - Scripts ou outputs limpos da simulação do ataque.
* `/lab_defesa` - Ficheiros de configuração do servidor FreeRADIUS utilizados no laboratório.

## ⚠️ Aviso Legal (Disclaimer)
Todas as capturas de tráfego, injeções de pacotes e simulações de ataque descritas neste repositório foram realizadas num **ambiente laboratorial estritamente controlado**, criado especificamente para fins académicos e de investigação.
