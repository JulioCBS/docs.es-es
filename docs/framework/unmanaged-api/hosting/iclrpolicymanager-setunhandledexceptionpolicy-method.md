---
title: "ICLRPolicyManager::SetUnhandledExceptionPolicy (Método)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRPolicyManager.SetUnhandledExceptionPolicy
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRPolicyManager::SetUnhandledExceptionPolicy
helpviewer_keywords:
- ICLRPolicyManager::SetUnhandledExceptionPolicy method [.NET Framework hosting]
- SetUnhandledExceptionPolicy method [.NET Framework hosting]
ms.assetid: 5268480e-280a-4931-b7a3-dc3ffdf7f78f
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 59ff5cfd93d8077388694ee2e155133a88319c47
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/21/2017
---
# <a name="iclrpolicymanagersetunhandledexceptionpolicy-method"></a><span data-ttu-id="c840e-102">ICLRPolicyManager::SetUnhandledExceptionPolicy (Método)</span><span class="sxs-lookup"><span data-stu-id="c840e-102">ICLRPolicyManager::SetUnhandledExceptionPolicy Method</span></span>
<span data-ttu-id="c840e-103">Especifica el comportamiento de common language runtime (CLR) cuando se produce una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="c840e-103">Specifies the behavior of the common language runtime (CLR) when an unhandled exception occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c840e-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c840e-104">Syntax</span></span>  
  
```  
HRESULT SetUnhandledExceptionPolicy (  
    [in] EClrUnhandledExceptionPolicy policy  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c840e-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c840e-105">Parameters</span></span>  
 `policy`  
 <span data-ttu-id="c840e-106">[in] Uno de los [EClrUnhandledException](../../../../docs/framework/unmanaged-api/hosting/eclrunhandledexception-enumeration.md) valores, que indica si se establece el comportamiento de CLR o el host.</span><span class="sxs-lookup"><span data-stu-id="c840e-106">[in] One of the [EClrUnhandledException](../../../../docs/framework/unmanaged-api/hosting/eclrunhandledexception-enumeration.md) values, indicating whether the behavior is set by the CLR or the host.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c840e-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c840e-107">Return Value</span></span>  
  
|<span data-ttu-id="c840e-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c840e-108">HRESULT</span></span>|<span data-ttu-id="c840e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c840e-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c840e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c840e-110">S_OK</span></span>|<span data-ttu-id="c840e-111">`SetUnhandledExceptionPolicy`se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="c840e-111">`SetUnhandledExceptionPolicy` returned successfully.</span></span>|  
|<span data-ttu-id="c840e-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c840e-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c840e-113">El CLR no se han cargado en un proceso o el CLR está en un estado en el que no se puede ejecutar código administrado o procesar la llamada correctamente.</span><span class="sxs-lookup"><span data-stu-id="c840e-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c840e-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c840e-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c840e-115">La llamada agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c840e-115">The call timed out.</span></span>|  
|<span data-ttu-id="c840e-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c840e-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c840e-117">El llamador no posee el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="c840e-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c840e-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c840e-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c840e-119">Se canceló un evento mientras un subproceso bloqueado o fibra esperó en él.</span><span class="sxs-lookup"><span data-stu-id="c840e-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c840e-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c840e-120">E_FAIL</span></span>|<span data-ttu-id="c840e-121">Se ha producido un error catastrófico desconocido.</span><span class="sxs-lookup"><span data-stu-id="c840e-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c840e-122">Cuando un método devuelve E_FAIL, CLR ya no es utilizable dentro del proceso.</span><span class="sxs-lookup"><span data-stu-id="c840e-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c840e-123">Las llamadas posteriores a métodos de hospedaje devuelven HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c840e-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c840e-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c840e-124">Remarks</span></span>  
 <span data-ttu-id="c840e-125">De forma predeterminada, CLR es el último controlador de todas las excepciones no controladas y su comportamiento predeterminado es anular el proceso.</span><span class="sxs-lookup"><span data-stu-id="c840e-125">By default, the CLR is the final handler for all unhandled exceptions, and its default behavior is to tear down the process.</span></span> <span data-ttu-id="c840e-126">El host puede cambiar este comportamiento estableciendo el `policy` valor en eHostDeterminedPolicy.</span><span class="sxs-lookup"><span data-stu-id="c840e-126">The host can change this behavior by setting the `policy` value to eHostDeterminedPolicy.</span></span> <span data-ttu-id="c840e-127">Este valor permite al host implementar su propio comportamiento predeterminado, al igual que con las versiones anteriores de CLR.</span><span class="sxs-lookup"><span data-stu-id="c840e-127">This value allows the host to implement its own default behavior, as with earlier versions of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c840e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c840e-128">Requirements</span></span>  
 <span data-ttu-id="c840e-129">**Plataformas:** vea [requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c840e-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c840e-130">**Encabezado:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c840e-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c840e-131">**Biblioteca:** incluye como recurso en MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c840e-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c840e-132">**Versiones de .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c840e-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c840e-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c840e-133">See Also</span></span>  
 [<span data-ttu-id="c840e-134">EClrUnhandledException (enumeración)</span><span class="sxs-lookup"><span data-stu-id="c840e-134">EClrUnhandledException Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrunhandledexception-enumeration.md)  
 [<span data-ttu-id="c840e-135">ICLRControl (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c840e-135">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="c840e-136">ICLRPolicyManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c840e-136">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="c840e-137">IHostPolicyManager (interfaz)</span><span class="sxs-lookup"><span data-stu-id="c840e-137">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)