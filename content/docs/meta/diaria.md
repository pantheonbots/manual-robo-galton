---
title: "Configurações de Meta Diária"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "meta"
weight: 17
toc: true
---

Configura as metas diárias das operações. Após qualquer meta configurada for atingida, o robô encerra suas operações no dia.

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>As metas são verificadas <ins>apenas no final</ins> de cada trade, portanto se você tem uma meta financeira diária de Loss de R$400 (ou $400 se estiver no forex), o robô <ins>não vai encerrar operações</ins> se sua posição atual estiver em -R$700 (ou -$700 se forex).</p>
</div>


## Meta Financeira

- **Limite financeiro de Gain:** Se o saldo financeiro positivo de suas operações ultrapassarem esse valor, o robô encerra as operações no dia. Por exemplo "100" equivale a R$100 (ou $100 se forex) de meta

- **Limite financeiro de Loss:** Se o saldo financeiro negativo de suas operações ultrapassarem esse valor, o robô encerra as operações no dia. Por exemplo "100" equivale a R$100 (ou $100 se forex) de meta. Detalhe: uma meta de perda diária de R$300 (ou $300 se forex) deve ser preenchida como "300" e não como "-300"

## Meta em Pontos

- **Limite em pontos de Gain:** Se o saldo em pontos positivos de suas operações ultrapassarem esse valor, o robô encerra as operações no dia.

- **Limite em pontos de Loss:** Se o saldo em pontos negativos de suas operações ultrapassarem esse valor, o robô encerra as operações no dia. Detalhe: uma meta de perda diária de 500 pontos deve ser preenchida como "500" e não como "-500"

## Meta em Operações

- **Limite total de operações:** Encerra as entradas caso o limite de operações - independente do saldo de cada uma - seja atingido. Em operações em conta hedge, onde todos os aumentos são entradas individuais, o robô considera todas essas entradas como parte de uma mesma operação

- **Limite total de operações de Gain:** Encerra as entradas caso o limite de operações com saldo positivas ou sem lucro seja atingido. Em operações em conta hedge, onde todos os aumentos são entradas individuais, o robô considera todas essas entradas como parte de uma mesma operação

- **Limite total de operações de Loss:** Encerra as entradas caso o limite de operações com saldo negativas seja atingido. Em operações em conta hedge, onde todos os aumentos são entradas individuais, o robô considera todas essas entradas como parte de uma mesma operação