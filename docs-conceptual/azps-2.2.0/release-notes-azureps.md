---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498675"
---
## <a name="220---june-2019"></a><span data-ttu-id="e149c-101">2.2.0 – 2019. június</span><span class="sxs-lookup"><span data-stu-id="e149c-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="e149c-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e149c-102">Az.Cdn</span></span>
* <span data-ttu-id="e149c-103">Frissített parancsmagok a rulesEngine szolgáltatás támogatásához a 2019. 04. 15. API-verzión</span><span class="sxs-lookup"><span data-stu-id="e149c-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-104">Az.Compute</span></span>
* <span data-ttu-id="e149c-105">A `NoWait` paraméter hozzáadása, amely elindítja a műveletet, és azonnal visszatér, még a művelet befejezése előtt.</span><span class="sxs-lookup"><span data-stu-id="e149c-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="e149c-106">Frissített parancsmagok:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e149c-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e149c-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e149c-107">Az.EventHub</span></span>
* <span data-ttu-id="e149c-108">A 9231-es hiba javítása – a Get-AzEventHubNamespace nem ad vissza címkéket</span><span class="sxs-lookup"><span data-stu-id="e149c-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="e149c-109">A 9230-as hiba javítása – a Get-AzEventHubNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="e149c-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-110">Az.Network</span></span>
* <span data-ttu-id="e149c-111">ResourceID és InputObject frissítése a Nat-átjárón</span><span class="sxs-lookup"><span data-stu-id="e149c-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="e149c-112">ResourceID és InputObject aliasának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e149c-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e149c-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="e149c-114">„Null értékű hivatkozás” hiba kijavítása a Get-AzPolicyEvent parancsmagban</span><span class="sxs-lookup"><span data-stu-id="e149c-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-116">Az IaaSVM szabályzat minimális megőrzési ideje 7 napról 1-re módosult</span><span class="sxs-lookup"><span data-stu-id="e149c-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e149c-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e149c-117">Az.ServiceBus</span></span>
* <span data-ttu-id="e149c-118">A 9182-es hiba javítása – a Get-AzServiceBusNamespace ResourceGroup paramétert ad vissza ResourceGroupName helyett</span><span class="sxs-lookup"><span data-stu-id="e149c-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e149c-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e149c-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="e149c-120">Az Update-AzServiceFabricReliability hibaüzenetében lévő gépelési hiba kijavítása</span><span class="sxs-lookup"><span data-stu-id="e149c-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="e149c-121">A Service Fabric parancssorok hiányzó karakterének pótlása</span><span class="sxs-lookup"><span data-stu-id="e149c-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-122">Az.Sql</span></span>
* <span data-ttu-id="e149c-123">A DnsZonePartner paraméter hozzáadása a New-AzureSqlInstance parancsmaghoz az AutoDr képesség a felügyelt példányon való támogatásához.</span><span class="sxs-lookup"><span data-stu-id="e149c-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="e149c-124">A Get-AzSqlDatabaseSecureConnectionPolicy parancsmag kivezetése</span><span class="sxs-lookup"><span data-stu-id="e149c-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="e149c-125">Threat Detection parancsmagok átnevezése Advanced Threat Protection névre</span><span class="sxs-lookup"><span data-stu-id="e149c-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="e149c-126">A New-AzSqlInstance, - StorageSizeInGB és - LicenseType paraméterek mostantól nem kötelezőek.</span><span class="sxs-lookup"><span data-stu-id="e149c-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-127">Az.Websites</span></span>
* <span data-ttu-id="e149c-128">javítja azt a hibát, amely miatt a Set-AzWebApp és a Set-AzWebAppSlot a -WebApp tulajdonsággal való használata eltávolította a címkéket</span><span class="sxs-lookup"><span data-stu-id="e149c-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="e149c-129">2.1.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="e149c-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="e149c-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e149c-130">Az.ApiManagement</span></span>
* <span data-ttu-id="e149c-131">Új parancsmagok a globális és API-szintű diagnosztika kezeléshez</span><span class="sxs-lookup"><span data-stu-id="e149c-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="e149c-132">**Get-AzApiManagementDiagnostic** – A globális vagy API hatókörre konfigurált diagnosztika beolvasása</span><span class="sxs-lookup"><span data-stu-id="e149c-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="e149c-133">**New-AzApiManagementDiagnostic** – Új diagnosztika létrehozása a globális vagy API szintű hatókörhöz</span><span class="sxs-lookup"><span data-stu-id="e149c-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="e149c-134">**New-AzApiManagementHttpMessageDiagnostic** – Diagnosztikai beállítás létrehozása arra vonatkozóan, hogy mely fejléceknél naplózzon a rendszer, és mekkora legyen a törzs mérete bájtban</span><span class="sxs-lookup"><span data-stu-id="e149c-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="e149c-135">**New-AzApiManagementPipelineDiagnosticSetting** – Diagnosztikai beállítások létrehozása az átjáróra érkező és onnan induló HTTP-üzenetekhez.</span><span class="sxs-lookup"><span data-stu-id="e149c-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="e149c-136">**New-AzApiManagementSamplingSetting** – Mintavételezési beállítások létrehozása diagnosztikai kérésekhez/válaszokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="e149c-137">**Remove-AzApiManagementDiagnostic** – Diagnosztikai entitás eltávolítása globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="e149c-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="e149c-138">**Set-AzApiManagementDiagnostic** – Diagnosztikai entitás frissítése globális vagy API hatókörben</span><span class="sxs-lookup"><span data-stu-id="e149c-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="e149c-139">Új parancsmagok az ApiManagement szolgáltatás gyorsítótárának kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="e149c-140">**Get-AzApiManagementCache** – Az azonosító által megadott vagy az összes gyorsítótár részleteinek beolvasása</span><span class="sxs-lookup"><span data-stu-id="e149c-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="e149c-141">**New-AzApiManagementCache** – Új alapértelmezett gyorsítótár létrehozása vagy gyorsítótár létrehozása adott Azure-régióban</span><span class="sxs-lookup"><span data-stu-id="e149c-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="e149c-142">**Remove-AzApiManagementCache** – Gyorsítótár eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e149c-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="e149c-143">**Update-AzApiManagementCache** – Gyorsítótár frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="e149c-144">Új parancsmagok az API-séma kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="e149c-145">**New-AzApiManagementSchema** – Új séma létrehozása egy API-hoz</span><span class="sxs-lookup"><span data-stu-id="e149c-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="e149c-146">**Get-AzApiManagementSchema** – Az API-ban konfigurált sémák beolvasása</span><span class="sxs-lookup"><span data-stu-id="e149c-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="e149c-147">**Remove-AzApiManagementSchema** – Az API-ban konfigurált sémák eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e149c-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="e149c-148">**Set-AzApiManagementSchema** – Az API-ban konfigurált séma frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="e149c-149">Új parancsmag a felhasználói jogkivonat létrehozásához</span><span class="sxs-lookup"><span data-stu-id="e149c-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="e149c-150">**New-AzApiManagementUserToken** – Új, alapértelmezés szerint 8 órán át érvényes felhasználói jogkivonat létrehozása. Ezen parancsmag használatával lehet a „GIT” felhasználó számára jogkivonatot létrehozni.</span><span class="sxs-lookup"><span data-stu-id="e149c-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="e149c-151">Új parancsmag a hálózat állapotának lekérdezéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="e149c-152">**Get-AzApiManagementNetworkStatus** – Azon erőforrások hálózati állapotának beolvasása, amelyektől az API Management szolgáltatás függ.</span><span class="sxs-lookup"><span data-stu-id="e149c-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="e149c-153">Ez hasznos lehet, ha az ApiManagement szolgáltatást virtuális hálózatra telepíti, és ellenőrizni kell, hogy rendben működnek-e a függőségek.</span><span class="sxs-lookup"><span data-stu-id="e149c-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="e149c-154">A **New-AzApiManagement** parancsmag frissítése az ApiManagement szolgáltatás kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="e149c-155">Mostantól az új „Consumption” SKU is támogatott</span><span class="sxs-lookup"><span data-stu-id="e149c-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="e149c-156">Mostantól az „EnableClientCertificate” jelző a „Consumption” SKU-hoz is bekapcsolható</span><span class="sxs-lookup"><span data-stu-id="e149c-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="e149c-157">Az új **New-AzApiManagementSslSetting** parancsmag lehetővé teszi a „TLS/SSL” beállítás konfigurálását a „Háttér” és „Előtér” esetén is.</span><span class="sxs-lookup"><span data-stu-id="e149c-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="e149c-158">Ez egy ApiManagement szolgáltatás előterén a titkosítások, mint például a 3DES, valamint a szerverprotokollok, mint például a Http2 konfigurálására is alkalmas.</span><span class="sxs-lookup"><span data-stu-id="e149c-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="e149c-159">Mostantól támogatott a „DeveloperPortal” gazdanév ApiManagement szolgáltatáson történő konfigurálása.</span><span class="sxs-lookup"><span data-stu-id="e149c-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="e149c-160">A **Get-AzApiManagementSsoToken** parancsmagok frissítése a „PsApiManagement” objektum bemenetként való használatához</span><span class="sxs-lookup"><span data-stu-id="e149c-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="e149c-161">A parancsmag frissítése a hibaüzenetek beágyazott megjelenítéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="e149c-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Hibakód: ValidationError Hibaüzenet: Egy vagy több mező hibás értéket tartalmaz: Hiba részletei:    [Kód=ValidationError, Üzenet=Hiba a log-to-eventhub elemben, 3. sor, 10. oszlop: A naplózó nem található, Cél=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="e149c-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="e149c-163">Az **Export-AzApiManagementApi** parancsmag frissítse az API-k OpenApi 3.0 formátumban való exportálásához</span><span class="sxs-lookup"><span data-stu-id="e149c-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="e149c-164">Az **Import-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e149c-165">API importálása az OpenApi 3.0 dokumentumspecifikációból</span><span class="sxs-lookup"><span data-stu-id="e149c-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="e149c-166">A bármely (Swagger, Wadl, Wsdl, OpenAPI) dokumentumban megadott PsApiManagementSchema tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="e149c-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="e149c-167">A bármely dokumentumban megadott ServiceUrl tulajdonság felülbírálása</span><span class="sxs-lookup"><span data-stu-id="e149c-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="e149c-168">A **Get-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) való visszaadásához</span><span class="sxs-lookup"><span data-stu-id="e149c-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="e149c-169">A **Set-AzApiManagementPolicy** parancsmag frissítése a szabályzat nem XML-nek megfelelő feloldójeles formátumban (rawxml használatával) és XML-nek megfelelő feloldójeles formátumban (xml használatával) való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="e149c-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="e149c-170">A **New-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="e149c-171">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="e149c-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e149c-172">API létrehozása ApiVersionSet tulajdonságban</span><span class="sxs-lookup"><span data-stu-id="e149c-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="e149c-173">API klónozása SourceApiId és SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="e149c-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="e149c-174">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="e149c-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e149c-175">A **Set-AzApiManagementApi** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="e149c-176">API konfigurálása OpenId engedélyezési kiszolgálón</span><span class="sxs-lookup"><span data-stu-id="e149c-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="e149c-177">API frissítése ApiVersionSet tulajdonságba</span><span class="sxs-lookup"><span data-stu-id="e149c-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="e149c-178">Lehetőség a SubscriptionRequired API hatókörben való konfigurálására</span><span class="sxs-lookup"><span data-stu-id="e149c-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="e149c-179">A **New-AzApiManagementRevision** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="e149c-180">Létező változat klónozása (címkék, termékek, műveletek és szabályzatok másolása) a SourceApiRevision használatával</span><span class="sxs-lookup"><span data-stu-id="e149c-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="e149c-181">Az új változat a szülő ApiId értékét veszi át</span><span class="sxs-lookup"><span data-stu-id="e149c-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="e149c-182">ApiRevisionDescription biztosítása</span><span class="sxs-lookup"><span data-stu-id="e149c-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="e149c-183">A „ServiceUrl” felülírása API klónozáskor</span><span class="sxs-lookup"><span data-stu-id="e149c-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="e149c-184">A **New-AzApiManagementIdentityProvider** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="e149c-185">AAD vagy AADB2C konfigurálása hitelesítésszolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="e149c-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="e149c-186">SignupPolicy, SigninPolicy, ProfileEditingPolicy és PasswordResetPolicy beállítása</span><span class="sxs-lookup"><span data-stu-id="e149c-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="e149c-187">A **New-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e149c-188">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="e149c-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e149c-189">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="e149c-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e149c-190">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e149c-191">A **Set-AzApiManagementSubscription** parancsmag frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="e149c-192">A Scope és a UserId tulajdonságot használó új előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="e149c-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="e149c-193">A ProductId és a UserId tulajdonságot használó régi előfizetési modellhez való alkalmazkodáshoz</span><span class="sxs-lookup"><span data-stu-id="e149c-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="e149c-194">Támogatás hozzáadása az AllowTracing előfizetési szinten való engedélyezéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="e149c-195">Az alábbi parancsmagok frissültek a ResourceID bemenetként való elfogadásához</span><span class="sxs-lookup"><span data-stu-id="e149c-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="e149c-196">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e149c-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="e149c-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="e149c-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="e149c-198">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e149c-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="e149c-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="e149c-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="e149c-200">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e149c-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="e149c-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="e149c-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="e149c-202">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e149c-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="e149c-203">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e149c-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="e149c-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="e149c-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="e149c-205">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e149c-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="e149c-206">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e149c-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="e149c-207">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e149c-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-208">Az.Automation</span></span>
* <span data-ttu-id="e149c-209">A Get-AzAutomationJobOutputRecord frissítése a JSON- és a szövegrekordértékek kezeléséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="e149c-210">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="e149c-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="e149c-211">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="e149c-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="e149c-212">A Start-AzAutomationDscCompilationJob viselkedésének módosítása a munka elindítására a befejezésre való várakozás helyett</span><span class="sxs-lookup"><span data-stu-id="e149c-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="e149c-213">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="e149c-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="e149c-214">A Get-AzAutomationDscNode azon hibájának javítása, amely miatt a -Name használatakor az összes csomópontot visszaadta.</span><span class="sxs-lookup"><span data-stu-id="e149c-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="e149c-215">Most már csak az egyező csomópontot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e149c-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-216">Az.Compute</span></span>
* <span data-ttu-id="e149c-217">A ProtectFromScaleIn és a ProtectFromScaleSetAction paraméterek hozzáadása az Update-AzVmssVM parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="e149c-218">A New-azvm fedőparaméter-készlet mostantól alapértelmezetten egy elérhető helyet használ, ha az USA keleti régiója nem támogatott</span><span class="sxs-lookup"><span data-stu-id="e149c-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-220">Az ADLS SDK frissítése a httpclient használatához, integrált adatsíkteszteléssel az Azure-keretrendszerben</span><span class="sxs-lookup"><span data-stu-id="e149c-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e149c-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e149c-221">Az.Monitor</span></span>
* <span data-ttu-id="e149c-222">A hibás paraméternevek kijavítása a súgópéldákban</span><span class="sxs-lookup"><span data-stu-id="e149c-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-223">Az.Network</span></span>
* <span data-ttu-id="e149c-224">DisableBgpRoutePropagation jelölő hozzáadása az érvényes útválasztási táblázathoz</span><span class="sxs-lookup"><span data-stu-id="e149c-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="e149c-225">Frissített parancsmag:</span><span class="sxs-lookup"><span data-stu-id="e149c-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="e149c-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="e149c-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="e149c-227">A dupla kötőjel kijavítása a New-AzApplicationGatewayTrustedRootCertificate dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="e149c-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-228">Az.Resources</span></span>
* <span data-ttu-id="e149c-229">Új Get-AzureRmDenyAssignment parancsmag hozzáadása a megtagadási hozzárendelések lekéréséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-230">Az.Sql</span></span>
* <span data-ttu-id="e149c-231">Advanced Threat Protection parancsmagok átnevezése Advanced Data Security névre és a sebezhetőségi felmérés alapértelmezett engedélyezése</span><span class="sxs-lookup"><span data-stu-id="e149c-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="e149c-232">2.0.0 – 2019. május</span><span class="sxs-lookup"><span data-stu-id="e149c-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-233">Az.Accounts</span></span>
* <span data-ttu-id="e149c-234">Az Authentication Library frissítése a felhasználóneves/jelszavas hitelesítéssel kapcsolatos ADFS-problémák kijavításához</span><span class="sxs-lookup"><span data-stu-id="e149c-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e149c-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e149c-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="e149c-236">Csak a Bing jogi nyilatkozat jelenik meg a Bing Search-szolgáltatásoknál.</span><span class="sxs-lookup"><span data-stu-id="e149c-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="e149c-237">A sikertelen fióklétrehozás hibájának javítása.</span><span class="sxs-lookup"><span data-stu-id="e149c-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-238">Az.Compute</span></span>
* <span data-ttu-id="e149c-239">Közelségi elhelyezési csoport szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="e149c-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="e149c-240">A következő új parancsmagok lettek hozzáadva:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e149c-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="e149c-241">Az új ProximityPlacementGroupId paraméter hozzá lett adva a következő parancsmagokhoz:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e149c-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="e149c-242">A StorageAccountType paraméter hozzá lett adva a New-AzGalleryImageVersion parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="e149c-243">A New-AzGalleryImageVersion TargetRegion paramétere tartalmazhatja a következőt: StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="e149c-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="e149c-244">A SkipShutdown kapcsolóparaméter hozzá lett adva a Stop-AzVM és Stop-AzVmss parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="e149c-245">Kompatibilitástörő változások</span><span class="sxs-lookup"><span data-stu-id="e149c-245">Breaking changes</span></span>
    - <span data-ttu-id="e149c-246">A Set-AzVMBootDiagnostics parancsmag új neve: Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="e149c-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="e149c-247">Az Export-AzLogAnalyticThrottledRequests parancsmag új neve: Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="e149c-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="e149c-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="e149c-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="e149c-249">Az Azure Deployment Manager-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="e149c-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="e149c-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="e149c-250">Az.Dns</span></span>
