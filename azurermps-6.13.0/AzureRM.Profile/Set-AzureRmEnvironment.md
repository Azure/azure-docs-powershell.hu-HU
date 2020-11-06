---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 073126f3f750f2decf7189c53733c5fcaaabee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494972"
---
# <span data-ttu-id="d1276-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1276-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="d1276-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d1276-102">SYNOPSIS</span></span>
<span data-ttu-id="d1276-103">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="d1276-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1276-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d1276-104">SYNTAX</span></span>

### <span data-ttu-id="d1276-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d1276-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureAnalysisServicesEndpointSuffix] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1276-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1276-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d1276-107">DESCRIPTION</span></span>
<span data-ttu-id="d1276-108">Az Set-AzureRMEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="d1276-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="d1276-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d1276-109">EXAMPLES</span></span>

### <span data-ttu-id="d1276-110">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="d1276-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
```

<span data-ttu-id="d1276-111">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzureRmEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzureRmEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="d1276-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d1276-112">PARAMETERS</span></span>

### <span data-ttu-id="d1276-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="d1276-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="d1276-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d1276-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="d1276-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="d1276-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="d1276-117">-AdTenant</span></span>
<span data-ttu-id="d1276-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="d1276-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-119">-ARMEndpoint</span></span>
<span data-ttu-id="d1276-120">Az Azure Resource Manager végpontja.</span><span class="sxs-lookup"><span data-stu-id="d1276-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="d1276-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="d1276-122">Az Azure Analysis Services szolgáltatás végpontjának DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="d1276-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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

### <span data-ttu-id="d1276-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="d1276-124">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="d1276-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="d1276-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="d1276-126">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="d1276-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="d1276-127">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="d1276-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="d1276-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="d1276-129">A fő Vault-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="d1276-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d1276-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="d1276-131">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.</span><span class="sxs-lookup"><span data-stu-id="d1276-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="d1276-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="d1276-133">Az üzemeltetési keresési lekérdezések elérésének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="d1276-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d1276-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="d1276-135">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyeknek az üzemeltetési szolgáltatásokra vonatkozó kérelmeket engedélyeztek.</span><span class="sxs-lookup"><span data-stu-id="d1276-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="d1276-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d1276-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="d1276-137">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="d1276-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="d1276-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="d1276-138">-DataLakeAudience</span></span>
<span data-ttu-id="d1276-139">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="d1276-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="d1276-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1276-140">-DefaultProfile</span></span>
<span data-ttu-id="d1276-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d1276-141">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1276-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="d1276-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="d1276-143">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="d1276-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="d1276-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-144">-GalleryEndpoint</span></span>
<span data-ttu-id="d1276-145">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="d1276-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="d1276-146">-GraphAudience</span></span>
<span data-ttu-id="d1276-147">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="d1276-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="d1276-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-148">-GraphEndpoint</span></span>
<span data-ttu-id="d1276-149">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="d1276-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="d1276-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="d1276-151">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="d1276-152">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d1276-152">-Name</span></span>
<span data-ttu-id="d1276-153">A módosítani kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-153">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="d1276-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="d1276-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="d1276-155">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="d1276-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="d1276-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="d1276-157">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="d1276-158">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="d1276-158">-Scope</span></span>
<span data-ttu-id="d1276-159">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="d1276-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d1276-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-160">-ServiceEndpoint</span></span>
<span data-ttu-id="d1276-161">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="d1276-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="d1276-163">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="d1276-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1276-164">-StorageEndpoint</span></span>
<span data-ttu-id="d1276-165">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="d1276-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d1276-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="d1276-167">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d1276-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="d1276-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d1276-168">-Confirm</span></span>
<span data-ttu-id="d1276-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d1276-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1276-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1276-170">-WhatIf</span></span>
<span data-ttu-id="d1276-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d1276-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1276-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d1276-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1276-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1276-173">CommonParameters</span></span>
<span data-ttu-id="d1276-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d1276-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1276-175">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1276-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1276-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1276-176">INPUTS</span></span>

### <span data-ttu-id="d1276-177">System. String</span><span class="sxs-lookup"><span data-stu-id="d1276-177">System.String</span></span>

### <span data-ttu-id="d1276-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1276-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1276-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d1276-179">OUTPUTS</span></span>

### <span data-ttu-id="d1276-180">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1276-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="d1276-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d1276-181">NOTES</span></span>

## <span data-ttu-id="d1276-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d1276-182">RELATED LINKS</span></span>

[<span data-ttu-id="d1276-183">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1276-183">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="d1276-184">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1276-184">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="d1276-185">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="d1276-185">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

