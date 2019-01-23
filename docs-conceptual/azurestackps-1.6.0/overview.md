---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240135"
---
# <a name="azure-stack-module-160"></a>Azure Stack 1.6.0-s modul

## <a name="requirements"></a>Követelmények:
A minimális támogatott Azure Stack-verzió az 1811-es.

Megjegyzés: Ha korábbi verziót használ, telepítse az 1.6.0-s verziót

## <a name="install"></a>Telepítés
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Kibocsátási megjegyzések
* Az 1811-es frissítésben támogatott
* Azs.Compute.Admin modul
    * A New-DataDiskObject hiányzó Azs előtagja kijavítva, valamint alias hozzáadva a jövőbeli elavulásra való figyelmeztetéssel.
* Azs.Update.Admin modul
    * Figyelmeztetés hozzáadva, amely a Test-AzureStack futtatását javasolja az Install-AzsUpdate előtt
* Azs.Fabric.Admin
    * Új parancsmag (A szolgáltatásokat az Azure Stack a 1811-es frissítéstől kezdődően támogatja)
        * Get-AzsDrive
        * Get-AzsVolume
        * Get-AzsStorageSubSystem
    * Elavulás
        * A Get-AzsInfrastructureVolume mostantól a Get-AzsVolume parancsmag aliasa
* Azs.InfrastructureInsights.Admin
    *  Új parancsmag: Repair-AzsAlert
* Azs.Storage.Admin
    * Ki lett javítva a nem használt alapértelmezett kvótaértékekkel kapcsolatos hiba
* Azs.Subscriptions.Admin modul
    * A New-AddonPlanDefinitionObject hiányzó Azs előtagja kijavítva, valamint alias hozzáadva a jövőbeli elavulásra való figyelmeztetéssel.
