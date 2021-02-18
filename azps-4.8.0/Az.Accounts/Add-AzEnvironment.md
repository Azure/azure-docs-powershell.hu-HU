---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 2db2e90dc1292bdfe67907e5a180b08a09a54718
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406009"
---
# <span data-ttu-id="8ec6f-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="8ec6f-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="8ec6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec6f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec6f-103">Végpontokat és metaadatokat ad hozzá az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="8ec6f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ec6f-104">SYNTAX</span></span>

### <span data-ttu-id="8ec6f-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ec6f-105">Name (Default)</span></span>
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

### <span data-ttu-id="8ec6f-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-106">ARMEndpoint</span></span>
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

### <span data-ttu-id="8ec6f-107">Feltárás</span><span class="sxs-lookup"><span data-stu-id="8ec6f-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec6f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ec6f-108">DESCRIPTION</span></span>
<span data-ttu-id="8ec6f-109">A Add-AzEnvironment parancsmag végpontokat és metaadatokat ad hozzá, hogy az Azure Resource Manager-parancsmagok az Azure Resource Manager új példányához csatlakozzon.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="8ec6f-110">Az AzureCloud és az AzureChinaCloud beépített környezetek az Azure Resource Manager meglévő nyilvános példányait célják meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="8ec6f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ec6f-111">EXAMPLES</span></span>

### <span data-ttu-id="8ec6f-112">1. példa: Új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="8ec6f-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="8ec6f-113">Ebben a példában egy új Azure-környezetet hozunk létre minta végpontokkal az Add-AzEnvironment használatával, majd a Set-AzEnvironment parancsmag használatával módosítjuk a létrehozott környezet ActiveDirectoryEndpoint és GraphEndpoint attribútumainak értékét.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="8ec6f-114">2. példa: Új környezet felfedezése az Uri-n keresztül</span><span class="sxs-lookup"><span data-stu-id="8ec6f-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="8ec6f-115">Ebben a példában egy új Azure-környezetet fedezünk fel az `https://configuredmetadata.net` Uri környezetből.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="8ec6f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec6f-116">PARAMETERS</span></span>

