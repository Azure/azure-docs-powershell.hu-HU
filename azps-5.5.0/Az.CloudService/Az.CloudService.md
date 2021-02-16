---
Module Name: Az.CloudService
Module Guid: a41eb61d-c5a1-4e9b-81a7-b8905fff7f2c
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
ms.openlocfilehash: c9ab8aaefc7d97c7d1082b76b1dcef1546fe96d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145090"
---
# <span data-ttu-id="69f01-101">Az.CloudService modul</span><span class="sxs-lookup"><span data-stu-id="69f01-101">Az.CloudService Module</span></span>
## <span data-ttu-id="69f01-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="69f01-102">Description</span></span>
<span data-ttu-id="69f01-103">Microsoft Azure PowerShell: CloudService parancsmagok</span><span class="sxs-lookup"><span data-stu-id="69f01-103">Microsoft Azure PowerShell: CloudService cmdlets</span></span>

## <span data-ttu-id="69f01-104">Az.CloudService parancsmagok</span><span class="sxs-lookup"><span data-stu-id="69f01-104">Az.CloudService Cmdlets</span></span>
### [<span data-ttu-id="69f01-105">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-105">Get-AzCloudService</span></span>](Get-AzCloudService.md)
<span data-ttu-id="69f01-106">Adatok megjelenítése a felhőszolgáltatásról.</span><span class="sxs-lookup"><span data-stu-id="69f01-106">Display information about a cloud service.</span></span>

### [<span data-ttu-id="69f01-107">Get-AzCloudServiceInstanceView</span><span class="sxs-lookup"><span data-stu-id="69f01-107">Get-AzCloudServiceInstanceView</span></span>](Get-AzCloudServiceInstanceView.md)
<span data-ttu-id="69f01-108">Egy felhőszolgáltatás állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="69f01-108">Gets the status of a cloud service.</span></span>

### [<span data-ttu-id="69f01-109">Get-AzCloudServiceNetworkInterfaces</span><span class="sxs-lookup"><span data-stu-id="69f01-109">Get-AzCloudServiceNetworkInterfaces</span></span>](Get-AzCloudServiceNetworkInterfaces.md)
<span data-ttu-id="69f01-110">Szerezze be egy felhőszolgáltatás hálózati felületét.</span><span class="sxs-lookup"><span data-stu-id="69f01-110">Get the network interfaces of a cloud service.</span></span>

### [<span data-ttu-id="69f01-111">Get-AzCloudServicePublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="69f01-111">Get-AzCloudServicePublicIPAddress</span></span>](Get-AzCloudServicePublicIPAddress.md)
<span data-ttu-id="69f01-112">Szerezze be egy felhőszolgáltatás nyilvános IP-címét.</span><span class="sxs-lookup"><span data-stu-id="69f01-112">Get the public IP address of a cloud service.</span></span>

### [<span data-ttu-id="69f01-113">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="69f01-113">Get-AzCloudServiceRoleInstance</span></span>](Get-AzCloudServiceRoleInstance.md)
<span data-ttu-id="69f01-114">Szerepkörpéldányt kap egy felhőszolgáltatásból.</span><span class="sxs-lookup"><span data-stu-id="69f01-114">Gets a role instance from a cloud service.</span></span>

### [<span data-ttu-id="69f01-115">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="69f01-115">Get-AzCloudServiceRoleInstanceRemoteDesktopFile</span></span>](Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md)
<span data-ttu-id="69f01-116">Távoli asztali fájlt kap egy szerepkörpéldányhoz egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="69f01-116">Gets a remote desktop file for a role instance in a cloud service.</span></span>

### [<span data-ttu-id="69f01-117">Get-AzCloudServiceRoleInstanceView</span><span class="sxs-lookup"><span data-stu-id="69f01-117">Get-AzCloudServiceRoleInstanceView</span></span>](Get-AzCloudServiceRoleInstanceView.md)
<span data-ttu-id="69f01-118">A felhőszolgáltatás szerepkörpéldányának futásidővel kapcsolatos állapotáról olvassa be az adatokat.</span><span class="sxs-lookup"><span data-stu-id="69f01-118">Retrieves information about the run-time state of a role instance in a cloud service.</span></span>

