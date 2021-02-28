---
title: "Configurações de Saída"
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

Os Parâmetros aqui descritos são responsáveis pelo comportamento da saída da operação, como um Take Profit um Stop Loss ou ainda várias outras opções intermediárias disponíveis para configuração. Esse meio termo é considerado como uma proteção da sua operação.

A partir deste ponto, a configuração desses vários parâmetros de proteção tornará teu setup único, pois há uma variedade enorme de combinações desses parâmetros de proteção 

## Intervalos de operação

- **Intervalo para a próxima entrada:** Tempo em segundos de intervalo forçado entre as entradas.

- **Intervalo após operação positiva:** Tempo em segundos de intervalo forçado após uma operação de saldo positivo ou igual à 0 (zero)

- **Intervalo após operação negativa:** Tempo em segundos de intervalo forçado após uma operação de saldo negativo

## Take Profit

- **Tipo da ordem no Take Profit:** Configura se o Take Profit será à mercado ou no book.

- **Take Profit em pontos:** Distância em pontos **relativo ao preço médio**.

## Take Profit Dinâmico

Com o TP Dinâmico ligado, o robô irá monitorar os aumentos de posição. À cada aumento realizado, o robô irá remover do valor configurado no Take Profit (descrito acima) o valor configurado abaixo.

<ins>Exemplo</ins>: Uma operação comprada com alvo de 100 pontos no mini-índice, e "Decremento" configurado em 10 pontos, se o robô realizou 2 aumentos de posição o TP atual se torna 80 de alvo em **relação ao preço médio**.

- **Ativar Take Profit Dinâmico**: Liga ou desliga o Take Profit Dinâmico.

- **Decremento à cada aumento**: Valor a ser subtraído do Take Profit à cada aumento de posição.

- **Take Profit Mínimo**: Valor mínimo a ser configurado em caso de TP Dinâmico ligado. Funciona como uma trava de segurança. Aceita valores negativos. Essa opção é importante para não deixar o seu take profit muito negativo, pois dependendo da configuração do decremento isso pode ser possível. O robô aceita valores negativos pois pode haver casos onde é aceitavel sair de uma posição pesada com um prejuízo controlado do que correr mais risco desnecessário por mais tempo. Tempo este que pode ser usado para recuperar o prejuízo.

## Stop Loss

- **Referência do Stop Loss**: Indica se o stop loss vai ser fixo em relação ao ponto de entrada ou ao preço médio, sendo necessário reajuste após aumento de posição.

- **Stop Loss em pontos**: Distância em pontos do preço de entrada (ou do preço médio se assim configurado)

## Saída Parcial

- **Usar Saída Parcial**: Liga ou desliga a saída parcial.

- **Alvo em pontos**: Take profit de cada saída parcial. O número de contratos/lotes usado é o mesmo do aumento de posição atual. Exemplo: Entrada de 1 contrato com 2 aumentos de 2 e 3 contratos respectivamente. No primeiro aumento (de 2 contratos/lotes) o robô fará uma saída parcial de 2 contratos, e no segundo aumento (de 3 contratos/lotes) o robô fará uma saída parcial de 3 contratos