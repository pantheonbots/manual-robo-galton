---
title: "Configurações de Saída"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "saida"
weight: 13
toc: true
---

Os Parâmetros aqui descritos são responsáveis pelo comportamento da saída da operação, como um Take Profit um Stop Loss ou ainda várias outras opções intermediárias disponíveis para configuração. Esse meio termo é considerado como uma proteção da sua operação.

A partir deste ponto, a configuração desses vários parâmetros de proteção tornará teu setup único, pois há uma variedade enorme de combinações desses parâmetros de proteção 

## Intervalos de operação

- **Intervalo para a próxima entrada:** Tempo em segundos de intervalo forçado entre as entradas.

- **Intervalo após operação positiva:** Tempo em segundos de intervalo forçado após uma operação de saldo positivo ou igual à 0 (zero)

- **Intervalo após operação negativa:** Tempo em segundos de intervalo forçado após uma operação de saldo negativo

## Take Profit

- **Tipo da ordem no Take Profit:** Configura se o Take Profit será à mercado ou no book.

- **Take Profit em pontos:** Distância em pontos relativo ao preço médio.

## Take Profit Dinâmico

Com o TP Dinâmico ligado, o robô irá monitorar os aumentos de posição. À cada aumento realizado, o robô irá remover do valor configurado no Take Profit (descrito acima) o valor configurado abaixo.

<ins>Exemplo</ins>: Uma operação comprada com alvo de 100 pontos no mini-índice, e "Decremento" configurado em 10 pontos, se o robô realizou 2 aumentos de posição o TP atual se torna 80.

- **Ativar Take Profit Dinâmico**: Liga ou desliga o Take Profit Dinâmico.

- **Decremento à cada aumento**: Valor a ser subtraído do Take Profit à cada aumento de posição.

- **Take Profit Mínimo**: Valor mínimo a ser configurado em caso de TP Dinâmico ligado. Funciona como uma trava de segurança. Aceita valores negativos.

## Stop Loss

- **Referência do Stop Loss**: Indica se o stop loss vai ser fixo em relação ao ponto de entrada ou ao preço médio, sendo necessário reajuste após aumento de posição.

- **Stop Loss em pontos**: Distância em pontos do preço de entrada (ou do preço médio se assim configurado)

## Break Even

O Break Even possui 4 níveis, que trabalham de forma semelhante ao trailing stop (ou stop móvel). A diferença é que no break even você tem o controle da distância e proteção individualmente, mas limitados somente à 4 niveis.

- **(1~4) Distância em pontos:** Distância em pontos do preço entrada que ao atingir o robô fará o reajuste do Stop Loss

- **(1~4) Ganho mínimo em pontos:** Distância em pontos do preço de entrada que será usada como proteção da operação

## Trailing Stop

- **Remove o Take Profit ao iniciar o Trailing Stop:** Se ativado. ao realizar a primeira proteção (ou ao realizar a primeira modificação do stop), o robô remove o take profit. Desta forma a operação fica sem alvo, e num mercado direcional pode atingir alvos mais longos

- **Ativa a partir de X pontos (0 ativa imediatamente):** Distância em pontos a partir do preço entrada que ao atingir o robô fará o <ins>acionamento</ins> do trailing stop. Neste momento não há é realizado nenhum ajuste do stop loss. Se 0, o trailing já está ativo e realizará a alteração do stop loss assim que atingir a distância do preço de entrada

- **Distância em pontos (0 não usar):** Distância em pontos a partir do <ins>preço atual</ins> que o robô fará o ajuste do stop loss

- **Passos em pontos (0 não usar):** Intervalo em pontos a partir do <ins>preço de ativação</ins> que o trailing fará o reajuste do stop loss