### <span data-ttu-id="8ec6f-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="8ec6f-118">Az Azure Active Directory-hitelesítés alapszolgáltatóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="8ec6f-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-120">Megadja az Azure Resource Manager- vagy RDFE-végpontokra vonatkozó kérelmeket hitelesítésseló jogkivonatok célközönségét.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="8ec6f-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="8ec6f-121">-AdTenant</span></span>
<span data-ttu-id="8ec6f-122">Az alapértelmezett Active Directory-bérlő.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="8ec6f-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-123">-ARMEndpoint</span></span>
<span data-ttu-id="8ec6f-124">Az Azure Resource Manager végpontja</span><span class="sxs-lookup"><span data-stu-id="8ec6f-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="8ec6f-125">-AutoDiscover</span><span class="sxs-lookup"><span data-stu-id="8ec6f-125">-AutoDiscover</span></span>
<span data-ttu-id="8ec6f-126">Környezeteket fedez fel alapértelmezett vagy konfigurált végponton keresztül.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="8ec6f-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-128">Az Azure Analysis Services erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="8ec6f-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="8ec6f-130">Az Azure Log Analytics API-val való kommunikáció során használt végpont.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="8ec6f-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-132">Az Azure Attestation szolgáltatás erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="8ec6f-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="8ec6f-134">Az Azure Attestation szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="8ec6f-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="8ec6f-136">Az Azure Data Lake Analytics-feladat- és katalógusszolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="8ec6f-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="8ec6f-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="8ec6f-138">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="8ec6f-139">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="8ec6f-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="8ec6f-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="8ec6f-141">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="8ec6f-142">Példa erre: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="8ec6f-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="8ec6f-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-144">Az Azure Key Vault adatszolgáltatásának erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="8ec6f-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="8ec6f-146">Az Azure Log Analytics API-val való kommunikáció során használt végpont.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="8ec6f-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-148">Az Azure Log Analytics API-val hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="8ec6f-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-150">Az Azure Synapse Analytics erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="8ec6f-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="8ec6f-152">Az Azure Synapse Analytics DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="8ec6f-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6f-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="8ec6f-154">A kért jogkivonat címzettjeként megadott Azure Batch szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8ec6f-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="8ec6f-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="8ec6f-155">-DataLakeAudience</span></span>
<span data-ttu-id="8ec6f-156">Az AD Data Lake services Végponttal hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="8ec6f-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec6f-157">-DefaultProfile</span></span>
<span data-ttu-id="8ec6f-158">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ec6f-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ec6f-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="8ec6f-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="8ec6f-160">Azt jelzi, hogy az Active Directory összevonási szolgáltatások (ADFS) a helyeken való hitelesítés engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="8ec6f-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-161">-GalleryEndpoint</span></span>
<span data-ttu-id="8ec6f-162">Az Azure Resource Manager üzembe helyezési sablonjainak végpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="8ec6f-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="8ec6f-163">-GraphAudience</span></span>
<span data-ttu-id="8ec6f-164">Az AD Graph-végponttal hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="8ec6f-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-165">-GraphEndpoint</span></span>
<span data-ttu-id="8ec6f-166">A Graph(Active Directory metaadat-) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="8ec6f-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="8ec6f-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="8ec6f-168">Az felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="8ec6f-169">-Name</span><span class="sxs-lookup"><span data-stu-id="8ec6f-169">-Name</span></span>
<span data-ttu-id="8ec6f-170">A hozzáadni megfelelő környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-170">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="8ec6f-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="8ec6f-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="8ec6f-172">Azt az URL-címet adja meg, amelyből a .publishsettings fájlok letölthetők.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="8ec6f-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="8ec6f-174">Az Azure Resource Manager-kérelmek URL-címe.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="8ec6f-175">-Scope</span><span class="sxs-lookup"><span data-stu-id="8ec6f-175">-Scope</span></span>
<span data-ttu-id="8ec6f-176">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8ec6f-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-177">-ServiceEndpoint</span></span>
<span data-ttu-id="8ec6f-178">Az RDFE-kérelmek végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="8ec6f-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="8ec6f-180">Az Azure SQL-adatbáziskiszolgálók tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="8ec6f-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec6f-181">-StorageEndpoint</span></span>
<span data-ttu-id="8ec6f-182">A tárterület-hozzáférés (blob, tábla, várólista és fájl) végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="8ec6f-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8ec6f-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="8ec6f-184">Az Azure Traffic Manager-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="8ec6f-185">-Uri</span><span class="sxs-lookup"><span data-stu-id="8ec6f-185">-Uri</span></span>
<span data-ttu-id="8ec6f-186">Megadja a környezetek lehívását lehetővé tő internetes erőforrás URI azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-186">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="8ec6f-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ec6f-187">-Confirm</span></span>
<span data-ttu-id="8ec6f-188">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec6f-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec6f-189">-WhatIf</span></span>
<span data-ttu-id="8ec6f-190">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ec6f-191">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec6f-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec6f-192">CommonParameters</span></span>
<span data-ttu-id="8ec6f-193">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec6f-194">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ec6f-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec6f-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ec6f-195">INPUTS</span></span>

### <span data-ttu-id="8ec6f-196">System.String</span><span class="sxs-lookup"><span data-stu-id="8ec6f-196">System.String</span></span>

### <span data-ttu-id="8ec6f-197">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ec6f-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ec6f-198">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec6f-198">OUTPUTS</span></span>

### <span data-ttu-id="8ec6f-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8ec6f-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="8ec6f-200">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ec6f-200">NOTES</span></span>

## <span data-ttu-id="8ec6f-201">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ec6f-201">RELATED LINKS</span></span>

[<span data-ttu-id="8ec6f-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="8ec6f-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="8ec6f-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="8ec6f-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="8ec6f-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="8ec6f-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

