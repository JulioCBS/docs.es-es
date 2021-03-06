---
title: Cuándo se deben implementar contenedores de Windows para máquinas virtuales de Azure (nube IaaS)
description: Modernizar aplicaciones .NET existentes con contenedores de Windows y la nube de Azure | Cuándo se deben implementar contenedores de Windows para máquinas virtuales de Azure (nube IaaS)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 51217e2c94fd9727c8f7907e791cdebaec98f14f
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2018
ms.locfileid: "53152154"
---
# <a name="when-to-deploy-windows-containers-to-azure-vms-iaas-cloud"></a>Cuándo se deben implementar contenedores de Windows para máquinas virtuales de Azure (nube IaaS)

Si su organización usa máquinas virtuales de Azure, incluso si también usa contenedores de Windows, siguen siendo ocuparse de IaaS. Esto significa que tratar con las operaciones de infraestructura, revisiones de sistema operativo de la máquina virtual y la complejidad de la infraestructura para aplicaciones altamente escalables cuando necesite implementar en varias máquinas virtuales en una infraestructura con equilibrio de carga. Los escenarios principales para usar contenedores de Windows en una máquina virtual de Azure son:

-   **Entorno de desarrollo/pruebas**: Una máquina virtual en la nube es ideal para desarrollo y pruebas en la nube. Puede crear rápidamente o detener el entorno según sus necesidades.

-   **Necesidades de escalabilidad pequeña y mediana**: En escenarios donde podría necesitar un par de máquinas virtuales para su entorno de producción, administra un pequeño número de máquinas virtuales podría ser asequible hasta que se puede mover a los entornos de PaaS más avanzados, como los orquestadores.

-   **Entorno de producción con herramientas de implementación existentes**: Puede mover desde un entorno local en el que han invertido en herramientas para realizar implementaciones complejas en las máquinas virtuales o servidores sin sistema operativo (por ejemplo, Puppet o herramientas similares). Para mover a la nube con unos cambios mínimos en los procedimientos de implementación del entorno de producción, aún puede usar estas herramientas para implementar en máquinas virtuales de Azure. Sin embargo, deseará usar contenedores de Windows como la unidad de implementación para mejorar la experiencia de implementación.

>[!div class="step-by-step"]
>[Anterior](when-to-deploy-windows-containers-in-your-on-premises-iaas-vm-infrastructure.md)
>[Siguiente](when-to-deploy-windows-containers-to-azure-container-instances-ACI.md)