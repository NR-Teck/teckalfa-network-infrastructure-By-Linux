# TeckAlfa — Infraestrutura de Rede e Sistemas

## Sobre o projecto

Este projecto documenta a implementação de uma infraestrutura de rede
empresarial virtualizada para a organização TeckAlfa.

O laboratório utiliza VMware, pfSense, Ubuntu Server, Ubuntu Desktop e
Samba Active Directory.

## Arquitectura

A infraestrutura é constituída por:

- pfSense;
- DC01;
- desktop01;
- Samba Active Directory;
- DNS;
- Kerberos;
- SMB;
- ACLs;
- Cockpit;
- VPN;
- correio electrónico interno.

## Rede

```text
Rede interna: 192.168.10.0/24
Gateway:      192.168.10.1
DC01:         192.168.10.10
desktop01:    192.168.10.128
