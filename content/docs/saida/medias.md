---
title: "Saídas no Toque da Média"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "saida"
weight: 14
toc: true
---

O Robô Galton possui 2 médias de saída, que podem ser usadas em conjunto ou separadamente.

O toque na saída da média pode ser usado tanto em <ins>setups conservadores</ins> para alvos mais longos como para <ins>setups agressivos</ins> para proteção de movimentos bruscos do mercado.

## Média de Saída Primária

A média de saída primária é uma média móvel configurável onde o robô encerrará a operação imediatamente caso o preço toque na mesma.

- **Usar média de saída primária:** Liga ou desliga a média de proteção primária

- **Período da média de saída primária:** Período da média móvel de saída primária

- **Suavização da média de saída primária:** Tipo de suavização da média de saída primária

- **Cálculo da média de saída primária:** Preço usado no cálculo da média de saída primária

Abaixo, um exemplo visual de um setup à favor da tendência com saída no toque na média primária:

<div class="moldura">
    <img src="../../images/saida-01.png" alt="Setup à favor da tendência com saída no toque da média de saída primária">
    <p class="legenda">Setup à favor da tendência com saída no toque da média de saída primária</p>
</div>

## Média de Saída Secundária

A média de saída secundária funciona exatamente da mesma forma que a primária, podendo ser usado em conjunto ou não. O diferencial está na opção condicional da ativação. Esta média pode ser ativada somente caso o robô faça "x" aumentos de posição.

- **Usar média de saída secundária:** Liga ou desliga a média de proteção secundária. Opções: <ins>Sim</ins>, <ins>Não</ins> ou <ins>Após "X" aumentos</ins>

- **Aumentos mínimos:** Aumentos mínimos que o robô deve realizar antes de ativar a média secundária. Se o valor for 0 (zero), a média nao será usada

- **Período da média de saída secundária:** Período da média móvel de saída secundária

- **Suavização da média de saída secundária:** Tipo de suavização da média de saída secundária

- **Cálculo da média de saída secundária:** Preço usado no cálculo da média de saída secundária