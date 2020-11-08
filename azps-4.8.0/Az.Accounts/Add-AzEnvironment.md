---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: ba5a398e21543bc4b19c09309884ceb11fed3197
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183769"
---
# <span data-ttu-id="c3189-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3189-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="c3189-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3189-102">SYNOPSIS</span></span>
<span data-ttu-id="c3189-103">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="c3189-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="c3189-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3189-104">SYNTAX</span></span>

### <span data-ttu-id="c3189-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3189-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3189-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3189-107">Feltárási</span><span class="sxs-lookup"><span data-stu-id="c3189-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3189-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3189-108">DESCRIPTION</span></span>
<span data-ttu-id="c3189-109">Az Add-AzEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="c3189-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="c3189-110">A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.</span><span class="sxs-lookup"><span data-stu-id="c3189-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="c3189-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c3189-111">EXAMPLES</span></span>

### <span data-ttu-id="c3189-112">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="c3189-112">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment `
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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="c3189-113">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="c3189-114">2. példa: új környezet létrehozása URI-kapcsolaton keresztül</span><span class="sxs-lookup"><span data-stu-id="c3189-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="c3189-115">Ebben a példában egy új Azure-környezetet keresünk az https://configuredmetadata.net URI azonosítóból.</span><span class="sxs-lookup"><span data-stu-id="c3189-115">In this example, we are discovering a new Azure environment from the https://configuredmetadata.net Uri.</span></span>

## <span data-ttu-id="c3189-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3189-116">PARAMETERS</span></span>

### <span data-ttu-id="c3189-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c3189-118">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="c3189-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c3189-120">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="c3189-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c3189-121">-AdTenant</span></span>
<span data-ttu-id="c3189-122">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="c3189-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-123">-ARMEndpoint</span></span>
<span data-ttu-id="c3189-124">Az Azure Resource Manager végpontja</span><span class="sxs-lookup"><span data-stu-id="c3189-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="c3189-125">– Automatikus észlelés</span><span class="sxs-lookup"><span data-stu-id="c3189-125">-AutoDiscover</span></span>
<span data-ttu-id="c3189-126">Az alapértelmezett vagy konfigurált végponton keresztüli környezetek felfedezése.</span><span class="sxs-lookup"><span data-stu-id="c3189-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="c3189-128">Az Azure Analysis Services-erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c3189-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="c3189-130">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="c3189-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="c3189-132">Annak az Azure tanúsítvány-szolgáltatásnak az erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c3189-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="c3189-134">Az Azure tanúsítási szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c3189-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="c3189-136">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="c3189-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="c3189-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="c3189-138">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c3189-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="c3189-139">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="c3189-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="c3189-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="c3189-141">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c3189-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="c3189-142">Példa a vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="c3189-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="c3189-144">Az Azure Key Vault-adatszolgáltatások erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c3189-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="c3189-146">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="c3189-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="c3189-148">Az Azure log Analytics API-t hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c3189-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="c3189-150">Az Azure szinapszis-Analytics erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c3189-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="c3189-152">Az Azure szinapszis-Analytics DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c3189-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c3189-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="c3189-154">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="c3189-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="c3189-155">-DataLakeAudience</span></span>
<span data-ttu-id="c3189-156">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c3189-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3189-157">-DefaultProfile</span></span>
<span data-ttu-id="c3189-158">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c3189-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3189-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c3189-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="c3189-160">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="c3189-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="c3189-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-161">-GalleryEndpoint</span></span>
<span data-ttu-id="c3189-162">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="c3189-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="c3189-163">-GraphAudience</span></span>
<span data-ttu-id="c3189-164">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c3189-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="c3189-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-165">-GraphEndpoint</span></span>
<span data-ttu-id="c3189-166">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="c3189-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c3189-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="c3189-168">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="c3189-169">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c3189-169">-Name</span></span>
<span data-ttu-id="c3189-170">A hozzáadni kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-170">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c3189-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c3189-172">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="c3189-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="c3189-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c3189-174">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="c3189-175">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="c3189-175">-Scope</span></span>
<span data-ttu-id="c3189-176">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="c3189-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c3189-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-177">-ServiceEndpoint</span></span>
<span data-ttu-id="c3189-178">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="c3189-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="c3189-180">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="c3189-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c3189-181">-StorageEndpoint</span></span>
<span data-ttu-id="c3189-182">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c3189-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="c3189-184">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3189-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="c3189-185">-URI</span><span class="sxs-lookup"><span data-stu-id="c3189-185">-Uri</span></span>
<span data-ttu-id="c3189-186">Az internetes erőforrás URI-ja a beolvasási környezetekhez.</span><span class="sxs-lookup"><span data-stu-id="c3189-186">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3189-187">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3189-187">-Confirm</span></span>
<span data-ttu-id="c3189-188">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3189-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3189-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3189-189">-WhatIf</span></span>
<span data-ttu-id="c3189-190">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3189-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3189-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3189-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3189-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3189-192">CommonParameters</span></span>
<span data-ttu-id="c3189-193">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3189-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3189-194">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c3189-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3189-195">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3189-195">INPUTS</span></span>

### <span data-ttu-id="c3189-196">System. String</span><span class="sxs-lookup"><span data-stu-id="c3189-196">System.String</span></span>

### <span data-ttu-id="c3189-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3189-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3189-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3189-198">OUTPUTS</span></span>

### <span data-ttu-id="c3189-199">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3189-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c3189-200">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3189-200">NOTES</span></span>

## <span data-ttu-id="c3189-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3189-201">RELATED LINKS</span></span>

[<span data-ttu-id="c3189-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3189-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c3189-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3189-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="c3189-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c3189-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

