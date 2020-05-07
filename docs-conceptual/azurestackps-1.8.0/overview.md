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
# <a name="azure-stack-module-180"></a><span data-ttu-id="81ca6-103">Azure Stack 1.8.0-s modul</span><span class="sxs-lookup"><span data-stu-id="81ca6-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="81ca6-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="81ca6-104">Requirements:</span></span>

<span data-ttu-id="81ca6-105">A minimális támogatott Azure Stack-verzió az 1910-es.</span><span class="sxs-lookup"><span data-stu-id="81ca6-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="81ca6-106">Megjegyzés: Az Azure Stack korábbi verzióiért tekintse meg a következőt: [Az Azure Stack PowerShell telepítése](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="81ca6-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="81ca6-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="81ca6-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="81ca6-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="81ca6-108">Release Notes</span></span>

* <span data-ttu-id="81ca6-109">Az 1910-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="81ca6-109">Supported with 1910 update</span></span>
* <span data-ttu-id="81ca6-110">A változások a következők:</span><span class="sxs-lookup"><span data-stu-id="81ca6-110">Changes include:</span></span>

    - <span data-ttu-id="81ca6-111">**Új DRP adminisztrációs modul**: Az üzembehelyezési erőforrás-szolgáltató (Deployment Resource Provider, DRP) lehetővé teszi az erőforrás-szolgáltatók az Azure Stack Hubban való vezényelt üzembe helyezését.</span><span class="sxs-lookup"><span data-stu-id="81ca6-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="81ca6-112">Ezek a parancsok az Azure Resource Manager rétegén keresztül kezelik a DRP-t.</span><span class="sxs-lookup"><span data-stu-id="81ca6-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="81ca6-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="81ca6-113">**BRP**:</span></span>
        - <span data-ttu-id="81ca6-114">Az egyetlen szerepkört alkalmazó visszaállítás támogatása az Azure Stack-infrastruktúra biztonsági mentése kapcsán.</span><span class="sxs-lookup"><span data-stu-id="81ca6-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="81ca6-115">`RoleName` paraméter hozzáadva az R`estore-AzsBackup` parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="81ca6-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="81ca6-116">**FRP**: A **Drive** és a **Volume** erőforrások kompatibilitástörő változásai a következő API-verzió kapcsán: 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="81ca6-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="81ca6-117">A funkciókat az Azure Stack Hub 1910-es és újabb verziói támogatják:</span><span class="sxs-lookup"><span data-stu-id="81ca6-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="81ca6-118">Az ID, a `Name`, a `HealthStatus` és az `OperationalStatus` értéke módosult.</span><span class="sxs-lookup"><span data-stu-id="81ca6-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="81ca6-119">Új támogatott tulajdonságok a **Drive** erőforrásokhoz: `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` és `StoragePool`.</span><span class="sxs-lookup"><span data-stu-id="81ca6-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="81ca6-120">A **Drive** erőforrások `CanPool` és `CannotPoolReason` tulajdonságai elavultak; használja helyettük az `OperationalStatus` tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="81ca6-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
