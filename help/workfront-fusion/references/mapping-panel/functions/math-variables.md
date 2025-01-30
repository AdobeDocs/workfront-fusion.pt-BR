---
title: Variáveis matemáticas
description: As variáveis matemáticas a seguir estão disponíveis no painel  [!DNL Adobe Workfront Fusion mapping] .
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# Variáveis matemáticas

## pi

Representa o símbolo matemático $\pi$.

## [!UICONTROL random]

Retorna um número pseudo-aleatório de ponto flutuante no intervalo [`0`,`1`] (inclusive `0`, mas não `1`).

Use a seguinte fórmula para gerar um número pseudo-aleatório inteiro no intervalo [`min`,`max`] (incluindo `min` e `max`):

![Aleatório](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
