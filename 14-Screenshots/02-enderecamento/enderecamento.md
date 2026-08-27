# 02 — Endereçamento IP

## 2.1 Objectivo

Esta secção apresenta o plano de endereçamento IP utilizado na
infraestrutura de rede da TeckAlfa.

A rede interna utiliza a rede IPv4 `192.168.10.0/24`.

---

## 2.2 Rede interna

| Equipamento | Interface | Endereço IPv4 | Função |
|---|---|---|---|
| pfSense | LAN | 192.168.10.1/24 | Gateway |
| DC01 | ens33 | 192.168.10.10/24 | Servidor |
| desktop01 | ens33 | 192.168.10.128/24 | Cliente |

A máscara utilizada na rede interna é:

```text
255.255.255.0
