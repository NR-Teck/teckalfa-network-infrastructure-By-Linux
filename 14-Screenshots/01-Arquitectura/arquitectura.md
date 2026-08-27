### Interfaces do pfSense

O pfSense possui duas interfaces de rede principais.

A interface WAN encontra-se ligada à rede NAT do VMware e recebe
configuração através de DHCP.

A interface LAN constitui o gateway da rede interna TeckAlfa.

#### WAN

```text
IPv4:   192.168.198.137
Mask:   255.255.255.0
Gateway: 192.168.198.2
DHCP:   UP
