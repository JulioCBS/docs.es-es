---
title: "ICorProfilerCallback::ExceptionSearchFilterLeave (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ExceptionSearchFilterLeave
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ExceptionSearchFilterLeave
helpviewer_keywords:
- ICorProfilerCallback::ExceptionSearchFilterLeave method [.NET Framework profiling]
- ExceptionSearchFilterLeave method [.NET Framework profiling]
ms.assetid: c28a2a82-dd11-4385-843f-b509fb61753b
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 41d4d9e9eca19356109afe38c2a28f1b5da2f682
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackexceptionsearchfilterleave-method"></a><span data-ttu-id="ee032-102">ICorProfilerCallback::ExceptionSearchFilterLeave (Método)</span><span class="sxs-lookup"><span data-stu-id="ee032-102">ICorProfilerCallback::ExceptionSearchFilterLeave Method</span></span>
<span data-ttu-id="ee032-103">Notifica al generador de perfiles que un filtro de usuario solo ha terminado de ejecutar.</span><span class="sxs-lookup"><span data-stu-id="ee032-103">Notifies the profiler that a user filter has just finished executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee032-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee032-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFilterLeave();  
```  
  
## <a name="requirements"></a><span data-ttu-id="ee032-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee032-105">Requirements</span></span>  
 <span data-ttu-id="ee032-106">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ee032-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee032-107">**Encabezado:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ee032-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ee032-108">**Biblioteca:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee032-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee032-109">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee032-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee032-110">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee032-110">See Also</span></span>  
 [<span data-ttu-id="ee032-111">ICorProfilerCallback (interfaz)</span><span class="sxs-lookup"><span data-stu-id="ee032-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="ee032-112">ExceptionSearchFilterEnter (método)</span><span class="sxs-lookup"><span data-stu-id="ee032-112">ExceptionSearchFilterEnter Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterenter-method.md)