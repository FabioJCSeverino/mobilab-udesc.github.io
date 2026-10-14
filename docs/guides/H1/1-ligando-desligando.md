---
title: Ligando e desligando o H1-2
description: Passos essenciais para ligar, levantar, sentar e desligar o robô humanoide Unitree H1-2 com o controle remoto.
---

Este guia resume os passos essenciais. Para o procedimento completo, veja o [Quick Start oficial](https://support.unitree.com/home/en/H1_developer/quick_start) (o procedimento é o mesmo para o H1 e o H1-2) e o [guia de controle do docs.quadruped.de](https://www.docs.quadruped.de/projects/h1/html/controller.html).

<div align="center">
  <video width="860" controls preload="metadata">
    <source src="https://oss-global-cdn.unitree.com/static/H1%E6%95%99%E7%A8%8BEN.mp4" type="video/mp4"/>
  </video>
</div>

*Fonte: vídeo oficial da Unitree.*

Depois de ligar, a sequência para deixar o robô operável é:

- `L2 + B`: entra em damping.
- `L2 + UP`: entra em ready.
- `R2 + X`: ativa o controle de movimento.

A partir daí, o robô pode ser comandado pelos joysticks.

**Parada de emergência:** se o robô entrar em um estado anormal, pressione `L2 + B`. Ele entra em damping e desce devagar até o chão.

## Ligando com o robô suspenso

1. Garanta que o robô está suspenso, com os pés tocando o chão.
2. Ligue as duas baterias ao mesmo tempo: pressione rapidamente uma vez e depois segure por mais de 2 segundos.
3. A inicialização leva cerca de 120 segundos. Espere o som dos tornozelos chegando ao limite e aguarde mais 30 segundos.
4. `L2 + B` para entrar em damping e `L2 + UP` para entrar em ready. Os pés se abrem e os braços ficam ao lado da cintura.
5. Desça o pórtico até os pés tocarem o chão e o tronco ficar estável.
6. `R2 + X` para entrar no Sport Mode. O H1-2 dá alguns passos no lugar.
7. Quando o movimento estabilizar, solte o gancho e retire a corda. Use os joysticks para mover o robô e `START` para alternar entre parado em pé e caminhando.

## Desligando com o robô suspenso

1. Com o H1-2 em pé, prenda a corda de volta no gancho e levante até a corda ficar tensionada.
2. `L2 + B` para entrar em damping.
3. Desligue as duas baterias ao mesmo tempo: pressione rapidamente e depois segure.

Em damping, em vez de desligar, também é possível voltar ao estado ready com `R2 + X`.

## Ligando a partir de uma cadeira

**Atenção:** o quadril do H1-2 é largo. Use um assento largo e estável. O H1-2 precisa de ajuda para levantar e sentar: segure o suporte traseiro durante todo o movimento para ele não tombar para trás.

1. Sente o H1-2 na cadeira, instale as baterias e ligue-as.
2. Espere o clique dos tornozelos chegando ao limite mecânico.
3. `L2 + B` para entrar em damping e `L2 + UP` para levantar, segurando o suporte traseiro.
4. Com o robô em pé e estável, `R2 + X` para o modo de caminhada. Solte o suporte aos poucos, depois de confirmar o equilíbrio.

## Sentando e desligando

1. Posicione o H1-2 em frente à cadeira, de costas para ela.
2. `L2 + LEFT` para sentar. O robô dá um passo para trás e desce. Segure o suporte traseiro até ele estar sentado.
3. Desligue as baterias ou, se necessário, comande que ele levante de novo.
