---
title: Az Azure Stack Hub Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Hub Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: ec4591e4f44fa56b7482d2dec3f525cb02dbd94b
ms.sourcegitcommit: a24069b411d3a6011067770430b6dcdd4b2c2159
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/16/2020
ms.locfileid: "97532259"
---
# <a name="azure-stack-hub-module-202"></a>Azure Stack Hub 2.0.2-es modul

## <a name="requirements"></a>Követelmények:

A minimális támogatott Azure Stack Hub-verzió a 2002-es.

Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>Telepítés

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease -SkipPublisherCheck

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a>Kibocsátási megjegyzések

* Az 2002-es frissítésben támogatott  

  Az Azure Stack Hub 2.0.0 egy kompatibilitástörő változást tartalmazó kiadás. Ez a modul az AzureRM modul helyett az Az modult használja. Az [Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba az Azure Stack Hubban](/azure-stack/operator/azure-stack-powershell-install) című szakaszban talál egy áttelepítési útmutatót, valamint megtekintheti a kompatibilitástörő változások listáját.
