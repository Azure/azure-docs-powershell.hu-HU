---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491886"
---
# <span data-ttu-id="bb6b3-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb6b3-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="bb6b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6b3-103">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb6b3-104">SYNTAX</span></span>

### <span data-ttu-id="bb6b3-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb6b3-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb6b3-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6b3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb6b3-107">DESCRIPTION</span></span>
<span data-ttu-id="bb6b3-108">Az Add-AzureRmEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="bb6b3-109">A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="bb6b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bb6b3-110">EXAMPLES</span></span>

### <span data-ttu-id="bb6b3-111">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="bb6b3-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="bb6b3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb6b3-112">PARAMETERS</span></span>

### <span data-ttu-id="bb6b3-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="bb6b3-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6b3-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="bb6b3-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="bb6b3-117">-AdTenant</span></span>
<span data-ttu-id="bb6b3-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-119">-ARMEndpoint</span></span>
<span data-ttu-id="bb6b3-120">Az Azure Resource Manager végpontja</span><span class="sxs-lookup"><span data-stu-id="bb6b3-120">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="bb6b3-122">Az Azure Analysis Services szolgáltatás végpontjának DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="bb6b3-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```


### <span data-ttu-id="bb6b3-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="bb6b3-124">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="bb6b3-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="bb6b3-126">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="bb6b3-127">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="bb6b3-127">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="bb6b3-129">A fő Vault-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-129">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6b3-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="bb6b3-131">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="bb6b3-133">Az üzemeltetési keresési lekérdezések elérésének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6b3-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="bb6b3-135">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyeknek az üzemeltetési szolgáltatásokra vonatkozó kérelmeket engedélyeztek.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bb6b3-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="bb6b3-137">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="bb6b3-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="bb6b3-138">-DataLakeAudience</span></span>
<span data-ttu-id="bb6b3-139">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6b3-140">-DefaultProfile</span></span>
<span data-ttu-id="bb6b3-141">A credeetnails, a bérlő és az azuretal való kommunikációhoz használt előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb6b3-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="bb6b3-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="bb6b3-143">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-144">-GalleryEndpoint</span></span>
<span data-ttu-id="bb6b3-145">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="bb6b3-146">-GraphAudience</span></span>
<span data-ttu-id="bb6b3-147">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-148">-GraphEndpoint</span></span>
<span data-ttu-id="bb6b3-149">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="bb6b3-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="bb6b3-151">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-151">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb6b3-152">-Name</span></span>
<span data-ttu-id="bb6b3-153">A hozzáadni kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-153">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="bb6b3-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="bb6b3-155">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="bb6b3-157">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-157">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-158">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="bb6b3-158">-Scope</span></span>
<span data-ttu-id="bb6b3-159">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-160">-ServiceEndpoint</span></span>
<span data-ttu-id="bb6b3-161">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="bb6b3-163">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb6b3-164">-StorageEndpoint</span></span>
<span data-ttu-id="bb6b3-165">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bb6b3-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="bb6b3-167">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb6b3-168">-Confirm</span></span>
<span data-ttu-id="bb6b3-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6b3-170">-WhatIf</span></span>
<span data-ttu-id="bb6b3-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb6b3-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb6b3-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6b3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6b3-173">CommonParameters</span></span>
<span data-ttu-id="bb6b3-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb6b3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6b3-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6b3-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6b3-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb6b3-176">INPUTS</span></span>

### <span data-ttu-id="bb6b3-177">System. String</span><span class="sxs-lookup"><span data-stu-id="bb6b3-177">System.String</span></span>

### <span data-ttu-id="bb6b3-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bb6b3-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bb6b3-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb6b3-179">OUTPUTS</span></span>

### <span data-ttu-id="bb6b3-180">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb6b3-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="bb6b3-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb6b3-181">NOTES</span></span>

## <span data-ttu-id="bb6b3-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb6b3-182">RELATED LINKS</span></span>

[<span data-ttu-id="bb6b3-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb6b3-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="bb6b3-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb6b3-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="bb6b3-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bb6b3-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

