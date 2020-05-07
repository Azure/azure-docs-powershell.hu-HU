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
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053315"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="cc3ec-103">Azure Stack 1.6.0-s modul</span><span class="sxs-lookup"><span data-stu-id="cc3ec-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3ec-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="cc3ec-104">Requirements:</span></span>
<span data-ttu-id="cc3ec-105">A minimális támogatott Azure Stack-verzió az 1811-es.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="cc3ec-106">Megjegyzés: Ha korábbi verziót használ, telepítse az 1.6.0-s verziót</span><span class="sxs-lookup"><span data-stu-id="cc3ec-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="cc3ec-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="cc3ec-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="cc3ec-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="cc3ec-108">Release Notes</span></span>
* <span data-ttu-id="cc3ec-109">Az 1811-es frissítésben támogatott</span><span class="sxs-lookup"><span data-stu-id="cc3ec-109">Supported with 1811 update</span></span>
* <span data-ttu-id="cc3ec-110">Azs.Compute.Admin modul</span><span class="sxs-lookup"><span data-stu-id="cc3ec-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="cc3ec-111">A New-DataDiskObject hiányzó Azs előtagja kijavítva, valamint alias hozzáadva a jövőbeli elavulásra való figyelmeztetéssel.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="cc3ec-112">Azs.Update.Admin modul</span><span class="sxs-lookup"><span data-stu-id="cc3ec-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="cc3ec-113">Figyelmeztetés hozzáadva, amely a Test-AzureStack futtatását javasolja az Install-AzsUpdate előtt</span><span class="sxs-lookup"><span data-stu-id="cc3ec-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="cc3ec-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="cc3ec-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="cc3ec-115">Új parancsmag (A szolgáltatásokat az Azure Stack a 1811-es frissítéstől kezdődően támogatja)</span><span class="sxs-lookup"><span data-stu-id="cc3ec-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="cc3ec-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="cc3ec-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="cc3ec-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="cc3ec-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="cc3ec-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="cc3ec-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="cc3ec-119">Elavulás</span><span class="sxs-lookup"><span data-stu-id="cc3ec-119">Deprecation</span></span>
        * <span data-ttu-id="cc3ec-120">A Get-AzsInfrastructureVolume mostantól a Get-AzsVolume parancsmag aliasa</span><span class="sxs-lookup"><span data-stu-id="cc3ec-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="cc3ec-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="cc3ec-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="cc3ec-122">Új parancsmag: Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="cc3ec-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="cc3ec-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="cc3ec-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="cc3ec-124">Ki lett javítva a nem használt alapértelmezett kvótaértékekkel kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="cc3ec-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="cc3ec-125">Azs.Subscriptions.Admin modul</span><span class="sxs-lookup"><span data-stu-id="cc3ec-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="cc3ec-126">A New-AddonPlanDefinitionObject hiányzó Azs előtagja kijavítva, valamint alias hozzáadva a jövőbeli elavulásra való figyelmeztetéssel.</span><span class="sxs-lookup"><span data-stu-id="cc3ec-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
