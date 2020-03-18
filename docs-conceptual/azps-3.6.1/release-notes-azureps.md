---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036161"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="46979-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="46979-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="46979-104">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="46979-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-105">Az.Accounts</span></span>
* <span data-ttu-id="46979-106">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="46979-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="46979-107">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="46979-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="46979-108">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="46979-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46979-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-109">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-110">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="46979-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="46979-111">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="46979-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="46979-112">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="46979-113">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="46979-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-115">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="46979-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-116">Az.IotHub</span></span>
* <span data-ttu-id="46979-117">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46979-118">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="46979-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="46979-123">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="46979-124">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="46979-125">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="46979-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="46979-126">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="46979-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="46979-127">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="46979-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="46979-128">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="46979-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="46979-129">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46979-130">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46979-131">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="46979-132">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="46979-133">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="46979-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="46979-134">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="46979-135">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-136">Az.Monitor</span></span>
* <span data-ttu-id="46979-137">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="46979-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-138">Az.Network</span></span>
* <span data-ttu-id="46979-139">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="46979-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="46979-140">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="46979-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="46979-141">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="46979-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="46979-142">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="46979-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-143">Az.Resources</span></span>
* <span data-ttu-id="46979-144">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="46979-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="46979-145">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="46979-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="46979-146">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="46979-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="46979-147">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="46979-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="46979-148">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="46979-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="46979-149">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="46979-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="46979-150">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="46979-151">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="46979-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46979-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46979-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46979-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46979-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46979-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="46979-155">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="46979-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46979-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="46979-157">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="46979-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="46979-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-158">Az.Sql</span></span>
* <span data-ttu-id="46979-159">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="46979-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="46979-160">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="46979-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="46979-161">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="46979-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="46979-162">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="46979-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="46979-163">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="46979-164">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="46979-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="46979-165">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="46979-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="46979-166">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46979-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="46979-167">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="46979-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-168">Az.Storage</span></span>
* <span data-ttu-id="46979-169">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="46979-170">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="46979-171">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="46979-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="46979-172">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="46979-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="46979-173">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="46979-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-174">Az.Websites</span></span>
* <span data-ttu-id="46979-175">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46979-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="46979-176">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="46979-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="46979-177">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="46979-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="46979-178">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="46979-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="46979-179">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="46979-180">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="46979-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-181">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-181">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-182">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="46979-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="46979-183">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="46979-184">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="46979-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-185">Az.Accounts</span></span>
* <span data-ttu-id="46979-186">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="46979-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-187">Az.Automation</span></span>
* <span data-ttu-id="46979-188">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="46979-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-190">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="46979-191">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="46979-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-192">Az.Compute</span></span>
* <span data-ttu-id="46979-193">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="46979-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-194">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-195">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="46979-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-196">Az.IotHub</span></span>
* <span data-ttu-id="46979-197">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46979-198">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="46979-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46979-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="46979-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-203">Az.KeyVault</span></span>
* <span data-ttu-id="46979-204">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="46979-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-205">Az.Monitor</span></span>
* <span data-ttu-id="46979-206">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="46979-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="46979-207">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="46979-208">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="46979-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-209">Az.Network</span></span>
* <span data-ttu-id="46979-210">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="46979-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="46979-211">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="46979-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46979-212">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46979-213">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="46979-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="46979-214">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="46979-214">No new cmdlets are added.</span></span> <span data-ttu-id="46979-215">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="46979-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-217">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-218">Az.Resources</span></span>
* <span data-ttu-id="46979-219">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="46979-220">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46979-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="46979-221">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="46979-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="46979-222">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="46979-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="46979-223">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="46979-224">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="46979-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="46979-225">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="46979-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="46979-226">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="46979-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-227">Az.Sql</span></span>
* <span data-ttu-id="46979-228">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="46979-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="46979-229">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="46979-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="46979-230">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="46979-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46979-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46979-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46979-232">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="46979-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46979-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46979-233">Az.StorageSync</span></span>
* <span data-ttu-id="46979-234">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="46979-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="46979-235">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="46979-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-236">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-236">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-237">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="46979-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="46979-238">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-239">Az.Accounts</span></span>
* <span data-ttu-id="46979-240">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="46979-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="46979-241">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46979-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-242">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-243">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="46979-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="46979-244">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="46979-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="46979-245">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="46979-246">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-247">Az.Compute</span></span>
* <span data-ttu-id="46979-248">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="46979-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="46979-249">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="46979-250">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="46979-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="46979-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="46979-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="46979-252">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-253">Az.DataFactory</span></span>
* <span data-ttu-id="46979-254">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46979-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46979-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="46979-256">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="46979-257">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="46979-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46979-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-258">Az.HDInsight</span></span>
* <span data-ttu-id="46979-259">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="46979-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-260">Az.KeyVault</span></span>
* <span data-ttu-id="46979-261">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="46979-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-262">Az.Network</span></span>
* <span data-ttu-id="46979-263">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="46979-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="46979-264">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="46979-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="46979-265">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46979-266">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="46979-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="46979-267">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="46979-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="46979-268">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="46979-269">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="46979-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="46979-270">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="46979-271">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-271">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="46979-273">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="46979-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="46979-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46979-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="46979-275">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46979-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46979-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="46979-277">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="46979-278">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="46979-279">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="46979-280">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="46979-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-282">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="46979-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="46979-283">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-284">Az.Resources</span></span>
* <span data-ttu-id="46979-285">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="46979-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="46979-286">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-287">Az.Sql</span></span>
<span data-ttu-id="46979-288">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-289">Az.Storage</span></span>
* <span data-ttu-id="46979-290">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="46979-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="46979-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="46979-292">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="46979-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="46979-293">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="46979-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-294">Az.Websites</span></span>
* <span data-ttu-id="46979-295">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="46979-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="46979-296">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="46979-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="46979-297">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="46979-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-298">Az.Accounts</span></span>
* <span data-ttu-id="46979-299">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="46979-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-300">Az.Cdn</span></span>
* <span data-ttu-id="46979-301">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-302">Az.Compute</span></span>
* <span data-ttu-id="46979-303">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="46979-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="46979-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46979-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="46979-305">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="46979-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46979-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46979-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46979-307">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46979-308">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="46979-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="46979-309">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46979-310">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="46979-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="46979-311">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46979-312">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="46979-313">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46979-314">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="46979-315">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46979-316">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="46979-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="46979-317">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46979-318">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="46979-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="46979-319">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46979-320">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="46979-321">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="46979-322">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="46979-323">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="46979-324">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="46979-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-325">Az.DataFactory</span></span>
* <span data-ttu-id="46979-326">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="46979-327">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="46979-328">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="46979-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="46979-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="46979-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="46979-330">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="46979-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-331">Az.EventHub</span></span>
* <span data-ttu-id="46979-332">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="46979-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46979-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-333">Az.HDInsight</span></span>
* <span data-ttu-id="46979-334">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="46979-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46979-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46979-335">Az.MachineLearning</span></span>
* <span data-ttu-id="46979-336">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="46979-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="46979-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46979-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="46979-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="46979-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="46979-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46979-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="46979-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46979-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="46979-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46979-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="46979-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="46979-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="46979-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="46979-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-344">Az.Network</span></span>
* <span data-ttu-id="46979-345">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="46979-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-347">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="46979-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="46979-348">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="46979-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46979-349">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="46979-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46979-350">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="46979-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-351">Az.Resources</span></span>
* <span data-ttu-id="46979-352">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="46979-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-353">Az.Sql</span></span>
* <span data-ttu-id="46979-354">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="46979-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="46979-355">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="46979-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46979-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46979-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46979-357">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="46979-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-358">Az.Storage</span></span>
* <span data-ttu-id="46979-359">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="46979-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="46979-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="46979-361">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="46979-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="46979-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="46979-363">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="46979-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="46979-364">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-364">General</span></span>
* <span data-ttu-id="46979-365">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="46979-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-366">Az.Accounts</span></span>
* <span data-ttu-id="46979-367">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="46979-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="46979-368">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="46979-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46979-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-369">Az.Batch</span></span>
* <span data-ttu-id="46979-370">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="46979-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-371">Az.DataFactory</span></span>
* <span data-ttu-id="46979-372">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-373">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-374">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="46979-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="46979-375">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="46979-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46979-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46979-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="46979-377">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="46979-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-378">Az.KeyVault</span></span>
* <span data-ttu-id="46979-379">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="46979-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="46979-380">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="46979-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="46979-381">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-382">Az.Monitor</span></span>
* <span data-ttu-id="46979-383">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="46979-384">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="46979-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="46979-385">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="46979-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-386">Az.Network</span></span>
* <span data-ttu-id="46979-387">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-388">Az.Resources</span></span>
* <span data-ttu-id="46979-389">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="46979-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="46979-390">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="46979-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-391">Az.Sql</span></span>
* <span data-ttu-id="46979-392">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="46979-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-393">Az.Storage</span></span>
* <span data-ttu-id="46979-394">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="46979-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="46979-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="46979-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46979-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="46979-397">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="46979-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="46979-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="46979-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="46979-399">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="46979-400">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="46979-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="46979-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="46979-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="46979-403">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="46979-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="46979-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="46979-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="46979-405">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="46979-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="46979-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="46979-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="46979-407">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="46979-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-408">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-408">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-409">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="46979-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="46979-410">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="46979-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-411">Az.Compute</span></span>
* <span data-ttu-id="46979-412">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="46979-412">VM Reapply feature</span></span>
    - <span data-ttu-id="46979-413">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="46979-414">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="46979-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="46979-415">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46979-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="46979-416">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="46979-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="46979-417">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="46979-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46979-418">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="46979-419">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="46979-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="46979-420">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="46979-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="46979-421">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="46979-422">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46979-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46979-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46979-424">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46979-425">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="46979-425">Get the Order</span></span>
