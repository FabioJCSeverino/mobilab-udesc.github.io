---
id: pairdrop
title: Copiar e colar comandos com o PairDrop
description: Como usar o PairDrop para enviar comandos, URLs e arquivos entre o notebook e os óculos de VR (Meta Quest ou PICO).
---

Digitar URLs longas como `https://vuer.ai?ws=wss://<IP_DO_ROBO>:8012` com o teclado virtual dos óculos é lento e propenso a erros. O [PairDrop](https://pairdrop.net/) resolve isso: é uma página web que transfere textos e arquivos entre dispositivos diretamente pelo navegador, sem instalar nada e sem criar conta.

Funciona em qualquer navegador moderno, incluindo o navegador padrão do **Meta Quest** e do **PICO**.

## Conectando os dispositivos

1. No notebook, abra [https://pairdrop.net](https://pairdrop.net/).
2. Nos óculos, abra o navegador padrão e acesse o mesmo endereço.
3. Cada dispositivo recebe um nome aleatório, exibido na parte inferior da página (por exemplo, "Teal Penguin"). Se ambos estiverem na mesma rede, o outro dispositivo aparece como um ícone no centro da tela.

## Enviando um comando ou URL

1. No notebook, **clique com o botão direito** no ícone dos óculos (ou mantenha pressionado, em telas touch) e escolha enviar mensagem.
2. Cole o texto (comando, URL, IP etc.) e clique em **Enviar**.
3. Nos óculos, aparece uma janela com o texto recebido. Clique em **Copiar** e cole na barra de endereços ou no campo desejado.

O mesmo vale no sentido contrário: nos óculos, mantenha o gatilho pressionado sobre o ícone do notebook para enviar um texto para ele.

## Enviando arquivos

Clique (sem o botão direito) no ícone do dispositivo de destino e selecione os arquivos, ou arraste-os sobre o ícone. Isso é útil para trazer capturas de tela e gravações dos óculos para o notebook.

## Exemplos de uso

- URL do vuer para a teleoperação: `https://vuer.ai?ws=wss://<IP_DO_ROBO>:8012` (veja [Operação via Wi-Fi](/guides/G1/teleoperacao/execucao/via-wifi)).
- Endereço direto do servidor: `https://<IP_DO_ROBO>:8012`.
