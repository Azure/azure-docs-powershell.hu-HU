---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264410"
---
# <a name="azure-stack-module-180"></a>Azure Stack 1.8.0-s modul

## <a name="requirements"></a>Követelmények:

A minimális támogatott Azure Stack-verzió az 1910-es.

Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Telepítés

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Kibocsátási megjegyzések

* Az 1910-es frissítésben támogatott
* A változások a következők:

    - **Új DRP adminisztrációs modul**: Az üzembehelyezési erőforrás-szolgáltató (Deployment Resource Provider, DRP) lehetővé teszi az erőforrás-szolgáltatók az Azure Stack Hubban való vezényelt üzembe helyezését. Ezek a parancsok az Azure Resource Manager rétegén keresztül kezelik a DRP-t.

    - **BRP**:
        - Az egyetlen szerepkört alkalmazó visszaállítás támogatása az Azure Stack-infrastruktúra biztonsági mentése kapcsán.
        - `RoleName` paraméter hozzáadva az R`estore-AzsBackup` parancsmaghoz.

    - **FRP**: A **Drive** és a **Volume** erőforrások kompatibilitástörő változásai a következő API-verzió kapcsán: 2019-05-01. A funkciókat az Azure Stack Hub 1910-es és újabb verziói támogatják:
        - Az ID, a `Name`, a `HealthStatus` és az `OperationalStatus` értéke módosult.
        - Új támogatott tulajdonságok a **Drive** erőforrásokhoz: `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` és `StoragePool`.
        - A **Drive** erőforrások `CanPool` és `CannotPoolReason` tulajdonságai elavultak; használja helyettük az `OperationalStatus` tulajdonságot.