* <span data-ttu-id="46979-426">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46979-427">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="46979-427">Create new Order</span></span>
* <span data-ttu-id="46979-428">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46979-429">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-429">Remove the Order</span></span>
* <span data-ttu-id="46979-430">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="46979-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="46979-431">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="46979-431">Now creates Local Share</span></span>
* <span data-ttu-id="46979-432">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="46979-433">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="46979-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="46979-434">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="46979-435">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="46979-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="46979-436">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46979-437">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="46979-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="46979-438">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46979-439">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="46979-439">Create new Triggers</span></span>
* <span data-ttu-id="46979-440">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="46979-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46979-441">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-442">Az.DataFactory</span></span>
* <span data-ttu-id="46979-443">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="46979-444">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-446">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-447">Az.EventHub</span></span>
* <span data-ttu-id="46979-448">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="46979-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-449">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-450">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="46979-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="46979-451">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="46979-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="46979-452">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="46979-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="46979-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="46979-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-454">Az.Network</span></span>
* <span data-ttu-id="46979-455">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="46979-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="46979-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="46979-456">Az.PrivateDns</span></span>
* <span data-ttu-id="46979-457">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-459">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="46979-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="46979-460">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="46979-461">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="46979-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46979-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46979-462">Az.RedisCache</span></span>
* <span data-ttu-id="46979-463">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="46979-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="46979-464">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="46979-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="46979-465">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-466">Az.Resources</span></span>
- <span data-ttu-id="46979-467">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="46979-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="46979-468">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="46979-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="46979-469">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="46979-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="46979-470">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="46979-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="46979-471">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="46979-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-472">Az.Sql</span></span>
* <span data-ttu-id="46979-473">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="46979-474">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="46979-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="46979-475">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="46979-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="46979-476">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-476">General</span></span>
* <span data-ttu-id="46979-477">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="46979-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-478">Az.Accounts</span></span>
* <span data-ttu-id="46979-479">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="46979-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46979-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46979-480">Az.Advisor</span></span>
* <span data-ttu-id="46979-481">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46979-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-482">Az.Batch</span></span>
* <span data-ttu-id="46979-483">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="46979-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="46979-484">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="46979-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="46979-485">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="46979-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="46979-486">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="46979-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="46979-487">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="46979-488">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="46979-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="46979-489">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="46979-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="46979-490">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="46979-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="46979-491">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="46979-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="46979-492">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46979-493">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="46979-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="46979-494">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="46979-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="46979-495">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46979-496">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="46979-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="46979-497">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="46979-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="46979-498">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="46979-499">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="46979-500">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="46979-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="46979-501">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="46979-502">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="46979-503">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46979-504">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46979-505">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="46979-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="46979-506">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="46979-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="46979-507">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="46979-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="46979-508">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="46979-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="46979-509">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="46979-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="46979-510">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="46979-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="46979-511">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="46979-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="46979-512">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="46979-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="46979-513">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="46979-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="46979-514">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="46979-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="46979-515">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="46979-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="46979-516">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="46979-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="46979-517">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="46979-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="46979-518">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="46979-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-519">Az.Cdn</span></span>
* <span data-ttu-id="46979-520">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="46979-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="46979-521">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="46979-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-522">Az.Compute</span></span>
* <span data-ttu-id="46979-523">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="46979-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="46979-524">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="46979-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="46979-525">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="46979-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="46979-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46979-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="46979-527">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="46979-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46979-528">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="46979-529">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="46979-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="46979-530">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="46979-531">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="46979-531">Breaking changes</span></span>
    - <span data-ttu-id="46979-532">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="46979-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="46979-533">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="46979-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-534">Az.DataFactory</span></span>
* <span data-ttu-id="46979-535">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-537">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="46979-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="46979-538">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="46979-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="46979-539">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="46979-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="46979-540">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="46979-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="46979-541">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="46979-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="46979-542">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="46979-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-543">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-544">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="46979-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46979-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-545">Az.HDInsight</span></span>
* <span data-ttu-id="46979-546">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="46979-547">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="46979-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="46979-548">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="46979-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="46979-549">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="46979-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="46979-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46979-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46979-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46979-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46979-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46979-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46979-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46979-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="46979-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46979-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="46979-555">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="46979-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="46979-556">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46979-557">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46979-558">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="46979-559">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="46979-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="46979-560">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="46979-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="46979-561">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="46979-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="46979-562">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="46979-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="46979-563">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="46979-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="46979-564">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="46979-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="46979-565">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="46979-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="46979-566">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="46979-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="46979-567">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="46979-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-568">Az.IotHub</span></span>
* <span data-ttu-id="46979-569">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="46979-569">Breaking changes:</span></span>
    - <span data-ttu-id="46979-570">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="46979-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46979-571">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46979-572">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="46979-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46979-573">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46979-574">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="46979-575">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="46979-576">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="46979-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="46979-577">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="46979-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="46979-578">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="46979-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46979-579">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46979-580">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="46979-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46979-581">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-583">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="46979-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="46979-584">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="46979-585">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="46979-586">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="46979-587">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="46979-588">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="46979-589">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="46979-590">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="46979-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="46979-591">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="46979-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-592">Az.Resources</span></span>
* <span data-ttu-id="46979-593">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-594">Az.Network</span></span>
* <span data-ttu-id="46979-595">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="46979-596">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="46979-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46979-602">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="46979-603">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-603">New cmdlet:</span></span>
        - <span data-ttu-id="46979-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="46979-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="46979-605">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="46979-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="46979-606">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="46979-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="46979-607">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="46979-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="46979-608">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="46979-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="46979-609">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="46979-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="46979-610">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="46979-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="46979-611">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="46979-612">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-612">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="46979-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="46979-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46979-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46979-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46979-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="46979-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="46979-618">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="46979-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="46979-619">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46979-620">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46979-621">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46979-622">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="46979-623">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="46979-624">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="46979-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="46979-625">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-625">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="46979-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="46979-627">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46979-628">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46979-629">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46979-630">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46979-631">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46979-632">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="46979-633">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="46979-634">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-634">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="46979-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="46979-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="46979-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="46979-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="46979-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="46979-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="46979-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="46979-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="46979-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="46979-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="46979-641">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46979-642">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="46979-643">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="46979-644">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="46979-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="46979-645">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="46979-646">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46979-647">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="46979-648">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="46979-649">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="46979-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="46979-650">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="46979-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="46979-651">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="46979-652">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-652">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46979-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="46979-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46979-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="46979-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46979-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="46979-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46979-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-658">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="46979-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-659">Az.Sql</span></span>
