# TeckAlfa — Infraestrutura de Rede e Sistemas

## Sobre o projecto

Este projecto documenta a implementação de uma infraestrutura de rede
empresarial virtualizada para a organização **TeckAlfa**.

O laboratório foi desenvolvido com recurso a **VMware, pfSense,
Ubuntu Server, Ubuntu Desktop e Samba Active Directory**.

O objectivo é implementar uma infraestrutura funcional com serviços de
rede, autenticação centralizada, partilhas de ficheiros, controlo de
acessos, administração remota, VPN e correio electrónico interno.

---

## Arquitectura

A infraestrutura é constituída pelos seguintes componentes:

- **pfSense** — Firewall, gateway, routing, NAT e VPN
- **DC01** — Ubuntu Server e controlador de domínio
- **desktop01** — Estação de trabalho Ubuntu
- **Samba Active Directory** — Gestão centralizada do domínio
- **DNS** — Resolução de nomes interna
- **Kerberos** — Autenticação
- **SMB/CIFS** — Partilha de ficheiros
- **ACLs** — Controlo de acessos
- **Cockpit** — Administração através de interface Web
- **VPN** — Acesso remoto seguro
- **Mail Server** — Serviço de correio electrónico interno

---

## Rede

### Rede interna

```text
192.168.10.0/24
