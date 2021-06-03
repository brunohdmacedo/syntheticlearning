---
title: Como gerar Dados Sintéticos e treinar um modelo com eles?
date: 2021-06-02 17:00:15 +0200
categories: ["machine learning", "computação gráfica", "visão computacional", "dados sintéticos", "IMPA", "Unity"]
background: /assets/triangle-pink.png
description: Nesta apresentação, veremos como é possível realizar experimentos com a plataforma Unity para geração de dados sintéticos que podem ser utilizados no treinamento de modelos para tarefas como detecção e reconhecimento de objetos ou estimativa de pose.
permalink: /gerando-dados-sinteticos
---

## [Please, check the slides here.](/syntheticlearning/presentation2.html)

### Qual o custo de se construir um conjuto de dados sintéticos? Que ferramentas podem ser utilizadas para este processo? Qual a complexidade de integrar ao treinamento dos modelos?

Essas são apenas algumas das perguntas que você pode estar se fazendo se deseja saber mais sobre a geração de dados sintéticos para machine learning. Em se tratando de computação visual, plataformas de mídia como as *engines* Unreal e Unity e, mais recentemente, o NVidia Omniverse tem sido utilizadas como suporte para pesquisas e desenvolvimento de aplicações. Neste tipo de ambiente, podemos automatizar a construção de cenas com alto grau de controle de propriedades como aparência e pose dos objetos de interesse, parâmetros das câmeras ou variação dos objetos de fundo. Além disso, o controle sobre o tipo de dado gerado – imagens RGB, mapas de profundidade, máscaras de segmentação, nuvem de pontos etc – e o controle sobre a quantidade de dados gerados, permitindo um balanceamento dos exemplos entre categorias, são características importantes .

Nesta apresentação, veremos como é possível realizar experimentos com a plataforma Unity para geração de dados sintéticos que podem ser utilizados no treinamento de modelos para tarefas como detecção e reconhecimento de objetos ou estimativa de pose. A partir da discussão iniciada no [primeiro seminário](/por-que-dados-sinteticos), verificaremos como podemos obter imagens rotuladas automaticamente e também realizar operações de aleatorização de domínio (*domain randomization*).