* <span data-ttu-id="46979-660">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="46979-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="46979-661">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="46979-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="46979-662">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="46979-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="46979-663">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="46979-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="46979-664">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="46979-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="46979-665">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="46979-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46979-666">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="46979-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="46979-667">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="46979-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="46979-668">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="46979-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-669">Az.Storage</span></span>
* <span data-ttu-id="46979-670">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="46979-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="46979-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46979-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46979-673">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="46979-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="46979-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46979-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="46979-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46979-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="46979-676">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="46979-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="46979-677">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-677">General</span></span>
* <span data-ttu-id="46979-678">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="46979-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-679">Az.Accounts</span></span>
* <span data-ttu-id="46979-680">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="46979-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46979-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-681">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-682">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46979-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="46979-683">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="46979-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-684">Az.Automation</span></span>
* <span data-ttu-id="46979-685">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="46979-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="46979-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-686">Az.Batch</span></span>
* <span data-ttu-id="46979-687">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="46979-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-688">Az.Compute</span></span>
* <span data-ttu-id="46979-689">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46979-690">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="46979-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="46979-691">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="46979-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="46979-692">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="46979-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-693">Az.DataFactory</span></span>
* <span data-ttu-id="46979-694">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="46979-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="46979-695">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="46979-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="46979-696">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-698">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="46979-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46979-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46979-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="46979-700">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="46979-701">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="46979-702">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="46979-703">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-704">Az.IotHub</span></span>
* <span data-ttu-id="46979-705">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="46979-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="46979-706">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="46979-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="46979-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-707">Az.Monitor</span></span>
* <span data-ttu-id="46979-708">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="46979-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="46979-709">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="46979-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="46979-710">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="46979-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="46979-711">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="46979-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-712">Az.Network</span></span>
* <span data-ttu-id="46979-713">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="46979-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="46979-714">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="46979-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="46979-715">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-715">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="46979-717">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46979-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46979-718">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="46979-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="46979-719">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="46979-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46979-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46979-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46979-723">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="46979-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="46979-724">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="46979-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="46979-725">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="46979-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="46979-726">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="46979-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46979-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46979-727">Az.RedisCache</span></span>
* <span data-ttu-id="46979-728">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="46979-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-729">Az.Sql</span></span>
* <span data-ttu-id="46979-730">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-731">Az.Storage</span></span>
* <span data-ttu-id="46979-732">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="46979-733">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="46979-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46979-734">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46979-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="46979-735">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="46979-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46979-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46979-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46979-737">Az.StorageSync</span></span>
* <span data-ttu-id="46979-738">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="46979-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-739">Az.Websites</span></span>
* <span data-ttu-id="46979-740">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="46979-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="46979-741">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="46979-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46979-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-742">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-743">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="46979-744">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="46979-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="46979-745">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="46979-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-746">Az.Automation</span></span>
* <span data-ttu-id="46979-747">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="46979-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="46979-748">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="46979-749">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="46979-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-750">Az.Compute</span></span>
* <span data-ttu-id="46979-751">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="46979-752">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46979-753">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="46979-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="46979-754">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="46979-755">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="46979-756">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="46979-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="46979-757">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="46979-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="46979-758">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="46979-759">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-760">Az.DataFactory</span></span>
* <span data-ttu-id="46979-761">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="46979-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="46979-762">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46979-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-763">Az.HDInsight</span></span>
* <span data-ttu-id="46979-764">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="46979-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-765">Az.IotHub</span></span>
* <span data-ttu-id="46979-766">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="46979-767">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="46979-768">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-768">New cmdlets are:</span></span>
    - <span data-ttu-id="46979-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46979-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46979-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46979-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46979-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46979-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46979-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46979-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-773">Az.Monitor</span></span>
* <span data-ttu-id="46979-774">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="46979-775">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="46979-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="46979-776">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="46979-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="46979-777">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="46979-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="46979-778">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="46979-779">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="46979-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="46979-780">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="46979-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="46979-781">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="46979-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="46979-782">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="46979-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46979-783">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="46979-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="46979-784">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="46979-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46979-785">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="46979-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="46979-786">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="46979-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="46979-787">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="46979-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="46979-788">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="46979-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="46979-789">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="46979-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="46979-790">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="46979-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="46979-791">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="46979-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="46979-792">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="46979-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="46979-793">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="46979-793">Overall improved help files</span></span>
* <span data-ttu-id="46979-794">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="46979-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-795">Az.Network</span></span>
* <span data-ttu-id="46979-796">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="46979-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="46979-797">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="46979-798">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="46979-799">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="46979-800">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="46979-801">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="46979-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="46979-802">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="46979-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="46979-803">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="46979-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="46979-804">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="46979-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="46979-805">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="46979-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="46979-806">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="46979-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="46979-807">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="46979-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="46979-808">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-808">New cmdlets</span></span>
        - <span data-ttu-id="46979-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="46979-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="46979-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="46979-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="46979-811">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="46979-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46979-812">New-VpnSite</span></span>
        - <span data-ttu-id="46979-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46979-813">Update-VpnSite</span></span>
        - <span data-ttu-id="46979-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46979-814">New-VpnConnection</span></span>
        - <span data-ttu-id="46979-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46979-815">Update-VpnConnection</span></span>
* <span data-ttu-id="46979-816">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="46979-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-818">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="46979-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="46979-819">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="46979-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-820">Az.Resources</span></span>
* <span data-ttu-id="46979-821">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="46979-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-823">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="46979-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="46979-824">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="46979-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="46979-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46979-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46979-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46979-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46979-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46979-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46979-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46979-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="46979-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46979-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46979-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46979-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46979-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46979-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46979-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46979-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46979-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46979-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="46979-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46979-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46979-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46979-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46979-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46979-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46979-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="46979-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="46979-838">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="46979-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46979-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46979-839">Az.SignalR</span></span>
* <span data-ttu-id="46979-840">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-841">Az.Sql</span></span>
* <span data-ttu-id="46979-842">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="46979-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="46979-843">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="46979-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="46979-844">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="46979-845">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="46979-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="46979-846">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="46979-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-847">Az.Storage</span></span>
* <span data-ttu-id="46979-848">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="46979-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="46979-849">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="46979-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="46979-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46979-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="46979-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46979-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="46979-852">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="46979-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46979-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="46979-854">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="46979-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46979-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46979-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46979-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46979-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-859">Az.Websites</span></span>
* <span data-ttu-id="46979-860">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="46979-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="46979-861">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="46979-862">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="46979-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="46979-863">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="46979-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="46979-864">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-864">General</span></span>
* <span data-ttu-id="46979-865">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="46979-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-866">Az.Accounts</span></span>
* <span data-ttu-id="46979-867">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="46979-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="46979-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46979-868">Az.Aks</span></span>
* <span data-ttu-id="46979-869">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="46979-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="46979-870">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="46979-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46979-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-871">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-872">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="46979-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="46979-873">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="46979-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="46979-874">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="46979-875">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="46979-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="46979-876">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="46979-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46979-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-877">Az.Batch</span></span>
* <span data-ttu-id="46979-878">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="46979-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-879">Az.Cdn</span></span>
* <span data-ttu-id="46979-880">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="46979-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-881">Az.Compute</span></span>
* <span data-ttu-id="46979-882">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="46979-883">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="46979-884">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="46979-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="46979-885">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="46979-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="46979-886">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="46979-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="46979-887">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="46979-888">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="46979-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="46979-889">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-890">Az.DataFactory</span></span>
* <span data-ttu-id="46979-891">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="46979-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="46979-892">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="46979-893">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="46979-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="46979-894">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="46979-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-896">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="46979-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-897">Az.EventHub</span></span>
* <span data-ttu-id="46979-898">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="46979-899">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="46979-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="46979-900">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="46979-901">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="46979-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="46979-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46979-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46979-903">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="46979-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-904">Az.Monitor</span></span>
* <span data-ttu-id="46979-905">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="46979-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-906">Az.Network</span></span>
* <span data-ttu-id="46979-907">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="46979-908">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="46979-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="46979-909">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="46979-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="46979-910">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="46979-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="46979-911">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="46979-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="46979-912">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="46979-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="46979-913">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="46979-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-915">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="46979-916">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-916">Added example</span></span>
    - <span data-ttu-id="46979-917">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="46979-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="46979-918">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="46979-919">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="46979-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-921">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="46979-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-922">Az.Resources</span></span>
