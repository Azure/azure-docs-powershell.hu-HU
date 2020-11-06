---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490831"
---
# <span data-ttu-id="43191-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="43191-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="43191-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43191-102">SYNOPSIS</span></span>
<span data-ttu-id="43191-103">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="43191-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="43191-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43191-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43191-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="43191-105">DESCRIPTION</span></span>
<span data-ttu-id="43191-106">Az Add-AzureRmEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="43191-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="43191-107">A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.</span><span class="sxs-lookup"><span data-stu-id="43191-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="43191-108">Példák</span><span class="sxs-lookup"><span data-stu-id="43191-108">EXAMPLES</span></span>

### <span data-ttu-id="43191-109">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="43191-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="43191-110">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzureRmEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzureRmEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="43191-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="43191-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43191-111">PARAMETERS</span></span>

### <span data-ttu-id="43191-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="43191-113">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="43191-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="43191-115">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="43191-116">-AdTenant</span></span>
<span data-ttu-id="43191-117">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-117">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="43191-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="43191-119">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="43191-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="43191-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="43191-121">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="43191-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="43191-122">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="43191-122">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="43191-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="43191-124">A fő Vault-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-124">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="43191-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="43191-126">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.</span><span class="sxs-lookup"><span data-stu-id="43191-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="43191-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="43191-128">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="43191-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-129">-GalleryEndpoint</span></span>
<span data-ttu-id="43191-130">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="43191-131">-GraphAudience</span></span>
<span data-ttu-id="43191-132">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="43191-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-133">-GraphEndpoint</span></span>
<span data-ttu-id="43191-134">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="43191-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="43191-136">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-136">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-137">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43191-137">-Name</span></span>
<span data-ttu-id="43191-138">A hozzáadni kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-138">Specifies the name of the environment to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="43191-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="43191-140">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="43191-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="43191-142">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-142">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-143">-ServiceEndpoint</span></span>
<span data-ttu-id="43191-144">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="43191-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="43191-146">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="43191-147">-StorageEndpoint</span></span>
<span data-ttu-id="43191-148">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43191-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="43191-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="43191-150">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="43191-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43191-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43191-151">-Confirm</span></span>
<span data-ttu-id="43191-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43191-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43191-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43191-153">-WhatIf</span></span>
<span data-ttu-id="43191-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43191-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43191-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43191-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43191-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43191-156">CommonParameters</span></span>
<span data-ttu-id="43191-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43191-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43191-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43191-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43191-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43191-159">INPUTS</span></span>

## <span data-ttu-id="43191-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43191-160">OUTPUTS</span></span>

### <span data-ttu-id="43191-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="43191-161">PSAzureEnvironment</span></span>
<span data-ttu-id="43191-162">Ez a parancsmag az Azure-példányokkal való kommunikációhoz szükséges végpontok és metaadatok halmazát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="43191-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="43191-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43191-163">NOTES</span></span>

## <span data-ttu-id="43191-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43191-164">RELATED LINKS</span></span>

[<span data-ttu-id="43191-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="43191-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="43191-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="43191-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="43191-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="43191-167">Set-AzureRMEnvironment</span></span>]()

