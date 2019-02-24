---
title: Un paseo por C# - Guía de C#
description: ¿Nuevo en C#? Conozca los conceptos básicos del lenguaje.
ms.date: 08/10/2016
ms.assetid: ebc727cd-8112-42e7-b59c-3c2873ad661c
ms.openlocfilehash: bece954c095870651126e486c2c6eb978e78f96d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2018
ms.locfileid: "53150399"
---
# <a name="a-tour-of-the-c-language"></a>Un paseo por el lenguaje C#  

C# (pronunciado "si sharp" en inglés) es un lenguaje de programación sencillo, moderno, orientado a objetos y con seguridad de tipos. C# tiene sus raíces en la familia de lenguajes C, y a los programadores de C, C++, Java y JavaScript les resultará familiar inmediatamente.

C# es un lenguaje orientado a objetos, pero también incluye compatibilidad para programación ***orientada a componentes***. El diseño de software contemporáneo se basa cada vez más en componentes de software en forma de paquetes independientes y autodescriptivos de funcionalidad. La clave de estos componentes es que presentan un modelo de programación con propiedades, métodos y eventos; tienen atributos que proporcionan información declarativa sobre el componente; e incorporan su propia documentación. C# proporciona construcciones de lenguaje para admitir directamente estos conceptos, por lo que se trata de un lenguaje muy natural en el que crear y usar componentes de software.

Varias características de C# ayudan en la construcción de aplicaciones sólidas y duraderas: la ***recolección de elementos no utilizados*** automáticamente reclama la memoria ocupada por objetos no utilizados y no accesibles; el ***control de excepciones*** proporciona un enfoque estructurado y extensible para la detección de errores y la recuperación; y el diseño del lenguaje ***con seguridad de tipos*** hace imposible leer desde las variables sin inicializar, indizar matrices más allá de sus límites o realizar conversiones de tipos no comprobados.

C# tiene un ***sistema de tipo unificado***. Todos los tipos de C#, incluidos los tipos primitivos como `int` y `double`, se heredan de un único tipo `object` raíz. Por lo tanto, todos los tipos comparten un conjunto de operaciones comunes, y los valores de todos los tipos se pueden almacenar, transportar y utilizar de manera coherente. Además, C# admite tipos de valor y tipos de referencia definidos por el usuario, lo que permite la asignación dinámica de objetos, así como almacenamiento en línea de estructuras ligeras.

Para asegurarse de que las programas y las bibliotecas de C# pueden evolucionar a lo largo del tiempo de manera compatible, se ha puesto mucho énfasis en el ***versionamiento*** del diseño de C#. Muchos lenguajes de programación prestan poca atención a este problema y, como resultado, los programas escritos en dichos lenguajes se interrumpen con más frecuencia de lo necesario cuando se introducen nuevas versiones de las bibliotecas dependientes. Los aspectos del diseño de C# afectados directamente por las consideraciones de versionamiento incluyen los modificadores `virtual` y `override` independientes, las reglas para la resolución de sobrecargas de métodos y la compatibilidad para declaraciones explícitas de miembros de interfaz.

## <a name="hello-world"></a>Hola a todos

El programa "Hola mundo" tradicionalmente se usa para presentar un lenguaje de programación. En este caso, se usa C#:

