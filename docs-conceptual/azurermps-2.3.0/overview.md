---
title: Az Azure Stack PowerShell áttekintése | Microsoft Docs
description: Az Azure Stack PowerShell áttekintése telepítési és konfigurációs utasításokkal.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178459"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="68af8-103">AzureRM 2.3.0-s modul</span><span class="sxs-lookup"><span data-stu-id="68af8-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="68af8-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="68af8-104">Requirements:</span></span>
<span data-ttu-id="68af8-105">A minimális támogatott Azure Stack-verzió az 1808-as.</span><span class="sxs-lookup"><span data-stu-id="68af8-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="68af8-106">Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse</span><span class="sxs-lookup"><span data-stu-id="68af8-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="68af8-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="68af8-107">Install</span></span>
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a><span data-ttu-id="68af8-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="68af8-108">Release Notes</span></span>
* <span data-ttu-id="68af8-109">A 2.3.0-s kiadás tartalmaz egy listát a kompatibilitástörő változásokról.</span><span class="sxs-lookup"><span data-stu-id="68af8-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="68af8-110">Az 1.2.11-es verzióról történő frissítéshez készítettünk egy migrálási útmutatót a következő helyen: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="68af8-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="68af8-111">Ez a kiadás megegyezik a 2018-03-01-hybrid Azure Stack-specifikus API profillal.</span><span class="sxs-lookup"><span data-stu-id="68af8-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="68af8-112">Minden modul függősége nagyobb vagy egyenlő lett az AzureRM.Profile-modulhoz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="68af8-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="68af8-113">A modulok által támogatott API-verziók frissítve lettek.</span><span class="sxs-lookup"><span data-stu-id="68af8-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="68af8-114">Számítás – 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="68af8-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="68af8-115">Hálózat – 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="68af8-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="68af8-116">Tárolás – 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="68af8-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="68af8-117">Erőforrások – 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="68af8-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="68af8-118">Kulcstartó – 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="68af8-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="68af8-119">DNS – 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="68af8-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="68af8-120">A teljes API-verziótérkép az egyes erőforrástípusokhoz megtalálható a következő helyen: https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.</span><span class="sxs-lookup"><span data-stu-id="68af8-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="68af8-121">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="68af8-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="68af8-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="68af8-122">Azure Bridge</span></span>
<span data-ttu-id="68af8-123">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="68af8-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="68af8-124">Backup</span><span class="sxs-lookup"><span data-stu-id="68af8-124">Backup</span></span>
<span data-ttu-id="68af8-125">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="68af8-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="68af8-126">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="68af8-126">Configure where backups are stored</span></span>
- <span data-ttu-id="68af8-127">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="68af8-127">Perform backups</span></span>
- <span data-ttu-id="68af8-128">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="68af8-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="68af8-129">Commerce</span><span class="sxs-lookup"><span data-stu-id="68af8-129">Commerce</span></span>
<span data-ttu-id="68af8-130">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="68af8-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="68af8-131">Compute</span><span class="sxs-lookup"><span data-stu-id="68af8-131">Compute</span></span>
<span data-ttu-id="68af8-132">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platformrendszerképek, felügyelt lemezek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="68af8-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="68af8-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="68af8-133">Fabric</span></span>
<span data-ttu-id="68af8-134">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="68af8-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="68af8-135">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="68af8-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="68af8-136">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="68af8-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="68af8-137">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="68af8-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="68af8-138">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="68af8-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="68af8-139">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="68af8-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="68af8-140">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="68af8-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="68af8-141">Katalógus</span><span class="sxs-lookup"><span data-stu-id="68af8-141">Gallery</span></span>
<span data-ttu-id="68af8-142">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="68af8-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="68af8-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="68af8-143">Infrastructure Insights</span></span>
<span data-ttu-id="68af8-144">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="68af8-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="68af8-145">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="68af8-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="68af8-146">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="68af8-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="68af8-147">KeyVault</span><span class="sxs-lookup"><span data-stu-id="68af8-147">KeyVault</span></span>
<span data-ttu-id="68af8-148">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="68af8-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="68af8-149">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="68af8-149">Network</span></span>
<span data-ttu-id="68af8-150">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="68af8-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="68af8-151">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="68af8-151">Management of network quotas</span></span>
- <span data-ttu-id="68af8-152">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="68af8-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="68af8-153">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="68af8-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="68af8-154">Storage</span><span class="sxs-lookup"><span data-stu-id="68af8-154">Storage</span></span>
<span data-ttu-id="68af8-155">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="68af8-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="68af8-156">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="68af8-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="68af8-157">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="68af8-157">Manage storage quotas</span></span>
- <span data-ttu-id="68af8-158">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="68af8-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="68af8-159">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="68af8-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="68af8-160">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="68af8-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="68af8-161">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="68af8-161">View information about the individual storage components</span></span>
- <span data-ttu-id="68af8-162">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="68af8-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="68af8-163">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="68af8-163">Subscription Admin</span></span>
<span data-ttu-id="68af8-164">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="68af8-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="68af8-165">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="68af8-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="68af8-166">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="68af8-166">Manage plans and offers</span></span>
- <span data-ttu-id="68af8-167">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="68af8-167">View usage and performance information</span></span>
- <span data-ttu-id="68af8-168">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="68af8-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="68af8-169">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="68af8-169">Subscription</span></span>
<span data-ttu-id="68af8-170">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="68af8-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="68af8-171">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="68af8-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="68af8-172">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="68af8-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="68af8-173">Frissítés</span><span class="sxs-lookup"><span data-stu-id="68af8-173">Update</span></span>
<span data-ttu-id="68af8-174">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="68af8-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="68af8-175">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="68af8-175">In this module administrators can:</span></span>
- <span data-ttu-id="68af8-176">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="68af8-176">List and install available updates</span></span>
- <span data-ttu-id="68af8-177">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="68af8-177">Resume interrupted updates</span></span>
- <span data-ttu-id="68af8-178">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="68af8-178">View installed updates</span></span>
