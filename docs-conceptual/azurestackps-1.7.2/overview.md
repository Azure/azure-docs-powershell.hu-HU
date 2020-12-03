---
title: Az Azure Stack Admin PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack Admin PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427377"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="d1e77-103">Azure Stack 1.7.2-es modul</span><span class="sxs-lookup"><span data-stu-id="d1e77-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e77-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="d1e77-104">Requirements:</span></span>

<span data-ttu-id="d1e77-105">A minimális támogatott Azure Stack-verzió a 1904-es.</span><span class="sxs-lookup"><span data-stu-id="d1e77-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="d1e77-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="d1e77-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="d1e77-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="d1e77-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="d1e77-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="d1e77-108">Release Notes</span></span>

* <span data-ttu-id="d1e77-109">Az 1904-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="d1e77-109">Supported with 1904 update</span></span>
* <span data-ttu-id="d1e77-110">Ez egy kompatibilitástörő változást tartalmazó kiadás.</span><span class="sxs-lookup"><span data-stu-id="d1e77-110">This a breaking change release.</span></span> <span data-ttu-id="d1e77-111">A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="d1e77-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="d1e77-112">Kompatibilitástörő változás: Tanúsítványalapú titkosítási mód biztonsági mentésének módosításai.</span><span class="sxs-lookup"><span data-stu-id="d1e77-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="d1e77-113">A tartalomkulcsok támogatása elavult.</span><span class="sxs-lookup"><span data-stu-id="d1e77-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="d1e77-114">A kompatibilitástörő változásokkal kapcsolatos részletekért tekintse meg a következőt: https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="d1e77-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="d1e77-115">Azs.Storage.Admin modul</span><span class="sxs-lookup"><span data-stu-id="d1e77-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="d1e77-116">Javított hiba – Az Új tárterületkvóta megadott értékek hiányában az alapértelmezett értékeket használja.</span><span class="sxs-lookup"><span data-stu-id="d1e77-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>