### [<span data-ttu-id="69f01-119">Invoke-AzCloudServiceRebuild</span><span class="sxs-lookup"><span data-stu-id="69f01-119">Invoke-AzCloudServiceRebuild</span></span>](Invoke-AzCloudServiceRebuild.md)
<span data-ttu-id="69f01-120">A Szerepkörpéldányok újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei esetén, és inicializálja az általuk használt tárterület-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="69f01-120">Rebuild Role Instances reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="69f01-121">Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Szerepkörpéldányok újraimizálása használhatja.</span><span class="sxs-lookup"><span data-stu-id="69f01-121">If you do not want to initialize storage resources, you can use Reimage Role Instances.</span></span>

### [<span data-ttu-id="69f01-122">Invoke-AzCloudServiceReimage</span><span class="sxs-lookup"><span data-stu-id="69f01-122">Invoke-AzCloudServiceReimage</span></span>](Invoke-AzCloudServiceReimage.md)
<span data-ttu-id="69f01-123">Az aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei esetén.</span><span class="sxs-lookup"><span data-stu-id="69f01-123">Reimage asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="69f01-124">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="69f01-124">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>](Invoke-AzCloudServiceRoleInstanceRebuild.md)
<span data-ttu-id="69f01-125">A szerepkörpéldány újraépítése aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán, és inicializálja az általuk használt tárterület-erőforrásokat.</span><span class="sxs-lookup"><span data-stu-id="69f01-125">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="69f01-126">Ha nem szeretné inicializálni a tárterület-erőforrásokat, használhatja a Szerepkör-példány-reimage szerepkörpéldányt.</span><span class="sxs-lookup"><span data-stu-id="69f01-126">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

### [<span data-ttu-id="69f01-127">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="69f01-127">Invoke-AzCloudServiceRoleInstanceReimage</span></span>](Invoke-AzCloudServiceRoleInstanceReimage.md)
<span data-ttu-id="69f01-128">A Reimage szerepkörpéldány aszinkron művelet újratelepíti az operációs rendszert a webes szerepkörök vagy a dolgozók szerepkörei példányán.</span><span class="sxs-lookup"><span data-stu-id="69f01-128">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

### [<span data-ttu-id="69f01-129">New-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-129">New-AzCloudService</span></span>](New-AzCloudService.md)
<span data-ttu-id="69f01-130">Felhőszolgáltatás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="69f01-130">Create or update a cloud service.</span></span>
<span data-ttu-id="69f01-131">Felhívjuk a figyelmét arra, hogy egyes tulajdonságok csak a felhőszolgáltatás létrehozásakor beállíthatók.</span><span class="sxs-lookup"><span data-stu-id="69f01-131">Please note some properties can be set only during cloud service creation.</span></span>

### [<span data-ttu-id="69f01-132">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="69f01-132">New-AzCloudServiceDiagnosticsExtension</span></span>](New-AzCloudServiceDiagnosticsExtension.md)
<span data-ttu-id="69f01-133">Memória-objektum létrehozása diagnosztikai bővítményhez</span><span class="sxs-lookup"><span data-stu-id="69f01-133">Create a in-memory object for Diagnostics Extension</span></span>

### [<span data-ttu-id="69f01-134">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="69f01-134">New-AzCloudServiceExtensionObject</span></span>](New-AzCloudServiceExtensionObject.md)
<span data-ttu-id="69f01-135">Memóriában lévő objektum létrehozása bővítményhez</span><span class="sxs-lookup"><span data-stu-id="69f01-135">Create a in-memory object for Extension</span></span>

### [<span data-ttu-id="69f01-136">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="69f01-136">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerConfigurationObject.md)
<span data-ttu-id="69f01-137">Create a in-memory object for LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="69f01-137">Create a in-memory object for LoadBalancerConfiguration</span></span>

### [<span data-ttu-id="69f01-138">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="69f01-138">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>](New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md)
<span data-ttu-id="69f01-139">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="69f01-139">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

### [<span data-ttu-id="69f01-140">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="69f01-140">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>](New-AzCloudServiceRemoteDesktopExtensionObject.md)
<span data-ttu-id="69f01-141">Memóriában lévő objektum létrehozása távoli asztali bővítményhez</span><span class="sxs-lookup"><span data-stu-id="69f01-141">Create a in-memory object for Remote Desktop Extension</span></span>

