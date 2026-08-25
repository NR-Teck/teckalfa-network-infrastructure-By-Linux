# 11 — VPN

## 11.1 Objectivo

A VPN terá como objectivo permitir acesso remoto seguro à infraestrutura
interna da TeckAlfa.

## 11.2 Arquitectura prevista

```text
Cliente remoto
      |
    VPN
      |
   pfSense
      |
192.168.10.0/24
      |
   Recursos internos
