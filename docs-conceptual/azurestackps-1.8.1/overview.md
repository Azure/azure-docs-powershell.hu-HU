---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: ef034424c72d88b3ceb28956da9ca56e4a7f3941
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/15/2020
ms.locfileid: "79402714"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="3573b-103">Azure Stack 1.8.1-es modul</span><span class="sxs-lookup"><span data-stu-id="3573b-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="3573b-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="3573b-104">Requirements:</span></span>

<span data-ttu-id="3573b-105">A minimális támogatott Azure Stack-verzió az 1910-es.</span><span class="sxs-lookup"><span data-stu-id="3573b-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="3573b-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="3573b-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="3573b-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="3573b-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="3573b-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="3573b-108">Release Notes</span></span>

* <span data-ttu-id="3573b-109">Az 1910-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="3573b-109">Supported with 1910 update</span></span>