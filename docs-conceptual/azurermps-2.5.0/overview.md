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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 05/05/2020
ms.locfileid: "67038193"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="011b4-103">AzureRM 2.5.0-s modul</span><span class="sxs-lookup"><span data-stu-id="011b4-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="011b4-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="011b4-104">Requirements:</span></span>
<span data-ttu-id="011b4-105">A minimális támogatott Azure Stack-verzió a 1904-es.</span><span class="sxs-lookup"><span data-stu-id="011b4-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="011b4-106">Megjegyzés: korábbi verzió használata esetén az 1.2.11-es verziót telepítse</span><span class="sxs-lookup"><span data-stu-id="011b4-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="011b4-107">Telepítés</span><span class="sxs-lookup"><span data-stu-id="011b4-107">Install</span></span>
```powershell-interactive
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

## <a name="release-notes"></a><span data-ttu-id="011b4-108">Kibocsátási megjegyzések</span><span class="sxs-lookup"><span data-stu-id="011b4-108">Release Notes</span></span>
* <span data-ttu-id="011b4-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="011b4-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="011b4-110">Új Erőforrások modul a 2018-05-01-es API-verzióhoz a 2019-03-01-es hibrid profillal</span><span class="sxs-lookup"><span data-stu-id="011b4-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="011b4-111">A PolicyDefinition (2016-12-01) és PolicyAssisgment (2017-06-01, előzetes verzió) műveletek továbbra is a régi API-verziókkal futnak</span><span class="sxs-lookup"><span data-stu-id="011b4-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="011b4-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="011b4-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="011b4-113">Új számítási modul a 2017-12-01-es API-verzióhoz.</span><span class="sxs-lookup"><span data-stu-id="011b4-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="011b4-114">Ez a kiadás megegyezik a 2019-03-01-hybrid Azure Stack-specifikus API-profillal</span><span class="sxs-lookup"><span data-stu-id="011b4-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="011b4-115">Minden modul függősége nagyobb vagy egyenlő lett az AzureRM.Profile-modulhoz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="011b4-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="011b4-116">A modulok által támogatott API-verziók frissítve lettek.</span><span class="sxs-lookup"><span data-stu-id="011b4-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="011b4-117">Számítás – 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="011b4-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="011b4-118">Hálózat – 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="011b4-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="011b4-119">Tárolás – 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="011b4-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="011b4-120">Erőforrások – 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="011b4-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="011b4-121">Kulcstartó – 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="011b4-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="011b4-122">DNS – 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="011b4-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="011b4-123">A teljes API-verziótérkép az egyes erőforrástípusokhoz megtalálható a következő helyen: https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.</span><span class="sxs-lookup"><span data-stu-id="011b4-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="011b4-124">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="011b4-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="011b4-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="011b4-125">Azure Bridge</span></span>
<span data-ttu-id="011b4-126">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="011b4-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="011b4-127">Backup</span><span class="sxs-lookup"><span data-stu-id="011b4-127">Backup</span></span>
<span data-ttu-id="011b4-128">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="011b4-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="011b4-129">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="011b4-129">Configure where backups are stored</span></span>
- <span data-ttu-id="011b4-130">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="011b4-130">Perform backups</span></span>
- <span data-ttu-id="011b4-131">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="011b4-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="011b4-132">Commerce</span><span class="sxs-lookup"><span data-stu-id="011b4-132">Commerce</span></span>
<span data-ttu-id="011b4-133">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="011b4-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="011b4-134">Számítás</span><span class="sxs-lookup"><span data-stu-id="011b4-134">Compute</span></span>
<span data-ttu-id="011b4-135">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platformrendszerképek, felügyelt lemezek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="011b4-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="011b4-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="011b4-136">Fabric</span></span>
<span data-ttu-id="011b4-137">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="011b4-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="011b4-138">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="011b4-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="011b4-139">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="011b4-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="011b4-140">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="011b4-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="011b4-141">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="011b4-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="011b4-142">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="011b4-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="011b4-143">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="011b4-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="011b4-144">Katalógus</span><span class="sxs-lookup"><span data-stu-id="011b4-144">Gallery</span></span>
<span data-ttu-id="011b4-145">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="011b4-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="011b4-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="011b4-146">Infrastructure Insights</span></span>
<span data-ttu-id="011b4-147">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="011b4-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="011b4-148">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="011b4-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="011b4-149">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="011b4-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="011b4-150">KeyVault</span><span class="sxs-lookup"><span data-stu-id="011b4-150">KeyVault</span></span>
<span data-ttu-id="011b4-151">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="011b4-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="011b4-152">Hálózat</span><span class="sxs-lookup"><span data-stu-id="011b4-152">Network</span></span>
<span data-ttu-id="011b4-153">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="011b4-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="011b4-154">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="011b4-154">Management of network quotas</span></span>
- <span data-ttu-id="011b4-155">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="011b4-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="011b4-156">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="011b4-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="011b4-157">Tárterület</span><span class="sxs-lookup"><span data-stu-id="011b4-157">Storage</span></span>
<span data-ttu-id="011b4-158">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="011b4-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="011b4-159">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="011b4-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="011b4-160">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="011b4-160">Manage storage quotas</span></span>
- <span data-ttu-id="011b4-161">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="011b4-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="011b4-162">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="011b4-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="011b4-163">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="011b4-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="011b4-164">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="011b4-164">View information about the individual storage components</span></span>
- <span data-ttu-id="011b4-165">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="011b4-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="011b4-166">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="011b4-166">Subscription Admin</span></span>
<span data-ttu-id="011b4-167">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="011b4-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="011b4-168">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="011b4-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="011b4-169">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="011b4-169">Manage plans and offers</span></span>
- <span data-ttu-id="011b4-170">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="011b4-170">View usage and performance information</span></span>
- <span data-ttu-id="011b4-171">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="011b4-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="011b4-172">Előfizetést</span><span class="sxs-lookup"><span data-stu-id="011b4-172">Subscription</span></span>
<span data-ttu-id="011b4-173">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="011b4-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="011b4-174">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="011b4-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="011b4-175">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="011b4-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="011b4-176">Frissítés</span><span class="sxs-lookup"><span data-stu-id="011b4-176">Update</span></span>
<span data-ttu-id="011b4-177">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="011b4-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="011b4-178">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="011b4-178">In this module administrators can:</span></span>
- <span data-ttu-id="011b4-179">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="011b4-179">List and install available updates</span></span>
- <span data-ttu-id="011b4-180">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="011b4-180">Resume interrupted updates</span></span>
- <span data-ttu-id="011b4-181">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="011b4-181">View installed updates</span></span>