* <span data-ttu-id="e149c-251">Automatikus DNS NameServer-delegálás</span><span class="sxs-lookup"><span data-stu-id="e149c-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="e149c-252">A DNS-zóna létrehozási parancsmag további opcionális paraméterként elfogadja a szülőzóna nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="e149c-253">Névkiszolgálói rekordokat ad hozzá a szülőzónában az újonnan létrehozott gyermekzóna számára.</span><span class="sxs-lookup"><span data-stu-id="e149c-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="e149c-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e149c-254">Az.FrontDoor</span></span>
* <span data-ttu-id="e149c-255">Az Azure FrontDoor-parancsmagok első általánosan elérhető kiadása</span><span class="sxs-lookup"><span data-stu-id="e149c-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="e149c-256">A WAF-parancsmagok új neve tartalmazza a „Waf” sztringet</span><span class="sxs-lookup"><span data-stu-id="e149c-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="e149c-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e149c-257">Az.HDInsight</span></span>
* <span data-ttu-id="e149c-258">A következő két parancsmag el lett távolítva:</span><span class="sxs-lookup"><span data-stu-id="e149c-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="e149c-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e149c-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="e149c-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e149c-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e149c-261">Egy új, Set-AzHDInsightGatewayCredential nevű parancsmag lett hozzáadva a Grant-AzHDInsightHttpServicesAccess helyett</span><span class="sxs-lookup"><span data-stu-id="e149c-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="e149c-262">A Get-AzHDInsightJobOutput parancsmag frissítve lett, hogy különbséget tegyen az olvasói és a HDInsight-operátori szerepkör között:</span><span class="sxs-lookup"><span data-stu-id="e149c-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="e149c-263">Az olvasói szerepkörrel rendelkező felhasználóknak explicit módon meg kell adniuk a DefaultStorageAccountKey paramétert, ellenkező esetben hiba történik.</span><span class="sxs-lookup"><span data-stu-id="e149c-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="e149c-264">A HDInsight-operátori szerepkörrel rendelkező felhasználókat ez nem érinti.</span><span class="sxs-lookup"><span data-stu-id="e149c-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e149c-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e149c-265">Az.Monitor</span></span>
* <span data-ttu-id="e149c-266">Az SQR API (ütemezett lekérdezési szabály) új parancsmagjai</span><span class="sxs-lookup"><span data-stu-id="e149c-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="e149c-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="e149c-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="e149c-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="e149c-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="e149c-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="e149c-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="e149c-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="e149c-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="e149c-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="e149c-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="e149c-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="e149c-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="e149c-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e149c-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e149c-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e149c-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e149c-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e149c-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e149c-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e149c-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e149c-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e149c-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="e149c-278">[További](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) információk az SQR API-ról</span><span class="sxs-lookup"><span data-stu-id="e149c-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="e149c-279">A frissített Az.Monitor.md tartalmazza a GenV2 (nem klasszikus) metrikaalapú riasztási szabály parancsmagjait</span><span class="sxs-lookup"><span data-stu-id="e149c-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-280">Az.Network</span></span>
* <span data-ttu-id="e149c-281">A NAT-átjáró erőforrás támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="e149c-282">Új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e149c-282">New cmdlets</span></span>
        - <span data-ttu-id="e149c-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e149c-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="e149c-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e149c-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="e149c-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e149c-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="e149c-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e149c-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="e149c-287">Frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e149c-287">Updated cmdlets</span></span>
        - <span data-ttu-id="e149c-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e149c-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="e149c-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="e149c-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="e149c-290">Az alábbi parancsok frissítve lettek a következő szolgáltatás esetében: Egyéni útvonalak beállítása/eltávolítása a Brooklyn Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e149c-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="e149c-291">Frissült a New-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e149c-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="e149c-292">Frissült a Set-AzVirtualNetworkGateway: Az új opcionális -CustomRoute paraméter hozzá lett adva a címelőtagok egyéni útvonalként való beállításához a Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e149c-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e149c-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="e149c-294">A szabályzat-kiértékelési adatok lekérdezésének támogatása.</span><span class="sxs-lookup"><span data-stu-id="e149c-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="e149c-295">Az -Expand paraméter hozzá lett adva a Get-AzPolicyState parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="e149c-296">Az -Expand PolicyEvaluationDetails támogatása.</span><span class="sxs-lookup"><span data-stu-id="e149c-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-298">Az előfizetések közötti Azure–Azure Site Recovery átvitel támogatása.</span><span class="sxs-lookup"><span data-stu-id="e149c-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="e149c-299">Az Azure Site Recovery jövőbeni kompatibilitástörő változásainak jelölése.</span><span class="sxs-lookup"><span data-stu-id="e149c-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="e149c-300">Ki lett javítva az Azure Site Recovery helyreállítási és műveletterve.</span><span class="sxs-lookup"><span data-stu-id="e149c-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="e149c-301">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure hálózatleképezés.</span><span class="sxs-lookup"><span data-stu-id="e149c-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="e149c-302">Ki lett javítva a következő Azure Site Recovery-frissítés: Azure–Azure védelemirány felügyelt lemezek esetében.</span><span class="sxs-lookup"><span data-stu-id="e149c-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="e149c-303">További kisebb javítások.</span><span class="sxs-lookup"><span data-stu-id="e149c-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="e149c-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e149c-304">Az.Relay</span></span>
