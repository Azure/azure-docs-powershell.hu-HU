---
title: Az Azure Stack Hub Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Hub Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: fd1f2a3778e348ba41b46acb4bdce19e18a7f4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "81524965"
---
# <a name="azure-stack-hub-module-200"></a>Azure Stack Hub 2.0.0-s modul

## <a name="requirements"></a>Követelmények:

A minimális támogatott Azure Stack Hub-verzió a 2002-es.

Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Telepítés

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a>Kibocsátási megjegyzések

* Az 2002-es frissítésben támogatott  

  Az Azure Stack Hub 2.0.0 egy kompatibilitástörő változást tartalmazó kiadás. Ez a modul az AzureRM modul helyett az Az modult használja. Az [Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba az Azure Stack Hubban](https://aka.ms/AA7qsji) című szakaszban talál egy áttelepítési útmutatót, valamint megtekintheti a kompatibilitástörő változások listáját.
