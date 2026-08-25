# TeckAlfa Network Infrastructure

## Laboratório de Redes e Sistemas Computacionais

Este projecto apresenta a implementação e documentação de uma infraestrutura
de rede empresarial virtualizada para a organização fictícia **TeckAlfa**.

A infraestrutura foi desenvolvida com recurso a VMware, pfSense, Ubuntu Server,
Ubuntu Desktop e Samba Active Directory.

---

## Objectivos

O projecto tem como principais objectivos:

- Implementar uma rede empresarial virtualizada;
- Configurar um gateway e firewall;
- Implementar um Active Directory;
- Centralizar a gestão de utilizadores e grupos;
- Implementar DNS e Kerberos;
- Disponibilizar partilhas de ficheiros através de SMB;
- Implementar controlo de acesso através de ACLs;
- Integrar uma estação Ubuntu no domínio;
- Disponibilizar administração através do Cockpit;
- Implementar uma VPN;
- Implementar um serviço de correio electrónico interno;
- Testar e documentar toda a infraestrutura.

---

## Arquitectura

```text
                         INTERNET
                            |
                       VMware NAT
                            |
                    +---------------+
                    |    pfSense    |
                    | WAN: DHCP     |
                    | LAN: 192.168.10.1
                    +-------+-------+
                            |
                     192.168.10.0/24
                            |
              +-------------+-------------+
              |                           |
       +------v------+              +-----v------+
       |    DC01     |              | desktop01  |
       | .10.10      |              | .10.128    |
       |             |              |             |
       | Samba AD    |              | Ubuntu      |
       | DNS         |              | Desktop     |
       | Kerberos    |              | AD Client   |
       | SMB         |              |             |
       | Cockpit     |              |             |
       +-------------+              +-------------+
