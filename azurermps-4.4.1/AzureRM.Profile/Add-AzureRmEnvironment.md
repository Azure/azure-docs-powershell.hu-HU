---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680248"
---
# <span data-ttu-id="46812-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="46812-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="46812-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46812-102">SYNOPSIS</span></span>
<span data-ttu-id="46812-103">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="46812-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46812-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46812-104">SYNTAX</span></span>

### <span data-ttu-id="46812-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="46812-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46812-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46812-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="46812-107">DESCRIPTION</span></span>
<span data-ttu-id="46812-108">Az Add-AzureRmEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="46812-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="46812-109">A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.</span><span class="sxs-lookup"><span data-stu-id="46812-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="46812-110">Példák</span><span class="sxs-lookup"><span data-stu-id="46812-110">EXAMPLES</span></span>

### <span data-ttu-id="46812-111">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="46812-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="46812-112">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzureRmEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzureRmEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="46812-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="46812-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46812-113">PARAMETERS</span></span>

### <span data-ttu-id="46812-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="46812-115">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="46812-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="46812-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="46812-117">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="46812-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="46812-118">-AdTenant</span></span>
<span data-ttu-id="46812-119">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="46812-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-120">-ARMEndpoint</span></span>
<span data-ttu-id="46812-121">Az Azure Resource Manager végpontja</span><span class="sxs-lookup"><span data-stu-id="46812-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="46812-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="46812-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="46812-123">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="46812-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="46812-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="46812-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="46812-125">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="46812-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="46812-126">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="46812-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="46812-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="46812-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="46812-128">A fő Vault-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="46812-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="46812-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="46812-130">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.</span><span class="sxs-lookup"><span data-stu-id="46812-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46812-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="46812-131">-DataLakeAudience</span></span>
<span data-ttu-id="46812-132">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="46812-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="46812-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46812-133">-DefaultProfile</span></span>
<span data-ttu-id="46812-134">A credeetnails, a bérlő és az azuretal való kommunikációhoz használt előfizetés</span><span class="sxs-lookup"><span data-stu-id="46812-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46812-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="46812-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="46812-136">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="46812-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="46812-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-137">-GalleryEndpoint</span></span>
<span data-ttu-id="46812-138">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="46812-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="46812-139">-GraphAudience</span></span>
<span data-ttu-id="46812-140">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="46812-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="46812-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-141">-GraphEndpoint</span></span>
<span data-ttu-id="46812-142">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="46812-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="46812-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="46812-144">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="46812-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46812-145">-Name</span></span>
<span data-ttu-id="46812-146">A hozzáadni kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="46812-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="46812-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="46812-148">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="46812-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="46812-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="46812-150">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="46812-151">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="46812-151">-Scope</span></span>
<span data-ttu-id="46812-152">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="46812-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="46812-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-153">-ServiceEndpoint</span></span>
<span data-ttu-id="46812-154">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="46812-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="46812-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="46812-156">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="46812-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="46812-157">-StorageEndpoint</span></span>
<span data-ttu-id="46812-158">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="46812-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="46812-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="46812-160">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="46812-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="46812-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46812-161">-Confirm</span></span>
<span data-ttu-id="46812-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46812-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46812-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46812-163">-WhatIf</span></span>
<span data-ttu-id="46812-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46812-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46812-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46812-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46812-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46812-166">CommonParameters</span></span>
<span data-ttu-id="46812-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46812-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46812-168">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46812-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46812-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46812-169">INPUTS</span></span>

## <span data-ttu-id="46812-170">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46812-170">OUTPUTS</span></span>

### <span data-ttu-id="46812-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="46812-171">PSAzureEnvironment</span></span>
<span data-ttu-id="46812-172">Ez a parancsmag az Azure-példányokkal való kommunikációhoz szükséges végpontok és metaadatok halmazát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="46812-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="46812-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46812-173">NOTES</span></span>

## <span data-ttu-id="46812-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46812-174">RELATED LINKS</span></span>

[<span data-ttu-id="46812-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="46812-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="46812-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="46812-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="46812-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="46812-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

