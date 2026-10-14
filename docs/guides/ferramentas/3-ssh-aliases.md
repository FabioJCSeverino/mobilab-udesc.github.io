---
title: SSH aliases
description: Configure uma chave SSH e um alias SSH para acessar os robôs mais rápido, sem senha e sem confundir robôs.
---

Essa é uma forma de deixar o acesso aos robôs mais rápido, copiando uma chave SSH para o robô e criando um alias SSH.

## 1. Criar a chave

Se você ainda não tem uma chave ed25519, crie uma (o caminho padrão é `~/.ssh/id_ed25519`):

```sh
ssh-keygen -t ed25519 -C "seu-email"
```

## 2. Criar o alias

Adicione ao arquivo `~/.ssh/config`:

```text
Host h1
    HostName 192.168.123.164
    User unitree
    IdentityFile ~/.ssh/id_ed25519
    IdentitiesOnly yes
    HostKeyAlias h1
```

O `HostKeyAlias h1` é necessário porque o PC de desenvolvimento do G1 usa o mesmo IP, `192.168.123.164`. Sem ele, ao trocar de robô o SSH mostra `WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!`, porque guarda a chave do host por IP. Com o alias, a chave do H1-2 fica guardada sob o nome `h1`.

Se mesmo assim o aviso aparecer ao conectar pelo IP direto, veja [Aviso de chave do host alterada](#aviso-de-chave-do-host-alterada).

## 3. Copiar a chave para o robô

```sh
ssh-copy-id -i ~/.ssh/id_ed25519.pub h1
```

Execute este comando em um terminal interativo normal: ele pergunta se você aceita a chave do host (responda `yes`) e pede a senha do usuário `unitree` (no H1-2, `Unitree0408`). A opção `-i` instala essa chave específica, e não qualquer chave que esteja no `ssh-agent`.

## 4. Testar

```sh
ssh h1
```

O login deve ocorrer sem senha, em `unitree@unitree-h1-2-pc4`.

## Aviso de chave do host alterada

Se o SSH mostrar:

```text
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
```

É porque o H1-2 usa o mesmo IP do PC de desenvolvimento do G1 (`192.168.123.164`), e o host guardou a chave de outro robô. Remova a chave antiga e conecte de novo:

```sh
ssh-keygen -R 192.168.123.164
ssh unitree@192.168.123.164
```
