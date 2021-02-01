---
title: "Conhecendo a Estratégia"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "introducao"
weight: 1
toc: true
---

O robô Galton usa como estratégia base o retorno à media quando opera na contra tendência ou afastamento da média quando opera à favor da tendência. A estratégia dá sinais de entrada quando o preço ultrapassa uma distância previamente configurada de uma média móvel.

Como essa distância é fixa (mas configurável), e sabendo que o mercado pode se tornar extremamente volátil, se faz necessário ajustes constantes na distância e/ou na média, além de outros parâmetros. Nesta introdução, será apresentado apenas uma noção básica das entradas. Todos os exemplos serão para o ativo mini-índice (WIN).

## Como configurar

Configurar uma estratégia no robô Galton é bastante simples, pois basta traçar uma média móvel e uma distância fixa (*sempre em pontos*), que será replicada pra cima, e pra baixo.

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Todas as configurações de distância são medidas em pontos, seja em mini contratos, forex ou ações. Use a ferramenta "+" do Metatrader5 para medir a distância desejada no gráfico que equivale ao valor que deseja</p>
</div>

## Exemplo Média 12 DX 70

Abaixo, um exemplo de média móvel de 12 períodos com distancia de 70 pontos, no mini índice (M12 DX70) com tempo gráfico de 1 minuto:

<div class="moldura">
    <img src="../../images/intro-01.png" alt="Media móvel 12 (em preto) com as duas distâncias (DX) fixas de 70">
    <p class="legenda">Media móvel 12 (em preto) com as duas distâncias (DX) fixas de 70</p>
</div>

O Robô irá monitorar essa média e suas distâncias (vamos chamar a distância apenas de DX daqui pra frente) para realizar entradas.

- Para uma **compra** ser realizada, o preço precisa romper a DX inferior (azul)
- Para uma **venda** ser realizada, o preço precisa romper a DX superior (vermelha)

Abaixo, outro exemplo com a mesma configuração M12 DX70 com as setas azuis apontando compra e vermelho apontando venda:

<div class="moldura">
    <img src="../../images/intro-02.png" alt="Configuração M12 DX 70 com setas de entrada">
    <p class="legenda">Configuração M12 DX 70 com setas de entrada</p>
</div>

Muito frequentemente, o trade vai contra a sua posição. Quando isso acontece você tem a opção de realizar aumentos de posição para melhorar o seu preço médio. Segue um exemplo de uma operação vendida que precisou de 2 aumentos de posição para sair positivo:

<div class="moldura">
    <img src="../../images/intro-03.png" alt="No círculo azul, o preço médio aproximado após o segundo aumento ser realizado (segunda seta laranja)">
    <p class="legenda">No círculo azul, o preço médio aproximado após o segundo aumento ser realizado (segunda seta laranja)</p>
</div>


Na próxima seção abordaremos a dinâmica entre o período da média móvel e a distância DX, o que torna um setup agressivo ou conservador, e a importância das análises de volatilidade dos dias anteriores.