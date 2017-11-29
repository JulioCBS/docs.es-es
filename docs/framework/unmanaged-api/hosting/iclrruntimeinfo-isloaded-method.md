---
title: "ICLRRuntimeInfo::IsLoaded (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeInfo.IsLoaded
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeInfo::IsLoaded
helpviewer_keywords:
- IsLoaded method [.NET Framework hosting]
- ICLRRuntimeInfo::IsLoaded method [.NET Framework hosting]
ms.assetid: fdc5a3a7-71ff-4025-99a1-59e4ee0bfe1b
topic_type: apiref
caps.latest.revision: "18"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ac7ed77dd4cb141257a1b73ccd433c7d17ee1f38
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrruntimeinfoisloaded-method"></a><span data-ttu-id="c69ac-102">ICLRRuntimeInfo::IsLoaded (Método)</span><span class="sxs-lookup"><span data-stu-id="c69ac-102">ICLRRuntimeInfo::IsLoaded Method</span></span>
<span data-ttu-id="c69ac-103">Indica si common language runtime (CLR) asociado a la [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaz se carga en un proceso.</span><span class="sxs-lookup"><span data-stu-id="c69ac-103">Indicates whether the common language runtime (CLR) associated with the [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface is loaded into a process.</span></span> <span data-ttu-id="c69ac-104">Un tiempo de ejecución se puede cargar sin también está iniciando.</span><span class="sxs-lookup"><span data-stu-id="c69ac-104">A runtime can be loaded without also being started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c69ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c69ac-105">Syntax</span></span>  
  
```  
HRESULT IsLoaded(  
[in]  HANDLE hndProcess,  
[out, retval] BOOL *pbLoaded);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c69ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c69ac-106">Parameters</span></span>  
 `hndProcess`  
 <span data-ttu-id="c69ac-107">[in] Un identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="c69ac-107">[in] A handle to the process.</span></span>  
  
 `pbLoaded`  
 <span data-ttu-id="c69ac-108">[out] `true` si CLR se carga en el proceso; en caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="c69ac-108">[out] `true` if the CLR is loaded into the process; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c69ac-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c69ac-109">Return Value</span></span>  
 <span data-ttu-id="c69ac-110">Este método devuelve los siguientes HRESULT específicos así como los errores HRESULT que indican un error del método.</span><span class="sxs-lookup"><span data-stu-id="c69ac-110">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="c69ac-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c69ac-111">HRESULT</span></span>|<span data-ttu-id="c69ac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c69ac-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c69ac-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c69ac-113">S_OK</span></span>|<span data-ttu-id="c69ac-114">El método se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c69ac-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="c69ac-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="c69ac-115">E_POINTER</span></span>|<span data-ttu-id="c69ac-116">`pbLoaded` es null.</span><span class="sxs-lookup"><span data-stu-id="c69ac-116">`pbLoaded` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c69ac-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c69ac-117">Remarks</span></span>  
 <span data-ttu-id="c69ac-118">Este método es compatible con las interfaces y las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="c69ac-118">This method is backward-compatible with the following functions and interfaces:</span></span>  
  
-   <span data-ttu-id="c69ac-119">[ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interfaz (en la API de hospedaje de la versión 1 de .NET Framework).</span><span class="sxs-lookup"><span data-stu-id="c69ac-119">[ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface (in the .NET Framework version 1 hosting API).</span></span>  
  
-   <span data-ttu-id="c69ac-120">[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interfaz (en la API de hospedaje de .NET Framework 2.0).</span><span class="sxs-lookup"><span data-stu-id="c69ac-120">[ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface (in the .NET Framework 2.0 hosting API).</span></span>  
  
-   <span data-ttu-id="c69ac-121">En desuso `CorBindTo*` funciones (consulte [funciones de hospedaje de CLR en desuso](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) en la API de hospedaje de .NET Framework 2.0).</span><span class="sxs-lookup"><span data-stu-id="c69ac-121">Deprecated `CorBindTo*` functions (see [Deprecated CLR Hosting Functions](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) in the .NET Framework 2.0 hosting API).</span></span>  
  
 <span data-ttu-id="c69ac-122">Un host puede llamar a una de las regiones `CorBindTo*` funciones, como la [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md) función, para crear instancias de una versión específica de CLR.</span><span class="sxs-lookup"><span data-stu-id="c69ac-122">A host may call one of the deprecated `CorBindTo*` functions, such as the [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md) function, to instantiate a specific version of the CLR.</span></span> <span data-ttu-id="c69ac-123">El host, a continuación, puede llamar a la [ICLRMetaHost:: GetRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md) método y especifique el mismo número de versión para obtener un [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="c69ac-123">The host could then call the [ICLRMetaHost::GetRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md) method and specify the same version number to obtain a [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="c69ac-124">Si el host, a continuación, llama al método el `IsLoaded` método en el valor devuelto [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaz, `pbLoaded` devuelve `true`; en caso contrario, devuelve `false`.</span><span class="sxs-lookup"><span data-stu-id="c69ac-124">If the host then calls the `IsLoaded` method on the returned [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface, `pbLoaded` returns `true`; otherwise, it returns `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c69ac-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c69ac-125">Requirements</span></span>  
 <span data-ttu-id="c69ac-126">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c69ac-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c69ac-127">**Encabezado:** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="c69ac-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c69ac-128">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c69ac-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c69ac-129">**Versiones de .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c69ac-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c69ac-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="c69ac-130">See Also</span></span>  
 [<span data-ttu-id="c69ac-131">ICLRRuntimeInfo (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c69ac-131">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="c69ac-132">Interfaces de hospedaje</span><span class="sxs-lookup"><span data-stu-id="c69ac-132">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="c69ac-133">Hospedar aplicaciones de WPF</span><span class="sxs-lookup"><span data-stu-id="c69ac-133">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)