---
title: Método IXCLRDataMethodDefinition::EnumInstance
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::EnumInstance Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::EnumInstance Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 0fbb246f8c4bf791dd705aedf8eab6ef8bfeae56
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54680275"
---
# <a name="ixclrdatamethoddefinitionenuminstance-method"></a>Método IXCLRDataMethodDefinition::EnumInstance

Enumera las instancias de esta definición de método.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Sintaxis

```
HRESULT EnumInstance(
    [in, out] CLRDATA_ENUM         *handle,
    [out] IXCLRDataMethodInstance **instance
);
```

### <a name="parameters"></a>Parámetros

`handle` [in, out] Un identificador para enumerar las instancias.

`instance` [out] La instancia enumerada.

## <a name="remarks"></a>Comentarios

El método proporcionado forma parte de la `IXCLRDataMethodDefinition` interfaz y corresponde a la cuarta ranura de la tabla de métodos virtuales.

## <a name="requirements"></a>Requisitos

**Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).  
**Encabezado**: Ninguna  
**Biblioteca:** Ninguna  
**Versiones de .NET Framework:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Vea también

- [Enumeración CLRDataSourceType](../../../../docs/framework/unmanaged-api/debugging/clrdatasourcetype-enumeration.md)
- [Depuración](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Interfaz IXCLRDataMethodDefinition](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-interface.md)
- [Interfaz IXCLRDataMethodInstance](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-interface.md)