* <span data-ttu-id="46979-923">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="46979-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="46979-924">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="46979-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="46979-925">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="46979-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="46979-926">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-927">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-928">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="46979-929">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="46979-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="46979-930">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="46979-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="46979-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-932">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="46979-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="46979-933">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="46979-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="46979-934">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="46979-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="46979-935">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="46979-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="46979-936">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="46979-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="46979-937">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="46979-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-938">Az.Sql</span></span>
* <span data-ttu-id="46979-939">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="46979-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-940">Az.Storage</span></span>
* <span data-ttu-id="46979-941">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="46979-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="46979-942">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="46979-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="46979-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46979-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="46979-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46979-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="46979-945">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="46979-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="46979-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46979-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-947">Az.Websites</span></span>
* <span data-ttu-id="46979-948">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="46979-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="46979-949">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="46979-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-950">Az.Accounts</span></span>
* <span data-ttu-id="46979-951">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="46979-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="46979-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="46979-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="46979-953">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="46979-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="46979-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-954">Az.Automation</span></span>
* <span data-ttu-id="46979-955">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="46979-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-957">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="46979-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-958">Az.Compute</span></span>
* <span data-ttu-id="46979-959">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="46979-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46979-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46979-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46979-961">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="46979-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="46979-962">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="46979-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-963">Az.DataFactory</span></span>
* <span data-ttu-id="46979-964">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="46979-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="46979-965">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="46979-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-966">Az.EventHub</span></span>
* <span data-ttu-id="46979-967">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46979-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46979-968">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="46979-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-969">Az.KeyVault</span></span>
* <span data-ttu-id="46979-970">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46979-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46979-971">Az.LogicApp</span></span>
* <span data-ttu-id="46979-972">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="46979-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="46979-973">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="46979-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="46979-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="46979-974">Az.ManagedServices</span></span>
* <span data-ttu-id="46979-975">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-976">Az.Network</span></span>
* <span data-ttu-id="46979-977">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="46979-978">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-978">New cmdlets</span></span>
        - <span data-ttu-id="46979-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46979-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46979-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46979-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46979-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46979-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="46979-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="46979-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46979-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="46979-987">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="46979-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="46979-988">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="46979-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="46979-989">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="46979-990">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="46979-991">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="46979-992">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="46979-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="46979-993">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-993">Updated cmdlets</span></span>
        - <span data-ttu-id="46979-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46979-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46979-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46979-997">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="46979-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46979-998">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="46979-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="46979-999">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="46979-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46979-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46979-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="46979-1003">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="46979-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="46979-1004">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="46979-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="46979-1005">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="46979-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-1007">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="46979-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="46979-1008">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="46979-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1010">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46979-1011">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="46979-1012">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="46979-1013">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46979-1014">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="46979-1015">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46979-1016">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="46979-1017">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46979-1018">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="46979-1019">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1020">Az.Resources</span></span>
- <span data-ttu-id="46979-1021">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="46979-1022">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="46979-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-1024">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46979-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46979-1025">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="46979-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1026">Az.Sql</span></span>
* <span data-ttu-id="46979-1027">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="46979-1028">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="46979-1029">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="46979-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1030">Az.Storage</span></span>
* <span data-ttu-id="46979-1031">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="46979-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46979-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46979-1032">Az.StorageSync</span></span>
* <span data-ttu-id="46979-1033">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="46979-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="46979-1034">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="46979-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1035">Az.Websites</span></span>
* <span data-ttu-id="46979-1036">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="46979-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="46979-1037">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="46979-1038">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="46979-1039">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="46979-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1040">Az.Accounts</span></span>
* <span data-ttu-id="46979-1041">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="46979-1042">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="46979-1043">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="46979-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46979-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46979-1044">Az.Advisor</span></span>
* <span data-ttu-id="46979-1045">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="46979-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="46979-1046">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="46979-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46979-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-1048">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="46979-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="46979-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="46979-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="46979-1050">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="46979-1051">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="46979-1052">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="46979-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="46979-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46979-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="46979-1054">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="46979-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1055">Az.Automation</span></span>
* <span data-ttu-id="46979-1056">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="46979-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1057">Az.Compute</span></span>
* <span data-ttu-id="46979-1058">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-1059">Az.DataFactory</span></span>
* <span data-ttu-id="46979-1060">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46979-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46979-1061">Az.EventGrid</span></span>
* <span data-ttu-id="46979-1062">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-1063">Az.IotHub</span></span>
* <span data-ttu-id="46979-1064">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="46979-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1065">Az.Network</span></span>
* <span data-ttu-id="46979-1066">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="46979-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="46979-1067">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="46979-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46979-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="46979-1069">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="46979-1070">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="46979-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-1072">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="46979-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1074">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1075">Az.Resources</span></span>
    - <span data-ttu-id="46979-1076">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="46979-1077">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="46979-1078">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="46979-1079">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-1081">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="46979-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1082">Az.Sql</span></span>
* <span data-ttu-id="46979-1083">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="46979-1084">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="46979-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="46979-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46979-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46979-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46979-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46979-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46979-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46979-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="46979-1091">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="46979-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1092">Az.Storage</span></span>
* <span data-ttu-id="46979-1093">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="46979-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="46979-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46979-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="46979-1095">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="46979-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="46979-1096">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="46979-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="46979-1097">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="46979-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="46979-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46979-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46979-1100">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="46979-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="46979-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46979-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="46979-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46979-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46979-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46979-1103">Az.StorageSync</span></span>
* <span data-ttu-id="46979-1104">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="46979-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="46979-1105">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="46979-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1106">Az.Accounts</span></span>
* <span data-ttu-id="46979-1107">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="46979-1108">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="46979-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="46979-1109">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="46979-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="46979-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="46979-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="46979-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1112">Az.Compute</span></span>
* <span data-ttu-id="46979-1113">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="46979-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="46979-1114">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="46979-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46979-1115">Az.Dns</span></span>
* <span data-ttu-id="46979-1116">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="46979-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46979-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46979-1117">Az.EventGrid</span></span>
* <span data-ttu-id="46979-1118">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="46979-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="46979-1119">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-1119">New cmdlets:</span></span>
    - <span data-ttu-id="46979-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46979-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46979-1121">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="46979-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46979-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46979-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46979-1123">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="46979-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="46979-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46979-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46979-1125">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="46979-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46979-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46979-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46979-1127">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46979-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46979-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46979-1129">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="46979-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="46979-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="46979-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46979-1131">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="46979-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="46979-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="46979-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="46979-1133">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="46979-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="46979-1134">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="46979-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46979-1135">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="46979-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="46979-1136">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="46979-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="46979-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="46979-1138">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46979-1139">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46979-1140">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="46979-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="46979-1141">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="46979-1142">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="46979-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="46979-1143">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="46979-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="46979-1144">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="46979-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="46979-1145">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="46979-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="46979-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="46979-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="46979-1147">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="46979-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="46979-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="46979-1149">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="46979-1150">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="46979-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="46979-1153">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="46979-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="46979-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="46979-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="46979-1155">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="46979-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1156">Az.Network</span></span>
