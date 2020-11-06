---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490939"
---
# <span data-ttu-id="aabfb-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="aabfb-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="aabfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aabfb-102">SYNOPSIS</span></span>
<span data-ttu-id="aabfb-103">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="aabfb-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="aabfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aabfb-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabfb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aabfb-105">DESCRIPTION</span></span>
<span data-ttu-id="aabfb-106">Az Set-AzureRMEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="aabfb-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="aabfb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aabfb-107">EXAMPLES</span></span>

### <span data-ttu-id="aabfb-108">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="aabfb-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="aabfb-109">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzureRmEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzureRmEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="aabfb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aabfb-110">PARAMETERS</span></span>

### <span data-ttu-id="aabfb-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="aabfb-112">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="aabfb-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="aabfb-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="aabfb-114">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="aabfb-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="aabfb-115">-AdTenant</span></span>
<span data-ttu-id="aabfb-116">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-116">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="aabfb-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="aabfb-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="aabfb-118">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="aabfb-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="aabfb-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="aabfb-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="aabfb-120">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="aabfb-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="aabfb-121">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="aabfb-121">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="aabfb-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="aabfb-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="aabfb-123">A fő Vault-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="aabfb-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="aabfb-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="aabfb-125">Annak a hozzáférési tokeneknek a célközönségét adja meg, amelyek engedélyezik a Key Vault-szolgáltatások kérését.</span><span class="sxs-lookup"><span data-stu-id="aabfb-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="aabfb-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="aabfb-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="aabfb-127">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="aabfb-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="aabfb-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-128">-GalleryEndpoint</span></span>
<span data-ttu-id="aabfb-129">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="aabfb-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="aabfb-130">-GraphAudience</span></span>
<span data-ttu-id="aabfb-131">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="aabfb-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="aabfb-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-132">-GraphEndpoint</span></span>
<span data-ttu-id="aabfb-133">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="aabfb-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="aabfb-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="aabfb-135">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-135">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="aabfb-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aabfb-136">-Name</span></span>
<span data-ttu-id="aabfb-137">A módosítani kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="aabfb-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="aabfb-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="aabfb-139">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="aabfb-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="aabfb-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="aabfb-141">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-141">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="aabfb-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-142">-ServiceEndpoint</span></span>
<span data-ttu-id="aabfb-143">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="aabfb-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="aabfb-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="aabfb-145">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="aabfb-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="aabfb-146">-StorageEndpoint</span></span>
<span data-ttu-id="aabfb-147">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="aabfb-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="aabfb-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="aabfb-149">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="aabfb-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="aabfb-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aabfb-150">-Confirm</span></span>
<span data-ttu-id="aabfb-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aabfb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabfb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabfb-152">-WhatIf</span></span>
<span data-ttu-id="aabfb-153">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aabfb-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aabfb-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aabfb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabfb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabfb-155">CommonParameters</span></span>
<span data-ttu-id="aabfb-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aabfb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabfb-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabfb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabfb-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aabfb-158">INPUTS</span></span>

## <span data-ttu-id="aabfb-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aabfb-159">OUTPUTS</span></span>

### <span data-ttu-id="aabfb-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="aabfb-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="aabfb-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aabfb-161">NOTES</span></span>

## <span data-ttu-id="aabfb-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aabfb-162">RELATED LINKS</span></span>

[<span data-ttu-id="aabfb-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="aabfb-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="aabfb-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="aabfb-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="aabfb-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="aabfb-165">Remove-AzureRMEnvironment</span></span>]()