### [<span data-ttu-id="69f01-142">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="69f01-142">New-AzCloudServiceRoleProfilePropertiesObject</span></span>](New-AzCloudServiceRoleProfilePropertiesObject.md)
<span data-ttu-id="69f01-143">Create a in-memory object for CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="69f01-143">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

### [<span data-ttu-id="69f01-144">New-AzCloudServiceVaultSecretGroupObject</span><span class="sxs-lookup"><span data-stu-id="69f01-144">New-AzCloudServiceVaultSecretGroupObject</span></span>](New-AzCloudServiceVaultSecretGroupObject.md)
<span data-ttu-id="69f01-145">Create a in-memory object for Secret Group</span><span class="sxs-lookup"><span data-stu-id="69f01-145">Create a in-memory object for Secret Group</span></span>

### [<span data-ttu-id="69f01-146">Remove-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-146">Remove-AzCloudService</span></span>](Remove-AzCloudService.md)
<span data-ttu-id="69f01-147">Töröl egy felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="69f01-147">Deletes a cloud service.</span></span>

### [<span data-ttu-id="69f01-148">Remove-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="69f01-148">Remove-AzCloudServiceRoleInstance</span></span>](Remove-AzCloudServiceRoleInstance.md)
<span data-ttu-id="69f01-149">Törli a szerepkörpéldányokat egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="69f01-149">Deletes role instances in a cloud service.</span></span>

### [<span data-ttu-id="69f01-150">Restart-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-150">Restart-AzCloudService</span></span>](Restart-AzCloudService.md)
<span data-ttu-id="69f01-151">Egy vagy több szerepkörpéldány újraindítása egy felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="69f01-151">Restarts one or more role instances in a cloud service.</span></span>

### [<span data-ttu-id="69f01-152">Restart-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="69f01-152">Restart-AzCloudServiceRoleInstance</span></span>](Restart-AzCloudServiceRoleInstance.md)
<span data-ttu-id="69f01-153">A szerepkör-példány újraindítása aszinkron művelet egy szerepkörpéldány újraindítását kéri a felhőszolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="69f01-153">The Reboot Role Instance asynchronous operation requests a reboot of a role instance in the cloud service.</span></span>

### [<span data-ttu-id="69f01-154">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="69f01-154">Set-AzCloudServiceUpdateDomain</span></span>](Set-AzCloudServiceUpdateDomain.md)
<span data-ttu-id="69f01-155">Frissíti a szerepkörpéldányokat a megadott frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="69f01-155">Updates the role instances in the specified update domain.</span></span>

### [<span data-ttu-id="69f01-156">Start-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-156">Start-AzCloudService</span></span>](Start-AzCloudService.md)
<span data-ttu-id="69f01-157">Elindítja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="69f01-157">Starts the cloud service.</span></span>

### [<span data-ttu-id="69f01-158">Stop-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-158">Stop-AzCloudService</span></span>](Stop-AzCloudService.md)
<span data-ttu-id="69f01-159">Kikapcsolja a felhőszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="69f01-159">Power off the cloud service.</span></span>
<span data-ttu-id="69f01-160">Felhívjuk a figyelmét arra, hogy az erőforrások továbbra is csatolva vannak, és az erőforrásokért díjat számítunk fel.</span><span class="sxs-lookup"><span data-stu-id="69f01-160">Note that resources are still attached and you are getting charged for the resources.</span></span>

### [<span data-ttu-id="69f01-161">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-161">Switch-AzCloudService</span></span>](Switch-AzCloudService.md)
<span data-ttu-id="69f01-162">Az IP-pontokat felcseréli két felhőszolgáltatás (kiterjesztett támogatás) terhelésegyenleg-elosztása között.</span><span class="sxs-lookup"><span data-stu-id="69f01-162">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

### [<span data-ttu-id="69f01-163">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="69f01-163">Update-AzCloudService</span></span>](Update-AzCloudService.md)
<span data-ttu-id="69f01-164">Felhőszolgáltatás létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="69f01-164">Create or update a cloud service.</span></span>
<span data-ttu-id="69f01-165">Felhívjuk a figyelmét arra, hogy egyes tulajdonságok csak a felhőszolgáltatás létrehozásakor beállíthatók.</span><span class="sxs-lookup"><span data-stu-id="69f01-165">Please note some properties can be set only during cloud service creation.</span></span>

