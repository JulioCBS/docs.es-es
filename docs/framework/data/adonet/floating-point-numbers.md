---
title: Números de punto flotante
ms.date: 03/30/2017
ms.assetid: 73c218c6-1c44-4402-a167-4f6262629a91
ms.openlocfilehash: a30252d7d25b3c3e09dd5e59f364d94aa40dd272
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55903970"
---
# <a name="floating-point-numbers"></a>Números de punto flotante
En este tema se describen algunos de los problemas que con frecuencia se encuentran los programadores al trabajar con números de punto flotante en [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)]. Estos problemas se deben a la forma que los equipos almacenan números de punto flotante y no son específicos de un proveedor determinado, como <xref:System.Data.SqlClient> o <xref:System.Data.OracleClient>.  
  
 En general, los números de punto flotante no tienen una representación binaria exacta. En realidad, el equipo almacena una aproximación del número. En diferentes momentos se pueden utilizar diferentes números de dígitos binarios para representar el número. Cuando un número de punto flotante se convierte de una representación a otra, los dígitos menos significativos de dicho número pueden variar ligeramente. Por lo general el cambio se produce cuando el número se convierte de un tipo a otro. La variación se produce si la conversión se realiza en una base de datos, entre tipos que representan valores de base de datos o entre tipos. Debido a estos cambios, los números que lógicamente deberían ser iguales pueden presentar cambios en sus dígitos menos significativos que hagan que muestren valores diferentes. La cantidad de dígitos de precisión en el número puede ser mayor o menor de la esperada. Cuando el formato del número cambia a cadena, puede que no muestre el valor esperado.  
  
 Para reducir estos efectos al mínimo, debe usar la coincidencia más próxima entre tipos de números que haya disponible. Por ejemplo, si está trabajando con SQL Server, el valor numérico exacto puede cambiar si convierte un valor de Transact-SQL de tipo real en un valor de tipo float. En el [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)], convirtiendo un <xref:System.Single> a un <xref:System.Double> también se puede producir resultados inesperados. En ambos casos, una estrategia adecuada consiste en establecer que todos los valores de la aplicación usen el mismo tipo numérico. También puede utilizar un tipo de decimal de precisión fija o bien convertir los números de punto flotante a un tipo decimal de precisión fija antes de trabajar con ellos.  
  
 Para solucionar problemas relacionados con la comparación de igualdad, puede codificar la aplicación de forma que se pasen por alto las diferentes en los dígitos menos significativos. Por ejemplo, en lugar de comparar dos números para comprobar si son iguales, puede restar un número del otro. Si la diferencia se sitúa en un margen aceptable de redondeo, la aplicación puede considerar los números como si fuesen iguales.  
  
## <a name="see-also"></a>Vea también
- [Por qué los números de punto flotante pierden precisión](/cpp/build/reference/why-floating-point-numbers-may-lose-precision)
- [Información general sobre ADO.NET](ado-net-overview.md)
