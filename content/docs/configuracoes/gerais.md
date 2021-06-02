---
title: "Configurações Gerais"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "configuracoes"
weight: 10
toc: true
---

Em geral essas configurações podem ser deixadas no valor padrão, com exceção do **Número Mágico**.

## Parâmetros

- **Nome do Setup:** Nome que vai identificar o seu setup. Parâmetro opcional. O nome fica visível no canto superior esquerdo do grafico, como mostrado abaixo:

- **Número Mágico:** Um número qualquer de sua escolha que vai ser usado para identificar as operações do robô. Este número deve ser único e não deve ser usado ao mesmo tempo em outro robô.

- **Tipo de preenchimento das ordens à mercado:** Configura qual vai ser a política de preenchimento. Abaixo segue uma breve explicação retirada do próprio site da MetaTrader5:

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Altere esse parâmetro apenas se souber o que está fazendo. Em caso de dúvidas, entre em contato para auxiliarmos</p>
</div>

> **ORDER_FILLING_FOK**: Esta política de preenchimento significa que uma ordem pode ser preenchida somente na quantidade especificada. Se a quantidade desejada do ativo não está disponível no mercado, a ordem não será executada. O volume requerido pode ser preenchido usando várias ofertas disponíveis no mercado no momento.


> **ORDER_FILLING_IOC**: Este modo significa que um negociador concorda em executar uma operação com o volume máximo disponível no mercado conforme indicado na ordem. No caso do volume integral de uma ordem não puder ser preenchido, o volume disponível dele será preenchido, e o volume restante será cancelado.

> **ORDER_FILLING_RETURN**: Esta política é usada somente para ordens a mercado (ORDER_TYPE_BUY e ORDER_TYPE_SELL), ordens limit e stop limit (ORDER_TYPE_BUY_LIMIT, ORDER_TYPE_SELL_LIMIT, ORDER_TYPE_BUY_STOP_LIMIT e ORDER_TYPE_SELL_STOP_LIMIT ) e somente para os ativos com execução a Mercado ou execução em um sistema de negociação externo (Exchange)***. No caso de um preenchimento parcial, uma ordem a mercado ou do tipo limit com volume remanescente não é cancelada, mas processada posteriormente.
Para a ativação das ordens ORDER_TYPE_BUY_STOP_LIMIT e ORDER_TYPE_SELL_STOP_LIMIT, uma ordem limit correspondente, ORDER_TYPE_BUY_LIMIT/ORDER_TYPE_SELL_LIMIT com o tipo de execução ORDER_FILLING_RETURN, é criada.
Em termos práticos, o valor padrão FOK é o mais usado. Até o momento da criação deste manual, somente a modal (servidor não DMA4) usa o valor RETURN em suas ordens.

- **Intervalo do timer interno (milisegundos):** Valor em milisegundos do timer de verificação de metas. Valor Padrão: 100

## Teclas de Atalho

Para a tecla ESC funcionar corretamente, é preciso "focar" no o gráfico do robô, ou seja, apenas clique em qualquer parte do gráfico do ativo.

- **Tecla ESC**: Ao pressionar a tecla ESC, o robô terá a seguinte resposta:

	- **Se o robô estiver posicionado**: O robô perguntará se você quer <ins>fechar manualmente</ins> todas as posições do ativo atual.

	- **Se o robô não estiver posicionado**: Pausa o robô manualmente. Enquanto pausado, o robô não fará operações. Para despausar, apenas aperte ESC novamente. Enquanto o robô estiver pausado, o seu painel ficará ligeiramente apagado para fácil identificação.

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Caso queira fechar as operações do robô manualmente é recomendável que faça pelo próprio robo através da tecla <b>ESC</b>!. Fechamentos pelo cliente do Metatrader 5 não são contabilizados pelo robô e os lucros ou prejuízos não serão contabilizados no painel </p>
</div>