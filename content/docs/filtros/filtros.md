---
title: "Filtros de Entrada"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "filtros"
weight: 12
toc: true
---

Os filtros de entrada tem o papel de impedir uma entrada que poderia ser perigosa ou muito agressiva, como por exemplo um movimento muito brusco, ou ainda filtrar uma compra quando outro indicador está indicando venda (e vice versa). No geral, os indicadores de filtro de entrada são mais úteis em setups mais conservadores e/ou que operam à favor da tendência, já que setups contra tendência são essencialmente agressivos e precisam da volatilidade para operar com eficiência

## Filtro de Média Movel

- **(1) Usar tendência por média móvel:** Se ligado, o robô fará apenas operações a favor da tendência da média móvel configurada.

- **(1) Período da média móvel:** Período da média móvel exponencial usada para indicar a tendência

## Filtro VWAP

- **(2) Usar tendência por VWAP:** Se ligado, o robô fará apenas operações a favor da tendência da VWAP configurada.

- **(2) Período da VWAP:** Período usado no indicador VWAP, sendo um dos 3: diário, semanal ou mensal.

## Filtro HiLo

- **(3) Usar tendência por HiLo:** Se ligado, o robô fará apenas operações a favor da tendência do indicador HiLo configurado.

- **(3) Período do HiLo:** Período usado no indicador HiLo.

- **(3) Suavização do HiLo:** Tipo de suavização usado para calcular.

## Filtro SuperTrend

- **(4) Usar tendência por SuperTrend:** Se ligado, o robô fará apenas operações a favor da tendência do indicador SuperTrend configurado.

- **(4) Período do CCI:** Período usado do CCI do SuperTrend.

- **(4) Cálculo do Preço do CCI:** Tipo de preço usado no CCI do SuperTrend.

- **(4) Período do ATR:** Período do ATR.

## Filtro Volume

- **(5) Usar Volume:** Se ligado, o robô fará apenas operações caso o volume estiver abaixo da média do volume configurado.

- **(5) Tipo do Volume:** A quantidade de trades do candle é representada pelo tipo "Tick". A quantidade de contratos é representada pelo tick "Real".

- **(5) Período da Média:** Período da média movel a ser calculada em cima do volume.

## Filtro Amplitude

- **(6) Usar Amplitude:** Se ligado, o robô filtrará operações de acordo com a amplitude do preço de referência.

- **(6) Direção do Filtro:** "<ins>Libera acima da amplitude máxima</ins>:" O robô irá monitorar o preço em relação à distância do preço de referência em pontos configurada. Por exemplo, se a distância for 500 no WIN, o robô irá liberar operações somente se o preço se distanciar 500 ou mais pontos do preço de referência. Vale para cima ou para baixo. A outra opção "<ins>Libera abaixo da amplitude máxima</ins>" funciona de forma inversa.

- **(6) Referência do preço:** Tipo do preço a ser usado como referência do filtro de amplitude.

- **(6) Distância em pontos da referência:** Distância em pontos que o robô vai considerar para liberar ou travar as operações dependendo da direção configurada.

## Filtro RSI (Ou IFR - Índice de Força Relativa) 

- **(7) Usar RSI:** Se ligado, bloqueia ou libera operações de acordo com a configuração do filtro.

- **(7) Período:** Período usado no indicador RSI.

- **(7) Sobrecomprado:** Nível a ser considerado sobrecomprado. Se o valor do RSI estiver <ins>acima</ins> deste valor, vai liberar <ins>somente vendas</ins>.

- **(7) Sobrevendido:** Nível a ser considerado sobrevendido. Se o valor do RSI estiver <ins>abaixo</ins> deste valor, vai liberar <ins>somente compras</ins>.

Abaixo exemplo visual de um setup M10 DX50 contra tendência com todas as compras canceladas (regiões em azul) pelo filtro de tendência de média móvel de período 80. Tambem no exemplo, indicado pelas setas vermelhas as vendas válidas. Os outros funcionam da mesma forma na validação do sinal:

<div class="moldura">
    <img src="../../images/entrada-08.png" alt="Setup M10 DX50 com filtro de tendência média móvel de 80 períodos">
    <p class="legenda">Setup M10 DX50 com filtro de tendência média móvel de 80 períodos</p>
</div>
