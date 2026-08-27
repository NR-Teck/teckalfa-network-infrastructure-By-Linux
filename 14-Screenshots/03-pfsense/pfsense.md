# 03 — pfSense

## 3.1 Objetivo

O pfSense é utilizado como router e firewall da infraestrutura de rede da TeckAlfa. É responsável pela comunicação entre a rede interna e a rede externa, pelo encaminhamento do tráfego e pelas regras de NAT.

## 3.2 Arquitetura de rede

A configuração utilizada no laboratório é composta por duas interfaces:

| Interface | Função | Endereço |
|---|---|---|
| WAN | Ligação externa | 192.168.198.137 |
| LAN | Rede interna | 192.168.10.1/24 |

A rede interna utilizada no laboratório é:

`192.168.10.0/24`

O pfSense utiliza o endereço `192.168.10.1` como gateway da rede interna.

## 3.3 Configuração da WAN

A interface WAN encontra-se configurada para obter o endereço IPv4 através de DHCP.

### Configuração validada

- IPv4 Configuration Type: DHCP
- Endereço IPv4 atribuído: `192.168.198.137`
- Interface: WAN

A atribuição do endereço `192.168.198.137` confirma que a interface WAN recebeu correctamente um endereço IPv4.

### Captura

![Configuração da WAN](./capturas/03-pfsense-wan.png)

## 3.4 Configuração da LAN

A interface LAN constitui a rede interna do laboratório.

### Configuração

- Endereço IPv4: `192.168.10.1`
- Máscara: `255.255.255.0`
- Rede: `192.168.10.0/24`

O endereço `192.168.10.1` é utilizado como gateway pelos equipamentos da rede interna.

### Captura

![Configuração da LAN](./capturas/03-pfsense-lan.png)

## 3.5 Gateway

O gateway utilizado para a saída da rede interna é disponibilizado através da interface WAN do pfSense.

### Captura

![Gateway](./capturas/03-pfsense-gateway.png)

## 3.6 NAT

O pfSense realiza NAT para permitir que os equipamentos da rede interna tenham acesso à rede externa através do endereço da interface WAN.

A configuração de NAT foi mantida de acordo com a configuração do laboratório.

### Captura

![NAT](./capturas/03-pfsense-nat.png)

## 3.7 Conclusão

A configuração do pfSense foi validada com sucesso.

A infraestrutura apresenta:

- WAN configurada por DHCP;
- endereço WAN `192.168.198.137`;
- LAN configurada com `192.168.10.1/24`;
- gateway interno disponibilizado pelo pfSense;
- NAT configurado para a comunicação com a rede externa.

Esta configuração permite ao DC01 e aos restantes equipamentos da rede interna comunicar através do pfSense.
