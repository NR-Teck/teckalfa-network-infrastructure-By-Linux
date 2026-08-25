# 01 — Arquitectura da Infraestrutura

## 1.1 Introdução

Este projecto apresenta a implementação de uma infraestrutura de rede
empresarial virtualizada para a organização TeckAlfa.

O laboratório foi desenvolvido com recurso a VMware, pfSense, Ubuntu
Server, Ubuntu Desktop e Samba Active Directory.

## 1.2 Objectivos

Os principais objectivos são:

- Implementar uma rede empresarial;
- Implementar firewall e routing;
- Implementar NAT;
- Implementar Active Directory;
- Implementar DNS;
- Implementar Kerberos;
- Criar utilizadores e grupos;
- Implementar partilhas SMB;
- Implementar ACLs;
- Integrar uma estação Ubuntu no domínio;
- Disponibilizar administração através do Cockpit;
- Implementar uma VPN;
- Implementar um serviço de correio electrónico interno;
- Realizar testes de funcionamento.

## 1.3 Arquitectura lógica

```text
                         INTERNET
                             |
                         VMware NAT
                             |
                      +--------------+
                      |   pfSense    |
                      | WAN: DHCP    |
                      | LAN: .1      |
                      +------+-------+
                             |
                      192.168.10.0/24
                             |
                +------------+------------+
                |                         |
         +------v------+           +------v------+
         |    DC01     |           |  desktop01  |
         | .10.10      |           | .10.128     |
         |             |           |             |
         | Samba AD    |           | Ubuntu      |
         | DNS         |           | Desktop     |
         | Kerberos    |           |             |
         | SMB         |           |             |
         | Cockpit     |           |             |
         +-------------+           +-------------+
