# Auto Script SSH/VPN

### Sistem Minimal
|Sistem|Minimal|Disarankan|
|--|--|--|
|Arch|amd64|amd64|
|OS|Debian 10|Debian 11|
|CPU|1 Core|2 Cores atau lebih|
|RAM|amd64|amd64|
|Storage|15 GB|20 GB|

### Fitur
|Tunnel Type|Port List|
|----|----|
|OpenSSH|`22`|
|Dropbear| `80` `143` `443` <br> `446` [*Stunnel*]  <br> `445` [*Stunnel WS*]|
|Stunnel|Dropbear `446`<br> SSH Websocket `445`<br> Softether `1195`<br> OpenVPN `2296`|
|SSH WebSocket|`80` `443` `8880`|
|SSH WebSocket TLS|`80` `443`|
|SlowDNS|`5300`|
|OHP|OpenSSH `2083`<br> OpenVPN `2087`|
|OpenVPN|TCP `2294`<br>UDP `2295`<br>TLS `2296` [*Stunnel*]<br>OHP `2087`|
|HTTP Proxy|`8080`|
|Socks5 Proxy|`80` `443` `990`|
|BadVPN-udpgw|`7200` `7300` `7400`|
|SoftetherVPN|Remote `5555`<br> TCP/UDP `1194`<br> TLS `1195` [*Stunnel*]<br> SSTP `4433`<br> L2TP IPSec `500` `1701` `4500`|
|Trojan-GFW|`2443`|
|Hysteria|`80` `443`|
|V2Ray|VMess WS TLS `80` `443`<br> VMess WS NonTLS `80` `443` `8881`<br> VLess TCP XTLS `5443`<br> VMess gRPC `80` `443` `11443`<br>Trojan TCP TLS `3443`<br> Trojan WS TLS `80` `443`|
|XRay|VMess WS TLS `80` `443`<br> VMess WS NonTLS `80` `443` `2095`<br> VLess TCP XTLS `6443`<br> VMess gRPC `80` `443` `11444`<br>Trojan TCP TLS `3445`<br> Trojan WS TLS `80` `443`|

## Instalasi

### Langkah 1

    addgroup dip
    apt update -y && apt upgrade -y --fix-missing && update-grub && sleep 2 && reboot

### Langkah 2

    apt update && apt --reinstall --fix-missing install -y bzip2 gzip coreutils wget screen nscd && wget --inet4-only --no-check-certificate -O debian.sh 'https://script2.gegevps.com/debian.sh' && chmod +x debian.sh && screen -S debian ./debian.sh