* <span data-ttu-id="46979-1157">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="46979-1158">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1158">New cmdlets</span></span>
        - <span data-ttu-id="46979-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="46979-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="46979-1160">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="46979-1161">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1161">New cmdlets</span></span> 
        - <span data-ttu-id="46979-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="46979-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="46979-1163">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="46979-1164">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1164">New cmdlets</span></span> 
        - <span data-ttu-id="46979-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46979-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="46979-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46979-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46979-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46979-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46979-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="46979-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46979-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46979-1170">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="46979-1171">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1171">New cmdlets</span></span>
        - <span data-ttu-id="46979-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46979-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46979-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46979-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46979-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46979-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46979-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="46979-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="46979-1176">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="46979-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="46979-1177">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="46979-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="46979-1178">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="46979-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="46979-1179">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="46979-1180">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="46979-1181">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="46979-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="46979-1182">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="46979-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="46979-1183">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="46979-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="46979-1184">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="46979-1185">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="46979-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="46979-1186">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="46979-1187">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="46979-1188">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="46979-1189">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="46979-1190">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46979-1191">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="46979-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="46979-1192">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="46979-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="46979-1193">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="46979-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="46979-1194">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="46979-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="46979-1195">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="46979-1196">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46979-1197">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46979-1198">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-1200">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1201">Az.Resources</span></span>
* <span data-ttu-id="46979-1202">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="46979-1203">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46979-1204">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46979-1205">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-1207">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="46979-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1208">Az.Sql</span></span>
* <span data-ttu-id="46979-1209">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="46979-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="46979-1210">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="46979-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="46979-1211">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="46979-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46979-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46979-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46979-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46979-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46979-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46979-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46979-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="46979-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46979-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1217">Az.Storage</span></span>
* <span data-ttu-id="46979-1218">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="46979-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="46979-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="46979-1220">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="46979-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="46979-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1222">Az.Websites</span></span>
* <span data-ttu-id="46979-1223">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="46979-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="46979-1224">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="46979-1225">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="46979-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="46979-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-1226">Az.Cdn</span></span>
* <span data-ttu-id="46979-1227">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="46979-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1228">Az.Compute</span></span>
* <span data-ttu-id="46979-1229">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="46979-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="46979-1230">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="46979-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-1231">Az.EventHub</span></span>
* <span data-ttu-id="46979-1232">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="46979-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="46979-1233">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="46979-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1234">Az.Network</span></span>
* <span data-ttu-id="46979-1235">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="46979-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="46979-1236">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46979-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="46979-1238">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1240">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="46979-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-1242">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="46979-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-1244">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="46979-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="46979-1245">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="46979-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1246">Az.Sql</span></span>
* <span data-ttu-id="46979-1247">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="46979-1248">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="46979-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46979-1249">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="46979-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="46979-1250">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="46979-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1251">Az.Websites</span></span>
* <span data-ttu-id="46979-1252">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="46979-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="46979-1253">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="46979-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46979-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-1255">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="46979-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="46979-1256">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="46979-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="46979-1257">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="46979-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="46979-1258">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="46979-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="46979-1259">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="46979-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="46979-1260">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="46979-1261">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="46979-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="46979-1262">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="46979-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="46979-1263">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="46979-1264">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="46979-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="46979-1265">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="46979-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="46979-1266">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="46979-1267">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="46979-1268">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="46979-1269">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="46979-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="46979-1270">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="46979-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="46979-1271">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="46979-1272">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="46979-1273">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="46979-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="46979-1274">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="46979-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="46979-1275">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="46979-1276">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="46979-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="46979-1277">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="46979-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="46979-1278">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="46979-1279">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="46979-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="46979-1280">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="46979-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="46979-1281">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="46979-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="46979-1282">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="46979-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="46979-1283">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="46979-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="46979-1284">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="46979-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="46979-1285">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="46979-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="46979-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="46979-1287">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="46979-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="46979-1288">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46979-1289">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="46979-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="46979-1290">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="46979-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="46979-1291">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="46979-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="46979-1292">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="46979-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="46979-1293">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="46979-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="46979-1294">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="46979-1295">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="46979-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46979-1296">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="46979-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="46979-1297">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="46979-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="46979-1298">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="46979-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="46979-1299">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46979-1300">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="46979-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46979-1301">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="46979-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="46979-1302">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="46979-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="46979-1303">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="46979-1304">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="46979-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="46979-1305">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="46979-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="46979-1306">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="46979-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="46979-1307">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="46979-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="46979-1308">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="46979-1309">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="46979-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="46979-1310">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="46979-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="46979-1311">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46979-1312">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46979-1313">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46979-1314">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46979-1315">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46979-1316">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46979-1317">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46979-1318">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46979-1319">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="46979-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="46979-1320">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46979-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="46979-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="46979-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="46979-1322">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46979-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="46979-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="46979-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="46979-1324">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46979-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="46979-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="46979-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="46979-1326">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="46979-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="46979-1327">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="46979-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="46979-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="46979-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="46979-1329">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="46979-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="46979-1330">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="46979-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="46979-1331">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="46979-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1332">Az.Automation</span></span>
* <span data-ttu-id="46979-1333">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="46979-1334">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="46979-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="46979-1335">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="46979-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="46979-1336">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="46979-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="46979-1337">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="46979-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="46979-1338">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="46979-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="46979-1339">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="46979-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1340">Az.Compute</span></span>
* <span data-ttu-id="46979-1341">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="46979-1342">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="46979-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-1344">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="46979-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-1345">Az.Monitor</span></span>
* <span data-ttu-id="46979-1346">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="46979-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1347">Az.Network</span></span>
* <span data-ttu-id="46979-1348">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="46979-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="46979-1349">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="46979-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="46979-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="46979-1351">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1352">Az.Resources</span></span>
* <span data-ttu-id="46979-1353">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1354">Az.Sql</span></span>
* <span data-ttu-id="46979-1355">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="46979-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="46979-1356">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="46979-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1357">Az.Accounts</span></span>
* <span data-ttu-id="46979-1358">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="46979-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-1360">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="46979-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="46979-1361">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="46979-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1362">Az.Compute</span></span>
* <span data-ttu-id="46979-1363">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="46979-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="46979-1364">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="46979-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="46979-1365">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="46979-1366">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="46979-1367">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="46979-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="46979-1368">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="46979-1369">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="46979-1369">Breaking changes</span></span>
    - <span data-ttu-id="46979-1370">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="46979-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="46979-1371">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="46979-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46979-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46979-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="46979-1373">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="46979-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="46979-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46979-1374">Az.Dns</span></span>
* <span data-ttu-id="46979-1375">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="46979-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="46979-1376">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="46979-1377">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="46979-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46979-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="46979-1379">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="46979-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="46979-1380">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="46979-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="46979-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-1381">Az.HDInsight</span></span>
* <span data-ttu-id="46979-1382">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="46979-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="46979-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46979-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="46979-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46979-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46979-1385">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="46979-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46979-1386">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="46979-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="46979-1387">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="46979-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="46979-1388">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="46979-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-1389">Az.Monitor</span></span>
* <span data-ttu-id="46979-1390">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="46979-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="46979-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="46979-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="46979-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="46979-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="46979-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="46979-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="46979-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="46979-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="46979-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="46979-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="46979-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="46979-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="46979-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46979-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46979-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46979-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46979-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46979-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46979-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46979-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46979-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46979-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46979-1402">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="46979-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="46979-1403">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="46979-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1404">Az.Network</span></span>
* <span data-ttu-id="46979-1405">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="46979-1406">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1406">New cmdlets</span></span>
        - <span data-ttu-id="46979-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46979-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="46979-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46979-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="46979-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46979-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="46979-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46979-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="46979-1411">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="46979-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46979-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="46979-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46979-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="46979-1414">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="46979-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="46979-1415">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="46979-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="46979-1416">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="46979-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46979-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="46979-1418">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="46979-1419">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="46979-1420">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1422">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="46979-1423">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="46979-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="46979-1424">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="46979-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="46979-1425">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="46979-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="46979-1426">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="46979-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="46979-1427">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="46979-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="46979-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46979-1428">Az.Relay</span></span>
