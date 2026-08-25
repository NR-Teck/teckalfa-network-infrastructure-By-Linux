# 10 — Cockpit

## 10.1 Objectivo

O Cockpit disponibiliza uma interface web para administração do
servidor Ubuntu.

## 10.2 Serviço

O socket do Cockpit é verificado através de:

```bash
sudo systemctl status cockpit.socket --no-pager
