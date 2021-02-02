---
title: "Trava de Re-Entrada"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "trava"
weight: 14
toc: true
---

A trava de re-entrada é uma média configurável onde, caso ativada, passa a ser monitorada apenas após uma saída de operação, seja com saldo positivo ou negativo.

A partir deste momento, o robô não fará mais nenhuma entrada, ignorando qualquer sinal. Após o preço tocar nesta média configurada, o robô está liberado para fazer novas leituras de sinais de entrada

- **Usar trava de re-entrada:** Liga ou desliga a trava de re-entrada
 
- **Período da média da trava de re-entrada:** Período da média móvel da trava de re-entrada

- **uavização da média da trava de re-entrada:** Tipo de suavização da média da trava de re-entrada

- **Cálculo da média da trava de re-entrada:** Preço usado no cálculo da média da trava de re-entrada

## Exemplo

Abaixo um exemplo visual de uma trava de re-entrada em ação. Primeira seta azul comprou normalmente e atingiu o seu alvo no círculo preto. A trava foi ativada. O preço subiu e atravessou a trava (média preta).

Ao atingir a média o robô foi liberado a ler sinais, e logo em seguida deu sinal de venda (seta vermelha), que atingiu o take profit rapidamente (círculo preto). A partir deste momento, a trava é ligada novamente, e todos os sinais foram ignorados (setas em cinza).

O robô só é autorizado a realizar novas entradas após o preço tocar na média da trava (círculo laranja), o que faz o robô ler um sinal de venda logo em seguida:

<div class="moldura">
    <img src="../../images/trava.png" alt="Setup contra tendência com trava de re-entrada">
    <p class="legenda">Setup contra tendência com trava de re-entrada</p>
</div>