* <span data-ttu-id="46979-1429">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="46979-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-1431">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="46979-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1432">Az.Storage</span></span>
* <span data-ttu-id="46979-1433">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="46979-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="46979-1434">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="46979-1435">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="46979-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="46979-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="46979-1437">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="46979-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="46979-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="46979-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="46979-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1441">Az.Websites</span></span>
* <span data-ttu-id="46979-1442">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="46979-1443">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="46979-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="46979-1444">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="46979-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-1445">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-1446">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="46979-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="46979-1447">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46979-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46979-1448">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46979-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46979-1449">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46979-1450">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46979-1451">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46979-1452">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1453">Az.Accounts</span></span>
* <span data-ttu-id="46979-1454">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46979-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-1455">Az.Batch</span></span>
* <span data-ttu-id="46979-1456">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-1457">Az.Cdn</span></span>
* <span data-ttu-id="46979-1458">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-1460">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1461">Az.Compute</span></span>
* <span data-ttu-id="46979-1462">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="46979-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="46979-1463">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1464">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-1465">Az.DataFactory</span></span>
* <span data-ttu-id="46979-1466">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="46979-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-1468">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46979-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46979-1469">Az.EventGrid</span></span>
* <span data-ttu-id="46979-1470">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="46979-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-1471">Az.EventHub</span></span>
* <span data-ttu-id="46979-1472">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="46979-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="46979-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46979-1473">Az.HDInsight</span></span>
* <span data-ttu-id="46979-1474">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-1475">Az.IotHub</span></span>
* <span data-ttu-id="46979-1476">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-1477">Az.KeyVault</span></span>
* <span data-ttu-id="46979-1478">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1479">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46979-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46979-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="46979-1481">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="46979-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46979-1482">Az.Media</span></span>
* <span data-ttu-id="46979-1483">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-1484">Az.Monitor</span></span>
  * <span data-ttu-id="46979-1485">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="46979-1486">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="46979-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="46979-1487">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="46979-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="46979-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46979-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46979-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46979-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46979-1490">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46979-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="46979-1491">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="46979-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1492">Az.Network</span></span>
* <span data-ttu-id="46979-1493">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1494">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="46979-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="46979-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="46979-1496">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-1498">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="46979-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46979-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="46979-1500">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1502">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1503">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="46979-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="46979-1504">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="46979-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="46979-1505">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="46979-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46979-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46979-1506">Az.RedisCache</span></span>
* <span data-ttu-id="46979-1507">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1508">Az.Resources</span></span>
* <span data-ttu-id="46979-1509">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1510">Az.Sql</span></span>
* <span data-ttu-id="46979-1511">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="46979-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="46979-1512">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1513">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="46979-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="46979-1514">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="46979-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="46979-1515">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="46979-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="46979-1516">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="46979-1517">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="46979-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1518">Az.Websites</span></span>
* <span data-ttu-id="46979-1519">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="46979-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="46979-1520">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="46979-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46979-1521">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="46979-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="46979-1522">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="46979-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="46979-1523">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="46979-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-1524">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-1525">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="46979-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="46979-1526">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46979-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46979-1527">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46979-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46979-1528">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46979-1529">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46979-1530">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46979-1531">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46979-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1532">Az.Accounts</span></span>
* <span data-ttu-id="46979-1533">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="46979-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46979-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46979-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="46979-1535">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="46979-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="46979-1536">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1537">Az.Automation</span></span>
* <span data-ttu-id="46979-1538">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="46979-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="46979-1539">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="46979-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="46979-1540">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1541">Az.Compute</span></span>
* <span data-ttu-id="46979-1542">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46979-1543">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="46979-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="46979-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="46979-1545">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="46979-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-1546">Az.DataFactory</span></span>
* <span data-ttu-id="46979-1547">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="46979-1548">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="46979-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1549">Az.Resources</span></span>
* <span data-ttu-id="46979-1550">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="46979-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="46979-1551">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="46979-1552">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="46979-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="46979-1553">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46979-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="46979-1554">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="46979-1555">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46979-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1556">Az.Sql</span></span>
* <span data-ttu-id="46979-1557">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="46979-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1558">Az.Storage</span></span>
* <span data-ttu-id="46979-1559">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="46979-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="46979-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46979-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="46979-1561">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="46979-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="46979-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46979-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46979-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46979-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46979-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="46979-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="46979-1566">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="46979-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46979-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46979-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46979-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46979-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46979-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="46979-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46979-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="46979-1571">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="46979-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46979-1572">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="46979-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="46979-1573">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="46979-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="46979-1574">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46979-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46979-1575">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46979-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46979-1576">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46979-1577">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46979-1578">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46979-1579">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1580">Az.Automation</span></span>
* <span data-ttu-id="46979-1581">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="46979-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="46979-1582">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="46979-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="46979-1583">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="46979-1583">Pre-Post script</span></span>
    * <span data-ttu-id="46979-1584">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="46979-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1585">Az.Compute</span></span>