* <span data-ttu-id="e149c-305">Az elgépelések ki lettek javítva az ügyféloldali üzenetekben</span><span class="sxs-lookup"><span data-stu-id="e149c-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e149c-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e149c-306">Az.ServiceBus</span></span>
* <span data-ttu-id="e149c-307">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="e149c-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-308">Az.Storage</span></span>
* <span data-ttu-id="e149c-309">A Storage ügyféloldali kódtárának frissítése a 10.0.1-es verziójára (az SDK összes objektuma esetében módosul a névtér a Microsoft.WindowsAzure.Storage. *névtérről a Microsoft.Azure.Storage.* névtérre)</span><span class="sxs-lookup"><span data-stu-id="e149c-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="e149c-310">Frissítés a Microsoft.Azure.Management.Storage 11.0.0-s verziójára az új API-verzió (2019. 04. 01.) támogatásához.</span><span class="sxs-lookup"><span data-stu-id="e149c-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="e149c-311">A Tárfiók létrehozása parancs esetében az alapértelmezett Storage-fiókaltípus a Storage helyett mostantól a StorageV2.</span><span class="sxs-lookup"><span data-stu-id="e149c-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="e149c-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e149c-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="e149c-313">A Storage-fiók Sku.Name parancsmagkimenete módosul, hogy igazodjon a bemeneti SkuName paraméterhez, egy aláhúzásjel („_”) hozzáadásával – például a StandardLRS a Standard_LRS névre módosul</span><span class="sxs-lookup"><span data-stu-id="e149c-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="e149c-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e149c-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="e149c-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e149c-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="e149c-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e149c-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-317">Az.Websites</span></span>
* <span data-ttu-id="e149c-318">Az Altípus tulajdonság mostantól meg lesz adva a Get-AzWebApp által visszaadott PSSite objektumokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="e149c-319">A Get-AzWebApp\*Metrics és a Get-AzAppServicePlanMetrics megjelölve elavultként</span><span class="sxs-lookup"><span data-stu-id="e149c-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="e149c-320">1.8.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="e149c-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e149c-321">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="e149c-321">Highlights since the last major release</span></span>
* <span data-ttu-id="e149c-322">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="e149c-322">General availability of `Az` module</span></span>
* <span data-ttu-id="e149c-323">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e149c-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e149c-324">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e149c-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e149c-325">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e149c-326">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e149c-327">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e149c-328">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e149c-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-329">Az.Accounts</span></span>
* <span data-ttu-id="e149c-330">Eltávolítás-AzureRm megfelelően törölni a Mac modulok frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="e149c-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e149c-331">Az.Batch</span></span>
* <span data-ttu-id="e149c-332">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e149c-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e149c-333">Az.Cdn</span></span>
* <span data-ttu-id="e149c-334">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e149c-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e149c-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="e149c-336">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-337">Az.Compute</span></span>
* <span data-ttu-id="e149c-338">Az AEM telepítési kapcsolatos problémák megoldásához, ha a lemezek erőforrás-azonosítók kisbetűs resourcegroups volt az erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e149c-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="e149c-339">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-340">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e149c-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e149c-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e149c-341">Az.DataFactory</span></span>
* <span data-ttu-id="e149c-342">Adjon hozzá SsisProperties, ha a NodeCount felügyelt integrációs modul nem null értékű.</span><span class="sxs-lookup"><span data-stu-id="e149c-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-344">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e149c-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e149c-345">Az.EventGrid</span></span>
* <span data-ttu-id="e149c-346">A Súgó szöveg jelzi, hogy erőforrásokat kell létrehozni a create/update eseményt előfizetés parancsmagok használata előtt végpont frissítése.</span><span class="sxs-lookup"><span data-stu-id="e149c-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e149c-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e149c-347">Az.EventHub</span></span>
* <span data-ttu-id="e149c-348">Új parancsmagok hozzáadása az NetworkRuleSet, Namespace</span><span class="sxs-lookup"><span data-stu-id="e149c-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="e149c-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="e149c-349">Az.HDInsight</span></span>
* <span data-ttu-id="e149c-350">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e149c-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e149c-351">Az.IotHub</span></span>
* <span data-ttu-id="e149c-352">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e149c-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e149c-353">Az.KeyVault</span></span>
* <span data-ttu-id="e149c-354">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-355">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e149c-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="e149c-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e149c-356">Az.MachineLearning</span></span>
* <span data-ttu-id="e149c-357">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="e149c-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e149c-358">Az.Media</span></span>
* <span data-ttu-id="e149c-359">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e149c-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e149c-360">Az.Monitor</span></span>
  * <span data-ttu-id="e149c-361">Riasztási szabály (nem klasszikus) GenV2 mérőszám-alapú új parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e149c-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="e149c-362">Új AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="e149c-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="e149c-363">Új AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="e149c-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="e149c-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e149c-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e149c-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e149c-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="e149c-366">Adjon hozzá AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="e149c-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="e149c-367">Frissített verzió 0.22.0-preview figyelő SDK</span><span class="sxs-lookup"><span data-stu-id="e149c-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-368">Az.Network</span></span>
* <span data-ttu-id="e149c-369">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-370">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e149c-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="e149c-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="e149c-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="e149c-372">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e149c-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="e149c-374">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="e149c-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="e149c-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="e149c-376">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-378">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-379">Frissített táblázatos formában az SQL azure-beli virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="e149c-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="e149c-380">A hozzáadott alternatív módszert AzureFileShare hely beolvasása</span><span class="sxs-lookup"><span data-stu-id="e149c-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="e149c-381">Frissített ScheduleRunDays SchedulePolicy objektumban időzóna szerint</span><span class="sxs-lookup"><span data-stu-id="e149c-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e149c-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e149c-382">Az.RedisCache</span></span>
* <span data-ttu-id="e149c-383">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-384">Az.Resources</span></span>
* <span data-ttu-id="e149c-385">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e149c-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-386">Az.Sql</span></span>
* <span data-ttu-id="e149c-387">Cserélje le a függőségi figyelő SDK közös kód</span><span class="sxs-lookup"><span data-stu-id="e149c-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="e149c-388">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-389">Továbbfejlesztett folyamat, amely több oszlop osztályozási.</span><span class="sxs-lookup"><span data-stu-id="e149c-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="e149c-390">Termékváltozat tulajdonságok (termékváltozat neve, családi, kapacitás) válasz a Get-AzSqlServerServiceObjective és formátum táblaként alapértelmezés szerint tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e149c-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="e149c-391">Lehetővé teszi a Get-AzSqlServerServiceObjective anélkül, hogy a régióban egy már létező kiszolgáló hely alapján.</span><span class="sxs-lookup"><span data-stu-id="e149c-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="e149c-392">Hozzon létre felügyelt példányt az időzóna-paraméter támogatása.</span><span class="sxs-lookup"><span data-stu-id="e149c-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="e149c-393">Javítsa ki a helyettesítő karakterek dokumentációja</span><span class="sxs-lookup"><span data-stu-id="e149c-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-394">Az.Websites</span></span>
* <span data-ttu-id="e149c-395">a Set-AzWebApp és a Set-AzWebAppSlot távolítja el a címkék a végrehajtási javítások</span><span class="sxs-lookup"><span data-stu-id="e149c-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="e149c-396">A parancsmagok frissítése többes számú főneveket, és egyes elavult többes számú nevét.</span><span class="sxs-lookup"><span data-stu-id="e149c-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="e149c-397">A webhelyek SDK frissítése.</span><span class="sxs-lookup"><span data-stu-id="e149c-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="e149c-398">A AdminSiteName tulajdonság PSAppServicePlan eltávolítani.</span><span class="sxs-lookup"><span data-stu-id="e149c-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="e149c-399">1.7.0 – 2019. április</span><span class="sxs-lookup"><span data-stu-id="e149c-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e149c-400">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="e149c-400">Highlights since the last major release</span></span>
* <span data-ttu-id="e149c-401">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="e149c-401">General availability of `Az` module</span></span>
* <span data-ttu-id="e149c-402">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e149c-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e149c-403">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e149c-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e149c-404">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e149c-405">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e149c-406">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e149c-407">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="e149c-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-408">Az.Accounts</span></span>
* <span data-ttu-id="e149c-409">Frissített Add-AzEnvironment és Set-AzEnvironment parancsmag az AzureAnalysisServicesEndpointResourceId paraméter elfogadásához</span><span class="sxs-lookup"><span data-stu-id="e149c-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e149c-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e149c-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="e149c-411">ServiceClient használata DataPlane-parancsmagokban és az eredeti hitelesítési logika eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e149c-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="e149c-412">Az Add-AzureASAccount burkolóként való megadása a Connect-AzAccount számára a kompatibilitástörő változás elkerüléséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-413">Az.Automation</span></span>
* <span data-ttu-id="e149c-414">Ki lett javítva a New-AzAutomationSoftwareUpdateConfiguration parancsmag belefoglalásokat érintő hibája.</span><span class="sxs-lookup"><span data-stu-id="e149c-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="e149c-415">Az IncludedKbNumber és az IncludedPackageNameMask paraméter mostantól működőképes.</span><span class="sxs-lookup"><span data-stu-id="e149c-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="e149c-416">Hibajavítás az Azure Automation frissítéskezelési dinamikus csoportja esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-417">Az.Compute</span></span>
* <span data-ttu-id="e149c-418">HyperVGeneration paraméter hozzáadása a New-AzDiskConfig és a New-AzSnapshotConfig parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="e149c-419">Virtuális gépek más bérlők katalógus-rendszerképével való létrehozásának engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e149c-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="e149c-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="e149c-421">Ki lett javítva a New-AzContainerGroup üres záró argumentumot hozzáadó -Command paraméterével kapcsolatos hiba</span><span class="sxs-lookup"><span data-stu-id="e149c-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e149c-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e149c-422">Az.DataFactory</span></span>
* <span data-ttu-id="e149c-423">Az ADF .Net SDK verziója 3.0.2-re frissült.</span><span class="sxs-lookup"><span data-stu-id="e149c-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="e149c-424">A Set-AzDataFactoryV2 parancsmag a RepoConfiguration beállításaihoz tartozó kiegészítő paraméterekkel lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="e149c-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-425">Az.Resources</span></span>
* <span data-ttu-id="e149c-426">Továbbfejlesztett szolgáltatókezelés a Get-AzResource esetében, -ResourceId vagy -ResourceGroupName, -Name és -ResourceType paraméterek megadásakor</span><span class="sxs-lookup"><span data-stu-id="e149c-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="e149c-427">Továbbfejlesztett hibakezelés a Test-AzDeployment és a Test-AzResourceGroupDeployment esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="e149c-428">A hibákat nem a telepítés ellenőrzése során kezeli, hanem a parancs kimenetébe foglalja bele</span><span class="sxs-lookup"><span data-stu-id="e149c-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="e149c-429">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e149c-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="e149c-430">-IgnoreDynamicParameters kapcsolóparaméter hozzáadása telepítési parancsmagokhoz a rendszer által feltett kérdések szkriptekben és feladatokban való mellőzéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="e149c-431">További információ: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="e149c-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-432">Az.Sql</span></span>
* <span data-ttu-id="e149c-433">Adatbázisadat-besorolás támogatása.</span><span class="sxs-lookup"><span data-stu-id="e149c-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-434">Az.Storage</span></span>
* <span data-ttu-id="e149c-435">Részletes hibaüzenet megjelenítése Storage-környezet -UseConnectedAccount paraméterrel történő létrehozásakor az Azure-fiókba való bejelentkezés nélkül</span><span class="sxs-lookup"><span data-stu-id="e149c-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="e149c-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e149c-436">New-AzStorageContext</span></span>
* <span data-ttu-id="e149c-437">Adott Storage-fiók Blob service-tulajdonságai kezelésének támogatása Management plane API-val</span><span class="sxs-lookup"><span data-stu-id="e149c-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="e149c-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e149c-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e149c-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e149c-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="e149c-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e149c-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="e149c-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e149c-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="e149c-442">Az -AsJob támogatása blobok és fájlok feltöltéséhez, valamint parancsmagok letöltéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="e149c-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e149c-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e149c-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="e149c-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="e149c-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e149c-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="e149c-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e149c-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="e149c-447">1.6.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="e149c-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="e149c-448">A legutóbbi nagyobb kiadás óta megjelent kiemelt újdonságok</span><span class="sxs-lookup"><span data-stu-id="e149c-448">Highlights since the last major release</span></span>
* <span data-ttu-id="e149c-449">A(z) `Az` modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="e149c-449">General availability of `Az` module</span></span>
* <span data-ttu-id="e149c-450">Ha további információt szeretne a(z) `Az` modulról, látogasson el a következő helyre: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="e149c-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="e149c-451">Új Location-, ResourceGroup- és ResourceName-befejezők hozzáadása: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="e149c-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="e149c-452">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz az Az.Compute és az Az.Network esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="e149c-453">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e149c-454">Mostantól támogatottak a Python 2-runbookok az Az.Automation esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="e149c-455">Az.LogicApp: Új parancsmagok az integrációs fiók szerelvényeihez és a Batch-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-456">Az.Automation</span></span>
* <span data-ttu-id="e149c-457">Az Azure Automation frissítéskezelése módosult, hogy támogassa az alábbi új funkciókat:</span><span class="sxs-lookup"><span data-stu-id="e149c-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="e149c-458">Dinamikus csoportosítás</span><span class="sxs-lookup"><span data-stu-id="e149c-458">Dynamic grouping</span></span>
    * <span data-ttu-id="e149c-459">Előzetesen és utólagosan futtatandó szkriptek</span><span class="sxs-lookup"><span data-stu-id="e149c-459">Pre-Post script</span></span>
    * <span data-ttu-id="e149c-460">Újraindítási beállítás</span><span class="sxs-lookup"><span data-stu-id="e149c-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-461">Az.Compute</span></span>
