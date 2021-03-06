---
title: Abgeleitete mathematische Funktionen (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- arithmetic operations, derived math functions
- cosecant function
- arcsecant function
- arccotangent function
- functions [Visual Basic], derived math functions
- inverse functions
- math functions, derived
- derived math functions
- cotangent function
- angles
- secant function
- trigonometric functions
- logarithms
- arccosecant function
- hyperbolic functions
- arcsine function
- degrees
- arccosine function
ms.assetid: 63e449d8-9444-44fb-8db1-6d9cf346e2aa
ms.openlocfilehash: 87faa623f5b145eec8b88e350fce4171125324dc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
ms.locfileid: "33596807"
---
# <a name="derived-math-functions-visual-basic"></a>Abgeleitete mathematische Funktionen (Visual Basic)
Die folgende Tabelle zeigt den nicht systeminternen mathematische Funktionen, die von systeminternen mathematischen Funktionen abgeleitet werden, können die <xref:System.Math?displayProperty=nameWithType> Objekt. Sie können die systeminternen mathematischen Funktionen zugreifen, indem hinzufügen `Imports System.Math` zur Datei oder zum Projekt.  
  
|Funktion|Abgeleitete äquivalente|  
|--------------|-------------------------|  
|Secant (Sec(x))|1 / Cos(x)|  
|Cosecant (Csc(x))|1 / Sin(x)|  
|Kotangens (Ctan(x))|1 / Tan(x)|  
|Arkussinus (Asin(x))|Atan (X / Sqrt (-X * X + 1))|  
|Umgekehrte Kosinus (Acos(x))|Atan (-X / Sqrt (-X * X + 1)) + 2 \* Atan(1)|  
|Inverse sekans (Asec(x))|2 * Atan(1) – Atan(Sign(x) / Sqrt (X \* x – 1))|  
|Inverse kosekans (Acsc(x))|Atan(Sign(x) / Sqrt (X * x – 1))|  
|Umgekehrten Kotangens (Acot(x))|2 * Atan(1) - ARCTAN(x)|  
|Hyperbolischer Sinus (Sinh(x))|(Exp(x) – eingesetzte / 2|  
|Hyperbolischer Kosinus (Cosh(x))|(Exp(x) + eingesetzte / 2|  
|Hyperbolischer Tangens (Tanh(x))|(Exp(x) – eingesetzte / (Exp(x) + eingesetzte|  
|Hyperbolischen sekans (Sech(x))|2 / (Exp(x) + eingesetzte|  
|Hypberbolischen kosekans (Csch(x))|2 / (Exp(x) – eingesetzte|  
|Hyperbolischen Kotangens (Coth(x))|(Exp(x) + eingesetzte / (Exp(x) – eingesetzte|  
|Umgekehrter hyperbolischer Sinus (Asinh(x))|Protokoll (X + Sqrt (X * X + 1))|  
|Umgekehrter hyperbolischer Kosinus (Acosh(x))|Protokoll (X + Sqrt (X * x – 1))|  
|Umgekehrter hyperbolischer Tangens (Atanh(x))|Protokoll ((1 + x) / (1 – X)) / 2|  
|Umgekehrten hyperbolischen sekans (AsecH(x))|Log ((Sqrt (-X * X + 1) + 1) / x)|  
|Umgekehrten hyperbolischen kosekans (Acsch(x))|Log((Sign(x) * Sqrt (X \* X + 1) + 1) / x)|  
|Umgekehrten hyperbolischen Kotangens (Acoth(x))|Protokoll ((x + 1) / (x – 1)) / 2|  
  
## <a name="see-also"></a>Siehe auch  
 [Mathematische Funktionen](../../../visual-basic/language-reference/functions/math-functions.md)