* <span data-ttu-id="46979-1586">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="46979-1587">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-1588">Az.KeyVault</span></span>
* <span data-ttu-id="46979-1589">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1590">Az.Network</span></span>
* <span data-ttu-id="46979-1591">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="46979-1592">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1594">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="46979-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="46979-1595">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1596">Az.Resources</span></span>
* <span data-ttu-id="46979-1597">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="46979-1598">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1599">Az.Sql</span></span>
* <span data-ttu-id="46979-1600">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="46979-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1601">Az.Storage</span></span>
* <span data-ttu-id="46979-1602">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="46979-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46979-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46979-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46979-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46979-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="46979-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="46979-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="46979-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="46979-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="46979-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1609">Az.Websites</span></span>
* <span data-ttu-id="46979-1610">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="46979-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="46979-1611">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="46979-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1612">Az.Accounts</span></span>
* <span data-ttu-id="46979-1613">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="46979-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="46979-1614">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1615">Az.Automation</span></span>
* <span data-ttu-id="46979-1616">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="46979-1617">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="46979-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="46979-1618">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="46979-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-1619">Az.Cdn</span></span>
* <span data-ttu-id="46979-1620">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="46979-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1621">Az.Compute</span></span>
* <span data-ttu-id="46979-1622">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-1623">Az.DataFactory</span></span>
* <span data-ttu-id="46979-1624">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="46979-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46979-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46979-1625">Az.LogicApp</span></span>
* <span data-ttu-id="46979-1626">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="46979-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1627">Az.Network</span></span>
* <span data-ttu-id="46979-1628">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1630">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="46979-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="46979-1631">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="46979-1631">SDK Update</span></span>
* <span data-ttu-id="46979-1632">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="46979-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="46979-1633">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1634">Az.Resources</span></span>
* <span data-ttu-id="46979-1635">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="46979-1636">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="46979-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="46979-1637">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="46979-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="46979-1638">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="46979-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="46979-1639">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="46979-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="46979-1640">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="46979-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1641">Az.Sql</span></span>
* <span data-ttu-id="46979-1642">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="46979-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="46979-1643">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="46979-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1644">Az.Storage</span></span>
* <span data-ttu-id="46979-1645">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46979-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="46979-1646">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="46979-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="46979-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46979-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="46979-1648">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="46979-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1649">Az.Automation</span></span>
* <span data-ttu-id="46979-1650">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="46979-1651">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="46979-1652">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-1654">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1655">Az.Compute</span></span>
* <span data-ttu-id="46979-1656">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="46979-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="46979-1657">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="46979-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="46979-1658">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="46979-1659">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="46979-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-1661">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="46979-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46979-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46979-1662">Az.EventHub</span></span>
* <span data-ttu-id="46979-1663">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="46979-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="46979-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-1664">Az.KeyVault</span></span>
* <span data-ttu-id="46979-1665">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="46979-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46979-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46979-1666">Az.LogicApp</span></span>
* <span data-ttu-id="46979-1667">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="46979-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="46979-1668">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="46979-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="46979-1669">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="46979-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="46979-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46979-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46979-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46979-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46979-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46979-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46979-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46979-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="46979-1674">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="46979-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="46979-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46979-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46979-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46979-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="46979-1679">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="46979-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46979-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-1680">Az.Monitor</span></span>
* <span data-ttu-id="46979-1681">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1682">Az.Network</span></span>
* <span data-ttu-id="46979-1683">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="46979-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="46979-1685">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="46979-1686">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="46979-1687">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="46979-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="46979-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1688">Az.Resources</span></span>
* <span data-ttu-id="46979-1689">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="46979-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46979-1690">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="46979-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="46979-1691">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="46979-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="46979-1692">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="46979-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1693">Az.Sql</span></span>
* <span data-ttu-id="46979-1694">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="46979-1695">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="46979-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1696">Az.Websites</span></span>
* <span data-ttu-id="46979-1697">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="46979-1698">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="46979-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1699">Az.Accounts</span></span>
* <span data-ttu-id="46979-1700">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="46979-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46979-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46979-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="46979-1702">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="46979-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1703">Az.Compute</span></span>
* <span data-ttu-id="46979-1704">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="46979-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="46979-1705">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="46979-1706">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="46979-1708">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="46979-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1709">Az.Resources</span></span>
* <span data-ttu-id="46979-1710">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="46979-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="46979-1711">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="46979-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46979-1712">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="46979-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="46979-1713">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="46979-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1714">Az.Sql</span></span>
* <span data-ttu-id="46979-1715">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="46979-1716">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="46979-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="46979-1717">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="46979-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="46979-1718">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="46979-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1719">Az.Accounts</span></span>
* <span data-ttu-id="46979-1720">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="46979-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46979-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46979-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="46979-1722">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="46979-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="46979-1724">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="46979-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="46979-1725">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="46979-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1726">Az.Accounts</span></span>
* <span data-ttu-id="46979-1727">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46979-1728">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46979-1729">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="46979-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="46979-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46979-1730">Az.Aks</span></span>
* <span data-ttu-id="46979-1731">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46979-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1732">Az.Automation</span></span>
* <span data-ttu-id="46979-1733">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="46979-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="46979-1734">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46979-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46979-1735">Az.Cdn</span></span>
* <span data-ttu-id="46979-1736">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1737">Az.Compute</span></span>
* <span data-ttu-id="46979-1738">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="46979-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="46979-1739">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="46979-1740">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="46979-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46979-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46979-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46979-1742">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46979-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46979-1743">Az.DataFactory</span></span>
* <span data-ttu-id="46979-1744">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-1746">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="46979-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="46979-1747">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="46979-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="46979-1748">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-1749">Az.IotHub</span></span>
* <span data-ttu-id="46979-1750">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46979-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-1751">Az.KeyVault</span></span>
* <span data-ttu-id="46979-1752">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1753">Az.Network</span></span>
* <span data-ttu-id="46979-1754">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1755">Az.Resources</span></span>
* <span data-ttu-id="46979-1756">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="46979-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="46979-1757">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="46979-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="46979-1758">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="46979-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="46979-1759">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="46979-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="46979-1760">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="46979-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="46979-1761">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="46979-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="46979-1762">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="46979-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-1764">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="46979-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="46979-1765">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="46979-1765">Fix some error messages.</span></span>
* <span data-ttu-id="46979-1766">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="46979-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="46979-1767">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="46979-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46979-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46979-1768">Az.SignalR</span></span>
* <span data-ttu-id="46979-1769">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1770">Az.Sql</span></span>
* <span data-ttu-id="46979-1771">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46979-1772">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="46979-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="46979-1773">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="46979-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="46979-1774">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="46979-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1775">Az.Storage</span></span>
* <span data-ttu-id="46979-1776">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46979-1777">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="46979-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="46979-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="46979-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="46979-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="46979-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="46979-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46979-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="46979-1781">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1782">Az.Websites</span></span>
* <span data-ttu-id="46979-1783">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="46979-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46979-1784">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="46979-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="46979-1785">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="46979-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="46979-1786">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="46979-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46979-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1787">Az.Accounts</span></span>
* <span data-ttu-id="46979-1788">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="46979-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1789">Az.Compute</span></span>
* <span data-ttu-id="46979-1790">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="46979-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="46979-1791">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="46979-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="46979-1792">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-1794">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="46979-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="46979-1795">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46979-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46979-1796">Az.EventGrid</span></span>
* <span data-ttu-id="46979-1797">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="46979-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="46979-1798">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="46979-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="46979-1799">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46979-1800">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="46979-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46979-1801">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="46979-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46979-1802">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="46979-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="46979-1803">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="46979-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46979-1804">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="46979-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46979-1805">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="46979-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46979-1806">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="46979-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="46979-1807">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="46979-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="46979-1808">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="46979-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46979-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46979-1809">Az.IotHub</span></span>
* <span data-ttu-id="46979-1810">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="46979-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46979-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46979-1811">Az.LogicApp</span></span>
* <span data-ttu-id="46979-1812">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="46979-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1813">Az.Resources</span></span>
* <span data-ttu-id="46979-1814">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="46979-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="46979-1815">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="46979-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="46979-1816">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="46979-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46979-1817">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="46979-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="46979-1818">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="46979-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="46979-1819">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="46979-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46979-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46979-1820">Az.SignalR</span></span>
* <span data-ttu-id="46979-1821">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1822">Az.Sql</span></span>
* <span data-ttu-id="46979-1823">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="46979-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46979-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1824">Az.Storage</span></span>
* <span data-ttu-id="46979-1825">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="46979-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="46979-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46979-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="46979-1827">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="46979-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="46979-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46979-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1829">Az.Websites</span></span>
* <span data-ttu-id="46979-1830">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="46979-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="46979-1831">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="46979-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="46979-1832">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="46979-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="46979-1833">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-1833">General</span></span>

- <span data-ttu-id="46979-1834">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="46979-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="46979-1835">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1835">Online help for each module</span></span>
- <span data-ttu-id="46979-1836">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="46979-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="46979-1837">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="46979-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1838">Az.Accounts</span></span>
- <span data-ttu-id="46979-1839">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="46979-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="46979-1840">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="46979-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46979-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="46979-1842">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="46979-1842">Fixes for #7002</span></span>
- <span data-ttu-id="46979-1843">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="46979-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46979-1844">Az.Batch</span></span>
- <span data-ttu-id="46979-1845">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="46979-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="46979-1846">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="46979-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="46979-1847">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="46979-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="46979-1848">Az.Billing</span></span>
- <span data-ttu-id="46979-1849">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="46979-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="46979-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="46979-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="46979-1851">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="46979-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="46979-1852">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="46979-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46979-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="46979-1854">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="46979-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="46979-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46979-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="46979-1856">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46979-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="46979-1858">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="46979-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46979-1859">Az.Monitor</span></span>
- <span data-ttu-id="46979-1860">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="46979-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46979-1861">Az.KeyVault</span></span>
- <span data-ttu-id="46979-1862">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="46979-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="46979-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46979-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="46979-1864">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="46979-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="46979-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46979-1865">Az.Media</span></span>
- <span data-ttu-id="46979-1866">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="46979-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46979-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1867">Az.Network</span></span>
<span data-ttu-id="46979-1868">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="46979-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="46979-1869">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="46979-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="46979-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46979-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="46979-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="46979-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46979-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="46979-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="46979-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="46979-1878">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="46979-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46979-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="46979-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46979-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46979-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46979-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46979-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="46979-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46979-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="46979-1884">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="46979-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="46979-1885">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="46979-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="46979-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46979-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46979-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46979-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46979-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46979-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="46979-1889">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="46979-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="46979-1890">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="46979-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46979-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="46979-1892">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="46979-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46979-1893">Az.Profile</span></span>
- <span data-ttu-id="46979-1894">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46979-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="46979-1896">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="46979-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1897">Az.Resources</span></span>
- <span data-ttu-id="46979-1898">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46979-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="46979-1900">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="46979-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="46979-1901">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="46979-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="46979-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="46979-1903">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="46979-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="46979-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1904">Az.Sql</span></span>
- <span data-ttu-id="46979-1905">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="46979-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="46979-1906">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="46979-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="46979-1907">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="46979-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1908">Az.Storage</span></span>
- <span data-ttu-id="46979-1909">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46979-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1910">Az.Websites</span></span>
- <span data-ttu-id="46979-1911">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="46979-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="46979-1912">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="46979-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="46979-1913">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-1913">General</span></span>

