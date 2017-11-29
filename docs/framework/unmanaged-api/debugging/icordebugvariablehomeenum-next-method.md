---
title: "ICorDebugVariableHomeEnum::Next (método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
api_name: ICorDebugVariableHomeEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugVariableHomeEnum::Next
helpviewer_keywords:
- ICorDebugVariableHomeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: eb9ea96c-5b58-4655-8104-094fc8b393b8
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 480317a4ec0515411f1ca8156a5bc4d06aa3f38a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvariablehomeenumnext-method"></a><span data-ttu-id="4144a-102">ICorDebugVariableHomeEnum::Next (método)</span><span class="sxs-lookup"><span data-stu-id="4144a-102">ICorDebugVariableHomeEnum::Next Method</span></span>
<span data-ttu-id="4144a-103">Obtiene el número especificado de [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instancias que contienen información sobre las variables locales y argumentos en una función.</span><span class="sxs-lookup"><span data-stu-id="4144a-103">Gets the specified number of [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances that contain information about the local variables and arguments in a function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4144a-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4144a-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)] ICorDebugVariableHome *homes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4144a-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4144a-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="4144a-106">[in] Número de objetos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4144a-106">[in] The number of objects to be retrieved.</span></span>  
  
 `homes`  
 <span data-ttu-id="4144a-107">Una matriz de punteros, cada uno de los cuales señala a un [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objeto que proporciona información sobre una variable local o argumento de una función.</span><span class="sxs-lookup"><span data-stu-id="4144a-107">An array of pointers, each of which points to a [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) object that provides information about  a local variable or argument of a function.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="4144a-108">[out] El número de instancias realmente devueltos en objetos.</span><span class="sxs-lookup"><span data-stu-id="4144a-108">[out] The number of instances actually returned in objects.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4144a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4144a-109">Return Value</span></span>  
 <span data-ttu-id="4144a-110">El método devuelve los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="4144a-110">The method returns the following values.</span></span>  
  
|<span data-ttu-id="4144a-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="4144a-111">HRESULT</span></span>|<span data-ttu-id="4144a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4144a-112">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="4144a-113">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4144a-113">The method completed successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="4144a-114">Recupera el número real de instancias, como se refleja en `pceltFetched`, es menor que el número de instancias solicitadas.</span><span class="sxs-lookup"><span data-stu-id="4144a-114">The actual number of instances retrieved, as reflected in `pceltFetched`, is less than the number of instances requested.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4144a-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4144a-115">Remarks</span></span>  
 <span data-ttu-id="4144a-116">El [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) método recupera un máximo de `celt` objetos a partir de la posición actual del enumerador.</span><span class="sxs-lookup"><span data-stu-id="4144a-116">The [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) method retrieves a maximum of  `celt` objects starting at the current position of the enumerator.</span></span> <span data-ttu-id="4144a-117">Cuando el método vuelve, `pceltFetched` contiene el número real de los objetos recuperados.</span><span class="sxs-lookup"><span data-stu-id="4144a-117">When the method returns, `pceltFetched` contains the actual number of objects retrieved.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4144a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4144a-118">Requirements</span></span>  
 <span data-ttu-id="4144a-119">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4144a-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4144a-120">**Encabezado:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4144a-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4144a-121">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4144a-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4144a-122">**Versiones de .NET framework:**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4144a-122">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4144a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4144a-123">See Also</span></span>  
 [<span data-ttu-id="4144a-124">Interfaz ICorDebugVariableHomeEnum</span><span class="sxs-lookup"><span data-stu-id="4144a-124">ICorDebugVariableHomeEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)  
 [<span data-ttu-id="4144a-125">Interfaz ICorDebugVariableHome</span><span class="sxs-lookup"><span data-stu-id="4144a-125">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)