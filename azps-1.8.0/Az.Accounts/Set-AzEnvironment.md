---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93665766"
---
# <span data-ttu-id="e7b0c-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7b0c-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="e7b0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b0c-103">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="e7b0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7b0c-104">SYNTAX</span></span>

### <span data-ttu-id="e7b0c-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7b0c-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7b0c-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7b0c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7b0c-107">DESCRIPTION</span></span>
<span data-ttu-id="e7b0c-108">Az Set-AzEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="e7b0c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e7b0c-109">EXAMPLES</span></span>

### <span data-ttu-id="e7b0c-110">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="e7b0c-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment
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

<span data-ttu-id="e7b0c-111">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="e7b0c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7b0c-112">PARAMETERS</span></span>

### <span data-ttu-id="e7b0c-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="e7b0c-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="e7b0c-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b0c-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="e7b0c-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="e7b0c-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="e7b0c-117">-AdTenant</span></span>
<span data-ttu-id="e7b0c-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="e7b0c-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-119">-ARMEndpoint</span></span>
<span data-ttu-id="e7b0c-120">Az Azure Resource Manager végpontja.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="e7b0c-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b0c-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="e7b0c-122">Az Azure Analysis Services-erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b0c-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="e7b0c-124">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b0c-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="e7b0c-126">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="e7b0c-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="e7b0c-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="e7b0c-128">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="e7b0c-129">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="e7b0c-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="e7b0c-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="e7b0c-131">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="e7b0c-132">Példa a vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="e7b0c-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="e7b0c-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b0c-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="e7b0c-134">Az Azure Key Vault-adatszolgáltatások erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="e7b0c-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="e7b0c-136">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="e7b0c-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b0c-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="e7b0c-138">Az Azure log Analytics API-t hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="e7b0c-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7b0c-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="e7b0c-140">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="e7b0c-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="e7b0c-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="e7b0c-141">-DataLakeAudience</span></span>
<span data-ttu-id="e7b0c-142">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="e7b0c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b0c-143">-DefaultProfile</span></span>
<span data-ttu-id="e7b0c-144">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b0c-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e7b0c-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="e7b0c-146">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="e7b0c-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-147">-GalleryEndpoint</span></span>
<span data-ttu-id="e7b0c-148">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="e7b0c-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="e7b0c-149">-GraphAudience</span></span>
<span data-ttu-id="e7b0c-150">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="e7b0c-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-151">-GraphEndpoint</span></span>
<span data-ttu-id="e7b0c-152">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="e7b0c-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="e7b0c-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="e7b0c-154">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="e7b0c-155">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7b0c-155">-Name</span></span>
<span data-ttu-id="e7b0c-156">A módosítani kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="e7b0c-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="e7b0c-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="e7b0c-158">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="e7b0c-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="e7b0c-160">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="e7b0c-161">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="e7b0c-161">-Scope</span></span>
<span data-ttu-id="e7b0c-162">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="e7b0c-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-163">-ServiceEndpoint</span></span>
<span data-ttu-id="e7b0c-164">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="e7b0c-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="e7b0c-166">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="e7b0c-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7b0c-167">-StorageEndpoint</span></span>
<span data-ttu-id="e7b0c-168">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="e7b0c-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7b0c-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="e7b0c-170">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="e7b0c-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7b0c-171">-Confirm</span></span>
<span data-ttu-id="e7b0c-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b0c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b0c-173">-WhatIf</span></span>
<span data-ttu-id="e7b0c-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7b0c-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7b0c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b0c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b0c-176">CommonParameters</span></span>
<span data-ttu-id="e7b0c-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7b0c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b0c-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b0c-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b0c-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7b0c-179">INPUTS</span></span>

### <span data-ttu-id="e7b0c-180">System. String</span><span class="sxs-lookup"><span data-stu-id="e7b0c-180">System.String</span></span>

### <span data-ttu-id="e7b0c-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7b0c-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7b0c-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7b0c-182">OUTPUTS</span></span>

### <span data-ttu-id="e7b0c-183">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7b0c-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e7b0c-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7b0c-184">NOTES</span></span>

## <span data-ttu-id="e7b0c-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7b0c-185">RELATED LINKS</span></span>

[<span data-ttu-id="e7b0c-186">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7b0c-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="e7b0c-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7b0c-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="e7b0c-188">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7b0c-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

