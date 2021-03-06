---
title: FUSION_INSTALL_REFERENCE (Estructura)
ms.date: 03/30/2017
api_name:
- FUSION_INSTALL_REFERENCE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- FUSION_INSTALL_REFERENCE
helpviewer_keywords:
- FUSION_INSTALL_REFERENCE structure [.NET Framework fusion]
ms.assetid: ae181ec8-36bf-4ed1-9a02-ca27d417c80b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 34349466594381441c11f947d682b018f95461e9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491615"
---
# <a name="fusioninstallreference-structure"></a>FUSION_INSTALL_REFERENCE (Estructura)
Representa una referencia a la que hace que una aplicación a un ensamblado que ha instalado la aplicación en la caché global de ensamblados.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
typedef struct _FUSION_INSTALL_REFERENCE_ {  
    DWORD    cbSize,  
    DWORD    dwFlags,  
    GUID     guidScheme,  
    LPCWSTR  szIdentifier,  
    LPCWSTR  szNonCanonicalData  
} FUSION_INSTALL_REFERENCE, *LPFUSION_INSTALL_REFERENCE;  
```  
  
## <a name="members"></a>Miembros  
  
|Miembro|Descripción|  
|------------|-----------------|  
|`cbSize`|El tamaño de la estructura en bytes.|  
|`dwFlags`|Reservado para extensibilidad futura. Este valor debe ser 0 (cero).|  
|`guidScheme`|La entidad que agrega la referencia. Este campo puede tener uno de los valores siguientes:<br /><br /> -FUSION_REFCOUNT_MSI_GUID: El ensamblado se hace referencia a una aplicación que se instaló mediante el instalador de Microsoft Windows. El `szIdentifier` campo se establece en `MSI`y el `szNonCanonicalData` campo se establece en `Windows Installer`. Este esquema se utiliza para los ensamblados en paralelo de Windows.<br />-   FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID: El ensamblado se hace referencia a una aplicación que aparece en el **agregar o quitar programas** interfaz. El `szIdentifier` campo proporciona el token que registra la aplicación con el **agregar o quitar programas** interfaz.<br />-FUSION_REFCOUNT_FILEPATH_GUID: Una aplicación que se representa mediante un archivo en el sistema de archivos al que hace referencia el ensamblado. El `szIdentifier` campo proporciona la ruta de acceso a este archivo.<br />-   FUSION_REFCOUNT_OPAQUE_STRING_GUID: Se hace referencia al ensamblado por una aplicación que se representa sólo mediante una cadena opaca. El `szIdentifier` campo proporciona esta cadena opaca. La caché global de ensamblados no comprueba la existencia de referencias opacas cuando se quita este valor.<br />-FUSION_REFCOUNT_OSINSTALL_GUID: Este valor está reservado.|  
|`szIdentifier`|Una cadena única que identifica la aplicación que instala al ensamblado en la caché global de ensamblados. Su valor depende del valor de la `guidScheme` campo.|  
|`szNonCanonicalData`|Una cadena que solo entiende la entidad que agrega la referencia. La caché global de ensamblados almacena esta cadena, pero no lo usa.|  
  
## <a name="requirements"></a>Requisitos  
 **Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Encabezado**: Fusion.h  
  
 **Versiones de .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vea también
- [Estructuras de fusión](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)
- [Caché global de ensamblados](../../../../docs/framework/app-domains/gac.md)
