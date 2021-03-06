---
title: Seguridad para subprocesos en expresiones regulares
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- .NET Framework regular expressions, threads
- regular expressions, threads
- searching with regular expressions, threads
- parsing text with regular expressions, threads
- pattern-matching with regular expressions, threads
ms.assetid: 7c4a167b-5236-4cde-a2ca-58646230730f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1c0bcab0757bc48f6a8216dd5878f0289e49a275
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075016"
---
# <a name="thread-safety-in-regular-expressions"></a>Seguridad para subprocesos en expresiones regulares
La clase <xref:System.Text.RegularExpressions.Regex> es en sí misma segura para subprocesos e inmutable (de solo lectura). Es decir, se pueden crear objetos **Regex** en cualquier subproceso y compartirlos entre varios subprocesos; los métodos de coincidencia pueden llamarse desde cualquier subproceso y no modifican nunca el estado global.  
  
 Pero los objetos de resultado (**Match** y **MatchCollection)** que devuelve **Regex** deben usarse en un único subproceso. Aunque muchos de estos objetos son lógicamente inmutables, sus implementaciones pueden retrasar el cálculo de algunos resultados para mejorar el rendimiento y, en consecuencia, los llamadores deben serializar el acceso a ellos.  
  
 Si es necesario compartir objetos de resultado de **Regex** en varios subprocesos, estos objetos se pueden convertir en instancias seguras para subprocesos llamando a sus métodos sincronizados. A excepción de los enumeradores, todas las clases de expresiones regulares son seguras para subprocesos o pueden convertirse en objetos seguros para subprocesos mediante un método sincronizado.  
  
 Los enumeradores son la única excepción. Las aplicaciones debe serializar las llamadas a enumeradores de colecciones. La regla es que, si una colección puede enumerarse simultáneamente en más de un subproceso, se deben sincronizar los métodos de enumerador en el objeto raíz de la colección que recorre el enumerador.  
  
## <a name="see-also"></a>Vea también

- [Expresiones regulares de .NET](../../../docs/standard/base-types/regular-expressions.md)
