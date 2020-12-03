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
ms.openlocfilehash: 166c5339c95507b8a9ef1a32d46f589b8d792794
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427955"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="a233b-103">Azure Stack Hub 2.0.0-s modul</span><span class="sxs-lookup"><span data-stu-id="a233b-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a233b-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="a233b-104">Requirements:</span></span>

<span data-ttu-id="a233b-105">A minimális támogatott Azure Stack Hub-verzió a 2002-es.</span><span class="sxs-lookup"><span data-stu-id="a233b-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="a233b-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="a233b-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="a233b-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="a233b-107">Install</span></span>

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


## <a name="release-notes"></a><span data-ttu-id="a233b-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="a233b-108">Release Notes</span></span>

* <span data-ttu-id="a233b-109">Az 2002-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="a233b-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="a233b-110">Az Azure Stack Hub 2.0.0 egy kompatibilitástörő változást tartalmazó kiadás.</span><span class="sxs-lookup"><span data-stu-id="a233b-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="a233b-111">Ez a modul az AzureRM modul helyett az Az modult használja.</span><span class="sxs-lookup"><span data-stu-id="a233b-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="a233b-112">Az [Áttelepítés az AzureRM modulból az Azure PowerShell Az modulba az Azure Stack Hubban](/azure-stack/operator/azure-stack-powershell-install) című szakaszban talál egy áttelepítési útmutatót, valamint megtekintheti a kompatibilitástörő változások listáját.</span><span class="sxs-lookup"><span data-stu-id="a233b-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>