* <span data-ttu-id="e149c-462">Ki lett javítva az elérési útvonal feloldásával kapcsolatos hiba a Get-AzVmBootDiagnosticsData esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="e149c-463">A Compute ügyfélkódtár frissült a 25.0.0 verzióra</span><span class="sxs-lookup"><span data-stu-id="e149c-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e149c-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e149c-464">Az.KeyVault</span></span>
* <span data-ttu-id="e149c-465">Helyettesítő karakterek támogatásának hozzáadása a KeyVault-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-466">Az.Network</span></span>
* <span data-ttu-id="e149c-467">Az Intelligens veszélyforrás-felderítés támogatásának hozzáadása az Azure Firewallhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="e149c-468">Az Application Gateway-tűzfalszabályzat legfelső szintű erőforrása és egyéni szabályok hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-470">A SnapshotRetentionInDays hozzáadása az Azure-beli virtuális gépek szabályzatához az azonnali RP támogatása érdekében</span><span class="sxs-lookup"><span data-stu-id="e149c-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="e149c-471">Folyamat támogatásának hozzáadása a regisztrációtörlési tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-472">Az.Resources</span></span>
* <span data-ttu-id="e149c-473">Helyettesítő karakterek támogatásának hozzáadása a Get-AzResource és Get-AzResourceGroup esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="e149c-474">Az ARM általános hívása esetén használt hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-475">Az.Sql</span></span>
* <span data-ttu-id="e149c-476">A Fenyegetésészlelés parancsmagjainak paramétere (ExcludeDetectionType) a DetectionType helyett string[] lett, hogy a jövőben is használható legyen az új DetectionType-ok hozzáadásakor, valamint az automatikus kitöltés támogatása érdekében.</span><span class="sxs-lookup"><span data-stu-id="e149c-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-477">Az.Storage</span></span>
* <span data-ttu-id="e149c-478">Tárfiók felügyeleti szabályzata lekérésének/beállításának/eltávolításának támogatása</span><span class="sxs-lookup"><span data-stu-id="e149c-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="e149c-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e149c-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e149c-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e149c-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e149c-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="e149c-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="e149c-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="e149c-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="e149c-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="e149c-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="e149c-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="e149c-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-485">Az.Websites</span></span>
* <span data-ttu-id="e149c-486">Ki lett javítva az ARM-sablon azon hibája, amely miatt meghiúsul az összes tárolóhely a New-AzWebApp - IncludeSourceWebAppSlots használatával történő klónozása</span><span class="sxs-lookup"><span data-stu-id="e149c-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="e149c-487">1.5.0 – 2019. március</span><span class="sxs-lookup"><span data-stu-id="e149c-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-488">Az.Accounts</span></span>
* <span data-ttu-id="e149c-489">A Register-AzModule parancs hozzáadása az AutoRest által létrehozott parancsmagok támogatásához</span><span class="sxs-lookup"><span data-stu-id="e149c-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="e149c-490">A Connect-AzAccount példáinak frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-491">Az.Automation</span></span>
* <span data-ttu-id="e149c-492">A bizonyos havi ütemezések lekérésekor jelentkező hiba kijavítva számos Azure Automation-parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="e149c-493">Ki lett javítva a hiba, amely miatt a Get-AzAutomationDscNode csak az első 20 csomópontot adta vissza.</span><span class="sxs-lookup"><span data-stu-id="e149c-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="e149c-494">Most már az összes csomópontot visszaadja</span><span class="sxs-lookup"><span data-stu-id="e149c-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e149c-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e149c-495">Az.Cdn</span></span>
* <span data-ttu-id="e149c-496">Új Powershell-parancsmagok hozzáadva az Egyéni tartományi Https engedélyezése/letiltása szolgáltatáshoz, a régiek elavultak</span><span class="sxs-lookup"><span data-stu-id="e149c-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-497">Az.Compute</span></span>
* <span data-ttu-id="e149c-498">Helyettesítő karakterek támogatásának hozzáadása a Get-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e149c-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e149c-499">Az.DataFactory</span></span>
* <span data-ttu-id="e149c-500">Az ADF .Net SDK verziója 3.0.1-re frissült</span><span class="sxs-lookup"><span data-stu-id="e149c-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e149c-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e149c-501">Az.LogicApp</span></span>
* <span data-ttu-id="e149c-502">Ki lett javítva a hiba, amely miatt a ListWorkflows csak az eredmények első oldalát kérte le</span><span class="sxs-lookup"><span data-stu-id="e149c-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-503">Az.Network</span></span>
* <span data-ttu-id="e149c-504">Helyettesítő karakterek támogatásának hozzáadása a Network-parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-506">Azure-beli virtuális gépen futtatott SQL Server támogatásának hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e149c-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="e149c-507">SDK-frissítés</span><span class="sxs-lookup"><span data-stu-id="e149c-507">SDK Update</span></span>
* <span data-ttu-id="e149c-508">VMappContainer ellenőrzés eltávolítva a Get-ProtectableItem parancsmagból</span><span class="sxs-lookup"><span data-stu-id="e149c-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="e149c-509">Name és ServerName paraméterek hozzáadva a Get-ProtectableItem parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-510">Az.Resources</span></span>
* <span data-ttu-id="e149c-511">`-TemplateObject` paraméter hozzáadva az üzembe helyező parancsmagokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="e149c-512">További információ: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="e149c-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="e149c-513">Ki lett javítva a hiba, amely akkor jelentkezett, amikor a(z) `Get-AzResource` eredménye át lett irányítva a következőbe: `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="e149c-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="e149c-514">További információ: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="e149c-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="e149c-515">Ki lett javítva a JSON-adattípus módosításával kapcsolatos probléma, amely a(z) `Set-AzResource` futtatásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="e149c-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="e149c-516">További információ: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="e149c-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-517">Az.Sql</span></span>
* <span data-ttu-id="e149c-518">Az AuditingEndpointsCommunicator frissítése.</span><span class="sxs-lookup"><span data-stu-id="e149c-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="e149c-519">Ki lett javítva az új diagnosztikai beállítások létrehozásakor jelentkező ritka eset viselkedése.</span><span class="sxs-lookup"><span data-stu-id="e149c-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-520">Az.Storage</span></span>
* <span data-ttu-id="e149c-521">A BlockBlobStorage altípus támogatása a Storage-fiók létrehozásakor      - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e149c-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="e149c-522">1.4.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="e149c-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="e149c-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e149c-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="e149c-524">Az AddAzureASAccount parancsmag elavult</span><span class="sxs-lookup"><span data-stu-id="e149c-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-525">Az.Automation</span></span>
* <span data-ttu-id="e149c-526">Az Import-AzAutomationDscNodeConfiguration súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="e149c-527">A konfigurációnév-ellenőrzés hozzáadva az Import-AzAutomationDscConfiguration parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="e149c-528">Továbbfejlesztett hibakezelés az Import-AzAutomationDscConfiguration parancsmag esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="e149c-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e149c-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="e149c-530">A CustomSubdomainName új választható paraméterként hozzáadva a New-AzCognitiveServicesAccount parancsmaghoz, amellyel altartomány adható meg az erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-531">Az.Compute</span></span>
* <span data-ttu-id="e149c-532">Kijavítva az azonosító paraméterkészleteivel kapcsolatos probléma</span><span class="sxs-lookup"><span data-stu-id="e149c-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="e149c-533">Frissült a Get-AzVMExtension parancsmag, hogy az összes telepített bővítményt listázza, ha a Name paraméter nincs megadva</span><span class="sxs-lookup"><span data-stu-id="e149c-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="e149c-534">A Tag és a ResourceId paraméterek hozzáadva az Update-AzImage parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="e149c-535">A Get-AzVmssVM példányazonosító nélkül, az InstanceView használatával példánynézetben listázni tudja a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="e149c-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-537">Parancsmagok hozzáadása a törölt ADL-elemek enumerálásához és visszaállításához</span><span class="sxs-lookup"><span data-stu-id="e149c-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="e149c-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="e149c-538">Az.EventHub</span></span>
* <span data-ttu-id="e149c-539">Új SkipEmptyArchives logikai tulajdonság hozzáadva az üres archívumok kihagyásához az Eventhub CaptureDescription osztályában</span><span class="sxs-lookup"><span data-stu-id="e149c-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="e149c-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e149c-540">Az.KeyVault</span></span>
* <span data-ttu-id="e149c-541">A Set-AzKeyVaultSecret címkézésének kijavítása</span><span class="sxs-lookup"><span data-stu-id="e149c-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e149c-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e149c-542">Az.LogicApp</span></span>
* <span data-ttu-id="e149c-543">Hozzáadva az integrációs fiókok alapszintű termékváltozatában</span><span class="sxs-lookup"><span data-stu-id="e149c-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="e149c-544">Hozzáadva az XSLT 2.0-ban, az XSLT 3.0-ban és a Liquid leképezéstípusok esetén</span><span class="sxs-lookup"><span data-stu-id="e149c-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="e149c-545">Új parancsmagok az integrációs fiók szerelvényeihez</span><span class="sxs-lookup"><span data-stu-id="e149c-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="e149c-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e149c-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e149c-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e149c-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e149c-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e149c-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="e149c-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e149c-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="e149c-550">Új parancsmagok az integrációs fiók kötegkonfigurációjához</span><span class="sxs-lookup"><span data-stu-id="e149c-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="e149c-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e149c-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e149c-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e149c-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e149c-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e149c-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="e149c-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e149c-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="e149c-555">A Logic Apps SDK frissítése a 4.1.0-s verzióra</span><span class="sxs-lookup"><span data-stu-id="e149c-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="e149c-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e149c-556">Az.Monitor</span></span>
* <span data-ttu-id="e149c-557">A Get-AzMetric súgójának frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-558">Az.Network</span></span>
* <span data-ttu-id="e149c-559">Az Add-AzApplicationGatewayCustomError súgójában lévő példa frissítése</span><span class="sxs-lookup"><span data-stu-id="e149c-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="e149c-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="e149c-561">Kibővített támogatás a New és a Get ApplicationInsights adatforráshoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="e149c-562">Új „ApplicationInsights” altípus hozzáadva az adott munkaterület Get specific és Get all Application Insights-adatforrásainak támogatásához.</span><span class="sxs-lookup"><span data-stu-id="e149c-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="e149c-563">A New-AzOperationalInsightsApplicationInsightsDataSource parancsmag hozzáadva adatforrás létrehozásához a következő Application Insights-erőforrásparaméterekkel: subscriptionId, resourceGroupName és name.</span><span class="sxs-lookup"><span data-stu-id="e149c-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="e149c-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-564">Az.Resources</span></span>
* <span data-ttu-id="e149c-565">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e149c-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e149c-566">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e149c-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="e149c-567">A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="e149c-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="e149c-568">Ki lett javítva a KeyCredentials ismételt létrehozását megakadályozó hiba</span><span class="sxs-lookup"><span data-stu-id="e149c-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-569">Az.Sql</span></span>
* <span data-ttu-id="e149c-570">Rugalmas SQL DB-skálázási szint támogatása hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="e149c-571">Ki lett javítva az a hiba, hogy a visszaállítási kérésben szereplő szükségtelen tulajdonságok megadása miatt a visszaállítás esetenként meghiúsult</span><span class="sxs-lookup"><span data-stu-id="e149c-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-572">Az.Websites</span></span>
* <span data-ttu-id="e149c-573">A Get-AzWebAppSlotMetrics példájának javítása</span><span class="sxs-lookup"><span data-stu-id="e149c-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="e149c-574">1.3.0 – 2019. február</span><span class="sxs-lookup"><span data-stu-id="e149c-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-575">Az.Accounts</span></span>
* <span data-ttu-id="e149c-576">Frissítés a ClientRuntime legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="e149c-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e149c-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e149c-577">Az.AnalysisServices</span></span>
<span data-ttu-id="e149c-578">Az Az.AnalysisServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="e149c-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-579">Az.Compute</span></span>
* <span data-ttu-id="e149c-580">AEM-bővítmény: Mostantól az UltraSSD, valamint a P60, P70 és P80 lemezek támogatottak.</span><span class="sxs-lookup"><span data-stu-id="e149c-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="e149c-581">A Set-AzVMBootDiagnostics súgóleírása frissült.</span><span class="sxs-lookup"><span data-stu-id="e149c-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="e149c-582">Az Update-AzImage súgóleírása és példája frissült.</span><span class="sxs-lookup"><span data-stu-id="e149c-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-583">Az.RecoveryServices</span></span>
<span data-ttu-id="e149c-584">Az Az.RecoveryServices modul általános rendelkezésre állása.</span><span class="sxs-lookup"><span data-stu-id="e149c-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-585">Az.Resources</span></span>
* <span data-ttu-id="e149c-586">Az erőforráscsoportok címkézése ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="e149c-587">További információ: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="e149c-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="e149c-588">Ki lett javítva az a hiba, amikor a `Get-AzureRmRoleAssignment` nem vette figyelembe az -ErrorAction paramétert.</span><span class="sxs-lookup"><span data-stu-id="e149c-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="e149c-589">További információ: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="e149c-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-590">Az.Sql</span></span>
* <span data-ttu-id="e149c-591">Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="e149c-592">Ki lett javítva az a hiba, amikor az Azure-fiókba való bejelentkezés hiánya nullref kivételt eredményezett az SQL-parancsmagok végrehajtásakor.</span><span class="sxs-lookup"><span data-stu-id="e149c-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="e149c-593">A nullref kivétel ki lett javítva a Get-AzSqlCapabilityben.</span><span class="sxs-lookup"><span data-stu-id="e149c-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="e149c-594">1.2.1 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="e149c-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-595">Az.Accounts</span></span>
* <span data-ttu-id="e149c-596">A hitelesítés megfelelő verziójával rendelkező kiadás</span><span class="sxs-lookup"><span data-stu-id="e149c-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="e149c-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e149c-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="e149c-598">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="e149c-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="e149c-600">Frissített hitelesítési függőségű kiadás</span><span class="sxs-lookup"><span data-stu-id="e149c-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="e149c-601">1.2.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="e149c-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-602">Az.Accounts</span></span>
* <span data-ttu-id="e149c-603">Interaktív felhasználónév-/jelszó-hitelesítés hozzáadva, csak a Windows PowerShell 5.1 esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="e149c-604">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e149c-605">Az Uninstall-AzureRm figyelmeztető üzenete hozzáadva a PS Core-ban</span><span class="sxs-lookup"><span data-stu-id="e149c-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="e149c-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="e149c-606">Az.Aks</span></span>
* <span data-ttu-id="e149c-607">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="e149c-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-608">Az.Automation</span></span>
* <span data-ttu-id="e149c-609">Mostantól támogatottak a Python 2-runbookok.</span><span class="sxs-lookup"><span data-stu-id="e149c-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="e149c-610">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="e149c-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="e149c-611">Az.Cdn</span></span>
* <span data-ttu-id="e149c-612">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-613">Az.Compute</span></span>
* <span data-ttu-id="e149c-614">Az Invoke-AzVMReimage parancsmag hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="e149c-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="e149c-615">A TempDisk paraméter hozzá lett adva a Set-AzVmss parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="e149c-616">A New-AzVM figyelmeztető üzenete ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="e149c-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e149c-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="e149c-618">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="e149c-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="e149c-619">Az.DataFactory</span></span>
* <span data-ttu-id="e149c-620">Az ADF .Net SDK verziója 3.0.0-ra frissült.</span><span class="sxs-lookup"><span data-stu-id="e149c-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-622">Ki lett javítva az ADLS-végponttal kapcsolatos probléma az MSI használatakor.</span><span class="sxs-lookup"><span data-stu-id="e149c-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="e149c-623">További információ: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="e149c-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="e149c-624">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e149c-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e149c-625">Az.IotHub</span></span>
* <span data-ttu-id="e149c-626">Az Encoding formátum hozzá lett adva az Add-IotHubRoutingEndpoint parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="e149c-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e149c-627">Az.KeyVault</span></span>
* <span data-ttu-id="e149c-628">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-629">Az.Network</span></span>
* <span data-ttu-id="e149c-630">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-631">Az.Resources</span></span>
* <span data-ttu-id="e149c-632">A helytelen példák ki lettek javítva a New-AzADAppCredential és a New-AzADSpCredential referenciadokumentációjában.</span><span class="sxs-lookup"><span data-stu-id="e149c-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="e149c-633">Ki lett javítva az a hiba, amikor a -TemplateFile paraméter nem lett feloldva az erőforráscsoportokat üzembe helyező parancsmagok végrehajtása előtt.</span><span class="sxs-lookup"><span data-stu-id="e149c-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="e149c-634">Az.Resources: A New-AzureRmPolicyDefinition -Mode alapértelmezett értékének dokumentációja ki lett javítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="e149c-635">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="e149c-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="e149c-636">Az.Resources: A következő hiba ki lett javítva: https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="e149c-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="e149c-637">Ki lett javítva a „PSResourceGroupDeployment” objektum formázásával kapcsolatos hiba.</span><span class="sxs-lookup"><span data-stu-id="e149c-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="e149c-638">További információ: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="e149c-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e149c-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e149c-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="e149c-640">Visszaállítás a VMSS-modell tanúsítványának hozzáadásakor bekövetkező kivétel-visszaadás esetén; javított hiba: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="e149c-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="e149c-641">Bizonyos hibaüzenetek ki lettek javítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-641">Fix some error messages.</span></span>
* <span data-ttu-id="e149c-642">Ki lett javítva az alapértelmezett ARM-sablonnal való fürtlétrehozás a New-AzServiceFabriCluster esetében, amely nem működött az Az-ba történő migrálással.</span><span class="sxs-lookup"><span data-stu-id="e149c-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="e149c-643">Ki lett javítva a fürt-/alkalmazástanúsítvány létrehozása, így mostantól csak a fürtnek megfelelő virtuálisgép-méretezési csoportokhoz (Virtual Machine Scale Sets) lesznek hozzáadva, a fürtazonosító bővítményben való ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="e149c-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e149c-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e149c-644">Az.SignalR</span></span>
* <span data-ttu-id="e149c-645">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-646">Az.Sql</span></span>
* <span data-ttu-id="e149c-647">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e149c-648">A LicenseType paraméter paraméterleírása frissítve lett a lehetséges értékekkel.</span><span class="sxs-lookup"><span data-stu-id="e149c-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="e149c-649">Ki lett javítva az a hiba, amikor egy felügyelt példány identitásának frissítése nem működött, ha az volt az egyetlen frissített tulajdonság.</span><span class="sxs-lookup"><span data-stu-id="e149c-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="e149c-650">Egyéni rendezések támogatása a felügyelt példányokon</span><span class="sxs-lookup"><span data-stu-id="e149c-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-651">Az.Storage</span></span>
* <span data-ttu-id="e149c-652">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e149c-653">Részletes hibaüzenet megjelenítése klasszikus naplózás/metrika get/set műveletei esetében a prémium szintű Storage-fiókon, mivel a prémium szintű Storage-fiók nem támogatja a klasszikus naplózást/metrikát.</span><span class="sxs-lookup"><span data-stu-id="e149c-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="e149c-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="e149c-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="e149c-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="e149c-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="e149c-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e149c-656">Az.TrafficManager</span></span>
* <span data-ttu-id="e149c-657">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-658">Az.Websites</span></span>
* <span data-ttu-id="e149c-659">Frissítve lettek az online súgók helytelen URL-címei.</span><span class="sxs-lookup"><span data-stu-id="e149c-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="e149c-660">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól a megfelelő erőforráscsoportba és helyre tölti fel a tanúsítványt, ha az alkalmazás ASE-n üzemel.</span><span class="sxs-lookup"><span data-stu-id="e149c-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="e149c-661">Ki lett javítva a New-AzWebAppSSLBinding, amely mostantól nem írja felül a címkéket SSL-tanúsítvány alkalmazáshoz való kötésekor.</span><span class="sxs-lookup"><span data-stu-id="e149c-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="e149c-662">1.1.0 – 2019. január</span><span class="sxs-lookup"><span data-stu-id="e149c-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="e149c-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-663">Az.Accounts</span></span>
* <span data-ttu-id="e149c-664">A „Local” hatókör hozzá lett adva az Enable-AzureRmAlias parancshoz</span><span class="sxs-lookup"><span data-stu-id="e149c-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-665">Az.Compute</span></span>
* <span data-ttu-id="e149c-666">A Restart/Start/Stop/Remove/Set-AzVM és a Save-AzVMImage parancs azonosítójának paraméterkészletében már nem kötelező nevet megadni</span><span class="sxs-lookup"><span data-stu-id="e149c-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="e149c-667">Frissült az azonosító leírása a súgófájlokban</span><span class="sxs-lookup"><span data-stu-id="e149c-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="e149c-668">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="e149c-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-670">A DataPlane SDK-verziója frissítve lett az 1.1.14-es verzióra az SDK-javítások érdekében.</span><span class="sxs-lookup"><span data-stu-id="e149c-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="e149c-671">A getfilestatus és liststatus negatív acesstime és modificationtime értékeinek kezelése kijavítva, Aszinkron visszavonási jogkivonat kijavítva</span><span class="sxs-lookup"><span data-stu-id="e149c-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="e149c-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="e149c-672">Az.EventGrid</span></span>
* <span data-ttu-id="e149c-673">Frissítve a 2019-01-01-es API-verzió használatára.</span><span class="sxs-lookup"><span data-stu-id="e149c-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="e149c-674">A következő parancsmagok frissítve lettek a 2019-01-01-es API-verzióban található új forgatókönyvek támogatásához</span><span class="sxs-lookup"><span data-stu-id="e149c-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="e149c-675">New-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="e149c-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e149c-676">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="e149c-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e149c-677">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="e149c-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e149c-678">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="e149c-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="e149c-679">Update-AzureRmEventGridSubscription: Új választható paraméterek lettek hozzáadva, amelyekkel megadhatók a következők:</span><span class="sxs-lookup"><span data-stu-id="e149c-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="e149c-680">Az esemény élettartama,</span><span class="sxs-lookup"><span data-stu-id="e149c-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="e149c-681">Az események kézbesítési kísérleteinek maximális száma,</span><span class="sxs-lookup"><span data-stu-id="e149c-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="e149c-682">A kézbesíthetetlen üzenet végpontja.</span><span class="sxs-lookup"><span data-stu-id="e149c-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="e149c-683">Új felsorolási értékek (storageQueue és hybridConnection) lettek hozzáadva a New-AzureRmEventGridSubscription és az Update-AzureRmEventGridSubscription parancsmag EndpointType beállításához.</span><span class="sxs-lookup"><span data-stu-id="e149c-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="e149c-684">Figyelmeztető üzenet jelenik meg, ha az esemény-előfizetés létrehozása vagy frissítése várhatóan manuális felhasználói műveletet von maga után.</span><span class="sxs-lookup"><span data-stu-id="e149c-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="e149c-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="e149c-685">Az.IotHub</span></span>
* <span data-ttu-id="e149c-686">Frissítve az IoT Hub SDK legújabb verziójára</span><span class="sxs-lookup"><span data-stu-id="e149c-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="e149c-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="e149c-687">Az.LogicApp</span></span>
* <span data-ttu-id="e149c-688">A Get-AzLogicApp mindent listáz, ami nem rendelkezik megadott névvel</span><span class="sxs-lookup"><span data-stu-id="e149c-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-689">Az.Resources</span></span>
* <span data-ttu-id="e149c-690">Ki lett javítva a paraméterkészlettel kapcsolatos hiba, amely a Get-AzResource parancs -ODataQuery és -ResourceId paramétereinek megadásakor jelentkezett</span><span class="sxs-lookup"><span data-stu-id="e149c-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="e149c-691">További információ: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="e149c-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="e149c-692">Ki lett javítva a -Custom paraméter kezelése a New/Set-AzPolicyDefinition parancsban</span><span class="sxs-lookup"><span data-stu-id="e149c-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e149c-693">Az elgépelés ki lett javítva a New-AzDeployment dokumentációjában</span><span class="sxs-lookup"><span data-stu-id="e149c-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="e149c-694">A -MailNickname paraméter mostantól kötelező a New-AzADUser esetében</span><span class="sxs-lookup"><span data-stu-id="e149c-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="e149c-695">További információ: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="e149c-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="e149c-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="e149c-696">Az.SignalR</span></span>
* <span data-ttu-id="e149c-697">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="e149c-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-698">Az.Sql</span></span>
* <span data-ttu-id="e149c-699">A Tárolókezelési ügyfélfüggőség át lett alakítva az általános SDK-implementációra.</span><span class="sxs-lookup"><span data-stu-id="e149c-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="e149c-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-700">Az.Storage</span></span>
* <span data-ttu-id="e149c-701">A Tároló környezetének StorageAccountName neve a tároló valódi fiókneveként lett beállítva, ha az Sas-jogkivonat, OAuth vagy Anonymous segítségével lett létrehozva</span><span class="sxs-lookup"><span data-stu-id="e149c-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="e149c-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e149c-702">New-AzStorageContext</span></span>
* <span data-ttu-id="e149c-703">A Blob-pillanatkép objektum SAS-jogkivonatának a -FullUri paraméterrel való létrehozásakor a visszaadott URI most már a pillanatkép URI-ja lesz</span><span class="sxs-lookup"><span data-stu-id="e149c-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="e149c-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="e149c-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-705">Az.Websites</span></span>
* <span data-ttu-id="e149c-706">Ki lett javítva egy dátumelemzéssel kapcsolatos hiba a Get-AzDeletedWebApp parancsmagban</span><span class="sxs-lookup"><span data-stu-id="e149c-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="e149c-707">Az Az.Accounts modullal kapcsolatos visszamenőleges kompatibilitási probléma kijavítva</span><span class="sxs-lookup"><span data-stu-id="e149c-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="e149c-708">1.0.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="e149c-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="e149c-709">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="e149c-709">General</span></span>

