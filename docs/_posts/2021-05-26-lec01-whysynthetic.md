---
title: Por que usar dados sintéticos?
categories: ["machine learning", "computação gráfica", "visão computacional", "dados sintéticos", "IMPA"]
date: 2021-05-26 17:00:15 +0200
background: /assets/triangle-blue.png
description: Neste seminário, vamos apresentar problemas que motivam o uso de dados sintéticos e discutir questões técnicas para o treinamento de modelos de aprendizado de máquina a partir de trabalhos recentes na área.
permalink: /por-que-dados-sinteticos
---

## [Please, check the slides here.](/presentation1.html)

### Como as máquinas aprendem?

*Esta é uma pergunta que talvez não admita uma resposta simples. No entanto, sem adentrar questões filosóficas, podemos analisar alguns casos. *

A forma mais comum de treinar modelos de aprendizado de máquina hoje em dia é o *aprendizado supervisionado*. Nesta abordagem, usamos dados rotulados para aprender um modelo, uma função que respeita determinadas hipóteses. Conhecemos os valores de entrada (os dados) e os valores de saída (os rótulos) desta função e, com isso, podemos ajustar os parâmetros do nosso modelo, justamente por saber quando ele está acertando e quando ele está errando. Este cenário nos leva a uma das primeiras dificuldades em se construir conjuntos de dados: 

> "Como conseguir os rótulos corretos dos dados?"

Pensando em um exemplo clássico de visão computacional, se quisermos construir um modelo para diferenciar entre cadeiras e sofás, como conseguimos imagens cujo conteúdo sabemos que são cadeiras ou sofás? Para rotular os dados, precisamos que um ser humano avalie cada exemplo e anote o que está presente de acordo com o objetivo do problema. Além de aumentar o custo de aquisição dos dados, esta componente humana em um processo tão repetitivo aumenta a probabilidade de inserção de erros no processo. Este é um exemplo de situação que motiva o uso de dados, pois tendo o controle da geração dos dados, podemos ter os rótulos de cada exemplo automaticamente.

Ao adotar este paradigma, no entanto, algumas questões precisam ser respondidas, por exemplo: é preciso que as imagens sejam fotorrealistas? Ainda precisamos de dados reais no treinamento? Como aumentar as chances de um modelo treinado com dados sintéticos funcionar bem em dados reais? Neste seminário, vamos apresentar problemas que motivam o uso de dados sintéticos, tais como custo, viés e privacidade, e discutir questões técnicas para o treinamento de modelos de aprendizado de máquina a partir de trabalhos recentes na área. Com essa introdução, buscamos compreender os pré-requisitos para um bom uso de dados sintéticos e a capacidade de generalização dos modelos treinados.