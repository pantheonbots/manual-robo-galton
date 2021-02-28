---
title: "Horários"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "horarios"
weight: 16
toc: true
---

Configura as opções de horário de operação do robô. O Galton possui 2 blocos de operação. O primeiro bloco é obrigatório o preenchimento, sendo segundo opcional.

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Fique atento na configuração dos horários de operação! Uma causa de um robô não operante é a inconsistência dos horários de operação.</p>
</div>

## Primeiro horário

- **Primeiro Horário de Início (entradas):** Define o horário que o robô iniciará suas operações de entrada

- **Primeiro Horário de Término (entradas):** Define o horário que o robô encerrará as operações de entradas. Caso o robô esteja posicionado após este horário, a operação nao é encerrada. O robô apenas não fará mais entradas mas dará continuidade na operação normalmente.

## Segundo horário (opcional)

- **Usar o Segundo Horário:** Configura o uso ou não de um segundo bloco de horário de operações. Se não estiver ligado, os horários configurados no segundo bloco são ignorados

- **Segundo Horário de Início (entradas):** Define o horário que o robô iniciará suas operações de entrada

- **Segundo Horário de Término (entradas):** Define o horário que o robô encerrará as operações de entradas. Caso o robô esteja posicionado após este horário, a operação nao é encerrada. O robô apenas não fará mais entradas mas dará continuidade na operação normalmente.

## Daytrade / Fechamento de Posições

Use essa opção caso esteja operando Day Trade, forçando o fechamento independente se no lucro ou prejuízo

- **Fechar operações no final do dia:** Liga ou desliga o fechamento forçado das operações no horário configurado.

- **Horário de fechamento (posições):** Horário de fechamento se a opção DayTrade estiver ligada

<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Fique atento! O horário de fechamento deve ser <u>sempre</u> posterior ao horário de término de operações</p>
</div>
