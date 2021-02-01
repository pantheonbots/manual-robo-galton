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

**Nome do Setup:** Nome que vai identificar o seu setup. Parâmetro opcional. O nome fica visível no canto superior esquerdo do grafico, como mostrado abaixo:

**Tipo de preenchimento das ordens à mercado:** Configura qual vai ser a política de preenchimento. Abaixo segue uma breve explicação retirada do próprio site da MetaTrader5:

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Altere esse parâmetro apenas se souber o que está fazendo. Em caso de dúvidas, entre em contato para auxiliarmos</p>
</div>

> **ORDER_FILLING_FOK**: Esta política de preenchimento significa que uma ordem pode ser preenchida somente na quantidade especificada. Se a quantidade desejada do ativo não está disponível no mercado, a ordem não será executada. O volume requerido pode ser preenchido usando várias ofertas disponíveis no mercado no momento.


> **ORDER_FILLING_IOC**: Este modo significa que um negociador concorda em executar uma operação com o volume máximo disponível no mercado conforme indicado na ordem. No caso do volume integral de uma ordem não puder ser preenchido, o volume disponível dele será preenchido, e o volume restante será cancelado.


> **ORDER_FILLING_RETURN**: Esta política é usada somente para ordens a mercado (ORDER_TYPE_BUY e ORDER_TYPE_SELL), ordens limit e stop limit (ORDER_TYPE_BUY_LIMIT, ORDER_TYPE_SELL_LIMIT, ORDER_TYPE_BUY_STOP_LIMIT e ORDER_TYPE_SELL_STOP_LIMIT ) e somente para os ativos com execução a Mercado ou execução em um sistema de negociação externo (Exchange)***. No caso de um preenchimento parcial, uma ordem a mercado ou do tipo limit com volume remanescente não é cancelada, mas processada posteriormente.
Para a ativação das ordens ORDER_TYPE_BUY_STOP_LIMIT e ORDER_TYPE_SELL_STOP_LIMIT, uma ordem limit correspondente, ORDER_TYPE_BUY_LIMIT/ORDER_TYPE_SELL_LIMIT com o tipo de execução ORDER_FILLING_RETURN, é criada.
Em termos práticos, o valor padrão FOK é o mais usado. Até o momento da criação deste manual, somente a modal (servidor não DMA4) usa o valor RETURN em suas ordens.

**Número Mágico:** Um número qualquer de sua escolha que vai ser usado para identificar as operações do robô. Este número deve ser único e não deve ser usado ao mesmo tempo em outro robô.

**Spread máximo permitido:** Caso esse valor seja maior do que 0 (zero) o Galton vai monitorar o spread no momento que o setup der sinal de entrada. Se o spread for maior do que o valor informado, a operação é cancelada. Em ativos como mini índice ou mini dolar, o spread na maioria das vezes não oscila muito e é constante. Esse parâmetro pode ter mais utilidade em ativos do forex.