* <span data-ttu-id="46979-1914">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="46979-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1915">Az.Compute</span></span>

* <span data-ttu-id="46979-1916">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="46979-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46979-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="46979-1918">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="46979-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="46979-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46979-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="46979-1920">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="46979-1921">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="46979-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="46979-1922">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="46979-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46979-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46979-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="46979-1924">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="46979-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="46979-1925">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="46979-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="46979-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1926">Az.Resources</span></span>

* <span data-ttu-id="46979-1927">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="46979-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="46979-1928">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="46979-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="46979-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1929">Az.Sql</span></span>

* <span data-ttu-id="46979-1930">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="46979-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="46979-1931">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="46979-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="46979-1932">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="46979-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="46979-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-1933">Az.Storage</span></span>

* <span data-ttu-id="46979-1934">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="46979-1935">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="46979-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="46979-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46979-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46979-1937">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="46979-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46979-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="46979-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46979-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46979-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-1940">Az.Websites</span></span>

* <span data-ttu-id="46979-1941">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46979-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="46979-1942">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="46979-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="46979-1943">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="46979-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="46979-1944">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="46979-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46979-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46979-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="46979-1946">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="46979-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="46979-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46979-1947">Az.Automation</span></span>
* <span data-ttu-id="46979-1948">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="46979-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="46979-1949">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="46979-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="46979-1950">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="46979-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="46979-1951">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="46979-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="46979-1952">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="46979-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="46979-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-1953">Az.Compute</span></span>
* <span data-ttu-id="46979-1954">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="46979-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="46979-1955">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="46979-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46979-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="46979-1957">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="46979-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="46979-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46979-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46979-1959">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="46979-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46979-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-1960">Az.Network</span></span>
* <span data-ttu-id="46979-1961">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="46979-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="46979-1962">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="46979-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="46979-1963">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="46979-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="46979-1964">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="46979-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="46979-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46979-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46979-1966">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="46979-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="46979-1967">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="46979-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="46979-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46979-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46979-1969">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="46979-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="46979-1970">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="46979-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="46979-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46979-1971">Az.Relay</span></span>
* <span data-ttu-id="46979-1972">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="46979-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="46979-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-1973">Az.Resources</span></span>
* <span data-ttu-id="46979-1974">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="46979-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="46979-1975">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="46979-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="46979-1976">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="46979-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46979-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-1978">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="46979-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="46979-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-1979">Az.Sql</span></span>
* <span data-ttu-id="46979-1980">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="46979-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46979-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46979-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46979-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46979-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46979-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46979-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46979-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46979-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46979-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46979-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46979-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46979-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="46979-1989">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="46979-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="46979-1990">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="46979-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="46979-1991">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="46979-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="46979-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46979-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46979-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="46979-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46979-1994">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46979-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="46979-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="46979-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="46979-1996">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="46979-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="46979-1997">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="46979-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46979-1998">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="46979-1998">General</span></span>
* <span data-ttu-id="46979-1999">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="46979-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="46979-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46979-2000">Az.Profile</span></span>
* <span data-ttu-id="46979-2001">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="46979-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="46979-2002">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="46979-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="46979-2003">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="46979-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="46979-2004">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="46979-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="46979-2005">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="46979-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="46979-2006">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="46979-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="46979-2007">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="46979-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-2009">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="46979-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-2010">Az.Compute</span></span>
* <span data-ttu-id="46979-2011">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="46979-2012">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="46979-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="46979-2013">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="46979-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-2015">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="46979-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="46979-2016">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="46979-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="46979-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="46979-2017">Az.Insights</span></span>
* <span data-ttu-id="46979-2018">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="46979-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="46979-2019">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="46979-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="46979-2020">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="46979-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="46979-2021">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="46979-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-2022">Az.Network</span></span>
* <span data-ttu-id="46979-2023">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="46979-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="46979-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="46979-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="46979-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="46979-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46979-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="46979-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="46979-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46979-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="46979-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46979-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46979-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46979-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46979-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="46979-2031">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-2032">Az.Resources</span></span>
* <span data-ttu-id="46979-2033">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="46979-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="46979-2034">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="46979-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46979-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46979-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="46979-2036">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="46979-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46979-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46979-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="46979-2038">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="46979-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="46979-2039">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="46979-2040">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="46979-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="46979-2041">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="46979-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="46979-2042">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="46979-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="46979-2043">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="46979-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="46979-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46979-2044">Az.Profile</span></span>
* <span data-ttu-id="46979-2045">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="46979-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="46979-2046">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="46979-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-2047">Az.Compute</span></span>
* <span data-ttu-id="46979-2048">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="46979-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="46979-2049">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="46979-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46979-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46979-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="46979-2051">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="46979-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="46979-2052">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="46979-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="46979-2053">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="46979-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46979-2054">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="46979-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46979-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="46979-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-2056">Az.Network</span></span>
* <span data-ttu-id="46979-2057">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="46979-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="46979-2058">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="46979-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-2059">Az.Resources</span></span>
* <span data-ttu-id="46979-2060">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="46979-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="46979-2061">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="46979-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="46979-2062">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="46979-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="46979-2063">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46979-2063">Azure.Storage</span></span>
* <span data-ttu-id="46979-2064">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="46979-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="46979-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46979-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="46979-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46979-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46979-2067">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="46979-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="46979-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="46979-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="46979-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46979-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="46979-2070">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="46979-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46979-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46979-2071">Az.Compute</span></span>
* <span data-ttu-id="46979-2072">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="46979-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="46979-2073">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="46979-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="46979-2074">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="46979-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="46979-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46979-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="46979-2076">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="46979-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46979-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46979-2077">Az.Network</span></span>
* <span data-ttu-id="46979-2078">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="46979-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="46979-2079">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="46979-2079">new cmdlets added</span></span>
    - <span data-ttu-id="46979-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46979-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="46979-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46979-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="46979-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46979-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="46979-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46979-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="46979-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="46979-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="46979-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="46979-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="46979-2086">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="46979-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="46979-2087">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="46979-2088">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="46979-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46979-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46979-2089">Az.RedisCache</span></span>
* <span data-ttu-id="46979-2090">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="46979-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="46979-2091">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="46979-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="46979-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46979-2092">Az.Resources</span></span>
* <span data-ttu-id="46979-2093">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="46979-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46979-2094">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="46979-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="46979-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46979-2095">Az.Sql</span></span>
* <span data-ttu-id="46979-2096">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="46979-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46979-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46979-2097">Az.Websites</span></span>
* <span data-ttu-id="46979-2098">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="46979-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="46979-2099">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="46979-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="46979-2100">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="46979-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="46979-2101">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="46979-2101">Initial Release</span></span>
