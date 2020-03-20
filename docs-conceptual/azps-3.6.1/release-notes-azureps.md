---
title: Az Azure PowerShell kibocsátási megjegyzései
description: Megismerheti az Azure PowerShell-modulok legújabb frissítéseit.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111031"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="240bd-103">Az Azure PowerShell kibocsátási megjegyzései</span><span class="sxs-lookup"><span data-stu-id="240bd-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="240bd-104">3.6.1 – 2020. március</span><span class="sxs-lookup"><span data-stu-id="240bd-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-105">Az.Accounts</span></span>
* <span data-ttu-id="240bd-106">Azure PowerShell felmérési oldal megnyitása itt: Send-Feedback [#11020]</span><span class="sxs-lookup"><span data-stu-id="240bd-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="240bd-107">Azure PowerShell-felmérés URL-címének megjelenítése itt: Resolve-Error [#11021]</span><span class="sxs-lookup"><span data-stu-id="240bd-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="240bd-108">Az-verzió hozzáadva az UserAgenthez</span><span class="sxs-lookup"><span data-stu-id="240bd-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="240bd-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-109">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-110">Mostantól támogatott az egyéni tartomány lekérése és konfigurálása a DeveloperPortal végpontján [#11007]</span><span class="sxs-lookup"><span data-stu-id="240bd-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="240bd-111">Export-AzApiManagementAPi – Mostantól támogatott az Api-definíció Json formátumban való letöltése [#9987]</span><span class="sxs-lookup"><span data-stu-id="240bd-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="240bd-112">Import-AzApiManagementApi – Az OpenAPI 3.0-definíció Json-dokumentumokból való importálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="240bd-113">New-AzApiManagementIdentityProvider és Set-AzApiManagementIdentityProvider – A Signin Tenant konfigurálása az AAD B2C-szolgáltató esetében mostantól támogatott. [#9784]</span><span class="sxs-lookup"><span data-stu-id="240bd-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-115">A System.Buffershez hivatkozásának explicit hozzáadása a következőkben: csproj és psd1</span><span class="sxs-lookup"><span data-stu-id="240bd-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-116">Az.IotHub</span></span>
* <span data-ttu-id="240bd-117">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="240bd-118">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="240bd-119">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-120">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-121">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-122">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="240bd-123">A cél IoT-eszközökön lévő modulok IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="240bd-124">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="240bd-125">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="240bd-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="240bd-126">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="240bd-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="240bd-127">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="240bd-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="240bd-128">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="240bd-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="240bd-129">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="240bd-130">Parancsmag hozzáadva egy IoT Hubban lévő cél IoT-eszköz modulja kapcsolati sztringjének lekéréséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="240bd-131">Az IoT-eszközök szülő eszközének lekérése/beállítása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="240bd-132">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="240bd-133">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="240bd-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="240bd-134">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="240bd-135">Az eszközök szülő-gyermek kapcsolatainak kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-136">Az.Monitor</span></span>
* <span data-ttu-id="240bd-137">A Get-AzMetricDefinition kimeneti értéke javítva [#9714]</span><span class="sxs-lookup"><span data-stu-id="240bd-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-138">Az.Network</span></span>
* <span data-ttu-id="240bd-139">SQL Management SDK frissítve.</span><span class="sxs-lookup"><span data-stu-id="240bd-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="240bd-140">Kijavítottuk a PrivateLinkServiceConnectionState osztály eltérő elnevezéssel kapcsolatos hibáját.</span><span class="sxs-lookup"><span data-stu-id="240bd-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="240bd-141">Az ActionsRequired mező leképezése a követezőre: ActionRequired</span><span class="sxs-lookup"><span data-stu-id="240bd-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="240bd-142">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="240bd-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-143">Az.Resources</span></span>
* <span data-ttu-id="240bd-144">A Get-AzRoleAssignment null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="240bd-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="240bd-145">A -Force és a -PassThru kapcsoló nem kötelezőként lett megjelölve a Remove-AzADGroup esetében [#10849]</span><span class="sxs-lookup"><span data-stu-id="240bd-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="240bd-146">Javítva a hiba, amely miatt a MailNickname nem lett visszaadva Remove-AzADGroup esetében [#11167]</span><span class="sxs-lookup"><span data-stu-id="240bd-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="240bd-147">A Remove-AzADGroup folyamatművelet működési hibája kijavítva [#11171]</span><span class="sxs-lookup"><span data-stu-id="240bd-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="240bd-148">A GetAzureRoleAssignmentCommand null értékű hivatkozásra vonatkozó hibája javítva</span><span class="sxs-lookup"><span data-stu-id="240bd-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="240bd-149">Kompatibilitástörő változás hozzáadva a szabályzati parancsmagok soron következő változásaihoz</span><span class="sxs-lookup"><span data-stu-id="240bd-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="240bd-150">Frissült a Get-AzResourceGroup az erőforráscsoport-címke kiszolgálóoldali szűrésének elvégzéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="240bd-151">A címkeparancsmagok kiterjesztése a -ResourceID elfogadása érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="240bd-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="240bd-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="240bd-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="240bd-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="240bd-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="240bd-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="240bd-155">Új címkeparancsmag hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="240bd-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="240bd-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="240bd-157">A ScopedDeployment áthozva az SDK 3.3.0-ból</span><span class="sxs-lookup"><span data-stu-id="240bd-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-158">Az.Sql</span></span>
* <span data-ttu-id="240bd-159">PublicNetworkAccess hozzáadva a következőhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="240bd-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="240bd-160">Támogatás hozzáadva a biztonsági másolatok hosszú távú megőrzési konfigurációjához a felügyelt adatbázisok esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="240bd-161">LTR-szabályzat lekérése/beállítása felügyelt adatbázison</span><span class="sxs-lookup"><span data-stu-id="240bd-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="240bd-162">LTR biztonsági másolat(ok) lekérése felügyelt adatbázis, felügyelt példány vagy hely szerint</span><span class="sxs-lookup"><span data-stu-id="240bd-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="240bd-163">LTR biztonsági másolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="240bd-164">LTR biztonsági másolat visszaállítása új felügyelt adatbázis létrehozásához</span><span class="sxs-lookup"><span data-stu-id="240bd-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="240bd-165">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlServer és Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="240bd-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="240bd-166">MinimalTlsVersion hozzáadva a következőkhöz: New-AzSqlInstance és Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="240bd-167">Az SQL SDK-verzió felléptetése a következőhöz: AZ.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-168">Az.Storage</span></span>
* <span data-ttu-id="240bd-169">Támogatott AllowProtectedAppendWrite a következőben: ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="240bd-170">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="240bd-171">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet az AzureStorageTable típusának módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="240bd-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="240bd-172">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="240bd-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="240bd-173">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="240bd-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-174">Az.Websites</span></span>
* <span data-ttu-id="240bd-175">Címke paraméter hozzáadva a következőkhöz: New-AzAppServicePlan és Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="240bd-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="240bd-176">A parancsmag végrehajtásának leállítása, ha egy egyéni tartomány webhelyhez történő hozzáadásakor a rendszer kivételt ad vissza</span><span class="sxs-lookup"><span data-stu-id="240bd-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="240bd-177">Támogatás hozzáadva az olyan App Services műveletek elvégzéséhez, amelyek nem abban az erőforráscsoportban vannak, amelyben az App Service-csomag</span><span class="sxs-lookup"><span data-stu-id="240bd-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="240bd-178">Hozzáférési korlátozás alkalmazva a különböző erőforráscsoportokban lévő webalkalmazásokra/függvényekre</span><span class="sxs-lookup"><span data-stu-id="240bd-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="240bd-179">Az egyéni WebAppSlots-gazdanevek beállítására vonatkozó hiba kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="240bd-180">3.5.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="240bd-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-181">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-181">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-182">Frissült az ügyféloldali telemetria.</span><span class="sxs-lookup"><span data-stu-id="240bd-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="240bd-183">Az.IotHub: parancsmagok hozzáadva az eszközkezelés támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="240bd-184">Az.SqlVirtualMachine: parancsmagok hozzáadva a rendelkezésreállási csoport figyelőjéhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-185">Az.Accounts</span></span>
* <span data-ttu-id="240bd-186">A SubscriptionId, a TenantId és a végrehajtási idő hozzáadva az ügyféloldali telemetria adataihoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-187">Az.Automation</span></span>
* <span data-ttu-id="240bd-188">Ki lett javítva a „New-AzAutomationSoftwareUpdateConfiguration” referenciadokumentációjának 1. példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="240bd-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-190">Az SDK a 7.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="240bd-191">Tovább lett fejlesztve a hibaüzenet, amely akkor jelenik meg, ha a kiszolgáló üres törzset ad vissza válaszként</span><span class="sxs-lookup"><span data-stu-id="240bd-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-192">Az.Compute</span></span>
* <span data-ttu-id="240bd-193">A ProximityPlacementGroupId mostantól üres értékkel is rendelkezhet a frissítés során</span><span class="sxs-lookup"><span data-stu-id="240bd-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-194">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-195">Új parancsmag hozzáadva a WAF-ban használható felügyelt szabálydefiníciók lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-196">Az.IotHub</span></span>
* <span data-ttu-id="240bd-197">Az eszközök az IoT Hubban való kezelése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="240bd-198">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="240bd-199">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-200">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-201">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="240bd-202">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="240bd-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-203">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-204">Ki lett javítva az Add-AzKeyVaultKey.md duplikált szövege</span><span class="sxs-lookup"><span data-stu-id="240bd-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-205">Az.Monitor</span></span>
* <span data-ttu-id="240bd-206">Ki lett javítva a Get-AzLog parancsmag leírása.</span><span class="sxs-lookup"><span data-stu-id="240bd-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="240bd-207">Egy új, ActionGroupId nevű paraméter lett hozzáadva a „New-AzMetricAlertRuleV2” parancshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="240bd-208">A felhasználó a következőket adhatja meg: ActionGroupId(string) vagy ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="240bd-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-209">Az.Network</span></span>
* <span data-ttu-id="240bd-210">Hozzá lett adva egy extra paramétermegjegyzés a „New-AzPrivateLinkService” parancsmag „-EnableProxyProtocol” paraméteréhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="240bd-211">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="240bd-212">Hozzá lett adva egy csomagrögzítési példa a Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és Start-AzVirtualnetworkGatewayPacketCapture.md minden belső és külső csomagjának rögzítéséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="240bd-213">Az Azure Firewall-szabályzat mostantól támogatott a Vnet-tűzfalakon</span><span class="sxs-lookup"><span data-stu-id="240bd-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="240bd-214">Nem lettek hozzáadva új parancsmagok.</span><span class="sxs-lookup"><span data-stu-id="240bd-214">No new cmdlets are added.</span></span> <span data-ttu-id="240bd-215">Enyhítve lettek a tűzfalszabályzat korlátozásai a Vnet-tűzfalak esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-217">A fájlokként történő visszaállítás mostantól támogatott az SQL-adatbázisok esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-218">Az.Resources</span></span>
* <span data-ttu-id="240bd-219">Újra lettek tervezve a sablonalapú üzembehelyezési parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="240bd-220">Új parancsmagok lettek hozzáadva a felügyeleti csoportban való üzembe helyezés kezeléséhez: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="240bd-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="240bd-221">Új parancsmagok lettek hozzáadva a bérlői hatókörben való üzembe helyezés kezeléséhez: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="240bd-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="240bd-222">Az \*-AzDeployment parancsmagok kifejezetten az előfizetési hatókörben való működéshez lettek újratervezve</span><span class="sxs-lookup"><span data-stu-id="240bd-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="240bd-223">Az \*-AzSubscriptionDeployment aliasok lettek létrehozva az \*-AzDeployment parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="240bd-224">Ki lett javítva az „Update-AzADApplication” nem beállított „AvailableToOtherTenants” paraméter esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="240bd-225">Az ApplicationObjectWithoutCredentialParameterSet el lett távolítva az AmbiguousParameterSetException elkerülése érdekében.</span><span class="sxs-lookup"><span data-stu-id="240bd-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="240bd-226">A súgófájlok újra létre lettek hozva</span><span class="sxs-lookup"><span data-stu-id="240bd-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-227">Az.Sql</span></span>
* <span data-ttu-id="240bd-228">Az előfizetések közötti időponthoz kötött visszaállítás mostantól támogatott a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="240bd-229">A már meglévő felügyelt SQL-példány hardvergenerációjának módosítása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="240bd-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="240bd-230">Ki lettek javítva az „Update-AzSqlServerVulnerabilityAssessmentSetting” súgópéldái: paraméter/tulajdonságkimenet – EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="240bd-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="240bd-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="240bd-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="240bd-232">Parancsmagokat hozzáadva a rendelkezésreállási csoport figyelőjéhez</span><span class="sxs-lookup"><span data-stu-id="240bd-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="240bd-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="240bd-233">Az.StorageSync</span></span>
* <span data-ttu-id="240bd-234">Frissültek az „Invoke-AzStorageSyncCompatibilityCheck” támogatott karakterkészletei.</span><span class="sxs-lookup"><span data-stu-id="240bd-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="240bd-235">3.4.0 – 2020. február</span><span class="sxs-lookup"><span data-stu-id="240bd-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-236">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-236">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-237">Megjelent az Az.CosmosDB 0.1.0-s kezdeti verziója</span><span class="sxs-lookup"><span data-stu-id="240bd-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="240bd-238">Az.Network ConnectionMonitor V2 támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-239">Az.Accounts</span></span>
* <span data-ttu-id="240bd-240">A környezet automatikus mentésének letiltása, ha az AzureRmContext.json nem érhető el</span><span class="sxs-lookup"><span data-stu-id="240bd-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="240bd-241">Az Azure Powershell Common referenciájának frissítése 1.3.5-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="240bd-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-242">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-243">**Get-AzApiManagementApiSchema** Az API-val társított Open-API séma kijavítása   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="240bd-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="240bd-244">**New-AzApiManagementProduct**\* és **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="240bd-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="240bd-245">https://github.com/Azure/azure-powershell/issues/10472 dokumentációja kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="240bd-246">**Set-AzApiManagementApi** A ServiceUrl parancsmaggal való frissítését bemutató példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-247">Az.Compute</span></span>
* <span data-ttu-id="240bd-248">A virtuális gép állapotának korlátozása 100 értékre, hogy ne legyen szabályozás, ha a Get-AzVM -Status a virtuális gép neve nélkül lett végrehajtva.</span><span class="sxs-lookup"><span data-stu-id="240bd-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="240bd-249">Update-AzDiskEncryptionSet parancsmagok hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="240bd-250">Az EncryptionType és a DiskEncryptionSetId paraméterek hozzáadása a következő parancsmagokhoz:</span><span class="sxs-lookup"><span data-stu-id="240bd-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="240bd-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="240bd-252">A ColocationStatus paraméter hozzáadva a Get-AzProximityPlacementGroup parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-253">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-254">Az ADF .Net SDK frissítve lett a 4.7.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="240bd-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="240bd-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="240bd-256">LIST műveletek hozzáadása az erőforrásokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="240bd-257">Műveletek végrehajtásának lehetősége az állapotellenőrzés lépésein</span><span class="sxs-lookup"><span data-stu-id="240bd-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="240bd-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-258">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-259">A New-AzHDInsightCluster dokumentációs hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="240bd-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-260">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-261">Name alias hozzáadása a VaultName attribútumhoz, hogy a Remove-AzureKeyVault konzisztens legyen a New-AzureKeyVault paraméterrel.</span><span class="sxs-lookup"><span data-stu-id="240bd-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-262">Az.Network</span></span>
* <span data-ttu-id="240bd-263">Új példa hozzáadva a Set-AzNetworkWatcherConfigFlowLog.md fájlhoz a Traffic Analytics-letiltási forgatókönyv szemléltetésére.</span><span class="sxs-lookup"><span data-stu-id="240bd-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="240bd-264">Felügyeleti IP-konfiguráció támogatás hozzáadva az Azure Firewallhoz – egy dedikált alhálózat és nyilvános IP-cím, amelyet a tűzfal a forgalom felügyeléséhez használni fog</span><span class="sxs-lookup"><span data-stu-id="240bd-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="240bd-265">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="240bd-266">Hozzá lett adva a (nem kötelező) -PublicIpAddress-ManagementPublicIpAddress paraméter, amely egy nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="240bd-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="240bd-267">Hozzá lett adva a SetManagementIpConfiguration metódus a tűzfalobjektumok esetében – nyilvános IP-cím-objektumokat fogad el bemeneti adatként – az alhálózat nevének AzureFirewallManagementSubnet értéknek kell lennie</span><span class="sxs-lookup"><span data-stu-id="240bd-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="240bd-268">A Get-AzNetworkSecurityGroup példái javítva, hogy hálózati biztonsági csoportok példáit tartalmazzák hálózati adapterek helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="240bd-269">Javítottunk egy elírást a New-AzVpnSite parancsban, amely megakadályozta, hogy az erőforrásazonosító-kiegészítő kiegészítsen egy paramétert.</span><span class="sxs-lookup"><span data-stu-id="240bd-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="240bd-270">Az Application Gateway szabály-újraírási műveletkészletének URL-konfigurálása mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="240bd-271">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-271">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="240bd-273">A parancsmagok frissültek a nem kötelező UrlConfiguration paraméterrel</span><span class="sxs-lookup"><span data-stu-id="240bd-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="240bd-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="240bd-275">A Network Watcher Connection Monitor 2-es verziójú erőforrások támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="240bd-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="240bd-277">A javítandó erőforrások azonosítása előtti megfelelőségértékelés támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="240bd-278">-ResourceDiscoverMode paraméter hozzáadása a Start-AzPolicyRemediation parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="240bd-279">A szabályzatok metaadat-erőforrásainak elérésére szolgáló Get-AzPolicyMetadata parancsmag hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="240bd-280">A Get-AzPolicyState és a Get-AzPolicyStateSummary frissült a 2019-10-01 API-verzióhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-282">Azure Site Recovery-támogatás a replikált lemezek eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="240bd-283">Hozzáadott Azure Backup-támogatás a helyreállítási tárak létrehozása közbeni címkehozzáadáshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-284">Az.Resources</span></span>
* <span data-ttu-id="240bd-285">A -Scope választható a \*-AzPolicyAssignment parancsmagokban; az alapértelmezett érték a környezeti előfizetés</span><span class="sxs-lookup"><span data-stu-id="240bd-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="240bd-286">Az ADServicePrincipal jelszó és kulcs típusú hitelesítő adatokkal való létrehozását szemléltető példák hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-287">Az.Sql</span></span>
<span data-ttu-id="240bd-288">A New-AzSqlDatabaseSecondary parancsmag javítva, hogy a PartnerDatabaseName létezését ellenőrizze a DatabaseName létezése helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-289">Az.Storage</span></span>
* <span data-ttu-id="240bd-290">A Table/Queue Encryption Keytype készlet beállításának támogatása Storage-fiók létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="240bd-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="240bd-292">RequestId megjelenítése, ha a StorageException nem rendelkezik ExtendedErrorInformation paraméterrel</span><span class="sxs-lookup"><span data-stu-id="240bd-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="240bd-293">A Start-AzStorageBlobCopy parancsmag 6. példájának kijavítása</span><span class="sxs-lookup"><span data-stu-id="240bd-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-294">Az.Websites</span></span>
* <span data-ttu-id="240bd-295">A Set-AzWebapp és a Set-AzWebappSlot támogatja az AlwaysOn, a MinTls és a FtpsState tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="240bd-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="240bd-296">Javítva a hiba, amely miatt a HttpsOnly és az AppservicePlan Set-AzWebApp paranccsal történő egyidejű módosításakor a HttpsOnly paraméter alaphelyzetbe állt.</span><span class="sxs-lookup"><span data-stu-id="240bd-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="240bd-297">3.3.0 – 2020. január</span><span class="sxs-lookup"><span data-stu-id="240bd-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-298">Az.Accounts</span></span>
* <span data-ttu-id="240bd-299">Frissítve lettek az Add-AzEnvironment és Set-AzEnvironment parancsmagok, amelyek mostantól elfogadják az AzureAttestationServiceEndpointResourceId és AzureAttestationServiceEndpointSuffix paramétereket</span><span class="sxs-lookup"><span data-stu-id="240bd-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-300">Az.Cdn</span></span>
* <span data-ttu-id="240bd-301">A hibaválasz részleteinek láthatóvá tétele a New-AzCdnEndpoint parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-302">Az.Compute</span></span>
* <span data-ttu-id="240bd-303">Javítva lett a Set-AzVMCustomScriptExtension parancsmag az olyan virtuális gépek esetében, amelyek felügyelt operációsrendszer-lemeze nem rendelkezik operációsrendszer-profillal.</span><span class="sxs-lookup"><span data-stu-id="240bd-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="240bd-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="240bd-305">Javítva lettek a New-AzContainerGroup parancsmagpélda által használt paraméternevek</span><span class="sxs-lookup"><span data-stu-id="240bd-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="240bd-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="240bd-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="240bd-307">Hozzá lett adva a Get-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="240bd-308">Az Edge Storage-tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="240bd-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="240bd-309">Hozzá lett adva a New-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="240bd-310">Új Edge Storage-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="240bd-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="240bd-311">Hozzá lett adva a Remove-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="240bd-312">Az Edge Storage-tároló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="240bd-313">Hozzá lett adva az Invoke-AzDataBoxEdgeStorageContainer parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="240bd-314">Meghívási művelet az Edge Storage-tárolóban lévő adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="240bd-315">Hozzá lett adva a Get-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="240bd-316">Az Edge Storage-fiók lekérése</span><span class="sxs-lookup"><span data-stu-id="240bd-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="240bd-317">Hozzá lett adva a New-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="240bd-318">Új Edge Storage-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="240bd-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="240bd-319">Hozzá lett adva a Remove-AzDataBoxEdgeStorageAccount parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="240bd-320">Az Edge Storage-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="240bd-321">Hozzá lett adva az Invoke-AzDataBoxEdgeShare parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="240bd-322">Meghívási művelet a megosztott adatok frissítéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="240bd-323">Hozzá lett adva a Set-AzDataBoxEdgeStorageAccountCredential parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="240bd-324">Az Az.DataBoxEdge tárfiók hitelesítő adatainak beállítása</span><span class="sxs-lookup"><span data-stu-id="240bd-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-325">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-326">Hozzá lettek adva az AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId és VersionStatus tulajdonságok a Get-AzDataFactoryV2IntegrationRuntime parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="240bd-327">Az ADF .Net SDK frissítve lett a 4.6.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="240bd-328">A PublicIPs paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz statikus nyilvános IP-címekkel rendelkező Azure-SSIS IR létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="240bd-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="240bd-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="240bd-330">A hibás hivatkozás el lett távolítva a Get-AzDtlAllowedVMSizesPolicy.md parancsmagból</span><span class="sxs-lookup"><span data-stu-id="240bd-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-331">Az.EventHub</span></span>
* <span data-ttu-id="240bd-332">A 10634-es hiba javítása: Ki lett javítva a nullértékű objektumhivatkozás a remove eventhubnamespace esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="240bd-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-333">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-334">Ki lett javítva az Invoke-AzHDInsightHiveJob.md hibája.</span><span class="sxs-lookup"><span data-stu-id="240bd-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="240bd-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="240bd-335">Az.MachineLearning</span></span>
* <span data-ttu-id="240bd-336">El lettek távolítva az alábbi parancsmagok, mivel a MachineLearningCompute már nem érhető el</span><span class="sxs-lookup"><span data-stu-id="240bd-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="240bd-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="240bd-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="240bd-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="240bd-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="240bd-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="240bd-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="240bd-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="240bd-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="240bd-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="240bd-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="240bd-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="240bd-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="240bd-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="240bd-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-344">Az.Network</span></span>
* <span data-ttu-id="240bd-345">Frissítve lett a Microsoft.Azure.Management.Sql függősége: 1.36-preview helyett 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="240bd-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-347">Módosított Azure Site Recovery-támogatás azon felügyelt lemezeken található, inaktív állapotban titkosított virtuális gépeknél, amelyekhez felhasználó által kezelt kulcsok tartoznak a következő esetében: Azure – Azure-szolgáltató.</span><span class="sxs-lookup"><span data-stu-id="240bd-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="240bd-348">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a védelem engedélyezése során a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="240bd-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="240bd-349">Azure Site Recovery-támogatás a lemeztitkosítási csoportazonosító megadásának opcionálissá tételéhez a lemez szintjén a védelem engedélyezéséhez a következő esetében: VMware – Azure.</span><span class="sxs-lookup"><span data-stu-id="240bd-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="240bd-350">Azure Site Recovery-támogatás a Replikációval védett, lemeztitkosítási csoportleképezéssel ellátott elemek frissítéséhez a következő esetében: HyperV – Azure.</span><span class="sxs-lookup"><span data-stu-id="240bd-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-351">Az.Resources</span></span>
* <span data-ttu-id="240bd-352">Javítva lett egy hiba a Remove-AzTag súgódokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="240bd-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-353">Az.Sql</span></span>
* <span data-ttu-id="240bd-354">Javítva lett a sebezhetőségi felmérés csoportszintű alapkonfigurációs parancsmagjainak működése: az Azure-adatbázis főadatbázisában használható, a felügyelt példányok rendszeradatbázisaiban korlátozott.</span><span class="sxs-lookup"><span data-stu-id="240bd-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="240bd-355">Ki lett javítva egy hiba az SQL-példányok feladatátvételi csoportjainak létrehozása esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="240bd-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="240bd-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="240bd-357">Hozzá lett adva a DR, mint új érvényes licenctípus</span><span class="sxs-lookup"><span data-stu-id="240bd-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-358">Az.Storage</span></span>
* <span data-ttu-id="240bd-359">Hozzá lett adva egy kompatibilitástörő változáshoz kapcsolódó figyelmeztető üzenet a DefaultAction értékének módosítására vonatkozóan egy későbbi kiadásban</span><span class="sxs-lookup"><span data-stu-id="240bd-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="240bd-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="240bd-361">Támogatott a tárfiók legutóbbi szinkronizálási időpontjának lekérése a get-AzureRMStorageAccount parancsmag -IncludeGeoReplicationStats paraméterrel való futtatásával</span><span class="sxs-lookup"><span data-stu-id="240bd-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="240bd-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="240bd-363">3.2.0 – 2019. december</span><span class="sxs-lookup"><span data-stu-id="240bd-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="240bd-364">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-364">General</span></span>
* <span data-ttu-id="240bd-365">A .psd1 hivatkozásai frissítve, hogy minden modulhoz a relatív elérési utat használják</span><span class="sxs-lookup"><span data-stu-id="240bd-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-366">Az.Accounts</span></span>
* <span data-ttu-id="240bd-367">A megfelelő felhasználói ügynök beállítva az ügyféloldali telemetriához az Az 4.0 előzetes verziójában</span><span class="sxs-lookup"><span data-stu-id="240bd-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="240bd-368">Felhasználóbarát hibaüzenet megjelenítése, ha az Az 4.0 előzetes verziójában a környezet null értékű</span><span class="sxs-lookup"><span data-stu-id="240bd-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="240bd-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-369">Az.Batch</span></span>
* <span data-ttu-id="240bd-370">Ki lett javítva a [10602-es](https://github.com/Azure/azure-powershell/issues/10602) számú hiba, amely miatt a **New-AzBatchPool** nem megfelelően küldte el a „VirtualMachineConfiguration.ContainerConfiguration” és a „VirtualMachineConfiguration.DataDisks” paramétereket a kiszolgálónak.</span><span class="sxs-lookup"><span data-stu-id="240bd-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-371">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-372">Az ADF .Net SDK a 4.5.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-373">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-374">A WAF felügyeleti szabályok kizárása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="240bd-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="240bd-375">Hozzá lett adva a SocketAddr automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="240bd-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="240bd-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="240bd-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="240bd-377">Kivételkezelés</span><span class="sxs-lookup"><span data-stu-id="240bd-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-378">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-379">Ki lett javítva az esetleg nem beállított értékek hozzáférésével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="240bd-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="240bd-380">Az elliptikus görbéjű titkosítási tanúsítványok kezelése</span><span class="sxs-lookup"><span data-stu-id="240bd-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="240bd-381">A görbe tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-382">Az.Monitor</span></span>
* <span data-ttu-id="240bd-383">Opcionális argumentum hozzáadva a Diagnosztikai beállítások hozzáadása parancshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="240bd-384">Ez egy kapcsoló argumentum, amely megléte esetén azt jelzi, hogy a Log Analyticsbe történő exportálást egy rögzített séma (más néven</span><span class="sxs-lookup"><span data-stu-id="240bd-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="240bd-385">dedikált adattípus) szerint kell végrehajtani</span><span class="sxs-lookup"><span data-stu-id="240bd-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-386">Az.Network</span></span>
* <span data-ttu-id="240bd-387">Támogatás az Ip-csoportok számára az AzureFirewall alkalmazás, valamint a Nat- és a hálózati szabályok esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-388">Az.Resources</span></span>
* <span data-ttu-id="240bd-389">Ki lett javítva az a hiba, amely miatt a sablonalapú üzembe helyezés során a sablonparamétert nem lehet olvasni, ha a sablonparaméter és egy beépített paraméter neve között névütközés áll fenn.</span><span class="sxs-lookup"><span data-stu-id="240bd-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="240bd-390">Frissültek a szabályzat parancsmagjai a 2019. 09. 01. dátumú új API-verzió használatára, amely bevezeti a szabályzatkészlet-definíciókon belüli csoportos támogatást.</span><span class="sxs-lookup"><span data-stu-id="240bd-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-391">Az.Sql</span></span>
* <span data-ttu-id="240bd-392">Frissítve lett a sebezhetőségi felmérés automatikus engedélyezéséhez szükséges tárterület létrehozása a Storagev2-ben</span><span class="sxs-lookup"><span data-stu-id="240bd-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-393">Az.Storage</span></span>
* <span data-ttu-id="240bd-394">A blob-/tárolóidentitás-alapú SAS-token Oauth-hitelesítésen alapuló Storage-környezettel való létrehozásának támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="240bd-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="240bd-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="240bd-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="240bd-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="240bd-397">Támogatott lett a tárfiókhoz tartozó felhasználódelegálási kulcsok visszavonása, így minden identitásalapú SAS-token visszavonható</span><span class="sxs-lookup"><span data-stu-id="240bd-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="240bd-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="240bd-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="240bd-399">Frissítés a Microsoft.Azure.Management.Storage 14.2.0-s verziójára az új API-verzió (2019. 06. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="240bd-400">A QuotaGiB (gigabájtban megadott megosztási kvóta) esetében támogatottak az 5120-nál nagyobb értékek a fájlmegosztási parancsmagok felügyeleti síkján, és hozzá lett adva a Quota paraméteralias a QuotaGiB paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="240bd-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="240bd-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="240bd-403">A „QuotaGiB” paraméteralias hozzáadva a „kvóta” paraméterhez</span><span class="sxs-lookup"><span data-stu-id="240bd-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="240bd-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="240bd-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="240bd-405">Ki lett javítva az a hiba, amely miatt a Set-AzStorageContainerAcl parancsmag el tudta távolítani a tárolt hozzáférési szabályzatot</span><span class="sxs-lookup"><span data-stu-id="240bd-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="240bd-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="240bd-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="240bd-407">3.1.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="240bd-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-408">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-408">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-409">Az.DataBoxEdge 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="240bd-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="240bd-410">Az.SqlVirtualMachine 1.0.0 kiadva</span><span class="sxs-lookup"><span data-stu-id="240bd-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-411">Az.Compute</span></span>
* <span data-ttu-id="240bd-412">A virtuális gépek Reapply funkciója</span><span class="sxs-lookup"><span data-stu-id="240bd-412">VM Reapply feature</span></span>
    - <span data-ttu-id="240bd-413">A Reapply paraméter hozzá lett adva a Set-AzVM parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="240bd-414">A virtuálisgép-méretezési csoportok AutomaticRepairs funkciója:</span><span class="sxs-lookup"><span data-stu-id="240bd-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="240bd-415">Az EnableAutomaticRepair, az AutomaticRepairGracePeriod és az AutomaticRepairMaxInstanceRepairsPercent paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="240bd-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="240bd-416">Több-bérlős katalógus-rendszerkép támogatása a New-AzVM parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="240bd-417">A Spot hozzá lett adva a New-AzVM, a New-AzVMConfig és a New-AzVmss parancsmag Priority paraméterének argumentumbefejezőjéhez</span><span class="sxs-lookup"><span data-stu-id="240bd-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="240bd-418">A DiskIOPSReadWrite és a DiskMBpsReadWrite paraméter hozzá lett adva az Add-AzVmssDataDisk parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="240bd-419">A New-AzGalleryImageVersion parancsmag SourceImageId paramétere mostantól nem kötelező</span><span class="sxs-lookup"><span data-stu-id="240bd-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="240bd-420">A New-AzGalleryImageVersion parancsmag az OSDiskImage és a DataDiskImage paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="240bd-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="240bd-421">A HyperVGeneration paraméter mostantól elérhető a New-AzGalleryImageDefinition parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="240bd-422">A SkipExtensionsOnOverprovisionedVMs paraméter hozzá lett adva a New-AzVmss, a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="240bd-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="240bd-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="240bd-424">A(z) `Get-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="240bd-425">Megrendelés lekérése</span><span class="sxs-lookup"><span data-stu-id="240bd-425">Get the Order</span></span>
* <span data-ttu-id="240bd-426">A(z) `New-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="240bd-427">Új megrendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="240bd-427">Create new Order</span></span>
* <span data-ttu-id="240bd-428">A(z) `Remove-AzDataBoxEdgeOrder` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="240bd-429">Megrendelés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-429">Remove the Order</span></span>
* <span data-ttu-id="240bd-430">`New-AzDataBoxEdgeShare` parancsmag módosítása</span><span class="sxs-lookup"><span data-stu-id="240bd-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="240bd-431">Mostantól helyi megosztást hoz létre</span><span class="sxs-lookup"><span data-stu-id="240bd-431">Now creates Local Share</span></span>
* <span data-ttu-id="240bd-432">A(z) `Set-AzDataBoxEdgeRole` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="240bd-433">Mostantól az IotRole leképezhető a Share-re</span><span class="sxs-lookup"><span data-stu-id="240bd-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="240bd-434">A(z) `Invoke-AzDataBoxEdgeDevice` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="240bd-435">Frissítések keresésének, letöltésének, telepítésének indítása az eszközön</span><span class="sxs-lookup"><span data-stu-id="240bd-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="240bd-436">A(z) `Get-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="240bd-437">Triggerek információinak lekérdezése</span><span class="sxs-lookup"><span data-stu-id="240bd-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="240bd-438">A(z) `New-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="240bd-439">Új triggerek létrehozása</span><span class="sxs-lookup"><span data-stu-id="240bd-439">Create new Triggers</span></span>
* <span data-ttu-id="240bd-440">A(z) `Remove-AzDataBoxEdgeTrigger` parancsmag hozzá lett adva</span><span class="sxs-lookup"><span data-stu-id="240bd-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="240bd-441">Triggerek eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-442">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-443">Az ADF .Net SDK a 4.4.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="240bd-444">Az ExpressCustomSetup paraméter hozzá lett adva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz a beállítási konfigurációk és külső összetevők egyéni beállítási szkript nélkül történő engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-446">Frissült a Get-AzDataLakeStoreDeletedItem és a Restore-AzDataLakeStoreDeletedItem dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-447">Az.EventHub</span></span>
* <span data-ttu-id="240bd-448">A 10301-es hiba javítása: Az SAS-token dátumformátumának javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-449">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-450">Az Enable-AzFrontDoorCustomDomainHttps és a New-AzFrontDoorFrontendEndpointObject a MinimumTlsVersion paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="240bd-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="240bd-451">A New-AzFrontDoorHealthProbeSettingObject a HealthProbeMethod és az EnabledState paraméterrel bővült</span><span class="sxs-lookup"><span data-stu-id="240bd-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="240bd-452">Új parancsmag érhető el a Front Door létrehozásakor/frissítésekor megadandó BackendPoolsSettings objektum létrehozásához</span><span class="sxs-lookup"><span data-stu-id="240bd-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="240bd-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="240bd-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-454">Az.Network</span></span>
* <span data-ttu-id="240bd-455">A Start-AzVirtualNetworkGatewayConnectionPacketCapture.md és a Start-AzVirtualnetworkGatewayPacketCapture.md FilterData kapcsolójának példái módosultak.</span><span class="sxs-lookup"><span data-stu-id="240bd-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="240bd-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="240bd-456">Az.PrivateDns</span></span>
* <span data-ttu-id="240bd-457">A PrivateDns .net sdk frissült az 1.0.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-459">Mostantól Azure Site Recovery-támogatás érhető el a lemeztípus kiválasztásához a védelem engedélyezésekor.</span><span class="sxs-lookup"><span data-stu-id="240bd-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="240bd-460">Azure Site Recovery-hibajavítás a visszaállítási terv műveletének szerkesztéséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="240bd-461">SQL-visszaállítási támogatás az Azure Backuphoz a fájlstream-adatbázisok elfogadása érdekében.</span><span class="sxs-lookup"><span data-stu-id="240bd-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="240bd-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="240bd-462">Az.RedisCache</span></span>
* <span data-ttu-id="240bd-463">A MinimumTlsVersion paraméter hozzá lett adva a New-AzRedisCache és a Set-AzRedisCache parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="240bd-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="240bd-464">Emellett a MinimumTlsVersion hozzá lett adva a Get-AzRedisCache parancsmag kimenetéhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="240bd-465">Mostantól elérhető a -Size paraméter érvényesítése a Set-AzRedisCache és a New-AzRedisCache parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-466">Az.Resources</span></span>
- <span data-ttu-id="240bd-467">Frissültek a szabályzat parancsmagjai a 2019. 06. 01. dátumú új API-verzió használatára, amely tartalmazza az új EnforcementMode tulajdonságot a szabályzat-hozzárendelésekben.</span><span class="sxs-lookup"><span data-stu-id="240bd-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="240bd-468">Frissült a létrehozási szabályzat definíciójának súgóbeli példája</span><span class="sxs-lookup"><span data-stu-id="240bd-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="240bd-469">Kijavítottuk azt a hibát, amikor a Remove-AZADServicePrincipal -ServicePrincipalName null értékű hivatkozást ad vissza, ha az egyszerű szolgáltatásnév nem található.</span><span class="sxs-lookup"><span data-stu-id="240bd-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="240bd-470">Kijavítottuk azt a hibát, amikor a New-AZADServicePrincipal null értékű hivatkozást ad vissza, ha a bérlőnek nincs előfizetése.</span><span class="sxs-lookup"><span data-stu-id="240bd-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="240bd-471">A New-AzAdServicePrincipal módosult, és már csak a társított alkalmazáshoz ad hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="240bd-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-472">Az.Sql</span></span>
* <span data-ttu-id="240bd-473">Az adatbázisbeli ReadReplicaCount mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="240bd-474">A Set-AzSqlDatabase ki lett javítva nem beállított zónaredundancia esetén</span><span class="sxs-lookup"><span data-stu-id="240bd-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="240bd-475">3.0.0 – 2019. november</span><span class="sxs-lookup"><span data-stu-id="240bd-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="240bd-476">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-476">General</span></span>
* <span data-ttu-id="240bd-477">Megjelent az Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="240bd-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-478">Az.Accounts</span></span>
* <span data-ttu-id="240bd-479">A Resolve-Error aliast érintő elavulási üzenet hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="240bd-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="240bd-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="240bd-480">Az.Advisor</span></span>
* <span data-ttu-id="240bd-481">Új Működésbeli kiválóság kategória hozzáadva a Get-AzAdvisorRecommendation parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="240bd-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-482">Az.Batch</span></span>
* <span data-ttu-id="240bd-483">A `CoreQuota` átnevezve `BatchAccountContext` értékre a következőn: `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="240bd-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="240bd-484">Emellett egy új `LowPriorityCoreQuota` elem is található.</span><span class="sxs-lookup"><span data-stu-id="240bd-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="240bd-485">Ez hatással van a következőre: **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="240bd-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="240bd-486">A **New-AzBatchTask** `-ResourceFile` paraméter most már `PSResourceFile` objektumok gyűjteményét használja, amely az új **New-AzBatchResourceFile** parancsmaggal hozható létre.</span><span class="sxs-lookup"><span data-stu-id="240bd-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="240bd-487">Új **New-AzBatchResourceFile** parancsfájl a szükséges `PSResourceFile` objektumok létrehozásának elősegítéséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="240bd-488">Ezek az **New-AzBatchTask**`-ResourceFile` paraméterénél adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="240bd-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="240bd-489">Ez két új típusú erőforrásfájlt támogat a meglévő `HttpUrl` mód mellett:</span><span class="sxs-lookup"><span data-stu-id="240bd-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="240bd-490">Az `AutoStorageContainerName`-alapú erőforrásfájlok egy teljes automatikus tárolót töltenek le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="240bd-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="240bd-491">A `StorageContainerUrl`-alapú erőforrásfájlok az URL-címben megadott tárolót töltik le a Batch-csomópontra.</span><span class="sxs-lookup"><span data-stu-id="240bd-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="240bd-492">A `PSApplication`**Get-AzBatchApplication** által visszaadott `ApplicationPackages` tulajdonsága eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="240bd-493">Most már lekérhetők az alkalmazásokon belüli adott csomagok a **Get-AzBatchApplicationPackage** használatával.</span><span class="sxs-lookup"><span data-stu-id="240bd-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="240bd-494">Például: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="240bd-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="240bd-495">Az `ApplicationId` átnevezve `ApplicationName` értékre a **Get-AzBatchApplicationPackage**, a **New-AzBatchApplicationPackage**, a **Remove-AzBatchApplicationPackage**, a **Get-AzBatchApplication**, a **New-AzBatchApplication**, a **Remove-AzBatchApplication** és a **Set-AzBatchApplication** esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="240bd-496">Az `ApplicationId` mostantól az `ApplicationName` aliasa.</span><span class="sxs-lookup"><span data-stu-id="240bd-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="240bd-497">Az új `PSWindowsUserConfiguration` tulajdonság hozzáadva a következőhöz: `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="240bd-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="240bd-498">A `Version` átnevezve `Name` értékre a `PSApplicationPackage` esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="240bd-499">A `BlobSource` átnevezve `HttpUrl` értékre a `PSResourceFile` esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="240bd-500">Az `OSDisk` tulajdonság eltávolítva a következőből: `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="240bd-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="240bd-501">A **Set-AzBatchPoolOSVersion** eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="240bd-502">Ez a művelet már nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="240bd-503">`PSCloudServiceConfiguration``TargetOSVersion` eleme eltávolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="240bd-504">A `CurrentOSVersion` átnevezve `OSVersion` értékre a `PSCloudServiceConfiguration` esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="240bd-505">`DataEgressGiB` és `DataIngressGiB` eltávolítva a következőből: `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="240bd-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="240bd-506">A **Get-AzBatchNodeAgentSku** eltávolítva és a **Get-AzBatchSupportedImage** parancsmaggal helyettesítve.</span><span class="sxs-lookup"><span data-stu-id="240bd-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="240bd-507">A **Get-AzBatchSupportedImage** ugyanazokat az adatokat jeleníti meg, mint a **Get-AzBatchNodeAgentSku**, csak egyszerűbb formátumban.</span><span class="sxs-lookup"><span data-stu-id="240bd-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="240bd-508">Most már új, nem ellenőrzött rendszerképeket is visszaad a rendszer.</span><span class="sxs-lookup"><span data-stu-id="240bd-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="240bd-509">Minden rendszerképről további, `Capabilities` és `BatchSupportEndOfLife` típusú információk is szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="240bd-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="240bd-510">Lehetőség arra, hogy távoli fájlrendszereket lehessen csatlakoztatni egy készlet minden csomópontjára a **New-AzBatchPool** új `MountConfiguration` paraméterével.</span><span class="sxs-lookup"><span data-stu-id="240bd-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="240bd-511">Most már támogatja a hálózati biztonsági szabályokat, amelyek a letiltják a készletekhez való hozzáférést a forgalom forrásportja alapján.</span><span class="sxs-lookup"><span data-stu-id="240bd-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="240bd-512">Ez a `PSNetworkSecurityGroupRule``SourcePortRanges` tulajdonsága alapján történik.</span><span class="sxs-lookup"><span data-stu-id="240bd-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="240bd-513">Tároló futtatásakor a Batch támogatja a feladat végrehajtását a tároló munkakönyvtárában vagy a Batch-feladat munkakönyvtárában.</span><span class="sxs-lookup"><span data-stu-id="240bd-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="240bd-514">Ezt a `PSTaskContainerSettings``WorkingDirectory` tulajdonsága szabályozza.</span><span class="sxs-lookup"><span data-stu-id="240bd-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="240bd-515">Új lehetőség nyilvános IP-gyűjtemény megadására az érintett `PSNetworkConfiguration` elemen az új `PublicIPs` tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="240bd-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="240bd-516">Ez garantálja, hogy a készletben található csomópontok rendelkeznek majd IP-címmel a felhasználó által megadott IP-listáról.</span><span class="sxs-lookup"><span data-stu-id="240bd-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="240bd-517">Ha nincs megadva, a `PSSTartTask` alapértelmezett `WaitForSuccess` értéke `$True` (korábban `$False` volt).</span><span class="sxs-lookup"><span data-stu-id="240bd-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="240bd-518">Ha nincs megadva, a `PSAutoUserSpecification` alapértelmezett `Scope` értéke `Pool` (korábban Windowson `Task`, Linuxon pedig `Pool` volt).</span><span class="sxs-lookup"><span data-stu-id="240bd-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-519">Az.Cdn</span></span>
* <span data-ttu-id="240bd-520">A RulesEngine tartalmazza az új UrlRewriteAction és a CacheKeyQueryStringAction műveleteket.</span><span class="sxs-lookup"><span data-stu-id="240bd-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="240bd-521">Javítva számos olyan hiba, mint a New-AzDeliveryRuleCondition parancsmag hiányzó Selector bemenete.</span><span class="sxs-lookup"><span data-stu-id="240bd-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-522">Az.Compute</span></span>
* <span data-ttu-id="240bd-523">Lemeztitkosítási készlet funkció</span><span class="sxs-lookup"><span data-stu-id="240bd-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="240bd-524">Új parancsmagok:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="240bd-525">A DiskEncryptionSetId paraméter hozzá lett adva a következő parancsmagokhoz:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="240bd-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="240bd-526">A DiskEncryptionSetId és az EncryptionType paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="240bd-527">A PublicIPAddressVersion paraméter hozzá lett adva a New-AzVmssIPConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="240bd-528">Egyéni szkriptbővítmény FileUris tulajdonságának módosítása nyilvánosról védett beállításra</span><span class="sxs-lookup"><span data-stu-id="240bd-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="240bd-529">ScaleInPolicy hozzáadva a New-AzVmss, New-AzVmssConfig és Update-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="240bd-530">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="240bd-530">Breaking changes</span></span>
    - <span data-ttu-id="240bd-531">A New-AzDiskConfig esetében a DiskSizeGB helyett az UploadSizeInBytes paramétert kell használni, ha a CreateOption értéke Upload</span><span class="sxs-lookup"><span data-stu-id="240bd-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="240bd-532">A PublishingProfile.Source.ManagedImage.Id elemet a StorageProfile.Source.Id helyettesíti a GalleryImageVersion objektumban</span><span class="sxs-lookup"><span data-stu-id="240bd-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-533">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-534">Az ADF .Net SDK a 4.3.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-536">Az ADLS SDK-verziójának frissítése (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) , a következő javításokkal</span><span class="sxs-lookup"><span data-stu-id="240bd-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="240bd-537">Kivétel jelzésének elkerülése, amikor a lomtár vagy a könyvtár bejegyzésének CreationTime tulajdonsága nem deszerializálható.</span><span class="sxs-lookup"><span data-stu-id="240bd-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="240bd-538">Beállítás megjelenítése minden kérelem-időtúllépés esetén az adlsclient objektumban</span><span class="sxs-lookup"><span data-stu-id="240bd-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="240bd-539">Az eredeti syncflag átadásának javítása a badoffset helyreállításához</span><span class="sxs-lookup"><span data-stu-id="240bd-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="240bd-540">Az EnumerateDirectory javítása a folytatási token válaszellenőrzés utáni lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="240bd-541">Concat-hiba javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-542">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-543">Különféle elgépelések kijavítva a modulban</span><span class="sxs-lookup"><span data-stu-id="240bd-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="240bd-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-544">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-545">Kijavítva az a hiba, amely miatt az ügyfél a Nem érvényes Base-64-sztring hibát kapta, amikor a Get-AzHDInsightCluster használatával próbálta lekérni a fürtöt az ADLSGen1 tároló esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="240bd-546">Új, ApplicationId nevű paraméter hozzáadva az Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig és New-AzHDInsightCluster nevű három parancsmaghoz, hogy az ügyfél megadhassa a szolgáltatásnév alkalmazásazonosítóját az Azure Data Lake eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="240bd-547">A Microsoft.Azure.Management.HDInsight 2.1.0 módosítva a következőre: 5.1.0</span><span class="sxs-lookup"><span data-stu-id="240bd-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="240bd-548">Öt parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="240bd-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="240bd-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="240bd-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="240bd-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="240bd-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="240bd-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="240bd-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="240bd-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="240bd-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="240bd-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="240bd-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="240bd-554">Három parancsmag hozzáadva:</span><span class="sxs-lookup"><span data-stu-id="240bd-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="240bd-555">Get-AzHDInsightMonitoring a Get-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="240bd-556">Enable-AzHDInsightMonitoring az Enable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="240bd-557">Disable-AzHDInsightMonitoring a Disable-AzHDInsightOMS helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="240bd-558">A Get-AzHDInsightProperties javítva, hogy támogassa a képességinformációk adott helyről történő beszerzését.</span><span class="sxs-lookup"><span data-stu-id="240bd-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="240bd-559">Paraméterkészletek (Spark1, Spark2) eltávolítva a következőből: Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="240bd-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="240bd-560">Az Add-AzHDInsightSecurityProfile parancsmag súgódokumentumai példákkal bővültek.</span><span class="sxs-lookup"><span data-stu-id="240bd-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="240bd-561">A következő parancsmagok kimeneti típusa megváltozott:</span><span class="sxs-lookup"><span data-stu-id="240bd-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="240bd-562">A Get-AzHDInsightProperties kimeneti típusa CapabilitiesResponse értékről AzureHDInsightCapabilities értékre változott.</span><span class="sxs-lookup"><span data-stu-id="240bd-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="240bd-563">A Remove-AzHDInsightCluster kimeneti típusa ClusterGetResponse értékről logikai értékre változott.</span><span class="sxs-lookup"><span data-stu-id="240bd-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="240bd-564">A Set-AzHDInsightGatewaySettings HttpConnectivitySettings kimeneti típusa GatewaySettings értékre változott.</span><span class="sxs-lookup"><span data-stu-id="240bd-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="240bd-565">Néhány forgatókönyvi teszteset hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="240bd-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="240bd-566">Néhány alias eltávolítva: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="240bd-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-567">Az.IotHub</span></span>
* <span data-ttu-id="240bd-568">Kompatibilitástörő változások:</span><span class="sxs-lookup"><span data-stu-id="240bd-568">Breaking changes:</span></span>
    - <span data-ttu-id="240bd-569">Az Add-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="240bd-570">Az Add-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="240bd-571">A Get-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="240bd-572">A Get-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="240bd-573">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="240bd-574">A Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties típus OperationsMonitoringProperties tulajdonsága el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="240bd-575">A New-AzIotHubExportDevice parancsmag már nem támogatja a New-AzIotHubExportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="240bd-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="240bd-576">A New-AzIotHubImportDevice parancsmag már nem támogatja a New-AzIotHubImportDevices aliast.</span><span class="sxs-lookup"><span data-stu-id="240bd-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="240bd-577">A Remove-AzIotHubEventHubConsumerGroup parancsmag a továbbiakban nem támogatja az EventHubEndpointName paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="240bd-578">A Remove-AzIotHubEventHubConsumerGroup parancsmaghoz tartozó __AllParameterSets paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="240bd-579">A Set-AzIotHub parancsmag a továbbiakban nem támogatja az OperationsMonitoringProperties paramétert, és nem található alias az eredeti paraméternévhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="240bd-580">A Set-AzIotHub parancsmaghoz tartozó UpdateOperationsMonitoringProperties paraméterkészlet el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-582">Azure Site Recovery-támogatás az olyan hálózati erőforrások konfigurálásához, mint a hálózati biztonsági csoportok, a nyilvános IP-címek és az Azure–Azure belső terheléselosztók.</span><span class="sxs-lookup"><span data-stu-id="240bd-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-583">Azure Site Recovery-támogatás felügyelt lemezekre történő íráshoz VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="240bd-584">Azure Site Recovery-támogatás hálózati adapter csökkentéséhez VMware-ről az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="240bd-585">Azure Site Recovery-támogatás a hálózat felgyorsításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-586">Azure Site Recovery-támogatás az automatikus frissítési ügynök biztosításához Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-587">Azure Site Recovery-támogatás standard SSD-meghajtóhoz Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-588">Azure Site Recovery-támogatás az Azure Disk Encryption kétlépéses hitelesítéséhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-589">Azure Site Recovery-támogatás az újonnan hozzáadott lemez védelméhez Azure-ból az Azure-ba történő helyreállításkor.</span><span class="sxs-lookup"><span data-stu-id="240bd-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-590">SoftDelete funkció hozzáadva a virtuális géphez, továbbá a softdelete-hez hozzáadott tesztek</span><span class="sxs-lookup"><span data-stu-id="240bd-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-591">Az.Resources</span></span>
* <span data-ttu-id="240bd-592">A Microsoft.Extensions.Caching.Memory függőségi szerelvény frissítése 1.1.1-esről 2.2-es verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-593">Az.Network</span></span>
* <span data-ttu-id="240bd-594">A PrivateEndpointConnection összes parancsmagjának módosítása az általános szolgáltató támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="240bd-595">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="240bd-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="240bd-601">Új parancsmag hozzáadása a PrivateLinkResource-hoz, valamint az általános szolgáltató támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="240bd-602">Új parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-602">New cmdlet:</span></span>
        - <span data-ttu-id="240bd-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="240bd-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="240bd-604">Új mezőket és paramétereket ad a Proxy Protocol V2 funkcióhoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="240bd-605">Hozzáadja az EnableProxyProtocol tulajdonságot a PrivateLinkService osztályban</span><span class="sxs-lookup"><span data-stu-id="240bd-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="240bd-606">Hozzáadja a LinkIdentifier tulajdonságot a PrivateEndpointConnection osztályban</span><span class="sxs-lookup"><span data-stu-id="240bd-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="240bd-607">New-AzPrivateLinkService frissítve az új, választható EnableProxyProtocol paraméter hozzáadásával.</span><span class="sxs-lookup"><span data-stu-id="240bd-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="240bd-608">Ki lett javítva a New-AzApplicationGatewaySku referenciadokumentációjában található helytelen paraméterleírás</span><span class="sxs-lookup"><span data-stu-id="240bd-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="240bd-609">Új parancsmagok az Azure Firewall-szabályzat támogatásához</span><span class="sxs-lookup"><span data-stu-id="240bd-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="240bd-610">A VirtualHub RouteTables gyermekerőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="240bd-611">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-611">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="240bd-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="240bd-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="240bd-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="240bd-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="240bd-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="240bd-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="240bd-617">Az új termékváltozat és VirtualWANType tulajdonság támogatásának hozzáadása a VirtualHub, illetve a VirtualWan esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="240bd-618">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="240bd-619">New-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="240bd-620">Update-AzVirtualHub: Sku paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="240bd-621">New-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="240bd-622">Update-AzVirtualWan: VirtualWANType paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="240bd-623">Az EnableInternetSecurity tulajdonság támogatásának hozzáadása a HubVnetConnection, a VpnConnection és az ExpressRouteConnection esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="240bd-624">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-624">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="240bd-626">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="240bd-627">New-AzureRmVirtualHubVnetConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="240bd-628">New-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="240bd-629">Update-AzureRmVpnConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="240bd-630">New-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="240bd-631">Set-AzureRmExpressRouteConnection: EnableInternetSecurity paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="240bd-632">TopLevel WebApplicationFirewall-szabályzat beállításának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="240bd-633">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-633">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="240bd-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="240bd-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="240bd-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="240bd-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="240bd-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="240bd-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="240bd-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="240bd-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="240bd-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="240bd-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="240bd-640">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="240bd-641">New-AzApplicationGatewayFirewallPolicy: PolicySetting, ManagedRule paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="240bd-642">A CustomRule Geo-Match operátorának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="240bd-643">A GeoMatch hozzáadva a FirewallCondition operátorához</span><span class="sxs-lookup"><span data-stu-id="240bd-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="240bd-644">perListener és a perSite tűzfalszabályzat támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="240bd-645">Opcionális paraméterekkel frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="240bd-646">New-AzApplicationGatewayHttpListener: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="240bd-647">New-AzApplicationGatewayPathRuleConfig: FirewallPolicy, FirewallPolicyId paraméter hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="240bd-648">Javítva: a PSBastion esetében a szükséges AzureBastionSubnet alhálózat nevében nem kell megkülönböztetni a kis- és nagybetűket</span><span class="sxs-lookup"><span data-stu-id="240bd-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="240bd-649">A hálózati szabályok céltartományneveinek és a NAT-szabályok lefordított tartományneveinek támogatása az Azure Firewallban</span><span class="sxs-lookup"><span data-stu-id="240bd-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="240bd-650">Az IpGroup legfelsőbb szintű RouteTables erőforrásának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="240bd-651">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-651">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="240bd-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="240bd-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="240bd-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-657">Az Add-AzServiceFabricApplicationCertificate parancsmag el lett távolítva, mivel az Add-AzVmssSecret lefedi ezt a forgatókönyvet.</span><span class="sxs-lookup"><span data-stu-id="240bd-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-658">Az.Sql</span></span>
* <span data-ttu-id="240bd-659">Törölt adatbázisok visszaállításának támogatása hozzáadva a felügyelt példányokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="240bd-660">A régi naplózási parancsmagok elavulttá váltak a kódban.</span><span class="sxs-lookup"><span data-stu-id="240bd-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="240bd-661">A következő elavult aliasok el lettek távolítva:</span><span class="sxs-lookup"><span data-stu-id="240bd-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="240bd-662">Get-AzSqlDatabaseIndexRecommendations (a Get-AzSqlDatabaseIndexRecommendation használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="240bd-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="240bd-663">Get-AzSqlDatabaseRestorePoints (a Get-AzSqlDatabaseRestorePoint használata javasolt helyette)</span><span class="sxs-lookup"><span data-stu-id="240bd-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="240bd-664">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag eltávolítva</span><span class="sxs-lookup"><span data-stu-id="240bd-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="240bd-665">Az elavult sebezhetőség-felmérési beállítások parancsmagjainak aliasai eltávolítva</span><span class="sxs-lookup"><span data-stu-id="240bd-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="240bd-666">A fejlett fenyegetésészlelési beállítások parancsmagjai elavulttá váltak</span><span class="sxs-lookup"><span data-stu-id="240bd-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="240bd-667">Parancsmagok hozzáadása egy adatbázis oszlopait érintő érzékenységi javaslatok letiltása és engedélyezése céljából.</span><span class="sxs-lookup"><span data-stu-id="240bd-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-668">Az.Storage</span></span>
* <span data-ttu-id="240bd-669">Nagy fájlok megosztásának engedélyezése Storage-fiók létrehozása vagy frissítése esetén</span><span class="sxs-lookup"><span data-stu-id="240bd-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="240bd-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="240bd-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="240bd-672">Fájlkezelő bezárása/lekérése esetén a fájlkönyvtár vagy fájl bemeneti elérési út ellenőrzése kimarad, hogy a DeletePending állapotban lévő objektum ne okozhasson hibát</span><span class="sxs-lookup"><span data-stu-id="240bd-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="240bd-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="240bd-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="240bd-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="240bd-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="240bd-675">2.8.0 – 2019. október</span><span class="sxs-lookup"><span data-stu-id="240bd-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="240bd-676">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-676">General</span></span>
* <span data-ttu-id="240bd-677">Az.HealthcareApis 1.0.0-s kiadás</span><span class="sxs-lookup"><span data-stu-id="240bd-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-678">Az.Accounts</span></span>
* <span data-ttu-id="240bd-679">A telemetria és az URL-címek újraírásának frissítése a létrehozott modulok esetében, a Windows-egységek tesztelésének javítása.</span><span class="sxs-lookup"><span data-stu-id="240bd-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="240bd-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-680">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-681">**Set-AzApiManagementApi** – Az API a következőre való frissítésének támogatása: ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="240bd-682">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="240bd-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-683">Az.Automation</span></span>
* <span data-ttu-id="240bd-684">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag a Linux újraindítási beállítási paramétere kapcsán.</span><span class="sxs-lookup"><span data-stu-id="240bd-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="240bd-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-685">Az.Batch</span></span>
* <span data-ttu-id="240bd-686">A **Get-AzBatchNodeAgentSku** elavult, így a 2.0.0-ás verziótól a **Get-AzBatchSupportImage** váltja fel.</span><span class="sxs-lookup"><span data-stu-id="240bd-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-687">Az.Compute</span></span>
* <span data-ttu-id="240bd-688">A Priority, EvictionPolicy és MaxPrice paraméterek hozzáadása a New-AzVM és a New-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="240bd-689">Az Add-AzVMAdditionalUnattendContent és az Add-AzVMSshPublicKey parancsmagok figyelmeztető üzenetének és súgójának kijavítása</span><span class="sxs-lookup"><span data-stu-id="240bd-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="240bd-690">A -skipVmBackup kivétel kijavítása felügyelt lemezekkel rendelkező Linux rendszerű virtuális gépek esetében a Set-AzVMDiskEncryptionExtension kapcsán.</span><span class="sxs-lookup"><span data-stu-id="240bd-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="240bd-691">A titkosítási beállítások frissítési hibájának kijavítása a Set-AzVMDiskEncryptionExtension kétmenetes forgatókönyvében.</span><span class="sxs-lookup"><span data-stu-id="240bd-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-692">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-693">CRUD-parancsok lettek hozzáadva az ADF V2-adatfolyamhoz: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow és Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="240bd-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="240bd-694">Műveleti parancsok lettek hozzáadva az ADF V2-adatfolyam hibakeresési munkamenetéhez: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand és Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="240bd-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="240bd-695">Az ADF .Net SDK a 4.2.0-ás verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-697">A fiókérvényesítés javítása, hogy a "-" jelölésű fiókok tartomány nélkül is továbbíthatók legyenek</span><span class="sxs-lookup"><span data-stu-id="240bd-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="240bd-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="240bd-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="240bd-699">A PowerShell az 1.0.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="240bd-700">Az SDK a 1.0.2-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="240bd-701">Frissítés a tesztekben az új SDK-verzióra való hivatkozáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="240bd-702">A kimeneti struktúra beágyazottról simítottra frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-703">Az.IotHub</span></span>
* <span data-ttu-id="240bd-704">Új útválasztási forrás hozzáadása: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="240bd-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="240bd-705">Kisebb hibajavítás: A Get-AzIothub nem adja vissza a következőt: subscriptionId</span><span class="sxs-lookup"><span data-stu-id="240bd-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-706">Az.Monitor</span></span>
* <span data-ttu-id="240bd-707">Új műveleticsoport-fogadók hozzáadva a következő műveleti csoporthoz:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="240bd-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="240bd-708">Az általános riasztási séma használata engedélyezve a fogadók számára.</span><span class="sxs-lookup"><span data-stu-id="240bd-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="240bd-709">Ez nem vonatkozik az SMS, az Azure App leküldéses üzenetei, az ITSM és a Voice fogadóira.</span><span class="sxs-lookup"><span data-stu-id="240bd-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="240bd-710">A webhookok mostantól az Azure Active Directory-hitelesítés használatát is támogatják.</span><span class="sxs-lookup"><span data-stu-id="240bd-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-711">Az.Network</span></span>
* <span data-ttu-id="240bd-712">Új Get-AzAvailableServiceAlias parancsmag hozzáadva, amely a szolgáltatásvégpont-szabályzatokhoz használható aliasok beszerzéséhez hívható meg.</span><span class="sxs-lookup"><span data-stu-id="240bd-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="240bd-713">Forgalomválasztók hozzáadásának támogatása a virtuális hálózati átjáró kapcsolataihoz</span><span class="sxs-lookup"><span data-stu-id="240bd-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="240bd-714">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-714">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="240bd-716">Parancsmagok frissítve választható paraméterekkel -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="240bd-717">Az ESP és AH protokollok támogatása a hálózati biztonsági szabályzati konfigurációkban</span><span class="sxs-lookup"><span data-stu-id="240bd-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="240bd-718">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="240bd-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="240bd-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="240bd-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="240bd-722">Tovább javult a Cortex-parancsmagok kivételeinek kezelése</span><span class="sxs-lookup"><span data-stu-id="240bd-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="240bd-723">A VirtualNetworkGateways új generációi és termékváltozatai</span><span class="sxs-lookup"><span data-stu-id="240bd-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="240bd-724">A VirtualNetworkGateways új generációinak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="240bd-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="240bd-725">A VirtualNetworkGateways új, nagy átviteli sebességű termékváltozatainak bevezetése.</span><span class="sxs-lookup"><span data-stu-id="240bd-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="240bd-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="240bd-726">Az.RedisCache</span></span>
* <span data-ttu-id="240bd-727">Frissült a Set-AzRedisCache referenciadokumentációja, amely most már tartalmazza a -Size paraméter hiányzó értékeit.</span><span class="sxs-lookup"><span data-stu-id="240bd-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-728">Az.Sql</span></span>
* <span data-ttu-id="240bd-729">Az Active Directory-rendszergazda a felügyelt példányon való beállításának támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-730">Az.Storage</span></span>
* <span data-ttu-id="240bd-731">Az Storage-ügyfélkódtár a 11.1.0-s verzióra frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="240bd-732">A Management plane API-val rendelkező tárolók listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="240bd-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="240bd-733">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="240bd-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="240bd-734">A tárfiókok előfizetésből történő listázása a NextPageLink segítségével fog történni</span><span class="sxs-lookup"><span data-stu-id="240bd-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="240bd-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="240bd-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="240bd-736">Az.StorageSync</span></span>
* <span data-ttu-id="240bd-737">A Reset-AzStorageSyncServerCertificate 9810-es hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="240bd-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-738">Az.Websites</span></span>
* <span data-ttu-id="240bd-739">Egy alkalmazáshoz tartozó ASP Set-AzWebApp általi frissítése sikertelen volt</span><span class="sxs-lookup"><span data-stu-id="240bd-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="240bd-740">2.7.0 – 2019. szeptember</span><span class="sxs-lookup"><span data-stu-id="240bd-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="240bd-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-741">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-742">Frissítve lett a „-Format” paraméter leírása a „Set-AzApiManagementPolicy” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="240bd-743">El lettek távolítva az elavult „Update-AzApiManagementDeployment” parancsmag referenciái a referenciadokumentációból.</span><span class="sxs-lookup"><span data-stu-id="240bd-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="240bd-744">A „Set-AzApiManagement” használható helyette.</span><span class="sxs-lookup"><span data-stu-id="240bd-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-745">Az.Automation</span></span>
* <span data-ttu-id="240bd-746">Ki lett javítva a „Register-AzAutomationDscNode” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="240bd-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="240bd-747">Hozzá lett adva az operációs rendszerrel kapcsolatos korlátozások pontosítása a Register-AzAutomationDSCNode parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="240bd-748">Ki lett javítva a Start-AzAutomationRunbook parancsmag null értékű hivatkozás okozta kivétele a -Wait paraméter esetén.</span><span class="sxs-lookup"><span data-stu-id="240bd-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-749">Az.Compute</span></span>
* <span data-ttu-id="240bd-750">Hozzá lett adva az UploadSizeInBytes paraméter a New-AzDiskConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="240bd-751">Hozzá lett adva az Incremental paraméter a New-AzSnapshotConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="240bd-752">Alacsony prioritású virtuálisgép-funkció hozzáadása:</span><span class="sxs-lookup"><span data-stu-id="240bd-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="240bd-753">Hozzá lett adva a MaxPrice, az EvictionPolicy és a Priority paraméter a New-AzVMConfig parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="240bd-754">Hozzá lett adva a MaxPrice paraméter a New-AzVmssConfig, az Update-AzVM és az Update-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="240bd-755">Ki lett javítva a Get-AzAvailabilitySet parancsmag virtuálisgép-hivatkozással kapcsolatos hibája, amely miatt a parancsmag az előfizetésben található összes rendelkezésreállási csoportot listázta.</span><span class="sxs-lookup"><span data-stu-id="240bd-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="240bd-756">Ki lett javítva a Get-AzRemoteDesktopFile parancsmag esetében jelentkező null kivétel.</span><span class="sxs-lookup"><span data-stu-id="240bd-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="240bd-757">Ki lett javítva virtuális merevlemezek Seek metódusa a végrelatív pozíció esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="240bd-758">Ki lett javítva az UltraSSD hibája a New-AzVM és az Update-AzVM parancsmagok esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-759">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-760">Hozzá lett adva 3 új parancs (az Add-AzDataFactoryV2TriggerSubscription, a Remove-AzDataFactoryV2TriggerSubscription és a Get-AzDataFactoryV2TriggerSubscriptionStatus) az ADF V2-höz</span><span class="sxs-lookup"><span data-stu-id="240bd-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="240bd-761">Az ADF .Net SDK a 4.1.3-as verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="240bd-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-762">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-763">Kompatibilitástörő változások a meghívással kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="240bd-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-764">Az.IotHub</span></span>
* <span data-ttu-id="240bd-765">Hozzá lett adva az IoTHubok földrajzilag párosított vészhelyreállítási régiójába történő feladatátvétel meghívásának támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="240bd-766">Hozzá lett adva az IoTHubok üzenetbővítés-kezelésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="240bd-767">Az új parancsmagok a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-767">New cmdlets are:</span></span>
    - <span data-ttu-id="240bd-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="240bd-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="240bd-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="240bd-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="240bd-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="240bd-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="240bd-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="240bd-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-772">Az.Monitor</span></span>
* <span data-ttu-id="240bd-773">A legújabb Monitor SDK-ra mutat, azaz a 0.24.1-preview verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="240bd-774">Nem kompatibilitástörő változásokkal bővíti a Metrics parancsmagokat, így az egységek számbavétele számos új értéket támogat.</span><span class="sxs-lookup"><span data-stu-id="240bd-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="240bd-775">Ezek írásvédett parancsmagok, ezért a parancsmagok bemenetében nem történik változás.</span><span class="sxs-lookup"><span data-stu-id="240bd-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="240bd-776">Az **ActionGroups**-kérések api-version értéke mostantól **2019-06-01**, korábban **2018-03-01** volt.</span><span class="sxs-lookup"><span data-stu-id="240bd-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="240bd-777">A forgatókönyvtesztek frissültek, így igazodnak a változáshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="240bd-778">Az **EmailReceiver** és a **WebhookReceiver** osztályok konstruktoraihoz hozzá lett adva egy új kötelező argumentum, a **useCommonAlertSchema** nevű logikai érték.</span><span class="sxs-lookup"><span data-stu-id="240bd-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="240bd-779">A kompatibilitástörő változás parancsmagok elől való elrejtése érdekében a rögzített érték jelenleg a **false** (hamis).</span><span class="sxs-lookup"><span data-stu-id="240bd-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="240bd-780">**MEGJEGYZÉS**: Ez egy átmeneti módosítás, amelyet a Riasztások csapatnak érvényesítenie kell.</span><span class="sxs-lookup"><span data-stu-id="240bd-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="240bd-781">A **Source** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="240bd-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="240bd-782">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="240bd-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="240bd-783">Az **AlertingAction** osztály (amely a **ScheduledQueryRuleSource** osztályhoz kapcsolódik) konstruktorai argumentumainak sorrendje módosult az előző SDK-hoz képest.</span><span class="sxs-lookup"><span data-stu-id="240bd-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="240bd-784">Ehhez a módosításhoz két egységteszt kijavítására volt szükség: azokat le lehetett fordítani, azonban nem teljesítették a teszteket.</span><span class="sxs-lookup"><span data-stu-id="240bd-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="240bd-785">A dinamikus küszöbérték kritériumainak támogatása a 2-es verziójú metrikariasztás esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="240bd-786">New-AzMetricAlertRuleV2Criteria: mostantól a dinamikus küszöbértékek kritériumait is létrehozza</span><span class="sxs-lookup"><span data-stu-id="240bd-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="240bd-787">Add-AzMetricAlertRuleV2: mostantól a dinamikus küszöbértékek kritériumait is elfogadja</span><span class="sxs-lookup"><span data-stu-id="240bd-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="240bd-788">Az ütemezett lekérdezési szabályok parancsmagjainak (SQR) fejlesztései</span><span class="sxs-lookup"><span data-stu-id="240bd-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="240bd-789">A parancsmagok a „Location” paraméter mindkét formátumát elfogadják: a helyet (például eastus) és a hely megjelenített nevét is (például USA keleti régiója)</span><span class="sxs-lookup"><span data-stu-id="240bd-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="240bd-790">Megfelelően ábrázolva lett az „Enabled” paraméter a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="240bd-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="240bd-791">Példák lettek hozzáadva az „ActionGroup” opcionális paraméterhez</span><span class="sxs-lookup"><span data-stu-id="240bd-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="240bd-792">Általánosan továbbfejlesztett súgófájlok</span><span class="sxs-lookup"><span data-stu-id="240bd-792">Overall improved help files</span></span>
* <span data-ttu-id="240bd-793">Ki lett javítva a „Set-AzActionRule” hatókörtípusának meghatározásával kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="240bd-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-794">Az.Network</span></span>
* <span data-ttu-id="240bd-795">Ki lett javítva a „New-AzApplicationGateway” referenciadokumentációjában található helytelen példa</span><span class="sxs-lookup"><span data-stu-id="240bd-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="240bd-796">Hozzá lett adva egy csomagrögzítés összes tulajdonságának lekérésével kapcsolatos megjegyzés a „Get-AzNetworkWatcherPacketCapture” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="240bd-797">Ki lett javítva a „Test-AzNetworkWatcherIPFlow” referenciadokumentációjában található példa a hálózati adapterek megfelelő számbavétele érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="240bd-798">Tovább lett fejlesztve a felhőkivétel-elemzés az esetleges további részletek megjelenítése érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="240bd-799">Tovább lett fejlesztve a felhőkivétel-elemzés az SDK-kivételek további típusainak kezelése érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="240bd-800">Ki lett javítva a biztonságiszabály-modellek helytelen leképezése</span><span class="sxs-lookup"><span data-stu-id="240bd-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="240bd-801">Hozzá lettek adva a privát IP-cím funkcióval kapcsolatos tulajdonságok a hálózati adapterhez</span><span class="sxs-lookup"><span data-stu-id="240bd-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="240bd-802">Hozzá lett adva a „PrivateEndpoint” tulajdonság PSResourceId típusúként a PSNetworkInterface osztályhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="240bd-803">Hozzá lett adva a „PrivateLinkConnectionProperties” tulajdonság PSIpConfigurationConnectivityInformation típusúként a PSNetworkInterfaceIPConfiguration osztályhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="240bd-804">Hozzá lett adva a PSIpConfigurationConnectivityInformation nevű új modellosztály</span><span class="sxs-lookup"><span data-stu-id="240bd-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="240bd-805">Hozzá lett adva az új ApplicationRuleProtocolType „mssql” az Azure Firewall-erőforráshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="240bd-806">MultiLink-támogatás a Virtuális WAN-ben</span><span class="sxs-lookup"><span data-stu-id="240bd-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="240bd-807">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-807">New cmdlets</span></span>
        - <span data-ttu-id="240bd-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="240bd-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="240bd-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="240bd-810">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="240bd-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="240bd-811">New-VpnSite</span></span>
        - <span data-ttu-id="240bd-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="240bd-812">Update-VpnSite</span></span>
        - <span data-ttu-id="240bd-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-813">New-VpnConnection</span></span>
        - <span data-ttu-id="240bd-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-814">Update-VpnConnection</span></span>
* <span data-ttu-id="240bd-815">Ki lettek javítva bizonyos PowerShell-példák dokumentumai, hogy az AzureRM-parancsmagok helyett az Az-parancsmagokat használják</span><span class="sxs-lookup"><span data-stu-id="240bd-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-817">Frissítve lett az AzureVMpolicy objektum a ProtectedItemsCount attribútummal</span><span class="sxs-lookup"><span data-stu-id="240bd-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="240bd-818">Tesztek lettek hozzáadva a virtuális gép szabályzatához és az eredeti Storage-fiók visszaállításához</span><span class="sxs-lookup"><span data-stu-id="240bd-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-819">Az.Resources</span></span>
* <span data-ttu-id="240bd-820">Ki lett javítva a hiba, amely miatt a New-AzRoleAssignment parancsot nem lehetett meghívni a Scope paraméter nélkül.</span><span class="sxs-lookup"><span data-stu-id="240bd-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-822">Ki lett javítva az „Update-AzServiceFabricReliability” referenciadokumentációjának példájában található elgépelés</span><span class="sxs-lookup"><span data-stu-id="240bd-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="240bd-823">Új parancsmagok lettek hozzáadva az alkalmazás és a szolgáltatások felügyeletéhez:</span><span class="sxs-lookup"><span data-stu-id="240bd-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="240bd-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="240bd-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="240bd-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="240bd-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="240bd-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="240bd-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="240bd-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="240bd-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="240bd-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="240bd-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="240bd-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="240bd-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="240bd-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="240bd-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="240bd-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="240bd-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="240bd-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="240bd-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="240bd-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="240bd-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="240bd-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="240bd-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="240bd-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="240bd-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="240bd-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="240bd-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="240bd-837">A Service Fabric SDK az 1.2.0-s verzióra frissült, amely a Service Fabric erőforrás-szolgáltató 2019-03-01 api-versionjét használja.</span><span class="sxs-lookup"><span data-stu-id="240bd-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="240bd-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="240bd-838">Az.SignalR</span></span>
* <span data-ttu-id="240bd-839">Hozzá lettek adva az Update, Restart, CheckNameAvailability és GetUsage parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-840">Az.Sql</span></span>
* <span data-ttu-id="240bd-841">Frissítve lett a „Get-AzSqlElasticPool” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="240bd-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="240bd-842">Hozzá lett adva egy rugalmas készlet létrehozását bemutató virtuálismag-példa (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="240bd-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="240bd-843">El lett távolítva az EmailAddresses érvényesítése és annak ellenőrzése, hogy az EmailAdmins értéke hamis-e abban az esetben, ha az EmailAddresses üres a Set-AzSqlServerAdvancedThreatProtectionPolicy és a Set-AzSqlDatabaseAdvancedThreatProtectionPolicy parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="240bd-844">Engedélyezve lettek a kiszolgáló-/adatbázis-naplózási beállítások abban az esetben, ha több olyan diagnosztikai beállítás létezik, amelyek engedélyezik a naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="240bd-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="240bd-845">Ki lett javítva az e-mail-címek ellenőrzése több, SQL-sebezhetőségi felméréshez használt parancsmagban (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting és Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="240bd-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-846">Az.Storage</span></span>
* <span data-ttu-id="240bd-847">Frissítve lett a „Get-AzStorageAccountKey” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="240bd-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="240bd-848">A forrásfájl SMB-tulajdonságai (fájlattribútumok, fájl létrehozásának ideje, fájl utolsó írásának ideje) célfájlban történő megtartásának támogatása az Azure File-beli feltöltés/letöltés esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="240bd-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="240bd-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="240bd-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="240bd-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="240bd-851">Ki lett javítva a tulajdonság-/metaadathibával meghiúsuló blokkblobfeltöltés a tárolóképes ImmutabilityPolicy esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="240bd-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="240bd-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="240bd-853">Az Azure File-megosztások Management plane API-val történő kezelésének támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="240bd-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="240bd-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="240bd-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="240bd-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="240bd-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-858">Az.Websites</span></span>
* <span data-ttu-id="240bd-859">Ki lett javítva az a probléma, amely miatt a webalkalmazás Címkéi törölve lettek az alkalmazás új ASP-be történő migrálásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="240bd-860">Ki lett javítva a Publish-AzureWebapp parancs a Linux és Windows rendszeren történő működés érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="240bd-861">Frissítve lett a „Get-AzWebAppPublishingProfile” referenciadokumentációjában található példa</span><span class="sxs-lookup"><span data-stu-id="240bd-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="240bd-862">2.6.0 – 2019. augusztus</span><span class="sxs-lookup"><span data-stu-id="240bd-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="240bd-863">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-863">General</span></span>
* <span data-ttu-id="240bd-864">Különféle elgépelések kijavítva több modulban</span><span class="sxs-lookup"><span data-stu-id="240bd-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-865">Az.Accounts</span></span>
* <span data-ttu-id="240bd-866">Felhasználó által hozzárendelt MSI támogatása az Azure Functions-hitelesítésben (#9479)</span><span class="sxs-lookup"><span data-stu-id="240bd-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="240bd-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="240bd-867">Az.Aks</span></span>
* <span data-ttu-id="240bd-868">A Get-AzAks kimenetével kapcsolatos probléma ki lett javítva</span><span class="sxs-lookup"><span data-stu-id="240bd-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="240bd-869">További információ: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="240bd-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="240bd-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-870">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-871">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="240bd-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="240bd-872">Frissült a .net nuget verziója, amely nem kényszeríti ki a productId, az apiId, a groupId és a userId korlátozásait</span><span class="sxs-lookup"><span data-stu-id="240bd-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="240bd-873">**Get-AzApiManagementProduct** – A termékek API-val történő lekérdezése mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="240bd-874">**New-AzApiManagementApiRevision** – Ki lett javítva az a probléma, amely miatt az ApiRevisionDescription nem lett beállítva az új API-változat létrehozásakor https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="240bd-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="240bd-875">Ki lett javítva a PsApiManagementOAuth2AuthrozationServer modell elírása PsApiManagementOAuth2AuthorizationServer értékre</span><span class="sxs-lookup"><span data-stu-id="240bd-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="240bd-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-876">Az.Batch</span></span>
* <span data-ttu-id="240bd-877">Ki lett javítva a súgóüzenetben és a dokumentációban található elgépelés, nagy kezdőbetűs Windows értékre</span><span class="sxs-lookup"><span data-stu-id="240bd-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-878">Az.Cdn</span></span>
* <span data-ttu-id="240bd-879">Ki lett javítva egy elgépelés CDN modulátalakító segédben</span><span class="sxs-lookup"><span data-stu-id="240bd-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-880">Az.Compute</span></span>
* <span data-ttu-id="240bd-881">Új VmssId a New-AzVMConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="240bd-882">Új TerminateScheduledEvents és a TerminateScheduledEventNotBeforeTimeoutInMinutes paraméterek a New-AzVmssConfig és az Update-AzVmss parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="240bd-883">Új HyperVGeneration tulajdonság a VM-rendszerképobjektumhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="240bd-884">Új Host és HostGroup jellemzők</span><span class="sxs-lookup"><span data-stu-id="240bd-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="240bd-885">Új parancsmagok:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="240bd-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="240bd-886">Új HostId paraméter a New-AzVMConfig és a New-AzVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="240bd-887">Az Invoke-AzVMRunCommand dokumentációjában található példa frissítve lett a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="240bd-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="240bd-888">A -VolumeType leírása frissítve lett a set-AzVMDiskEncryptionExtension és a set-AzVmssDiskEncryptionExtension referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-889">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-890">A New-AzDataFactoryEncryptValue dokumentációjában a Windows szó nagy kezdőbetűsre lett javítva</span><span class="sxs-lookup"><span data-stu-id="240bd-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="240bd-891">Az ADF .Net SDK a 4.1.2-es verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="240bd-892">Új DataProxyIntegrationRuntimeName, DataProxyIntegrationRuntimeName és DataProxyStagingPath paraméterek lettek hozzáadva a Set-AzureRmDataFactoryV2IntegrationRuntime parancsmaghoz, lehetővé téve a helyi integrációs modul SSIS integrációs modul proxyjaként való beállítását</span><span class="sxs-lookup"><span data-stu-id="240bd-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="240bd-893">Frissítve lett a PSTriggerRun, hogy megjelenítse az aktivált folyamatokat, üzeneteket és tulajdonságokat, illetve a PSActivityRun, hogy megjelenítse a tevékenységtípust</span><span class="sxs-lookup"><span data-stu-id="240bd-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-895">Ki lett javítva a Get-DataLakeStoreDeletedItem lefagyása hibák vagy távoli kivételek esetén.</span><span class="sxs-lookup"><span data-stu-id="240bd-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-896">Az.EventHub</span></span>
* <span data-ttu-id="240bd-897">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNteworkRule paraméter a Set-AzEventHubNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="240bd-898">Ki lett javítva a 9558-as számú hiba: Set-AzEventHubNamespace a PUT helyett a PATCH kérést használta</span><span class="sxs-lookup"><span data-stu-id="240bd-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="240bd-899">új EnableKafka paraméter a Set-AzEventHubNamespace parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="240bd-900">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="240bd-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="240bd-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="240bd-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="240bd-902">Ki lett javítva egy elgépelés a dokumentációban, ahol az Azure csupa kisbetűvel szerepelt</span><span class="sxs-lookup"><span data-stu-id="240bd-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-903">Az.Monitor</span></span>
* <span data-ttu-id="240bd-904">Hibás paraméternév lett kijavítva a súgódokumentációban</span><span class="sxs-lookup"><span data-stu-id="240bd-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-905">Az.Network</span></span>
* <span data-ttu-id="240bd-906">Frissítve lett a New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="240bd-907">A PublicIpAddress elavult, mert a kiszolgálóoldalon nem használatos.</span><span class="sxs-lookup"><span data-stu-id="240bd-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="240bd-908">Hozzá lett adva egy opcionális Primary paraméter, amely azt jelzi, hogy a jelenlegi IP-konfiguráció elsődleges-e.</span><span class="sxs-lookup"><span data-stu-id="240bd-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="240bd-909">Javítva lett az SDK kérelemhiba-kivételének kezelése – kijavítja azt a problémát, amely miatt az SDK-kivételek kezelése korábban nem volt megfelelő, és a fontos hibarészletek nem jelentek meg</span><span class="sxs-lookup"><span data-stu-id="240bd-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="240bd-910">Be lett állítva, hogy az IPv6 IP-előtag ellenőrzési logikája ellenőrizze az IPv6-előtag hosszának megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="240bd-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="240bd-911">Frissült a Get-AzVirtualNetworkSubnetConfig: Új paraméterkészlet lett hozzáadva az alhálózat erőforrás-azonosítója szerinti lekéréshez.</span><span class="sxs-lookup"><span data-stu-id="240bd-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="240bd-912">Frissült az AzNetworkServiceTag Location paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="240bd-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-914">Frissült a New-AzOperationalInsightsLinuxSyslogDataSource dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="240bd-915">Példa hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-915">Added example</span></span>
    - <span data-ttu-id="240bd-916">A -Name paraméter leírása frissítve lett</span><span class="sxs-lookup"><span data-stu-id="240bd-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="240bd-917">Új példa lett hozzáadva a New-AzOperationalInsightsWindowsEventDataSource parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="240bd-918">Módosult a New-AzOperationalInsightsWindowsEventDataSource -Name paraméterének leírása</span><span class="sxs-lookup"><span data-stu-id="240bd-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-920">Frissült a Get-AzRecoveryServicesBackupJob.md</span><span class="sxs-lookup"><span data-stu-id="240bd-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-921">Az.Resources</span></span>
* <span data-ttu-id="240bd-922">A Microsoft.Resource mostantól támogatja a 2019-05-10-es új api-verziót</span><span class="sxs-lookup"><span data-stu-id="240bd-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="240bd-923">Mostantól támogatott a copy.count = 0 a változók, erőforrások és tulajdonságok esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="240bd-924">A condition = false vagy copy.count = 0 tulajdonságú erőforrások teljes módban törölve lesznek</span><span class="sxs-lookup"><span data-stu-id="240bd-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="240bd-925">A súgódokumentációhoz hozzá lett adva egy példa a szabályzatok előfizetési szinten történő hozzárendeléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-926">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-927">Ki lett javítva a 9658-as számú hiba: Elgépelt VirtualNetworkRule paraméter a Set-AzServiceBusNetworkRuleSet parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="240bd-928">Ki lett javítva a 9786-os számú hiba: nem lehetett csak figyelési jogokkal ellátott szabályt létrehozni</span><span class="sxs-lookup"><span data-stu-id="240bd-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="240bd-929">Új Test-AzServiceBusNameAvailability parancs lett hozzáadva annak ellenőrzésére, hogy az üzenetsor és a témakör neve elérhető-e</span><span class="sxs-lookup"><span data-stu-id="240bd-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-931">Ki lettek javítva a csomóponttípus-hozzáadási parancsmag hibái:</span><span class="sxs-lookup"><span data-stu-id="240bd-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="240bd-932">NullReferenceException hiba történt, ha az erőforráscsoport más, a Service Fabric-fürthöz nem kapcsolódó VMSS-sel rendelkezett.</span><span class="sxs-lookup"><span data-stu-id="240bd-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="240bd-933">Kijavított hiba: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="240bd-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="240bd-934">Ki lett javítva egy hiba, amely miatt a parancsmag futása meghiúsult, ha a virtualNetwork a fürttől eltérő erőforráscsoportban volt.</span><span class="sxs-lookup"><span data-stu-id="240bd-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="240bd-935">kijavított hiba: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="240bd-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="240bd-936">Az Add-AzServiceFabricApplicationCertificate parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="240bd-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-937">Az.Sql</span></span>
* <span data-ttu-id="240bd-938">Frissült a régi naplózási parancsmagok dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="240bd-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-939">Az.Storage</span></span>
* <span data-ttu-id="240bd-940">A Get/Close-AzStorageFileHandle súgója további parancsmagpélda-forgatókönyvek hozzáadásával és a paraméterek leírásának frissítésével változott</span><span class="sxs-lookup"><span data-stu-id="240bd-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="240bd-941">A StandardBlobTier mostantól támogatott a blobfeltöltési és -másolási műveletekhez</span><span class="sxs-lookup"><span data-stu-id="240bd-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="240bd-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="240bd-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="240bd-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="240bd-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="240bd-944">A rehidratálás prioritása mostantól támogatott a blobmásoláskor</span><span class="sxs-lookup"><span data-stu-id="240bd-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="240bd-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="240bd-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-946">Az.Websites</span></span>
* <span data-ttu-id="240bd-947">Magyarázat hozzáadva a Set-AzWebApp és a Set-AzWebAppSlot parancsmagok -AppSettings paraméteréhez</span><span class="sxs-lookup"><span data-stu-id="240bd-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="240bd-948">2.5.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="240bd-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-949">Az.Accounts</span></span>
* <span data-ttu-id="240bd-950">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="240bd-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="240bd-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="240bd-952">A Remove-AzApplicationInsightsApiKey dokumentáció példájában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-953">Az.Automation</span></span>
* <span data-ttu-id="240bd-954">Az erőforrássztringben található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-956">NetworkRuleSet támogatás hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="240bd-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-957">Az.Compute</span></span>
* <span data-ttu-id="240bd-958">A virtuálisgép-példány nézetobjektumaiból hiányzó tulajdonságok (ComputerName, OsName, OsVersion és HyperVGeneration) hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="240bd-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="240bd-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="240bd-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="240bd-960">A Remove-AzContainerRegistryReplication Replikáció paraméterében lévő elírás javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="240bd-961">További információ: https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="240bd-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-962">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-963">Az ADF .Net SDK a 4.1.0-s verzióra frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="240bd-964">A Get-AzDataFactoryV2PipelineRun dokumentációjában található elírás javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-965">Az.EventHub</span></span>
* <span data-ttu-id="240bd-966">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="240bd-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="240bd-967">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="240bd-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-968">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-969">A KeySize tanúsítványszabályzatokhoz történő meghatározásának támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="240bd-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="240bd-970">Az.LogicApp</span></span>
* <span data-ttu-id="240bd-971">A Get-AzIntegrationAccountMap javítása, hogy minden leképezéstípust listázzon</span><span class="sxs-lookup"><span data-stu-id="240bd-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="240bd-972">Új MapType paraméter hozzáadva a szűréshez</span><span class="sxs-lookup"><span data-stu-id="240bd-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="240bd-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="240bd-973">Az.ManagedServices</span></span>
* <span data-ttu-id="240bd-974">Az API 2019. 06. 01-én kiadott (GA) verziójának támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-975">Az.Network</span></span>
* <span data-ttu-id="240bd-976">A privát végpont és privát kapcsolatszolgáltatás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="240bd-977">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-977">New cmdlets</span></span>
        - <span data-ttu-id="240bd-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="240bd-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="240bd-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="240bd-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="240bd-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="240bd-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="240bd-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="240bd-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="240bd-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="240bd-986">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies jelző a VirtualNetwork alhálózatban</span><span class="sxs-lookup"><span data-stu-id="240bd-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="240bd-987">New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig frissítve</span><span class="sxs-lookup"><span data-stu-id="240bd-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="240bd-988">Hozzá lett adva a -PrivateEndpointNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát végpont esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="240bd-989">Hozzá lett adva a -PrivateLinkServiceNetworkPoliciesFlag opcionális paraméter, amely azt konfigurálja, hogy legyenek-e alkalmazva hálózati szabályzatok az ezen az alhálózaton található privát kapcsolati szolgáltatás esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="240bd-990">Az AzPrivateLinkService parancsmag ServiceName paramétere átnevezve a Name névre a ServiceName aliasszal a visszamenőleges kompatibilitás érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="240bd-991">ICMP-protokoll engedélyezése a hálózati biztonsági szabályzati konfigurációkhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="240bd-992">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-992">Updated cmdlets</span></span>
        - <span data-ttu-id="240bd-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="240bd-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="240bd-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="240bd-996">A ConnectionProtocolType (Ikev1/Ikev2) hozzáadva a New-AzVirtualNetworkGatewayConnection konfigurálható paramétereként</span><span class="sxs-lookup"><span data-stu-id="240bd-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="240bd-997">PrivateIpAddressVersion hozzáadva a LoadBalancerFrontendIpConfigurationhöz</span><span class="sxs-lookup"><span data-stu-id="240bd-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="240bd-998">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="240bd-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="240bd-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="240bd-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="240bd-1002">Application Gateway New-AzApplicationGatewayProbeConfig parancs frissítése a mintavétel egyéni portjának támogatásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="240bd-1003">Frissített New-AzApplicationGatewayProbeConfig: A Port opcionális paraméter hozzáadva, amelyet a rendszer a háttérrendszer-kiszolgáló mintavételére használ.</span><span class="sxs-lookup"><span data-stu-id="240bd-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="240bd-1004">Ez a paraméter a Standard_V2 és WAF_V2 termékváltozatokban használható.</span><span class="sxs-lookup"><span data-stu-id="240bd-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-1006">A mentett keresések alapértelmezett verziója 1 értékre frissítve.</span><span class="sxs-lookup"><span data-stu-id="240bd-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="240bd-1007">Null reguláris kifejezések kezelése javítva az egyéni naplókban</span><span class="sxs-lookup"><span data-stu-id="240bd-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1009">A Get-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="240bd-1010">A Get-AzRecoveryServicesBackupContainer.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="240bd-1011">A Get-AzRecoveryServicesVault.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="240bd-1012">A Wait-AzRecoveryServicesBackupJob.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="240bd-1013">A Set-AzRecoveryServicesVaultContext.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="240bd-1014">A Get-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="240bd-1015">A Get-AzRecoveryServicesBackupRecoveryPoint.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="240bd-1016">A Restore-AzRecoveryServicesBackupItem.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="240bd-1017">A tároló Azure-fájlmegosztásban való regisztrációjának törlésére szolgáló szolgáltatáshívás frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="240bd-1018">A Set-AzRecoveryServicesAsrAlertSetting.md frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1019">Az.Resources</span></span>
- <span data-ttu-id="240bd-1020">A New-AzResourceGroupDeployment dokumentációban hivatkozott hiányzó parancsmag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="240bd-1021">A szabályzat parancsmagjai frissítve a 2019. 01. 01. dátumú új API-verzió használatára</span><span class="sxs-lookup"><span data-stu-id="240bd-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-1023">Új parancsmag hozzáadva az SAS-token létrehozásához: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="240bd-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="240bd-1024">ellenőrző- és hibaüzenet hozzáadva az engedélyezési szabályok jogosultságaihoz, ha csak a Manage érték van hozzárendelve</span><span class="sxs-lookup"><span data-stu-id="240bd-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1025">Az.Sql</span></span>
* <span data-ttu-id="240bd-1026">A Set-AzSqlDatabaseSecondary parancsmag hiányzó példáinak javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="240bd-1027">A biztonságirés-felmérés e-mail-cím megadása nélkül beállított ismétlődő vizsgálatának javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="240bd-1028">Egy kis elírás javítása egy figyelmeztető üzenetben.</span><span class="sxs-lookup"><span data-stu-id="240bd-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1029">Az.Storage</span></span>
* <span data-ttu-id="240bd-1030">A Get-AzStorageAccount hivatkozási dokumentációjában található példa frissítése a helyes paraméternév használatára</span><span class="sxs-lookup"><span data-stu-id="240bd-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="240bd-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="240bd-1031">Az.StorageSync</span></span>
* <span data-ttu-id="240bd-1032">Az Invoke-AzStorageSyncChangeDetection parancsmag hozzáadása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="240bd-1033">A 9551-es hiba javítása a TierFilesOlderThanDays betartásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1034">Az.Websites</span></span>
* <span data-ttu-id="240bd-1035">A hiba elhárítása, amely miatt a Get-AzWebApp és a Set-AzWebApp nem adott vissza egyes SiteConfig tulajdonságokat</span><span class="sxs-lookup"><span data-stu-id="240bd-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="240bd-1036">Egy új Location paraméter hozzáadása a Get-AzDeletedWebApp és a Restore-AzDeletedWebApp parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="240bd-1037">A webalkalmazás-tárhelyek New-AzWebApp -IncludeSourceWebAppSlots használatával történő klónozásakor jelentkező hiba javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="240bd-1038">2.4.0 – 2019. július</span><span class="sxs-lookup"><span data-stu-id="240bd-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1039">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1040">Profilparancsmagok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="240bd-1041">A létrehozott parancsmagokban lévő környezetek és adatsíkok támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="240bd-1042">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen végpontot használt az adatsík parancsmagjaihoz Windows PowerShellben</span><span class="sxs-lookup"><span data-stu-id="240bd-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="240bd-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="240bd-1043">Az.Advisor</span></span>
* <span data-ttu-id="240bd-1044">Az Az.Advisor GA-kiadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="240bd-1045">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="240bd-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="240bd-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-1047">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="240bd-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="240bd-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="240bd-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="240bd-1049">Előfizetések felhasználó és termék szerinti lekérdezésének támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="240bd-1050">„/”, „/apis”, „/apis/echo-api” hatókör használatával történő lekérdezés támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="240bd-1051">A következő hibák ki lettek javítva: https://github.com/Azure/azure-powershell/issues/9307 és https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="240bd-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="240bd-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="240bd-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="240bd-1053">Az „ApiVersion” és az „ApiVersionSetId” megadhatóvá vált az API-k importálásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1054">Az.Automation</span></span>
* <span data-ttu-id="240bd-1055">A Set-AzAutomationConnectionFieldValue parancsmag sztringértékek kezelése esetén fellépő hibája javítva lett.</span><span class="sxs-lookup"><span data-stu-id="240bd-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1056">Az.Compute</span></span>
* <span data-ttu-id="240bd-1057">A HyperVGeneration paraméter hozzáadása a New-AzImageConfig parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-1058">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-1059">A tevékenység-, folyamat- és eseményindító-futtatási kimenetek lekérdezési ADF-parancsmagjainak frissítése a Select-Object folyamat támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="240bd-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="240bd-1060">Az.EventGrid</span></span>
* <span data-ttu-id="240bd-1061">Az elgépelés ki lett javítva a New-AzEventGridSubscription dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1062">Az.IotHub</span></span>
* <span data-ttu-id="240bd-1063">Az engedélyezési szabályzati kulcsok újragenerálásának támogatása hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1064">Az.Network</span></span>
* <span data-ttu-id="240bd-1065">A „RoutingPreference” hozzáadva a nyilvános IP-címkékhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="240bd-1066">Javítottuk a példákat a „Get-AzNetworkServiceTag” referenciadokumentációban</span><span class="sxs-lookup"><span data-stu-id="240bd-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="240bd-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="240bd-1068">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyState parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="240bd-1069">További információ: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="240bd-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-1071">Javítottuk a Get-AzOperationalInsightsDataSource parancsmagban visszaadott CustomLog adatforrásmodellt</span><span class="sxs-lookup"><span data-stu-id="240bd-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1073">Az IaaSVMs get-policy parancsának javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1074">Az.Resources</span></span>
    - <span data-ttu-id="240bd-1075">A Get-AzPolicyState -Top paraméter súgószövegének javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="240bd-1076">Ügyféloldali lapozás támogatásának hozzáadása a Get-AzPolicyAlias parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="240bd-1077">Új (-PolicyParameters és -PolicyParametersObject) paraméterek hozzáadása a Set-AzPolicyAssignment parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="240bd-1078">A Policy-parancsmagok néhány dokumentumának és példájának frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-1080">A 4938-as hiba javítása – A New-AzureRmServiceBusQueue parancsmag BadRequest értéket ad vissza a MaxSizeInMegabytes megadásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1081">Az.Sql</span></span>
* <span data-ttu-id="240bd-1082">A példány-feladatátvételi csoportok parancsmagjainak hozzáadása az előzetes kiadásból a nyilvános kiadáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="240bd-1083">Az Azure SQL Server\Database Auditing támogatása új parancsmagokkal.</span><span class="sxs-lookup"><span data-stu-id="240bd-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="240bd-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="240bd-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="240bd-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="240bd-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="240bd-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="240bd-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="240bd-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="240bd-1090">E-mailes korlátozások eltávolítása a sebezhetőségi felmérés beállításaiból</span><span class="sxs-lookup"><span data-stu-id="240bd-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1091">Az.Storage</span></span>
* <span data-ttu-id="240bd-1092">Az „-IndexDocument” és „-ErrorDocument404Path” paraméter módosítása kötelezőről opcionálisra a következő parancsmagban:</span><span class="sxs-lookup"><span data-stu-id="240bd-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="240bd-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="240bd-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="240bd-1094">A Get-AzStorageBlobContent súgójának frissítése egy példa hozzáadásával</span><span class="sxs-lookup"><span data-stu-id="240bd-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="240bd-1095">További hibaadatok megjelenítése, ha a parancsmag futtatása StorageException miatt meghiúsul</span><span class="sxs-lookup"><span data-stu-id="240bd-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="240bd-1096">Storage-fiók létrehozásának és frissítésének támogatása Azure Files AAD DS-hitelesítéssel</span><span class="sxs-lookup"><span data-stu-id="240bd-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="240bd-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="240bd-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="240bd-1099">Támogatás a fájlmegosztások, fájlkönyvtárak vagy fájlok fájlleíróinak listázásához vagy bezárásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="240bd-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="240bd-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="240bd-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="240bd-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="240bd-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="240bd-1102">Az.StorageSync</span></span>
* <span data-ttu-id="240bd-1103">Ez a modul most már része az összesített `Az` modulnak</span><span class="sxs-lookup"><span data-stu-id="240bd-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="240bd-1104">2.3.2 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="240bd-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1105">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1106">Javítva lett a hiba, amely miatt a rendszer egyes esetekben helytelen URL-címeket használt a Functions-hívásokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="240bd-1107">További információ: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="240bd-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="240bd-1108">Javítva lett az aliasok hibája az AzureRM–Az parancsmagok közötti átvitel esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="240bd-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="240bd-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="240bd-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="240bd-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1111">Az.Compute</span></span>
* <span data-ttu-id="240bd-1112">A „New-AzVm” és „New-AzVmss” egyszerű paraméterkészletek mostantól elfogadják a „ProximityPlacementGroup” paramétert.</span><span class="sxs-lookup"><span data-stu-id="240bd-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="240bd-1113">Az elgépelés ki lett javítva a „New-AzVM” referenciadokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="240bd-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="240bd-1114">Az.Dns</span></span>
* <span data-ttu-id="240bd-1115">Az elgépelés ki lett javítva a „Set-AzDnsZone” súgópéldáinál.</span><span class="sxs-lookup"><span data-stu-id="240bd-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="240bd-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="240bd-1116">Az.EventGrid</span></span>
* <span data-ttu-id="240bd-1117">Frissítve a 2019-06-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="240bd-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="240bd-1118">Új parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-1118">New cmdlets:</span></span>
    - <span data-ttu-id="240bd-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="240bd-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="240bd-1120">Létrehoz egy új Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="240bd-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="240bd-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="240bd-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="240bd-1122">Lekéri egy Event Grid-tartomány részleteit, vagy az aktuális Azure-előfizetéshez tartozó összes Event Grid-tartomány listáját.</span><span class="sxs-lookup"><span data-stu-id="240bd-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="240bd-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="240bd-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="240bd-1124">Eltávolít egy Azure Event Grid-tartományt.</span><span class="sxs-lookup"><span data-stu-id="240bd-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="240bd-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="240bd-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="240bd-1126">Újra létrehozza a megosztott hozzáférési kulcsot az Azure Event Grid-tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="240bd-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="240bd-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="240bd-1128">Lekéri az Event Grid-tartományban való esemény-közzétételhez használt megosztott hozzáférési kulcsokat.</span><span class="sxs-lookup"><span data-stu-id="240bd-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="240bd-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="240bd-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="240bd-1130">Új Azure Event Grid-tartományi témakört hoz létre.</span><span class="sxs-lookup"><span data-stu-id="240bd-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="240bd-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="240bd-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="240bd-1132">Lekéri egy Event Grid-tartományi témakör részleteit, vagy az aktuális Azure-előfizetés adott Event Grid-tartományához tartozó Event Grid-tartományi témakörök listáját</span><span class="sxs-lookup"><span data-stu-id="240bd-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="240bd-1133">Remove-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="240bd-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="240bd-1134">Eltávolít egy meglévő Azure Event Grid-tartományi témakört.</span><span class="sxs-lookup"><span data-stu-id="240bd-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="240bd-1135">Frissített parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="240bd-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="240bd-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="240bd-1137">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="240bd-1138">Új kötelező paraméterek lettek hozzáadva az új Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve új esemény-előfizetések létrehozását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="240bd-1139">Új paraméterkészletek lettek hozzáadva tartományok és tartományi témakörök esetében, lehetővé téve a meglévő paraméterek (például EndPointType, SubjectBeginsWith stb.) újbóli felhasználását.</span><span class="sxs-lookup"><span data-stu-id="240bd-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="240bd-1140">Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="240bd-1141">Esemény-előfizetés lejárati dátuma,</span><span class="sxs-lookup"><span data-stu-id="240bd-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="240bd-1142">Speciális szűrési paraméterek.</span><span class="sxs-lookup"><span data-stu-id="240bd-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="240bd-1143">Új felsorolási érték lett hozzáadva a servicebusqueue elem célértékeként.</span><span class="sxs-lookup"><span data-stu-id="240bd-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="240bd-1144">Nem engedélyezett az -IncludedEventType beállításnál az „All” érték használata és a következővel való helyettesítése:</span><span class="sxs-lookup"><span data-stu-id="240bd-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="240bd-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="240bd-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="240bd-1146">Új opcionális paraméterek (Top, ODataQuery és NextLink) az eredmények tördelésének és szűrésének támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="240bd-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="240bd-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="240bd-1148">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és Event Grid-tartományi témakörök átirányításának támogatásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="240bd-1149">Új kötelező paraméterek lettek hozzáadva az Event Grid-tartományok és/vagy Event Grid-tartományi témakörök nevének megadásához, lehetővé téve a meglévő esemény-előfizetések eltávolítását ezeken az erőforrásokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="240bd-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="240bd-1152">Hozzá lett adva az átalakítások támogatása és az új operátorértékek automatikus kitöltése (RegEx)</span><span class="sxs-lookup"><span data-stu-id="240bd-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="240bd-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="240bd-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="240bd-1154">Hozzá lett adva az új értékek automatikus kitöltése</span><span class="sxs-lookup"><span data-stu-id="240bd-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1155">Az.Network</span></span>
* <span data-ttu-id="240bd-1156">Virtuális hálózati átjárók erőforrás-támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="240bd-1157">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1157">New cmdlets</span></span>
        - <span data-ttu-id="240bd-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="240bd-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="240bd-1159">AvailablePrivateEndpointType hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="240bd-1160">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1160">New cmdlets</span></span>
        - <span data-ttu-id="240bd-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="240bd-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="240bd-1162">PrivatePrivateLinkService hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="240bd-1163">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1163">New cmdlets</span></span>
        - <span data-ttu-id="240bd-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="240bd-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="240bd-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="240bd-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="240bd-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="240bd-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="240bd-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="240bd-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="240bd-1169">PrivateEndpoint hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="240bd-1170">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1170">New cmdlets</span></span>
        - <span data-ttu-id="240bd-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="240bd-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="240bd-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="240bd-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="240bd-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="240bd-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="240bd-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="240bd-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="240bd-1175">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: UseLocalAzureIpAddress jelző a VpnConnection elemen</span><span class="sxs-lookup"><span data-stu-id="240bd-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="240bd-1176">Frissítve lett a New-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="240bd-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="240bd-1177">Frissítve lett a Set-AzVpnConnection: Új opcionális -UseLocalAzureIpAddress paraméter lett hozzáadva annak jelölésére, hogy helyi Azure-beli IP-címet kell használni forrásként a kapcsolat inicializálása során.</span><span class="sxs-lookup"><span data-stu-id="240bd-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="240bd-1178">Hozzá lett adva az írásvédett PeeredConnections mező az ExpressRoute-társhálózatlétesítések esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="240bd-1179">Hozzá lett adva az írásvédett GlobalReachEnabled mező az ExpressRoute esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="240bd-1180">Kompatibilitástörő változást okozó attribútum lett hozzáadva, amely jelzi az AllowGlobalReach mező elavulását az ExpressRouteCircuit-modellben</span><span class="sxs-lookup"><span data-stu-id="240bd-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="240bd-1181">Javítva lett a 8756-os hiba a TargetListenerID AzApplicationGatewayRedirectConfiguration-parancsmagokkal való használata során</span><span class="sxs-lookup"><span data-stu-id="240bd-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="240bd-1182">Javítva lett a hiba a New-AzApplicationGatewayPathRuleConfig parancsmagban, amely megakadályozta az átírási szabálykészlet beállítását.</span><span class="sxs-lookup"><span data-stu-id="240bd-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="240bd-1183">Javítva lett a VirtualNetworkTaps megjelenítése a NetworkInterfaceIpConfiguration esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="240bd-1184">Javítva lettek a Cortex Get-parancsmagok az összes rész felsorolásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="240bd-1185">Javítva lett a VirtualHub-hivatkozás létrehozása az ExpressRouteGateways, VpnGateway esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="240bd-1186">Hozzá lett adva a rendelkezésreállási zónák támogatása az AzureFirewall és a NatGateway esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="240bd-1187">Hozzá lett adva a Get-AzNetworkServiceTag parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="240bd-1188">Hozzá lett adva a több nyilvános IP-cím támogatása az Azure Firewall esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="240bd-1189">Frissítve lett a New-AzFirewall parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="240bd-1190">Hozzá lett adva a -PublicIpAddress paraméter, amely egy vagy több nyilvános IP-cím-objektumot fogad el</span><span class="sxs-lookup"><span data-stu-id="240bd-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="240bd-1191">Hozzá lett adva a -VirtualNetwork paraméter, amely virtuális hálózati objektumokat fogad el</span><span class="sxs-lookup"><span data-stu-id="240bd-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="240bd-1192">Hozzá lett adva az AddPublicIpAddress és RemovePublicIpAddress metódus a tűzfalobjektumok esetében, és nyilvános IP-cím-objektumokat fogadnak el bemeneti adatként</span><span class="sxs-lookup"><span data-stu-id="240bd-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="240bd-1193">Elavult a -PublicIpName és a -VirtualNetworkName paraméter</span><span class="sxs-lookup"><span data-stu-id="240bd-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="240bd-1194">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: VpnClient AAD-alapú hitelesítési beállítások megadása a virtuális hálózati átjárók erőforrásaihoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="240bd-1195">Frissült a New-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="240bd-1196">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva az AadTenantUri, AadAudienceId, AadIssuerUri opcionális paraméter a VpnClient AAD-alapú hitelesítési beállítások megadásához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="240bd-1197">Frissült a Set-AzVirtualNetworkGateway: Hozzá lett adva a RemoveAadAuthentication opcionális kapcsolóparaméter a VpnClient AAD-alapú hitelesítési beállítások eltávolításához az átjáró esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-1199">Engedélyezve lett a **pergb2018** tarifacsomag a „New-AzureRmOperationalInsightsWorkspace” parancs esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1200">Az.Resources</span></span>
* <span data-ttu-id="240bd-1201">További sablonexportálási beállítások támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="240bd-1202">Hozzá lett adva a „-SkipResourceNameParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="240bd-1203">Hozzá lett adva a „-SkipAllParameterization” paraméter az Export-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="240bd-1204">Hozzá lett adva a „-Resource” paraméter az Export-AzResourceGroup esetében az exportált erőforrások szűréséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-1206">Ki lett javítva az a hiba, hogy a ByExistingKeyVault tanúsítvány hozzáadása bizonyos esetekben helytelen ujjlenyomatot kért le</span><span class="sxs-lookup"><span data-stu-id="240bd-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1207">Az.Sql</span></span>
* <span data-ttu-id="240bd-1208">Javítva lett az Advanced Threat Protection Storage-végpontjának utótagja</span><span class="sxs-lookup"><span data-stu-id="240bd-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="240bd-1209">Javítva lett, hogy az Advanced Data Security engedélyezése felülbírálja az Advanced Threat Protection-szabályzatot</span><span class="sxs-lookup"><span data-stu-id="240bd-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="240bd-1210">Új parancsmagok lettek hozzáadva a Management.Sql esetében, amelyek lehetővé teszik az ügyfelek számára TDE-kulcsok hozzáadását és TDE-védő beállítását a felügyelt példányokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="240bd-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="240bd-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="240bd-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="240bd-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="240bd-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="240bd-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="240bd-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="240bd-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="240bd-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="240bd-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1216">Az.Storage</span></span>
* <span data-ttu-id="240bd-1217">A FileStorage és az SkuName Premium_ZRS altípus támogatása Storage-fiókok létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="240bd-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="240bd-1219">Egyértelműsítve lett a blobmódosíthatatlansági parancsmag leírása</span><span class="sxs-lookup"><span data-stu-id="240bd-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="240bd-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1221">Az.Websites</span></span>
* <span data-ttu-id="240bd-1222">Optimalizálva lett a Get-AzWebAppCertificate parancsmag, hogy erőforráscsoport szerint szűrjön a kiszolgálón, ne ügyfél szerint</span><span class="sxs-lookup"><span data-stu-id="240bd-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="240bd-1223">Hozzá lett adva a -UseDisasterRecovery kapcsolóparaméter a Get-AzWebAppSnapshot parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="240bd-1224">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="240bd-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="240bd-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-1225">Az.Cdn</span></span>
* <span data-ttu-id="240bd-1226">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="240bd-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1227">Az.Compute</span></span>
* <span data-ttu-id="240bd-1228">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="240bd-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="240bd-1229">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="240bd-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1230">Az.EventHub</span></span>
* <span data-ttu-id="240bd-1231">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="240bd-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="240bd-1232">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="240bd-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1233">Az.Network</span></span>
* <span data-ttu-id="240bd-1234">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="240bd-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="240bd-1235">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="240bd-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="240bd-1237">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1239">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="240bd-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-1241">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="240bd-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-1243">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="240bd-1244">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="240bd-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1245">Az.Sql</span></span>
* <span data-ttu-id="240bd-1246">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="240bd-1247">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="240bd-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="240bd-1248">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="240bd-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="240bd-1249">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="240bd-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1250">Az.Websites</span></span>
* <span data-ttu-id="240bd-1251">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="240bd-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="240bd-1252">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="240bd-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="240bd-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-1254">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="240bd-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="240bd-1255">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="240bd-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="240bd-1256">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="240bd-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="240bd-1257">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="240bd-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="240bd-1258">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="240bd-1259">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="240bd-1260">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="240bd-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="240bd-1261">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="240bd-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="240bd-1262">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="240bd-1263">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="240bd-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="240bd-1264">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="240bd-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="240bd-1265">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="240bd-1266">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="240bd-1267">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="240bd-1268">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="240bd-1269">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="240bd-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="240bd-1270">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="240bd-1271">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="240bd-1272">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="240bd-1273">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="240bd-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="240bd-1274">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="240bd-1275">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="240bd-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="240bd-1276">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="240bd-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="240bd-1277">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="240bd-1278">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="240bd-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="240bd-1279">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="240bd-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="240bd-1280">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="240bd-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="240bd-1281">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="240bd-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="240bd-1282">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="240bd-1283">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="240bd-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="240bd-1284">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="240bd-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="240bd-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="240bd-1286">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="240bd-1287">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="240bd-1288">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="240bd-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="240bd-1289">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="240bd-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="240bd-1290">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="240bd-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="240bd-1291">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="240bd-1292">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="240bd-1293">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="240bd-1294">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="240bd-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="240bd-1295">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="240bd-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="240bd-1296">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="240bd-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="240bd-1297">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="240bd-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="240bd-1298">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="240bd-1299">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="240bd-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="240bd-1300">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="240bd-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="240bd-1301">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="240bd-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="240bd-1302">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="240bd-1303">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="240bd-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="240bd-1304">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="240bd-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="240bd-1305">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="240bd-1306">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="240bd-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="240bd-1307">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="240bd-1308">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="240bd-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="240bd-1309">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="240bd-1310">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="240bd-1311">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="240bd-1312">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="240bd-1313">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="240bd-1314">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="240bd-1315">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="240bd-1316">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="240bd-1317">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="240bd-1318">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="240bd-1319">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="240bd-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="240bd-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="240bd-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="240bd-1321">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="240bd-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="240bd-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="240bd-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="240bd-1323">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="240bd-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="240bd-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="240bd-1325">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="240bd-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="240bd-1326">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="240bd-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="240bd-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="240bd-1328">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="240bd-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="240bd-1329">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="240bd-1330">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="240bd-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1331">Az.Automation</span></span>
* <span data-ttu-id="240bd-1332">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="240bd-1333">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="240bd-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="240bd-1334">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="240bd-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="240bd-1335">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="240bd-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="240bd-1336">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="240bd-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="240bd-1337">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="240bd-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="240bd-1338">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="240bd-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1339">Az.Compute</span></span>
* <span data-ttu-id="240bd-1340">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="240bd-1341">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="240bd-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-1343">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="240bd-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-1344">Az.Monitor</span></span>
* <span data-ttu-id="240bd-1345">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="240bd-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1346">Az.Network</span></span>
* <span data-ttu-id="240bd-1347">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="240bd-1348">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="240bd-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="240bd-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="240bd-1350">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1351">Az.Resources</span></span>
* <span data-ttu-id="240bd-1352">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1353">Az.Sql</span></span>
* <span data-ttu-id="240bd-1354">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="240bd-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="240bd-1355">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="240bd-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1356">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1357">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="240bd-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-1359">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="240bd-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="240bd-1360">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1361">Az.Compute</span></span>
* <span data-ttu-id="240bd-1362">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="240bd-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="240bd-1363">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="240bd-1364">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="240bd-1365">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="240bd-1366">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="240bd-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="240bd-1367">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="240bd-1368">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="240bd-1368">Breaking changes</span></span>
    - <span data-ttu-id="240bd-1369">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="240bd-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="240bd-1370">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="240bd-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="240bd-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="240bd-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="240bd-1372">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="240bd-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="240bd-1373">Az.Dns</span></span>
* <span data-ttu-id="240bd-1374">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="240bd-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="240bd-1375">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="240bd-1376">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="240bd-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="240bd-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="240bd-1378">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="240bd-1379">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="240bd-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="240bd-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-1380">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-1381">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="240bd-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="240bd-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="240bd-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="240bd-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="240bd-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="240bd-1384">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="240bd-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="240bd-1385">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="240bd-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="240bd-1386">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="240bd-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="240bd-1387">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="240bd-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-1388">Az.Monitor</span></span>
* <span data-ttu-id="240bd-1389">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="240bd-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="240bd-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="240bd-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="240bd-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="240bd-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="240bd-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="240bd-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="240bd-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="240bd-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="240bd-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="240bd-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="240bd-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="240bd-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="240bd-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="240bd-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="240bd-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="240bd-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="240bd-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="240bd-1401">[További](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="240bd-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="240bd-1402">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="240bd-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1403">Az.Network</span></span>
* <span data-ttu-id="240bd-1404">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="240bd-1405">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1405">New cmdlets</span></span>
        - <span data-ttu-id="240bd-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="240bd-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="240bd-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="240bd-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="240bd-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="240bd-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="240bd-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="240bd-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="240bd-1410">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="240bd-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="240bd-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="240bd-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="240bd-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="240bd-1413">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="240bd-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="240bd-1414">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="240bd-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="240bd-1415">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="240bd-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="240bd-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="240bd-1417">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="240bd-1418">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="240bd-1419">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1421">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="240bd-1422">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="240bd-1423">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="240bd-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="240bd-1424">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="240bd-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="240bd-1425">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="240bd-1426">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="240bd-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="240bd-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="240bd-1427">Az.Relay</span></span>
* <span data-ttu-id="240bd-1428">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="240bd-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-1430">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="240bd-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1431">Az.Storage</span></span>
* <span data-ttu-id="240bd-1432">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="240bd-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="240bd-1433">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="240bd-1434">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="240bd-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="240bd-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="240bd-1436">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="240bd-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="240bd-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="240bd-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="240bd-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1440">Az.Websites</span></span>
* <span data-ttu-id="240bd-1441">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="240bd-1442">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="240bd-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="240bd-1443">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="240bd-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-1444">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-1445">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="240bd-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="240bd-1446">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="240bd-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="240bd-1447">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="240bd-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="240bd-1448">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="240bd-1449">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="240bd-1450">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="240bd-1451">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1452">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1453">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="240bd-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-1454">Az.Batch</span></span>
* <span data-ttu-id="240bd-1455">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-1456">Az.Cdn</span></span>
* <span data-ttu-id="240bd-1457">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-1459">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1460">Az.Compute</span></span>
* <span data-ttu-id="240bd-1461">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="240bd-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="240bd-1462">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1463">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-1464">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-1465">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="240bd-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-1467">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="240bd-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="240bd-1468">Az.EventGrid</span></span>
* <span data-ttu-id="240bd-1469">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1470">Az.EventHub</span></span>
* <span data-ttu-id="240bd-1471">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="240bd-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="240bd-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="240bd-1472">Az.HDInsight</span></span>
* <span data-ttu-id="240bd-1473">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1474">Az.IotHub</span></span>
* <span data-ttu-id="240bd-1475">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-1476">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-1477">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1478">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="240bd-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="240bd-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="240bd-1480">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="240bd-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="240bd-1481">Az.Media</span></span>
* <span data-ttu-id="240bd-1482">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-1483">Az.Monitor</span></span>
  * <span data-ttu-id="240bd-1484">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="240bd-1485">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="240bd-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="240bd-1486">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="240bd-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="240bd-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="240bd-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="240bd-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="240bd-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="240bd-1489">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="240bd-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="240bd-1490">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="240bd-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1491">Az.Network</span></span>
* <span data-ttu-id="240bd-1492">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1493">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="240bd-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="240bd-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="240bd-1495">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-1497">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="240bd-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="240bd-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="240bd-1499">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1501">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1502">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="240bd-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="240bd-1503">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="240bd-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="240bd-1504">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="240bd-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="240bd-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="240bd-1505">Az.RedisCache</span></span>
* <span data-ttu-id="240bd-1506">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1507">Az.Resources</span></span>
* <span data-ttu-id="240bd-1508">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1509">Az.Sql</span></span>
* <span data-ttu-id="240bd-1510">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="240bd-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="240bd-1511">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1512">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="240bd-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="240bd-1513">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="240bd-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="240bd-1514">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="240bd-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="240bd-1515">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="240bd-1516">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="240bd-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1517">Az.Websites</span></span>
* <span data-ttu-id="240bd-1518">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="240bd-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="240bd-1519">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="240bd-1520">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="240bd-1521">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="240bd-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="240bd-1522">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="240bd-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-1523">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-1524">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="240bd-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="240bd-1525">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="240bd-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="240bd-1526">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="240bd-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="240bd-1527">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="240bd-1528">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="240bd-1529">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="240bd-1530">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="240bd-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1531">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1532">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="240bd-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="240bd-1534">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="240bd-1535">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1536">Az.Automation</span></span>
* <span data-ttu-id="240bd-1537">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="240bd-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="240bd-1538">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="240bd-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="240bd-1539">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1540">Az.Compute</span></span>
* <span data-ttu-id="240bd-1541">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="240bd-1542">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="240bd-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="240bd-1544">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="240bd-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-1545">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-1546">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="240bd-1547">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="240bd-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1548">Az.Resources</span></span>
* <span data-ttu-id="240bd-1549">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="240bd-1550">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="240bd-1551">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="240bd-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="240bd-1552">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="240bd-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="240bd-1553">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="240bd-1554">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="240bd-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1555">Az.Sql</span></span>
* <span data-ttu-id="240bd-1556">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1557">Az.Storage</span></span>
* <span data-ttu-id="240bd-1558">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="240bd-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="240bd-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="240bd-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="240bd-1560">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="240bd-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="240bd-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="240bd-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="240bd-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="240bd-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="240bd-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="240bd-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="240bd-1565">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="240bd-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="240bd-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="240bd-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="240bd-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="240bd-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="240bd-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="240bd-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="240bd-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="240bd-1570">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="240bd-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="240bd-1571">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="240bd-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="240bd-1572">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="240bd-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="240bd-1573">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="240bd-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="240bd-1574">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="240bd-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="240bd-1575">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="240bd-1576">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="240bd-1577">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="240bd-1578">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1579">Az.Automation</span></span>
* <span data-ttu-id="240bd-1580">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="240bd-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="240bd-1581">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="240bd-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="240bd-1582">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="240bd-1582">Pre-Post script</span></span>
    * <span data-ttu-id="240bd-1583">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="240bd-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1584">Az.Compute</span></span>
* <span data-ttu-id="240bd-1585">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="240bd-1586">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-1587">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-1588">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1589">Az.Network</span></span>
* <span data-ttu-id="240bd-1590">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="240bd-1591">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1593">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="240bd-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="240bd-1594">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1595">Az.Resources</span></span>
* <span data-ttu-id="240bd-1596">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="240bd-1597">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1598">Az.Sql</span></span>
* <span data-ttu-id="240bd-1599">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1600">Az.Storage</span></span>
* <span data-ttu-id="240bd-1601">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="240bd-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="240bd-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="240bd-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="240bd-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="240bd-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="240bd-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="240bd-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="240bd-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="240bd-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1608">Az.Websites</span></span>
* <span data-ttu-id="240bd-1609">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="240bd-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="240bd-1610">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="240bd-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1611">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1612">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="240bd-1613">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1614">Az.Automation</span></span>
* <span data-ttu-id="240bd-1615">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="240bd-1616">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="240bd-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="240bd-1617">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="240bd-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-1618">Az.Cdn</span></span>
* <span data-ttu-id="240bd-1619">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="240bd-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1620">Az.Compute</span></span>
* <span data-ttu-id="240bd-1621">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-1622">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-1623">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="240bd-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="240bd-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="240bd-1624">Az.LogicApp</span></span>
* <span data-ttu-id="240bd-1625">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="240bd-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1626">Az.Network</span></span>
* <span data-ttu-id="240bd-1627">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1629">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="240bd-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="240bd-1630">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="240bd-1630">SDK Update</span></span>
* <span data-ttu-id="240bd-1631">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="240bd-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="240bd-1632">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1633">Az.Resources</span></span>
* <span data-ttu-id="240bd-1634">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="240bd-1635">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="240bd-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="240bd-1636">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="240bd-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="240bd-1637">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="240bd-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="240bd-1638">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="240bd-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="240bd-1639">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="240bd-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1640">Az.Sql</span></span>
* <span data-ttu-id="240bd-1641">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="240bd-1642">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1643">Az.Storage</span></span>
* <span data-ttu-id="240bd-1644">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="240bd-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="240bd-1645">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="240bd-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="240bd-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="240bd-1647">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="240bd-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1648">Az.Automation</span></span>
* <span data-ttu-id="240bd-1649">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="240bd-1650">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="240bd-1651">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-1653">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1654">Az.Compute</span></span>
* <span data-ttu-id="240bd-1655">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="240bd-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="240bd-1656">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="240bd-1657">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="240bd-1658">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="240bd-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-1660">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="240bd-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="240bd-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1661">Az.EventHub</span></span>
* <span data-ttu-id="240bd-1662">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="240bd-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-1663">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-1664">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="240bd-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="240bd-1665">Az.LogicApp</span></span>
* <span data-ttu-id="240bd-1666">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="240bd-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="240bd-1667">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="240bd-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="240bd-1668">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="240bd-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="240bd-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="240bd-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="240bd-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="240bd-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="240bd-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="240bd-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="240bd-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="240bd-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="240bd-1673">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="240bd-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="240bd-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="240bd-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="240bd-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="240bd-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="240bd-1678">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="240bd-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="240bd-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-1679">Az.Monitor</span></span>
* <span data-ttu-id="240bd-1680">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1681">Az.Network</span></span>
* <span data-ttu-id="240bd-1682">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="240bd-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="240bd-1684">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="240bd-1685">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="240bd-1686">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="240bd-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1687">Az.Resources</span></span>
* <span data-ttu-id="240bd-1688">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="240bd-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="240bd-1689">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="240bd-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="240bd-1690">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="240bd-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="240bd-1691">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="240bd-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1692">Az.Sql</span></span>
* <span data-ttu-id="240bd-1693">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="240bd-1694">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="240bd-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1695">Az.Websites</span></span>
* <span data-ttu-id="240bd-1696">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="240bd-1697">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="240bd-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1698">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1699">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="240bd-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="240bd-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="240bd-1701">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1702">Az.Compute</span></span>
* <span data-ttu-id="240bd-1703">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="240bd-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="240bd-1704">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="240bd-1705">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="240bd-1707">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="240bd-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1708">Az.Resources</span></span>
* <span data-ttu-id="240bd-1709">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="240bd-1710">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="240bd-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="240bd-1711">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="240bd-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="240bd-1712">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="240bd-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1713">Az.Sql</span></span>
* <span data-ttu-id="240bd-1714">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="240bd-1715">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="240bd-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="240bd-1716">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="240bd-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="240bd-1717">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="240bd-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1718">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1719">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="240bd-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="240bd-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="240bd-1721">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="240bd-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="240bd-1723">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="240bd-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="240bd-1724">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="240bd-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1725">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1726">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="240bd-1727">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="240bd-1728">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="240bd-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="240bd-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="240bd-1729">Az.Aks</span></span>
* <span data-ttu-id="240bd-1730">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="240bd-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1731">Az.Automation</span></span>
* <span data-ttu-id="240bd-1732">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="240bd-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="240bd-1733">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="240bd-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="240bd-1734">Az.Cdn</span></span>
* <span data-ttu-id="240bd-1735">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1736">Az.Compute</span></span>
* <span data-ttu-id="240bd-1737">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="240bd-1738">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="240bd-1739">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="240bd-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="240bd-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="240bd-1741">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="240bd-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="240bd-1742">Az.DataFactory</span></span>
* <span data-ttu-id="240bd-1743">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-1745">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="240bd-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="240bd-1746">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="240bd-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="240bd-1747">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1748">Az.IotHub</span></span>
* <span data-ttu-id="240bd-1749">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="240bd-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-1750">Az.KeyVault</span></span>
* <span data-ttu-id="240bd-1751">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1752">Az.Network</span></span>
* <span data-ttu-id="240bd-1753">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1754">Az.Resources</span></span>
* <span data-ttu-id="240bd-1755">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="240bd-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="240bd-1756">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="240bd-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="240bd-1757">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="240bd-1758">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="240bd-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="240bd-1759">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="240bd-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="240bd-1760">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="240bd-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="240bd-1761">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="240bd-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-1763">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="240bd-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="240bd-1764">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1764">Fix some error messages.</span></span>
* <span data-ttu-id="240bd-1765">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="240bd-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="240bd-1766">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="240bd-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="240bd-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="240bd-1767">Az.SignalR</span></span>
* <span data-ttu-id="240bd-1768">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1769">Az.Sql</span></span>
* <span data-ttu-id="240bd-1770">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="240bd-1771">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="240bd-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="240bd-1772">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="240bd-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="240bd-1773">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="240bd-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1774">Az.Storage</span></span>
* <span data-ttu-id="240bd-1775">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="240bd-1776">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="240bd-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="240bd-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="240bd-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="240bd-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="240bd-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="240bd-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="240bd-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="240bd-1780">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1781">Az.Websites</span></span>
* <span data-ttu-id="240bd-1782">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="240bd-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="240bd-1783">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="240bd-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="240bd-1784">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="240bd-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="240bd-1785">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="240bd-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="240bd-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1786">Az.Accounts</span></span>
* <span data-ttu-id="240bd-1787">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1788">Az.Compute</span></span>
* <span data-ttu-id="240bd-1789">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="240bd-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="240bd-1790">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="240bd-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="240bd-1791">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-1793">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="240bd-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="240bd-1794">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="240bd-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="240bd-1795">Az.EventGrid</span></span>
* <span data-ttu-id="240bd-1796">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="240bd-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="240bd-1797">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="240bd-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="240bd-1798">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="240bd-1799">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="240bd-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="240bd-1800">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="240bd-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="240bd-1801">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="240bd-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="240bd-1802">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="240bd-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="240bd-1803">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="240bd-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="240bd-1804">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="240bd-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="240bd-1805">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="240bd-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="240bd-1806">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="240bd-1807">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="240bd-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="240bd-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="240bd-1808">Az.IotHub</span></span>
* <span data-ttu-id="240bd-1809">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="240bd-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="240bd-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="240bd-1810">Az.LogicApp</span></span>
* <span data-ttu-id="240bd-1811">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="240bd-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1812">Az.Resources</span></span>
* <span data-ttu-id="240bd-1813">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="240bd-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="240bd-1814">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="240bd-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="240bd-1815">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="240bd-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="240bd-1816">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="240bd-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="240bd-1817">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="240bd-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="240bd-1818">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="240bd-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="240bd-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="240bd-1819">Az.SignalR</span></span>
* <span data-ttu-id="240bd-1820">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1821">Az.Sql</span></span>
* <span data-ttu-id="240bd-1822">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="240bd-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="240bd-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1823">Az.Storage</span></span>
* <span data-ttu-id="240bd-1824">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="240bd-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="240bd-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="240bd-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="240bd-1826">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="240bd-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="240bd-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="240bd-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1828">Az.Websites</span></span>
* <span data-ttu-id="240bd-1829">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="240bd-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="240bd-1830">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="240bd-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="240bd-1831">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="240bd-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="240bd-1832">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-1832">General</span></span>

- <span data-ttu-id="240bd-1833">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="240bd-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="240bd-1834">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1834">Online help for each module</span></span>
- <span data-ttu-id="240bd-1835">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="240bd-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="240bd-1836">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="240bd-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1837">Az.Accounts</span></span>
- <span data-ttu-id="240bd-1838">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="240bd-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="240bd-1839">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="240bd-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="240bd-1841">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="240bd-1841">Fixes for #7002</span></span>
- <span data-ttu-id="240bd-1842">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="240bd-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="240bd-1843">Az.Batch</span></span>
- <span data-ttu-id="240bd-1844">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="240bd-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="240bd-1845">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="240bd-1846">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="240bd-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="240bd-1847">Az.Billing</span></span>
- <span data-ttu-id="240bd-1848">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="240bd-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="240bd-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="240bd-1850">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="240bd-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="240bd-1851">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="240bd-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="240bd-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="240bd-1853">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="240bd-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="240bd-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="240bd-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="240bd-1855">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="240bd-1857">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="240bd-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="240bd-1858">Az.Monitor</span></span>
- <span data-ttu-id="240bd-1859">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="240bd-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="240bd-1860">Az.KeyVault</span></span>
- <span data-ttu-id="240bd-1861">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="240bd-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="240bd-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="240bd-1863">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="240bd-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="240bd-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="240bd-1864">Az.Media</span></span>
- <span data-ttu-id="240bd-1865">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="240bd-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="240bd-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1866">Az.Network</span></span>
<span data-ttu-id="240bd-1867">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="240bd-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="240bd-1868">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="240bd-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="240bd-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="240bd-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="240bd-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="240bd-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="240bd-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="240bd-1877">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="240bd-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="240bd-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="240bd-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="240bd-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="240bd-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="240bd-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="240bd-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="240bd-1883">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="240bd-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="240bd-1884">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="240bd-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="240bd-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="240bd-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="240bd-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="240bd-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="240bd-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="240bd-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="240bd-1888">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="240bd-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="240bd-1889">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="240bd-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="240bd-1891">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="240bd-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="240bd-1892">Az.Profile</span></span>
- <span data-ttu-id="240bd-1893">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="240bd-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="240bd-1895">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="240bd-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1896">Az.Resources</span></span>
- <span data-ttu-id="240bd-1897">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="240bd-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="240bd-1899">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="240bd-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="240bd-1900">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="240bd-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="240bd-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="240bd-1902">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="240bd-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="240bd-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1903">Az.Sql</span></span>
- <span data-ttu-id="240bd-1904">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="240bd-1905">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="240bd-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="240bd-1906">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="240bd-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1907">Az.Storage</span></span>
- <span data-ttu-id="240bd-1908">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="240bd-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1909">Az.Websites</span></span>
- <span data-ttu-id="240bd-1910">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="240bd-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="240bd-1911">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="240bd-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="240bd-1912">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-1912">General</span></span>

* <span data-ttu-id="240bd-1913">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="240bd-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1914">Az.Compute</span></span>

* <span data-ttu-id="240bd-1915">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="240bd-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="240bd-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="240bd-1917">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="240bd-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="240bd-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="240bd-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="240bd-1919">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="240bd-1920">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="240bd-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="240bd-1921">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="240bd-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="240bd-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="240bd-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="240bd-1923">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="240bd-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="240bd-1924">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="240bd-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="240bd-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1925">Az.Resources</span></span>

* <span data-ttu-id="240bd-1926">[https://github.com/Azure/azure-powershell/issues/7679](https://github.com/Azure/azure-powershell/issues/7679 ) javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="240bd-1927">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="240bd-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="240bd-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1928">Az.Sql</span></span>

* <span data-ttu-id="240bd-1929">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="240bd-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="240bd-1930">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="240bd-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="240bd-1931">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="240bd-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="240bd-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-1932">Az.Storage</span></span>

* <span data-ttu-id="240bd-1933">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="240bd-1934">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="240bd-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="240bd-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="240bd-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="240bd-1936">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="240bd-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="240bd-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="240bd-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="240bd-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="240bd-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-1939">Az.Websites</span></span>

* <span data-ttu-id="240bd-1940">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="240bd-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="240bd-1941">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="240bd-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="240bd-1942">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="240bd-1943">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="240bd-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="240bd-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="240bd-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="240bd-1945">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="240bd-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="240bd-1946">Az.Automation</span></span>
* <span data-ttu-id="240bd-1947">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="240bd-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="240bd-1948">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="240bd-1949">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="240bd-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="240bd-1950">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="240bd-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="240bd-1951">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="240bd-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="240bd-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-1952">Az.Compute</span></span>
* <span data-ttu-id="240bd-1953">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="240bd-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="240bd-1954">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="240bd-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="240bd-1956">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="240bd-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="240bd-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="240bd-1958">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="240bd-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="240bd-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-1959">Az.Network</span></span>
* <span data-ttu-id="240bd-1960">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="240bd-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="240bd-1961">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="240bd-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="240bd-1962">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="240bd-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="240bd-1963">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="240bd-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="240bd-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="240bd-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="240bd-1965">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="240bd-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="240bd-1966">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="240bd-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="240bd-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="240bd-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="240bd-1968">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="240bd-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="240bd-1969">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="240bd-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="240bd-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="240bd-1970">Az.Relay</span></span>
* <span data-ttu-id="240bd-1971">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="240bd-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="240bd-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-1972">Az.Resources</span></span>
* <span data-ttu-id="240bd-1973">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="240bd-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="240bd-1974">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="240bd-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="240bd-1975">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="240bd-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="240bd-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-1977">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="240bd-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-1978">Az.Sql</span></span>
* <span data-ttu-id="240bd-1979">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="240bd-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="240bd-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="240bd-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="240bd-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="240bd-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="240bd-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="240bd-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="240bd-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="240bd-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="240bd-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="240bd-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="240bd-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="240bd-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="240bd-1988">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="240bd-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="240bd-1989">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="240bd-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="240bd-1990">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="240bd-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="240bd-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="240bd-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="240bd-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="240bd-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="240bd-1993">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="240bd-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="240bd-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="240bd-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="240bd-1995">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="240bd-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="240bd-1996">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="240bd-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="240bd-1997">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="240bd-1997">General</span></span>
* <span data-ttu-id="240bd-1998">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="240bd-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="240bd-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="240bd-1999">Az.Profile</span></span>
* <span data-ttu-id="240bd-2000">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="240bd-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="240bd-2001">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="240bd-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="240bd-2002">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="240bd-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="240bd-2003">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="240bd-2004">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="240bd-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="240bd-2005">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="240bd-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="240bd-2006">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="240bd-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-2008">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="240bd-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-2009">Az.Compute</span></span>
* <span data-ttu-id="240bd-2010">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="240bd-2011">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="240bd-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="240bd-2012">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="240bd-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-2014">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="240bd-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="240bd-2015">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="240bd-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="240bd-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="240bd-2016">Az.Insights</span></span>
* <span data-ttu-id="240bd-2017">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="240bd-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="240bd-2018">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="240bd-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="240bd-2019">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="240bd-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="240bd-2020">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="240bd-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-2021">Az.Network</span></span>
* <span data-ttu-id="240bd-2022">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="240bd-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="240bd-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="240bd-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="240bd-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="240bd-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="240bd-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="240bd-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="240bd-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="240bd-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="240bd-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="240bd-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="240bd-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="240bd-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="240bd-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="240bd-2030">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-2031">Az.Resources</span></span>
* <span data-ttu-id="240bd-2032">[https://github.com/Azure/azure-powershell/issues/7402](https://github.com/Azure/azure-powershell/issues/7402 ) javítása</span><span class="sxs-lookup"><span data-stu-id="240bd-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="240bd-2033">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="240bd-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="240bd-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="240bd-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="240bd-2035">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="240bd-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="240bd-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="240bd-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="240bd-2037">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="240bd-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="240bd-2038">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="240bd-2039">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="240bd-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="240bd-2040">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="240bd-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="240bd-2041">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="240bd-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="240bd-2042">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="240bd-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="240bd-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="240bd-2043">Az.Profile</span></span>
* <span data-ttu-id="240bd-2044">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="240bd-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="240bd-2045">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="240bd-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-2046">Az.Compute</span></span>
* <span data-ttu-id="240bd-2047">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="240bd-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="240bd-2048">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="240bd-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="240bd-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="240bd-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="240bd-2050">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="240bd-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="240bd-2051">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="240bd-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="240bd-2052">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="240bd-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="240bd-2053">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="240bd-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="240bd-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="240bd-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-2055">Az.Network</span></span>
* <span data-ttu-id="240bd-2056">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="240bd-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="240bd-2057">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="240bd-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-2058">Az.Resources</span></span>
* <span data-ttu-id="240bd-2059">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="240bd-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="240bd-2060">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="240bd-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="240bd-2061">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="240bd-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="240bd-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="240bd-2062">Azure.Storage</span></span>
* <span data-ttu-id="240bd-2063">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="240bd-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="240bd-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="240bd-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="240bd-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="240bd-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="240bd-2066">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="240bd-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="240bd-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="240bd-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="240bd-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="240bd-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="240bd-2069">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="240bd-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="240bd-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="240bd-2070">Az.Compute</span></span>
* <span data-ttu-id="240bd-2071">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="240bd-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="240bd-2072">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="240bd-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="240bd-2073">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="240bd-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="240bd-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="240bd-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="240bd-2075">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="240bd-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="240bd-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="240bd-2076">Az.Network</span></span>
* <span data-ttu-id="240bd-2077">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="240bd-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="240bd-2078">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="240bd-2078">new cmdlets added</span></span>
    - <span data-ttu-id="240bd-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="240bd-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="240bd-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="240bd-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="240bd-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="240bd-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="240bd-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="240bd-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="240bd-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="240bd-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="240bd-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="240bd-2085">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="240bd-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="240bd-2086">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="240bd-2087">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="240bd-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="240bd-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="240bd-2088">Az.RedisCache</span></span>
* <span data-ttu-id="240bd-2089">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="240bd-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="240bd-2090">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="240bd-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="240bd-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="240bd-2091">Az.Resources</span></span>
* <span data-ttu-id="240bd-2092">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="240bd-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="240bd-2093">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="240bd-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="240bd-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="240bd-2094">Az.Sql</span></span>
* <span data-ttu-id="240bd-2095">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="240bd-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="240bd-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="240bd-2096">Az.Websites</span></span>
* <span data-ttu-id="240bd-2097">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="240bd-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="240bd-2098">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="240bd-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="240bd-2099">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="240bd-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="240bd-2100">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="240bd-2100">Initial Release</span></span>
