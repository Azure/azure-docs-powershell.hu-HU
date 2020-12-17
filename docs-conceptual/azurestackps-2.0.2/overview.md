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
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="dd98e-103">Azure Stack Hub 2.0.2-es modul</span><span class="sxs-lookup"><span data-stu-id="dd98e-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="dd98e-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="dd98e-104">Requirements:</span></span>

<span data-ttu-id="dd98e-105">A minimális támogatott Azure Stack Hub-verzió a 2002-es.</span><span class="sxs-lookup"><span data-stu-id="dd98e-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="dd98e-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="dd98e-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="dd98e-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="dd98e-107">Install</span></span>

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


## <a name="release-notes"></a><span data-ttu-id="dd98e-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="dd98e-108">Release Notes</span></span>

* <span data-ttu-id="dd98e-109">Az 2002-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="dd98e-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="dd98e-110">Az Azure Stack Hub 2.0.0 egy kompatibilitástörő változást tartalmazó kiadás.</span><span class="sxs-lookup"><span data-stu-id="dd98e-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="dd98e-111">Ez a modul az AzureRM modul helyett az Az modult használja.</span><span class="sxs-lookup"><span data-stu-id="dd98e-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="dd98e-112">Az [Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba az Azure Stack Hubban](/azure-stack/operator/azure-stack-powershell-install) című szakaszban talál egy áttelepítési útmutatót, valamint megtekintheti a kompatibilitástörő változások listáját.</span><span class="sxs-lookup"><span data-stu-id="dd98e-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>
