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
ms.openlocfilehash: 3add10651334a9c8a1e4ebfd5c8b9cfbf0cc7981
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218017"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="a3d80-103">Azure Stack modul 1.3.0</span><span class="sxs-lookup"><span data-stu-id="a3d80-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d80-104">Követelmények:</span><span class="sxs-lookup"><span data-stu-id="a3d80-104">Requirements:</span></span>
<span data-ttu-id="a3d80-105">A minimális támogatott Azure Stack-verzió a 1804-es.</span><span class="sxs-lookup"><span data-stu-id="a3d80-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="a3d80-106">Megjegyzés: Ha korábbi verziót használ, telepítse az 1.2.11-es verziót</span><span class="sxs-lookup"><span data-stu-id="a3d80-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="a3d80-107">Ismert problémák:</span><span class="sxs-lookup"><span data-stu-id="a3d80-107">Known issues:</span></span>

- <span data-ttu-id="a3d80-108">A Riasztás bezárása művelethez az Azure Stack 1803-as verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="a3d80-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="a3d80-109">Bizonyos Storage-parancsmagokhoz az Azure Stack 1804-es verziója szükséges</span><span class="sxs-lookup"><span data-stu-id="a3d80-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="a3d80-110">A New-AzsOffer nem teszi lehetővé nyilvános állapotú ajánlatok létrehozását.</span><span class="sxs-lookup"><span data-stu-id="a3d80-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="a3d80-111">Utána meg kell hívni a Set-AzsOffer parancsmagot az állapot módosítására.</span><span class="sxs-lookup"><span data-stu-id="a3d80-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="a3d80-112">Az IP-készleteket nem lehet eltávolítani újratelepítés nélkül</span><span class="sxs-lookup"><span data-stu-id="a3d80-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="a3d80-113">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="a3d80-113">Breaking Changes</span></span>
<span data-ttu-id="a3d80-114">A 1.2.11-es verzióból migrált összes kompatibilitástörő változást itt találja: https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="a3d80-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="a3d80-115">Telepítés</span><span class="sxs-lookup"><span data-stu-id="a3d80-115">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="a3d80-116">Tartalom:</span><span class="sxs-lookup"><span data-stu-id="a3d80-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="a3d80-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="a3d80-117">Azure Bridge</span></span>
<span data-ttu-id="a3d80-118">Az Azure Stack AzureBridge felügyeleti moduljának előzetes kiadása, amelynek segítségével rendszerképeket tehet közzé az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="a3d80-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="a3d80-119">Backup</span><span class="sxs-lookup"><span data-stu-id="a3d80-119">Backup</span></span>
<span data-ttu-id="a3d80-120">A Backup felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="a3d80-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="a3d80-121">Konfigurálhatja a biztonsági másolatok tárolási helyét</span><span class="sxs-lookup"><span data-stu-id="a3d80-121">Configure where backups are stored</span></span>
- <span data-ttu-id="a3d80-122">Biztonsági mentéseket hajthat végre</span><span class="sxs-lookup"><span data-stu-id="a3d80-122">Perform backups</span></span>
- <span data-ttu-id="a3d80-123">Listázhatja és visszaállíthatja az elkészült biztonsági másolatokat</span><span class="sxs-lookup"><span data-stu-id="a3d80-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="a3d80-124">Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d80-124">Commerce</span></span>
<span data-ttu-id="a3d80-125">Az Azure Stack Commerce felügyeleti modul előzetes kiadása, amely lehetővé teszi az összesített adathasználat megtekintését a teljes Azure Stack rendszerben.</span><span class="sxs-lookup"><span data-stu-id="a3d80-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="a3d80-126">Compute</span><span class="sxs-lookup"><span data-stu-id="a3d80-126">Compute</span></span>
<span data-ttu-id="a3d80-127">Az Azure Stack Compute felügyeleti modul előzetes kiadása, amely a számítási kvóták, platform-rendszerképek és virtuálisgép-bővítmények felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="a3d80-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="a3d80-128">Fabric</span><span class="sxs-lookup"><span data-stu-id="a3d80-128">Fabric</span></span>
<span data-ttu-id="a3d80-129">Az Azure Stack Fabric felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti és felügyelheti az infrastruktúra-összetevőket:</span><span class="sxs-lookup"><span data-stu-id="a3d80-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="a3d80-130">Skálázásiegység-csomópontok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="a3d80-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="a3d80-131">Skálázásiegység-csomópontok kiürítése és folytatása az FRU-val kapcsolatos tevékenységekhez</span><span class="sxs-lookup"><span data-stu-id="a3d80-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="a3d80-132">Skálázásiegység-csomópontok javítása</span><span class="sxs-lookup"><span data-stu-id="a3d80-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="a3d80-133">Infrastruktúra-szerepkör újraindítása</span><span class="sxs-lookup"><span data-stu-id="a3d80-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="a3d80-134">Infrastruktúra-szerepkörpéldányok leállítása, indítása és lekapcsolása</span><span class="sxs-lookup"><span data-stu-id="a3d80-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="a3d80-135">Új IP-készletek létrehozása</span><span class="sxs-lookup"><span data-stu-id="a3d80-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="a3d80-136">Katalógus</span><span class="sxs-lookup"><span data-stu-id="a3d80-136">Gallery</span></span>
<span data-ttu-id="a3d80-137">Az Azure Stack Gallery felügyeleti modul előzetes kiadása, amely a katalóguselemek az Azure Stack-piactéren való felügyeletéhez szükséges funkciókat biztosít.</span><span class="sxs-lookup"><span data-stu-id="a3d80-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="a3d80-138">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="a3d80-138">Infrastructure Insights</span></span>
<span data-ttu-id="a3d80-139">Az Infrastructure Insights felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="a3d80-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="a3d80-140">Megtekintheti az Azure Stack bélyegző erőforrások állapotát</span><span class="sxs-lookup"><span data-stu-id="a3d80-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="a3d80-141">Megtekintheti és kezelheti a riasztásokat</span><span class="sxs-lookup"><span data-stu-id="a3d80-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="a3d80-142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3d80-142">KeyVault</span></span>
<span data-ttu-id="a3d80-143">Az Azure Stack KeyVault felügyeleti modul előzetes kiadása, amelynek segítségével a rendszergazda megtekintheti a KeyVault-kvótákat.</span><span class="sxs-lookup"><span data-stu-id="a3d80-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="a3d80-144">Network (Hálózat)</span><span class="sxs-lookup"><span data-stu-id="a3d80-144">Network</span></span>
<span data-ttu-id="a3d80-145">A Network felügyeleti modul előzetes kiadása, amely:</span><span class="sxs-lookup"><span data-stu-id="a3d80-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="a3d80-146">Lehetővé teszi a hálózati kvóták felügyeletét</span><span class="sxs-lookup"><span data-stu-id="a3d80-146">Management of network quotas</span></span>
- <span data-ttu-id="a3d80-147">Lehetővé teszi a hálózati erőforrások (például nyilvános IP-címek, virtuális hálózatok és terheléselosztók) megtekintését</span><span class="sxs-lookup"><span data-stu-id="a3d80-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="a3d80-148">Egy parancsmagot biztosít a felügyelet áttekintő megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="a3d80-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="a3d80-149">Storage</span><span class="sxs-lookup"><span data-stu-id="a3d80-149">Storage</span></span>
<span data-ttu-id="a3d80-150">Az Azure Stack Storage felügyeleti modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="a3d80-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="a3d80-151">Ebben a kiadásban a következő funkcionalitást biztosítjuk:</span><span class="sxs-lookup"><span data-stu-id="a3d80-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="a3d80-152">Tárhelykvóták kezelése</span><span class="sxs-lookup"><span data-stu-id="a3d80-152">Manage storage quotas</span></span>
- <span data-ttu-id="a3d80-153">Törölt tárolási erőforrások szemétgyűjtése</span><span class="sxs-lookup"><span data-stu-id="a3d80-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="a3d80-154">Törölt tárfiókok visszaállítása</span><span class="sxs-lookup"><span data-stu-id="a3d80-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="a3d80-155">Tárolók migrálása megosztások közt</span><span class="sxs-lookup"><span data-stu-id="a3d80-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="a3d80-156">Az egyéni tároló-összetevőkkel kapcsolatos összetevők megjelenítése</span><span class="sxs-lookup"><span data-stu-id="a3d80-156">View information about the individual storage components</span></span>
- <span data-ttu-id="a3d80-157">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="a3d80-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="a3d80-158">Subscription Admin</span><span class="sxs-lookup"><span data-stu-id="a3d80-158">Subscription Admin</span></span>
<span data-ttu-id="a3d80-159">Az Azure Stack Subscription adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="a3d80-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="a3d80-160">A modul a következő funkciókat biztosítja a rendszergazdák számára:</span><span class="sxs-lookup"><span data-stu-id="a3d80-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="a3d80-161">Csomagok és ajánlatok kezelése</span><span class="sxs-lookup"><span data-stu-id="a3d80-161">Manage plans and offers</span></span>
- <span data-ttu-id="a3d80-162">Használati és teljesítményadatok megtekintése</span><span class="sxs-lookup"><span data-stu-id="a3d80-162">View usage and performance information</span></span>
- <span data-ttu-id="a3d80-163">Az RBAC kezelése</span><span class="sxs-lookup"><span data-stu-id="a3d80-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="a3d80-164">Előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3d80-164">Subscription</span></span>
<span data-ttu-id="a3d80-165">Az Azure Stack Subscription modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="a3d80-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="a3d80-166">A modul a következő funkciókat biztosítja a felhasználók számára:</span><span class="sxs-lookup"><span data-stu-id="a3d80-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="a3d80-167">Előfizetések létrehozása, törlése és frissítése</span><span class="sxs-lookup"><span data-stu-id="a3d80-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="a3d80-168">Frissítés</span><span class="sxs-lookup"><span data-stu-id="a3d80-168">Update</span></span>
<span data-ttu-id="a3d80-169">Az Azure Stack Update adminisztrációs modul előzetes kiadása.</span><span class="sxs-lookup"><span data-stu-id="a3d80-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="a3d80-170">A modul használatával a rendszergazda:</span><span class="sxs-lookup"><span data-stu-id="a3d80-170">In this module administrators can:</span></span>
- <span data-ttu-id="a3d80-171">Listázhatja és telepítheti az elérhető frissítéseket</span><span class="sxs-lookup"><span data-stu-id="a3d80-171">List and install available updates</span></span>
- <span data-ttu-id="a3d80-172">Folytathatja a megszakított frissítéseket</span><span class="sxs-lookup"><span data-stu-id="a3d80-172">Resume interrupted updates</span></span>
- <span data-ttu-id="a3d80-173">Megtekintheti a telepített frissítéseket</span><span class="sxs-lookup"><span data-stu-id="a3d80-173">View installed updates</span></span>
