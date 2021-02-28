---
title: "Configurações da Estratégia"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "configuracoes"
weight: 11
toc: true
---

A configuração do setup começa por aqui. Nesta parte você define qual é a base do teu setup, se é contra tendência, se é à favor da tendência e outras opções básicas. É importante estar familiarizado com todos esses parâmetros, pois é aqui que você define a identidade da configuração, se é **agressivo**, **moderado** ou **conservador**.

## Início do Setup

- **Tipo de entrada:** Configura o robô apenas para compra, venda ou ambos.

- **Spread máximo permitido:** Caso esse valor seja maior do que 0 (zero) o Galton vai monitorar o spread no momento que o setup der sinal de entrada. Se o spread for maior do que o valor informado, a operação é cancelada. Em ativos como mini índice ou mini dolar, o spread na maioria das vezes não oscila muito e é constante. Esse parâmetro pode ter mais utilidade em ativos do forex.

- **Reversão da operação no sinal contrário:** Se ativado e caso o robô detecte um sinal contrário, fechará a operação atual (no lucro ou prejuízo) e inicia outra operação contrária.

<div class="moldura">
    <img src="../../images/reversao.png" alt="Reversão do sinal">
    <p class="legenda">Reversão do sinal</p>
</div>

A reversão ativada é bastante usada em médias curtas e DX baixo. À cada sinal contrário (setas azul e vermelho) o robô vai encerrar a operação atual e entrar no sentido do novo sinal. Dessa forma, ele cria uma espécie de zigzag dentro do canal criado pelo DX (mostrado pelas setas pretas)

- **Contratos/Lotes:** Número de contratos da primeira entrada.

- **Sinal apenas no fechamento do candle:** Se este parâmetro estiver ligado, o robô só irá verificar se houve rompimento da DX no fechamento do candle, ignorando qualquer sinal durante a formação do mesmo.

<div class="moldura">
    <img src="../../images/entrada-01.png" alt="Entradas somente no fechamento do candle">
    <p class="legenda">Entradas somente no fechamento do candle</p>
</div>

Com o parâmetro ligado, as entradas só serão validadas se o fechamento estiver pra fora da DX. Qualquer outro rompimento que seja fechado dentro é ignorado:

<div class="moldura">
    <img src="../../images/entrada-02.png" alt="Entradas ignoradas comparadas com entradas válidas num mesmo gráfico">
    <p class="legenda">Entradas ignoradas comparadas com entradas válidas num mesmo gráfico</p>
</div>

- **Somente uma entrada por candle:** Se este parâmetro estiver ligado, o robô só vai fazer 1 (uma) operação por candle. Abaixo uma situação onde várias entradas poderiam ser realizadas num único candle. Candle de grande extensão, onde uma entrada de alvo curto, e após a saída, continuaria dando sinal de venda. Se o parâmetro estiver ligado, todas essas possíveis entradas são ignoradas

<div class="moldura">
    <img src="../../images/entrada-03.png" alt="Possíveis múltiplas entradas no mesmo candle">
    <p class="legenda">Possíveis múltiplas entradas no mesmo candle</p>
</div>

- **Somente após o preço cruzar a DX:** Com esse parâmetro ligado, o sinal será válido somente se uma média de 1 período cruzar a DX. No exemplo visual abaixo temos o cruzamento identificado com as setas verdes, as entradas invalidadas na seta vermelha, e as entradas válidas em cor azul:

<div class="moldura">
    <img src="../../images/entrada-04.png" alt="Entradas válidas em azul pelo cruzamento indicado pela seta verde">
    <p class="legenda">Entradas válidas em azul pelo cruzamento indicado pela seta verde</p>
</div>

Este parâmetro é útil para impedir que o robô faça entradas sucessivas. Trabalha de forma semelhante à trava de re-entrada (detalhado mais pra frente)

- **Direção da entrada:** Indica se o robô irá operar na contra tendência ou a favor da tendência (opção favor da tendência somente na versão). Abaixo, exemplos visuais.

Entradas contra tendência:

<div class="moldura">
    <img src="../../images/entrada-05.png" alt="Entradas na contra tendência">
    <p class="legenda">Entradas na contra tendência</p>
</div>

Entradas à favor da tendência:

<div class="moldura">
    <img src="../../images/entrada-06.png" alt="Entradas à favor da tendência">
    <p class="legenda">Entradas à favor da tendência</p>
</div>

## Indicator da Média Principal

- **Período Média Móvel:** Período da média móvel principal, usada como base para calcular os DXs. Esta média é representada em preto em todos os exemplos desse manual
  
- **Suavização da Média Móvel:** Tipo de suavização da média

- **Cálculo da Média Móvel:** Preço usado no cálculo da média

- **Tipo do Indicador:** Se selecionado "DX Independente" é possível selecionar um valor para o DX superior e outro para o inferior. No modo "DX Clássico", o mesmo valor é usado para traçar a mesma distância superior e inferior
  
  - **[Clássico] Distância da Média Móvel (DX):**  Distância em pontos da média móvel que será traçado as médias de gatilho da estratégia
  
  - **[Independente] Distância Superior da Média Móvel (DX):** Distância em pontos acima da média móvel que será traçado o gatilho da estratégia
  
  - **[Independente] Distância Inferior da Média Móvel (DX):** Distância em pontos abaixo da média móvel que será traçado o gatilho da estratégia


- **Usar Desvio Padrão:** Se este parâmetro estiver ligado, o robô adiciona o valor do indicador "Desvio Padrão" à DX configurada acima, tornando o DX dinâmico.

- **Período Desvio Padrão:** Período usado para configurar o indicador Desvio Padrão

- **Usar ATR (Average True Range):** Se este parâmetro estiver ligado, o robô adiciona o valor do indicador "ATR" à DX configurada acima, tornando o DX dinâmico. Funciona exatamente da mesma forma que o Desvio Padrão

- **Período ATR:** Período usado para configurar o indicador ATR

## Considerações sobre o Desvio Padrão e o ATR

Com o Desvio Padrão ou o ATR ligado, o robô ignora a DX fixa, considerando apenas as médias mais externas. A DX fixa é exibida na tela apenas para comparação visual.

Como o indicador Desvio Padrão e o ATR são indicadores técnicos da familia dos "Osciladores", fica fácil compreender o uso em conjunto com uma DX fixa. Indicadores do tipo "oscilador" indicam apenas um número. Esse número é usado para somar à DX, criando um "colchão" de volatilidade em volta da DX, resultando em um setup menos agressivo e com melhores pontos de entrada

Abaixo, exemplo visual usando setup M4 DX25 com Desvio Padrão de 3 períodos:

<div class="moldura">
    <img src="../../images/entrada-07.png" alt="Setup M4 DX25 com desvio padrão de 3 períodos">
    <p class="legenda">Setup M4 DX25 com desvio padrão de 3 períodos</p>
</div>

Vale ressaltar que os indicadores Desvio Padrão e ATR acompanham o mercado tick à tick e seus valores tambem são alterados constantemente. Fique atento à esse detalhe caso use um setup onde há possibilidade de entrada em todos os ticks (não somente no fechamento do candle), pois após o fechamento do candle o Desvio Padrão ou o ATR pode indicar um valor diferente no momento da entrada da operação
