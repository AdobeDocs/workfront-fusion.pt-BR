---
title: Variáveis matemáticas
description: As variáveis matemáticas a seguir estão disponíveis no painel  [!DNL Adobe Workfront Fusion mapping] .
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# Variáveis matemáticas

## pi

Representa o símbolo matemático $\pi$.

## [!UICONTROL random]

Retorna um número pseudo-aleatório de ponto flutuante no intervalo [`0`,`1`] (inclusive `0`, mas não `1`).

Use a seguinte fórmula para gerar um número pseudo-aleatório inteiro no intervalo [`min`,`max`] (incluindo `min` e `max`):

![Random](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