- <span data-ttu-id="e149c-710">Az Az modul általános rendelkezésre állása</span><span class="sxs-lookup"><span data-stu-id="e149c-710">General Availability of Az Module</span></span>
- <span data-ttu-id="e149c-711">Online súgó az egyes modulokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-711">Online help for each module</span></span>
- <span data-ttu-id="e149c-712">További részletekért és az ütemtervért tekintse meg az [Az bejelentési oldalát](https://aka.ms/azps-announce).</span><span class="sxs-lookup"><span data-stu-id="e149c-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="e149c-713">Az AzureRM-ről való áttelepítéshez tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="e149c-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-714">Az.Accounts</span></span>
- <span data-ttu-id="e149c-715">Változások az Az.Profile-hoz képest</span><span class="sxs-lookup"><span data-stu-id="e149c-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="e149c-716">Rögzített táblázatformátumok profil- és a környezettípusokhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e149c-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e149c-717">Az.ApiManagement</span></span>
- <span data-ttu-id="e149c-718">A 7002-es hiba javításai</span><span class="sxs-lookup"><span data-stu-id="e149c-718">Fixes for #7002</span></span>
- <span data-ttu-id="e149c-719">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="e149c-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e149c-720">Az.Batch</span></span>
- <span data-ttu-id="e149c-721">A(z) `PSComputeNode` új `NodeAgentInformation` tulajdonsága mostantól lehetővé teszi annak megtekintését, hogy az Azure Batch-csomóponti ügynök melyik verziója fut a készlet egyes virtuális gépein.</span><span class="sxs-lookup"><span data-stu-id="e149c-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="e149c-722">A `PSDataDisk` alapértelmezett `Caching`-értéke mostantól `None` helyett `ReadWrite` lesz.</span><span class="sxs-lookup"><span data-stu-id="e149c-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="e149c-723">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="e149c-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="e149c-724">Az.Billing</span></span>
- <span data-ttu-id="e149c-725">Egyesíti a Billing, a Consumption és a UsageAggregates parancsmagot. További részleteket a [migrálási útmutatóban](https://aka.ms/azps-migration-guide) talál.</span><span class="sxs-lookup"><span data-stu-id="e149c-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="e149c-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="e149c-726">Az.CognitivServices</span></span>
- <span data-ttu-id="e149c-727">A New-AzureRmCognitiveServicesAccount műveletben elérhető SkuName és Typem bővítése befejezőkkel.</span><span class="sxs-lookup"><span data-stu-id="e149c-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="e149c-728">A GetSkusWithAccountParamSetName paraméter eltávolítása a Get-AzCognitiveServicesAccountSkus parancsmagból.</span><span class="sxs-lookup"><span data-stu-id="e149c-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e149c-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="e149c-730">ManagedIdentity-támogatás elérhetővé tétele</span><span class="sxs-lookup"><span data-stu-id="e149c-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="e149c-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="e149c-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="e149c-732">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e149c-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="e149c-734">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="e149c-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="e149c-735">Az.Monitor</span></span>
- <span data-ttu-id="e149c-736">Az Az.Insights neve mostantól Az.Monitor. Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="e149c-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e149c-737">Az.KeyVault</span></span>
- <span data-ttu-id="e149c-738">A kimenettípusokból az elavult „PurgeDisabled” tulajdonság el lett távolítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="e149c-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="e149c-739">Az.MachineLearning</span></span>
- <span data-ttu-id="e149c-740">Az Az.MachineLearningCompute modulból származó parancsmagokkal lett bővítve</span><span class="sxs-lookup"><span data-stu-id="e149c-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="e149c-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="e149c-741">Az.Media</span></span>
- <span data-ttu-id="e149c-742">Az elavult -Tags alias el lett távolítva a New-AzMediaService parancsmagból</span><span class="sxs-lookup"><span data-stu-id="e149c-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e149c-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-743">Az.Network</span></span>
<span data-ttu-id="e149c-744">Az Application Gateway konfigurációs RewriteRuleSets tulajdonsága mostantól támogatott.</span><span class="sxs-lookup"><span data-stu-id="e149c-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="e149c-745">Új hozzáadott parancsmagok:</span><span class="sxs-lookup"><span data-stu-id="e149c-745">New cmdlets added:</span></span>
        - <span data-ttu-id="e149c-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e149c-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e149c-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e149c-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e149c-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="e149c-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="e149c-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="e149c-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="e149c-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="e149c-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="e149c-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="e149c-754">A -RewriteRuleSet opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e149c-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="e149c-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e149c-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="e149c-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e149c-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e149c-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e149c-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="e149c-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e149c-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="e149c-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="e149c-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="e149c-760">A New-AzureRmApplicationGatewayUrlPathMapConfig az Identity használatával KeyVault-támogatást biztosít az Application Gatewayen.</span><span class="sxs-lookup"><span data-stu-id="e149c-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="e149c-761">A -KeyVaultSecretId, -KeyVaultSecret opcionális paraméterrel frissített parancsmagok</span><span class="sxs-lookup"><span data-stu-id="e149c-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="e149c-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e149c-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e149c-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e149c-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="e149c-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e149c-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="e149c-765">A New-AzApplicationGateway parancsmag frissítve lett a -UserAssignedIdentity opcionális paraméterrel</span><span class="sxs-lookup"><span data-stu-id="e149c-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="e149c-766">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="e149c-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="e149c-768">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="e149c-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e149c-769">Az.Profile</span></span>
- <span data-ttu-id="e149c-770">A modul új neve Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="e149c-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="e149c-772">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="e149c-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-773">Az.Resources</span></span>
- <span data-ttu-id="e149c-774">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e149c-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e149c-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="e149c-776">A tanúsítványok köznapi névvel és ujjlenyomattal történő megadása mostantól támogatott</span><span class="sxs-lookup"><span data-stu-id="e149c-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="e149c-777">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="e149c-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="e149c-778">Az.SIgnalR</span></span>
- <span data-ttu-id="e149c-779">PowerShell-parancsmagok általános rendelkezésre állása a SIgnalR számára</span><span class="sxs-lookup"><span data-stu-id="e149c-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="e149c-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-780">Az.Sql</span></span>
- <span data-ttu-id="e149c-781">Új Data_Exfiltration és Unsafe_Action észleléstípus hozzáadva a fenyegetésészlelés parancsmagjaihoz</span><span class="sxs-lookup"><span data-stu-id="e149c-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="e149c-782">Frissültek az SQL-naplózási parancsmagok dokumentációs példái</span><span class="sxs-lookup"><span data-stu-id="e149c-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="e149c-783">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="e149c-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-784">Az.Storage</span></span>
- <span data-ttu-id="e149c-785">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e149c-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-786">Az.Websites</span></span>
- <span data-ttu-id="e149c-787">Kisebb kompatibilitástörő változások; a részletekért tekintse meg a [migrálási útmutatót](https://aka.ms/azps-migration-guide).</span><span class="sxs-lookup"><span data-stu-id="e149c-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="e149c-788">0.7.0 – 2018. december</span><span class="sxs-lookup"><span data-stu-id="e149c-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="e149c-789">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="e149c-789">General</span></span>

* <span data-ttu-id="e149c-790">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="e149c-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-791">Az.Compute</span></span>

* <span data-ttu-id="e149c-792">Az UltraSSD és a katalógus-rendszerképek mostantól támogatottak a `New-AzVm(ss)`-parancsmagok egyszerű paraméterkészleteiben.</span><span class="sxs-lookup"><span data-stu-id="e149c-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="e149c-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="e149c-794">A záró perjel javítása az adls-fiók tartományában</span><span class="sxs-lookup"><span data-stu-id="e149c-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="e149c-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e149c-795">Az.FrontDoor</span></span>

* <span data-ttu-id="e149c-796">Egyes hibás hivatkozások javítása</span><span class="sxs-lookup"><span data-stu-id="e149c-796">Fixed some broken links</span></span>
    - <span data-ttu-id="e149c-797">A New-AzureRmFrontDoor és a Set-AzureRmFrontDoor cikkében javítottuk a New-AzureRmFrontDoorHealthProbeSettingObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="e149c-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="e149c-798">A New-AzureRmFrontDoorManagedRuleObject cikkében javítottuk a New-AzureRmFrontDoorRuleGroupOverrideObject parancsmag cikkére mutató hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="e149c-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="e149c-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="e149c-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="e149c-800">Az Azure-fájlmegosztás visszaállítási műveleteiben mostantól lehetőség van ügyféloldali érvényesítésre.</span><span class="sxs-lookup"><span data-stu-id="e149c-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="e149c-801">A storageAccountName és a storageAccountResourceGroupName használata mostantól nem kötelező az afs-visszaállítás során.</span><span class="sxs-lookup"><span data-stu-id="e149c-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="e149c-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-802">Az.Resources</span></span>

* <span data-ttu-id="e149c-803">https://github.com/Azure/azure-powershell/issues/7679 javítása</span><span class="sxs-lookup"><span data-stu-id="e149c-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="e149c-804">A Get-AzureRmRoleAssignment parancsmag frissítve az előfizetési hatókör használatával, ha azt megadták a klasszikus rendszergazdák kérésekor.</span><span class="sxs-lookup"><span data-stu-id="e149c-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="e149c-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-805">Az.Sql</span></span>

* <span data-ttu-id="e149c-806">Kisebb módosítások az AzureRM-ről Az-re történő váltás előkészítéséhez</span><span class="sxs-lookup"><span data-stu-id="e149c-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="e149c-807">Javítva lett a hiba, amely a Get-AzureRmSqlDatabaseVulnerabilityAssessment DotNet-maggal történő használatakor lépett fel</span><span class="sxs-lookup"><span data-stu-id="e149c-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="e149c-808">Módosult az SQL-naplózási parancsmagok súgóüzeneteinek dokumentációja.</span><span class="sxs-lookup"><span data-stu-id="e149c-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="e149c-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-809">Az.Storage</span></span>

* <span data-ttu-id="e149c-810">Az -EnableHierarchicalNamespace paraméter hozzáadva a New-AzureRmStorageAccount parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="e149c-811">Javítva lett a hiba, amely miatt a Fájl másolása parancsmag nem tudja újból felhasználni a forráskörnyezetet a célban, ha nincs megadva a -DestContext paraméter.</span><span class="sxs-lookup"><span data-stu-id="e149c-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="e149c-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e149c-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e149c-813">Statikus webhely-konfiguráció támogatása</span><span class="sxs-lookup"><span data-stu-id="e149c-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="e149c-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e149c-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="e149c-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="e149c-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="e149c-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-816">Az.Websites</span></span>

* <span data-ttu-id="e149c-817">Set-AzureRmWebApp és Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e149c-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="e149c-818">Egy új paraméter (-AzureStoragePath) adja meg a windowsos és linuxos tárolóalkalmazásokban csatlakoztatni kívánt Azure Storage-tárolók elérési útját.</span><span class="sxs-lookup"><span data-stu-id="e149c-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="e149c-819">Az új New-AzureRmWebAppAzureStoragePath parancsmag kimenetét paraméterként használhatja az Azure Storage elérési útjainak megadásához.</span><span class="sxs-lookup"><span data-stu-id="e149c-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="e149c-820">0.6.1 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="e149c-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="e149c-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e149c-821">Az.ApiManagement</span></span>
* <span data-ttu-id="e149c-822">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="e149c-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="e149c-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="e149c-823">Az.Automation</span></span>
* <span data-ttu-id="e149c-824">Swagger-alapú Azure Automation-parancsmagok érhetőek el.</span><span class="sxs-lookup"><span data-stu-id="e149c-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="e149c-825">Update Management-parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="e149c-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="e149c-826">Verziókövetési parancsmagok lettek hozzáadva.</span><span class="sxs-lookup"><span data-stu-id="e149c-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="e149c-827">Elérhető az új Remove-AzureRmAutomationHybridWorkerGroup parancsmag.</span><span class="sxs-lookup"><span data-stu-id="e149c-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="e149c-828">Ki lett javítva a DSC csomópontregisztrálási parancs működése.</span><span class="sxs-lookup"><span data-stu-id="e149c-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="e149c-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-829">Az.Compute</span></span>
* <span data-ttu-id="e149c-830">Ki lett javítva a SystemAssigned identitás problémája.</span><span class="sxs-lookup"><span data-stu-id="e149c-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="e149c-831">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="e149c-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="e149c-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="e149c-833">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="e149c-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="e149c-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="e149c-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="e149c-835">A Marketplace-parancsmagok példáinak leírásai frissültek.</span><span class="sxs-lookup"><span data-stu-id="e149c-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="e149c-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-836">Az.Network</span></span>
* <span data-ttu-id="e149c-837">A következő új parancsmagok érhetőek el: New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="e149c-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="e149c-838">Az ICMP újra bekerült a támogatott Azure Firewall hálózati protokollok közé.</span><span class="sxs-lookup"><span data-stu-id="e149c-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="e149c-839">Frissült a Test-AzureRmNetworkWatcherConnectivity parancsmag, új érvényesítési lehetőségek érhetőek el a célazonosítóra, címre és portra vonatkozóan.</span><span class="sxs-lookup"><span data-stu-id="e149c-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="e149c-840">Ki lettek javítva a memóriahasználattal kapcsolatos problémák a VirtualNetwork leképezésben.</span><span class="sxs-lookup"><span data-stu-id="e149c-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="e149c-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="e149c-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="e149c-842">Javítva lett a védett fájlmegosztások módosítási szabályzata.</span><span class="sxs-lookup"><span data-stu-id="e149c-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="e149c-843">A szabályzat időzónája mostantól nagybetűs.</span><span class="sxs-lookup"><span data-stu-id="e149c-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="e149c-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="e149c-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="e149c-845">Javítottuk a New-AzureRmRecoveryServicesAsrProtectableItem példáját.</span><span class="sxs-lookup"><span data-stu-id="e149c-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="e149c-846">Frissítve lettek a függőségek a típustársítási hiba elhárításához.</span><span class="sxs-lookup"><span data-stu-id="e149c-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="e149c-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="e149c-847">Az.Relay</span></span>
* <span data-ttu-id="e149c-848">A -KeyValue nem kötelező paraméter hozzá lett adva a New-AzureRmRelayKey parancsmaghoz, ami lehetővé teszi, hogy a felhasználó megadja a KeyValue értékét.</span><span class="sxs-lookup"><span data-stu-id="e149c-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="e149c-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-849">Az.Resources</span></span>
* <span data-ttu-id="e149c-850">Frissült a(z) `New-AzureRmPolicyAssignment` és a(z) `Set-AzureRmPolicyAssignment` erőforrás-identitásokkal kapcsolatos paramétereinek súgódokumentációja.</span><span class="sxs-lookup"><span data-stu-id="e149c-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="e149c-851">Hozzáadtunk a New-AzureRmPolicyDefinition parancsmaghoz egy példát, amely a -Metadata paramétert használja.</span><span class="sxs-lookup"><span data-stu-id="e149c-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="e149c-852">Ezeknek az új javításoknak köszönhetően megőrizhetőek a kis- és nagybetűk a NetStandard címkekulcsaiban: #7678 #7703.</span><span class="sxs-lookup"><span data-stu-id="e149c-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="e149c-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e149c-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="e149c-854">Elavulási üzenetek lettek hozzáadva a soron következő kompatibilitástörő változásokhoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="e149c-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-855">Az.Sql</span></span>
* <span data-ttu-id="e149c-856">Új parancsmagok érhetőek el a CRUD műveletekhez az Azure SQL Database felügyelt példányain és a felügyelt Azure SQL-adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="e149c-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="e149c-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e149c-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e149c-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e149c-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="e149c-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="e149c-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e149c-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e149c-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e149c-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e149c-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e149c-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="e149c-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="e149c-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="e149c-865">Mostantól elérhető a naplózási szabályzatok kibővített felügyelete a kiszolgálókon vagy adatbázisokon.</span><span class="sxs-lookup"><span data-stu-id="e149c-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="e149c-866">Egy új paraméter (PredicateExpression) lehetővé teszi a felügyeleti naplók szűrését.</span><span class="sxs-lookup"><span data-stu-id="e149c-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="e149c-867">A módosított parancsmagok mostantól SQL-ügyfeleket használnak a régebbi ügyfelek helyett.</span><span class="sxs-lookup"><span data-stu-id="e149c-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="e149c-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e149c-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e149c-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="e149c-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="e149c-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e149c-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="e149c-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="e149c-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="e149c-872">Javítva lett az Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings azon hibája, amely a tárfióknév paraméter beállítása esetén jelentkezett.</span><span class="sxs-lookup"><span data-stu-id="e149c-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="e149c-873">0.5.0 – 2018. november</span><span class="sxs-lookup"><span data-stu-id="e149c-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="e149c-874">Általános kérdések</span><span class="sxs-lookup"><span data-stu-id="e149c-874">General</span></span>
* <span data-ttu-id="e149c-875">Erőforrás-befejezők hozzáadva számos fő parancsmaghoz. Ezek lehetővé teszik a meglévő erőforrásnevek közötti váltást a parancsmagok interaktív hívásakor.</span><span class="sxs-lookup"><span data-stu-id="e149c-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="e149c-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e149c-876">Az.Profile</span></span>
* <span data-ttu-id="e149c-877">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="e149c-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="e149c-878">A TenantId paraméter a Connect-AzAccount parancsmagban át lett nevezve Tenant névre, és hozzá lett adva egy alias a TenantId-hez</span><span class="sxs-lookup"><span data-stu-id="e149c-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="e149c-879">Frissítve lett a TenantId leírása a Connect-AzAccount parancsmagnál</span><span class="sxs-lookup"><span data-stu-id="e149c-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="e149c-880">Javítva lett a sikertelen bejelentkezéshez tartozó hibaüzenet a bérlő tartományának megadásakor</span><span class="sxs-lookup"><span data-stu-id="e149c-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="e149c-881">Javítva lett a környezet nevének ütközésével kapcsolatos probléma az olyan fiókoknál, amelyeknél a bérlő nem tartalmaz előfizetéseket</span><span class="sxs-lookup"><span data-stu-id="e149c-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="e149c-882">Javítva lett a Data Lake-végpontokkal kapcsolatos probléma az MSI használatakor</span><span class="sxs-lookup"><span data-stu-id="e149c-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="e149c-883">Javítva lett az a probléma, amely miatt a Disconnect-AzAccount hibát jelenít meg, ha nincs kapcsolat</span><span class="sxs-lookup"><span data-stu-id="e149c-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="e149c-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e149c-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="e149c-885">Hozzá lett adva a Get-AzCognitiveServicesAccountSkus művelet.</span><span class="sxs-lookup"><span data-stu-id="e149c-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-886">Az.Compute</span></span>
* <span data-ttu-id="e149c-887">Hozzá lett adva az Add-AzVmssVMDataDisk és a Remove-AzVmssVMDataDisk parancsmag</span><span class="sxs-lookup"><span data-stu-id="e149c-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="e149c-888">A Get-AzVMImage megjeleníti az AutomaticOSUpgradeProperties értékét</span><span class="sxs-lookup"><span data-stu-id="e149c-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="e149c-889">Javítva lett az a probléma, amely miatt a SetAzVMChefExtension -BootstrapOptions és -JsonAttribute beállításának értéke nem JSON formátumban lett beállítva.</span><span class="sxs-lookup"><span data-stu-id="e149c-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-891">A DataLake csomag verziója 1.1.10-re frissült.</span><span class="sxs-lookup"><span data-stu-id="e149c-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="e149c-892">Hozzá lett adva az alapértelmezett egyidejűség a többszálas műveletekhez.</span><span class="sxs-lookup"><span data-stu-id="e149c-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="e149c-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="e149c-893">Az.Insights</span></span>
* <span data-ttu-id="e149c-894">Javítva lett a 7267-es hiba (Automatikus skálázási terület)</span><span class="sxs-lookup"><span data-stu-id="e149c-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="e149c-895">Problémák az új automatikus skálázási szabályok létrehozásakor: a számozott paraméterek nem megfelelően voltak beállítva (mindig az alapértelmezett értéket kapták).</span><span class="sxs-lookup"><span data-stu-id="e149c-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="e149c-896">Javítva lett a 7513-as hiba [Insights]. A Set-AzDiagnosticSetting a kategóriák explicit megadását igényelte a beállítások létrehozásakor</span><span class="sxs-lookup"><span data-stu-id="e149c-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="e149c-897">A parancsmag most már nem igényli a kategóriák explicit megjelölését a létrehozás során, tehát a dokumentációban leírt módon működik</span><span class="sxs-lookup"><span data-stu-id="e149c-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-898">Az.Network</span></span>
* <span data-ttu-id="e149c-899">A PeeringType kötelező paraméter lett a következő parancsmagoknál:</span><span class="sxs-lookup"><span data-stu-id="e149c-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="e149c-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="e149c-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="e149c-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="e149c-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="e149c-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e149c-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="e149c-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="e149c-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="e149c-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="e149c-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="e149c-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e149c-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="e149c-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="e149c-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="e149c-907">Szabályzatszervizelési parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-908">Az.Resources</span></span>
* <span data-ttu-id="e149c-909">https://github.com/Azure/azure-powershell/issues/7402 javítása</span><span class="sxs-lookup"><span data-stu-id="e149c-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="e149c-910">Lehetségessé vált az erőforrások felsorolása a -ResourceId paraméter a Get-AzResource parancsmaggal való használatával</span><span class="sxs-lookup"><span data-stu-id="e149c-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="e149c-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="e149c-911">Az.ServiceBus</span></span>
* <span data-ttu-id="e149c-912">A PSServiceBusMigrationConfigurationAttributes parancsmaghoz hozzá lett adva a MigrationState csak olvasható tulajdonság, amely a migrálás állapotának megállapításában segít.</span><span class="sxs-lookup"><span data-stu-id="e149c-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="e149c-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e149c-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="e149c-914">Javítva lett a tanúsítvány-hozzáadás a Linux Vmss-hez.</span><span class="sxs-lookup"><span data-stu-id="e149c-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="e149c-915">Javítva lett az „Add-AzServiceFabricClusterCertificate” parancsmag</span><span class="sxs-lookup"><span data-stu-id="e149c-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="e149c-916">A megfelelő ujjlenyomat használata az új tanúsítványokból (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="e149c-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="e149c-917">Kivétel helyes megjelenítése (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="e149c-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="e149c-918">Javítva lett az „Update-AzServiceFabricDurability” parancsmag, hogy frissítse a fürt konfigurációját a Vmss CreateOrUpdate művelet megkezdése előtt.</span><span class="sxs-lookup"><span data-stu-id="e149c-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="e149c-919">0.4.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="e149c-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="e149c-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="e149c-920">Az.Profile</span></span>
* <span data-ttu-id="e149c-921">Ki lett javítva a Get-AzSubscription parancsmaggal kapcsolatos hiba a CloudShellben.</span><span class="sxs-lookup"><span data-stu-id="e149c-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="e149c-922">A ClientRuntime legújabb verziójának használatához frissíteni kell az általános kódot.</span><span class="sxs-lookup"><span data-stu-id="e149c-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-923">Az.Compute</span></span>
* <span data-ttu-id="e149c-924">A virtuálisgép-méretek engedélyezési listája új méretekkel bővült, amelyekhez a „New-AzVm” parancsmag egyszerű paraméterkészletének használatakor be lesz kapcsolva a gyorsított hálózatkezelés.</span><span class="sxs-lookup"><span data-stu-id="e149c-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="e149c-925">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="e149c-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="e149c-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e149c-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="e149c-927">Virtuális hálózati szabályok támogatása</span><span class="sxs-lookup"><span data-stu-id="e149c-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="e149c-928">Get-AzDataLakeStoreVirtualNetworkRule: Beszerzi vagy listázza az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="e149c-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="e149c-929">Add-AzDataLakeStoreVirtualNetworkRule: Hozzáad egy virtuális hálózati szabályt a kiválasztott Data Lake Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="e149c-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e149c-930">Set-AzDataLakeStoreVirtualNetworkRule: Módosítja a megadott Data Lake Storage-fiókhoz tartozó virtuális hálózati szabályt.</span><span class="sxs-lookup"><span data-stu-id="e149c-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="e149c-931">Remove-AzDataLakeStoreVirtualNetworkRule: Törli az Azure Data Lake Storage virtuális hálózati szabályát.</span><span class="sxs-lookup"><span data-stu-id="e149c-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-932">Az.Network</span></span>
* <span data-ttu-id="e149c-933">Frissült a Test-AzNetworkWatcherConnectivity parancsmag, amely mostantól a háttérrendszerbe továbbítja a protokoll értékét.</span><span class="sxs-lookup"><span data-stu-id="e149c-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="e149c-934">A ResourceName argumentumbefejező minden parancsmaghoz hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="e149c-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-935">Az.Resources</span></span>
* <span data-ttu-id="e149c-936">Egy értelmezhető kivétel a forgatókönyvhöz történő hozzáadásával kiküszöböltük azokat az eseteket, amelyekben a Get-AzRoleDefinition értelmezhetetlen kivételt váltott ki (amikor az alapértelmezett profilhoz nem tartozik előfizetés és a hatóköre sem meghatározott).</span><span class="sxs-lookup"><span data-stu-id="e149c-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="e149c-937">Az alapértelmezett paraméterkészlet a „RoleDefinitionNameParameterSet” készletre módosult.</span><span class="sxs-lookup"><span data-stu-id="e149c-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="e149c-938">0.3.0 – 2018. október</span><span class="sxs-lookup"><span data-stu-id="e149c-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="e149c-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="e149c-939">Azure.Storage</span></span>
* <span data-ttu-id="e149c-940">Ki lett javítva az a blob-/fájlmásolási hiba, amikor a metaadatok másolása nem történt meg, ha a célhely rendelkezett metaadatokkal</span><span class="sxs-lookup"><span data-stu-id="e149c-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="e149c-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="e149c-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="e149c-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e149c-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="e149c-943">Támogatott lett az egyes helyek Storage-erőforráshasználatának lekérése, és egy figyelmeztető üzenet hívja fel a figyelmet arra, hogy a globális Storage-erőforráshasználat lekérdezése már elavultnak számít.</span><span class="sxs-lookup"><span data-stu-id="e149c-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="e149c-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e149c-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="e149c-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="e149c-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="e149c-946">A Get-AzCognitiveServicesAccountSkus már létező fiók nélkül is használható.</span><span class="sxs-lookup"><span data-stu-id="e149c-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="e149c-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="e149c-947">Az.Compute</span></span>
* <span data-ttu-id="e149c-948">Ki lett javítva a Get-AzVM -ResourceGroupName <rg>, hogy szükség esetén több mint 50 találatot is visszaadjon.</span><span class="sxs-lookup"><span data-stu-id="e149c-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="e149c-949">A SimpleParameterSet egy példája hozzá lett adva a New-AzVmss parancsmag súgójához.</span><span class="sxs-lookup"><span data-stu-id="e149c-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="e149c-950">Egy elgépelés ki lett javítva az Azure Disk Encryption folyamatjelző üzenetében</span><span class="sxs-lookup"><span data-stu-id="e149c-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="e149c-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e149c-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="e149c-952">Az ADF .Net SDK a 2.3.0-s verzióra lett frissítve.</span><span class="sxs-lookup"><span data-stu-id="e149c-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="e149c-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="e149c-953">Az.Network</span></span>
* <span data-ttu-id="e149c-954">Hozzá lett adva a NetworkProfile funkció.</span><span class="sxs-lookup"><span data-stu-id="e149c-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="e149c-955">Az alábbi új parancsmagok lettek hozzáadva</span><span class="sxs-lookup"><span data-stu-id="e149c-955">new cmdlets added</span></span>
    - <span data-ttu-id="e149c-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e149c-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="e149c-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e149c-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="e149c-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e149c-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="e149c-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="e149c-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="e149c-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="e149c-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="e149c-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="e149c-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="e149c-962">Szolgáltatástársítási hivatkozás lett hozzáadva az alhálózati modellhez</span><span class="sxs-lookup"><span data-stu-id="e149c-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="e149c-963">Hozzá lett adva a New-AzVirtualNetworkTap, a Get-AzVirtualNetworkTap, a Set-AzVirtualNetworkTap és a Remove-AzVirtualNetworkTap parancsmag</span><span class="sxs-lookup"><span data-stu-id="e149c-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="e149c-964">Hozzá lett adva a Set-AzNEtworkInterfaceTapConfig, a Get-AzNEtworkInterfaceTapConfig és a Remove-AzNEtworkInterfaceTapConfig parancsmag</span><span class="sxs-lookup"><span data-stu-id="e149c-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="e149c-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="e149c-965">Az.RedisCache</span></span>
* <span data-ttu-id="e149c-966">A továbbiakban bármilyen sztring megadható méretparaméterként.</span><span class="sxs-lookup"><span data-stu-id="e149c-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="e149c-967">A P5 hozzá lett adva a PSArgumentCompleter előugró ablakhoz</span><span class="sxs-lookup"><span data-stu-id="e149c-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="e149c-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e149c-968">Az.Resources</span></span>
* <span data-ttu-id="e149c-969">A hiányzó -Mode paraméter hozzá lett adva a Set-AzPolicyDefinition parancsmaghoz</span><span class="sxs-lookup"><span data-stu-id="e149c-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="e149c-970">A felhasználót tartalmazó forrásműveleteknél ki lett javítva a Get-AzProviderOperation parancsmag egy hibája</span><span class="sxs-lookup"><span data-stu-id="e149c-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="e149c-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="e149c-971">Az.Sql</span></span>
* <span data-ttu-id="e149c-972">Ki lett javítva egy hiba, amely miatt egyes biztonsági mentési parancsmagok nem ismerték fel az aktuális Azure-előfizetést</span><span class="sxs-lookup"><span data-stu-id="e149c-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="e149c-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="e149c-973">Az.Websites</span></span>
* <span data-ttu-id="e149c-974">Új Get-AzWebAppContainerContinuousDeploymentUrl parancsmag – lekéri a tároló folyamatos üzembehelyezési webhookjának URL-címét</span><span class="sxs-lookup"><span data-stu-id="e149c-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="e149c-975">Új New-AzWebAppContainerPSSession és Enter-WebAppContainerPSSession parancsmag – távoli PowerShell-munkamenetet kezdeményez egy windowsos tárolóalkalmazásba</span><span class="sxs-lookup"><span data-stu-id="e149c-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="e149c-976">0.2.0 – 2018. szeptember</span><span class="sxs-lookup"><span data-stu-id="e149c-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="e149c-977">Kezdeti kiadás</span><span class="sxs-lookup"><span data-stu-id="e149c-977">Initial Release</span></span>