[!code-csharp[Hello World](../../../samples/snippets/csharp/tour/hello/Program.cs#L1-L8)]

Normalmente, los archivos de código fuente de C# tienen la extensión de archivo `.cs`. Suponiendo que el programa "Hola mundo" se almacena en el archivo `hello.cs`, el programa podría compilarse con la línea de comandos:

```console
csc hello.cs
```

Se produce un ensamblado ejecutable denominado hello.exe. La salida que genera la aplicación, cuando se ejecuta es:

```console
Hello, World
```

> [!IMPORTANT]
> El comando `csc` compila el marco de trabajo completo y puede no estar disponible en todas las plataformas.


El programa "Hola mundo" empieza con una directiva `using` que hace referencia al espacio de nombres `System`. Los espacios de nombres proporcionan un método jerárquico para organizar las bibliotecas y los programas de C#. Los espacios de nombres contienen tipos y otros espacios de nombres; por ejemplo, el espacio de nombres `System` contiene varios tipos, como la clase `Console` a la que se hace referencia en el programa, y otros espacios de nombres, como `IO` y `Collections`. Una directiva `using` que hace referencia a un espacio de nombres determinado permite el uso no calificado de los tipos que son miembros de ese espacio de nombres. Debido a la directiva `using`, puede utilizar el programa `Console.WriteLine` como abreviatura de `System.Console.WriteLine`.

La clase `Hello` declarada por el programa "Hola mundo" tiene un miembro único, el método llamado `Main`. El método `Main` se declara con el modificador static. Mientras que los métodos de instancia pueden hacer referencia a una instancia de objeto envolvente determinada utilizando la palabra clave `this`, los métodos estáticos funcionan sin referencia a un objeto determinado. Por convención, un método estático denominado `Main` sirve como punto de entrada de un programa.

La salida del programa la genera el método `WriteLine` de la clase `Console` en el espacio de nombres `System`. Esta clase la proporcionan las bibliotecas de clase estándar, a las que, de forma predeterminada, el compilador hace referencia automáticamente.

Hay mucha más información sobre C#.  Los temas siguientes proporcionan introducciones a los elementos del lenguaje C#. Estas introducciones proporcionarán información básica sobre todos los elementos del lenguaje y ofrecerán los detalles necesarios para profundizar más en los elementos del lenguaje C#:

* [Estructura del programa](program-structure.md)
    - Conozca los principales conceptos organizativos del lenguaje C#: ***programas***, ***espacios de nombres***, ***tipos***, ***miembros*** y ***ensamblados***.
* [Tipos y variables](types-and-variables.md)
    - Obtenga información sobre los ***tipos de valor***, los ***tipos de referencia*** y las ***variables*** del lenguaje C#.
* [Expresiones](expressions.md)
    - Las ***expresiones*** se construyen con ***operandos*** y ***operadores***. Las expresiones producen un valor.
* [Instrucciones](statements.md)
    - Use ***instrucciones*** para expresar las acciones de un programa.
* [Clases y objetos](classes-and-objects.md)
    - Las ***clases*** son los tipos más fundamentales de C#. Los ***objetos*** son instancias de una clase. Las clases se generan mediante ***miembros***, que también se tratan en este tema.
* [Structs](structs.md)
    - Las ***estructuras*** son estructuras de datos que, a diferencia de las clases, son tipos de valor.
* [Matrices](arrays.md)
    - Una ***matriz*** es una estructura de datos que contiene un número de variables a las que se accede mediante índices calculados.
* [Interfaces](interfaces.md)
    - Una ***interfaz*** define un contrato que se puede implementar mediante clases y structs. Una interfaz puede contener métodos, propiedades, eventos e indexadores. Una interfaz no proporciona implementaciones de los miembros que define, simplemente especifica los miembros que se deben proporcionar mediante clases o structs que implementan la interfaz.
* [Enumeraciones](enums.md)
    - Un ***tipo de enumeración*** es un tipo de valor distinto con un conjunto de constantes con nombre.
* [Delegados](delegates.md)
    - Un ***tipo de delegado*** representa las referencias a métodos con una lista de parámetros determinada y un tipo de valor devuelto. Los delegados permiten tratar métodos como entidades que se puedan asignar a variables y se puedan pasar como parámetros. Los delegados son similares al concepto de punteros de función en otros lenguajes, pero a diferencia de los punteros de función, los delegados están orientados a objetos y presentan seguridad de tipos.
* [Atributos](attributes.md)
    * Los ***atributos*** permiten a los programas especificar información declarativa adicional sobre los tipos, miembros y otras entidades.

>[!div class="step-by-step"]
>[Siguiente](program-structure.md)
