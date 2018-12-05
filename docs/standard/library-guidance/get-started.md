---
title: Introducción a la creación de bibliotecas de .NET de alta calidad
description: Introducción a la creación de bibliotecas de . NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 6377e3fe606bf7603b418decdd0e3f9d2de6a510
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/28/2018
ms.locfileid: "50201248"
---
# <a name="get-started"></a><span data-ttu-id="82090-103">Primeros pasos</span><span class="sxs-lookup"><span data-stu-id="82090-103">Get started</span></span>

## <a name="cross-platform-targetingcross-platform-targetingmd"></a>[<span data-ttu-id="82090-104">Destinatarios multiplataforma</span><span class="sxs-lookup"><span data-stu-id="82090-104">Cross-platform targeting</span></span>](./cross-platform-targeting.md)

<span data-ttu-id="82090-105">Cómo usar .NET Standard y varios destinos para crear bibliotecas multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="82090-105">How to use .NET Standard and multi-targeting to create cross-platform libraries.</span></span> <span data-ttu-id="82090-106">.NET se ejecuta en muchos lugares, y las buenas bibliotecas .NET deben esforzarse por admitir tantas plataformas y desarrolladores como sea posible.</span><span class="sxs-lookup"><span data-stu-id="82090-106">.NET runs in many places, and good .NET libraries should strive to support as many platforms and developers as possible.</span></span>

## <a name="strong-namingstrong-namingmd"></a>[<span data-ttu-id="82090-107">Nombres seguros</span><span class="sxs-lookup"><span data-stu-id="82090-107">Strong naming</span></span>](./strong-naming.md)

<span data-ttu-id="82090-108">Obtenga información sobre los nombres seguros y sus ventajas e inconvenientes.</span><span class="sxs-lookup"><span data-stu-id="82090-108">Learn about strong naming and its advantages and disadvantages.</span></span> <span data-ttu-id="82090-109">Los nombres seguros de una biblioteca de .NET permite a la mayoría de los desarrolladores utilizarla y es un procedimiento recomendado.</span><span class="sxs-lookup"><span data-stu-id="82090-109">Strong naming a .NET library allows the most developers to use it and is a recommended best practice.</span></span>

## <a name="nuget-and-open-source-librariesnugetmd"></a>[<span data-ttu-id="82090-110">NuGet y bibliotecas de código abierto</span><span class="sxs-lookup"><span data-stu-id="82090-110">NuGet and open-source libraries</span></span>](./nuget.md)

<span data-ttu-id="82090-111">La mejor forma de crear paquetes de NuGet para las bibliotecas .NET de código abierto, incluidos los metadatos recomendado para todos los paquetes publicados para todo el mundo en NuGet.org.</span><span class="sxs-lookup"><span data-stu-id="82090-111">The best way to create NuGet packages for open-source .NET libraries, including recommended metadata for all packages published publicly on NuGet.org.</span></span>

### <a name="dependenciesdependenciesmd"></a>[<span data-ttu-id="82090-112">Dependencias</span><span class="sxs-lookup"><span data-stu-id="82090-112">Dependencies</span></span>](./dependencies.md)

<span data-ttu-id="82090-113">NuGet facilita el uso de paquetes existentes al crear una biblioteca de .NET.</span><span class="sxs-lookup"><span data-stu-id="82090-113">NuGet makes it easy to use existing packages when building a .NET library.</span></span> <span data-ttu-id="82090-114">Obtenga información sobre los orígenes comunes de las dependencias de NuGet de fricción y cómo evitarlos.</span><span class="sxs-lookup"><span data-stu-id="82090-114">Learn about NuGet dependencies' common sources of friction and how to avoid them.</span></span>

### <a name="sourcelinksourcelinkmd"></a>[<span data-ttu-id="82090-115">SourceLink</span><span class="sxs-lookup"><span data-stu-id="82090-115">SourceLink</span></span>](./sourcelink.md)

<span data-ttu-id="82090-116">SourceLink es una excelente herramienta que permite a los usuarios de la biblioteca de .NET depurar paso a paso por instrucciones el código fuente durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="82090-116">SourceLink is a great tool that allows users of your .NET library to step into its source code while debugging.</span></span> <span data-ttu-id="82090-117">Este artículo es una introducción de lo que SourceLink es y por qué debería usarlo.</span><span class="sxs-lookup"><span data-stu-id="82090-117">This article is an overview of what SourceLink is and why you should use it.</span></span>

### <a name="publishingpublish-nuget-packagemd"></a>[<span data-ttu-id="82090-118">Publicación</span><span class="sxs-lookup"><span data-stu-id="82090-118">Publishing</span></span>](./publish-nuget-package.md)

<span data-ttu-id="82090-119">Aunque NuGet.org es el repositorio más conocido y utilizado, hay muchos lugares para publicar paquetes de NuGet.</span><span class="sxs-lookup"><span data-stu-id="82090-119">While NuGet.org is the most widely known and used repository, there are many places to publish NuGet packages.</span></span> <span data-ttu-id="82090-120">Obtenga información sobre los diferentes repositorios de paquetes de NuGet disponibles y prácticas recomendadas de seguridad para la publicación de una biblioteca de .NET.</span><span class="sxs-lookup"><span data-stu-id="82090-120">Learn about the different NuGet package repositories available, and security best practices for publishing a .NET library.</span></span>

## <a name="versioningversioningmd"></a>[<span data-ttu-id="82090-121">Control de versiones</span><span class="sxs-lookup"><span data-stu-id="82090-121">Versioning</span></span>](./versioning.md)

<span data-ttu-id="82090-122">Las buenas bibliotecas de .NET evolucionan con el tiempo, agregando características, corrigiendo errores y mejorando el rendimiento en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="82090-122">Good .NET libraries evolve over time, adding features, fixing bugs, and improving performance in later releases.</span></span> <span data-ttu-id="82090-123">Obtenga información sobre los distintos números de versión y cómo comunican cambios importantes a los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="82090-123">Learn about the various version numbers and how to communicate breaking changes to developers.</span></span>

### <a name="breaking-changesbreaking-changesmd"></a>[<span data-ttu-id="82090-124">Cambios importantes</span><span class="sxs-lookup"><span data-stu-id="82090-124">Breaking changes</span></span>](./breaking-changes.md)

<span data-ttu-id="82090-125">Es importante para una biblioteca de .NET buscar el equilibrio entre la estabilidad para los usuarios existentes y la innovación para el futuro.</span><span class="sxs-lookup"><span data-stu-id="82090-125">It's important for a .NET library to find a balance between stability for existing users and innovation for the future.</span></span> <span data-ttu-id="82090-126">Obtenga información sobre los diferentes tipos de cambios importantes y estrategias para agregar nuevas características y mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="82090-126">Learn about the different kinds of breaking changes and strategies for adding new features while maintaining backwards compatibility.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="82090-127">[Anterior](./index.md)
[Siguiente](./cross-platform-targeting.md)</span><span class="sxs-lookup"><span data-stu-id="82090-127">[Previous](./index.md)
[Next](./cross-platform-targeting.md)</span></span>