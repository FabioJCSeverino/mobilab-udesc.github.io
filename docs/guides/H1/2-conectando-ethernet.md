---
title: Conectando com ethernet
description: Conecte o computador host ao PC4 (computador de desenvolvimento) do robô Unitree H1-2 por cabo Ethernet e acesse via SSH.
---

No H1-2, a porta Ethernet de desenvolvimento fica na **frente do robô, no primeiro conector de cima**. Ela é um conector de aviação: use o adaptador Unitree de aviação para RJ45 da foto abaixo para ligar um cabo Ethernet comum.

<img src="/img/guides/unitree-h1/ethernet-adapter.png" alt="Adaptador Ethernet do Unitree H1-2" width="600" />

*Fonte: [docs.quadruped.de, H1: interface de rede](https://www.docs.quadruped.de/projects/h1/html/interface.html#network-interface).*

**Atenção:** conecte e desconecte o adaptador somente com o robô desligado. O manual proíbe conectar ou desconectar conectores de aviação com o robô ligado (hot swap). Confira se o conector do adaptador está totalmente encaixado: em um teste, uma conexão frouxa não deu link.

```text
Porta Ethernet do host  <--- Cabo Ethernet --->  Adaptador no conector superior da frente do H1-2
192.168.123.222/24                               192.168.123.164 (PC4)
```

## Endereços IP

| IP | Dispositivo | Usuário | Senha |
| --- | --- | --- | --- |
| `192.168.123.161` | PC1, computador de controle de movimento, sem acesso do usuário | - | - |
| `192.168.123.164` | PC4, computador de desenvolvimento (hostname `unitree-h1-2-pc4`) | `unitree` | `Unitree0408` |
| `192.168.124.20` | Lidar Livox MID-360 (em versões antigas, `192.168.123.120`) | - | - |

Em uma varredura de ping em `192.168.123.0/24`, apenas o PC1 e o PC4 responderam. O MID-360 fica na sub-rede `192.168.124.x`, por isso não aparece na varredura.

## Conectar via SSH

```sh
ssh unitree@192.168.123.164
```

Usuário SSH: `unitree`, senha: `Unitree0408`.

Para não digitar a senha e não confundir os robôs, configure a chave SSH e o alias `h1` no guia [SSH aliases](/guides/ferramentas/ssh-aliases).

Para mais detalhes, veja o [manual oficial do H1-2](https://support.unitree.com/home/en/H1_developer/About_H1-2).
