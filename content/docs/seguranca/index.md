---
title: "Configurações de Segurança"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "seguranca"
weight: 18
toc: true
---

Esta seção é extremamente importante e é absolutamente necessário que se entenda todos os parâmetros. A parametrização adequada ao teu perfil é essencial para em momentos de instabilidade você possa se prevenir de eventuais sustos ou problemas de conexão com a corretora.

<div class="alert alert-danger d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>É possível que em casos de problemas detectados onde o robô é pausado e/ou removido do gráfico, fique alguma operação aberta, por isso a necessidade de verificação e possível intervenção manual.</p>
</div>

⚠️ Extremamente recomendado que deixe a **Trava de Segurança** LIGADA ⚠️

- **(Trava de Segurança) Pausa operações se detectado algum erro:** Pausa operações se detectado erro: Caso o robô se depare com uma situação onde é detectado um problema de conexao e/ou um erro é retornado pela corretora, o robô fará uma pausa nas operações.
 
- **Tempo em segundos de pausa após a trava ser acionada:** Após esse tempo, o robô volta a funcionar. Tempo padrão é 1800 segundos (30 minutos)


<div class="alert alert-warning d-flex" role="alert">
    <div class="flex-shrink-1 alert-icon">👉</div>
    <p>Em casos de parada de operação pelo acionamento da trava, e após verificações manuais você decida continuar as operações normalmente, é necessário remover o robô do gráfico e colocar novamente para reiniciar o timer interno (configurado acima) da trava</p>
</div>


## Temporizadores

- **Tempo em segundos para a confirmação da posição de entrada:** Toda entrada de posição precisa ser confirmada para captura do preço real e eventuais ajustes no take profit por conta do spread. Esta opção limita o tempo máximo de espera de confirmação. Se após esse tempo a operação não for confirmada, o robô irá disparar um erro

- **Tempo em segundos de pausa após fechamento manual:** Caso haja um fechamento manual das operaões (tecla ESC enquanto o estiver posicionado), o robô irá fazer uma breve pausa para não entrar logo em seguida. Tempo suficiente para fazer a pausa manual do robô (tecla ESC se não estiver posicionado)

## Outros

- **Remover o robô do gráfico após a trava ser acionada:** Com esta opção ativada, o robô é removido imediatamente do gráfico após **qualquer erro** ser detectado

- **Envia notificação para celular após erro ser detectado:** Com esta opção ativada, é enviado uma mensagem para o celular após qualquer erro ser detectado. Instruções para [Android](https://www.metatrader5.com/pt/mobile-trading/android/help/messages) e [iPhone/iPad](https://www.metatrader5.com/pt/mobile-trading/iphone/help/settings/settings_messages#notification_setup)



