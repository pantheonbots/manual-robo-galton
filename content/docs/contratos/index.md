---
title: "Aumentos de Posição"
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "contratos"
weight: 12
toc: true
---

Nesta seção você pode configurar os aumentos de posição caso a operação vá na direção oposta. O preenchimento é totalmente opcional mas na maioria das vezes salva a operação garantindo uma boa taxa de acerto.

O preenchimento dos valores é sempre relativo ao **ponto de entrada** da operação. Se sua estratégia faz aumentos à cada 200 pontos no mini índice, a distância deve ser preenchida de 200 em 200: 200, 400, 600, 800, etc

- **Tipo de ordem nos aumentos:** Configura se as ordens de aumento será enviadas no book no momento do inicio da operação ou se à mercado, sendo monitoradas as distâncias tick a tick
 
- **Distância em pontos (separados por vírgula):** Distância em pontos relativo ao ponto de entrada. Exemplo de preenchimento com um setup de 5 aumentos de 100 em 100 pontos no mini índice seria: **100,200,300,400,500**

- **Contratos/Lotes para cada aumento (separados por vírgula):** Quantidade de contratos que o robô vai adicionar na operação em cada nível de aumento. Exemplo de preenchimento para 5 níveis de aumento: **2,2,3,3,6**