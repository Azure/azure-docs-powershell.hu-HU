---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926170"
---
# <span data-ttu-id="c84d3-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c84d3-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="c84d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c84d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c84d3-103">Beállítja egy Azure-környezet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="c84d3-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="c84d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c84d3-104">SYNTAX</span></span>

### <span data-ttu-id="c84d3-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c84d3-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c84d3-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c84d3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c84d3-107">DESCRIPTION</span></span>
<span data-ttu-id="c84d3-108">A Set-AzEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="c84d3-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="c84d3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c84d3-109">EXAMPLES</span></span>

### <span data-ttu-id="c84d3-110">1. példa: Új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="c84d3-110">Example 1: Creating and modifying a new environment</span></span>
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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="c84d3-111">Ebben a példában egy új Azure-környezetet hozunk létre minta végpontokkal az Add-AzEnvironment használatával, majd a Set-AzEnvironment parancsmaggal módosítjuk a létrehozott környezet ActiveDirectoryEndpoint és GraphEndpoint attribútumainak értékét.</span><span class="sxs-lookup"><span data-stu-id="c84d3-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="c84d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c84d3-112">PARAMETERS</span></span>

### <span data-ttu-id="c84d3-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c84d3-114">Az Azure Active Directory-hitelesítés alapszolgáltatóját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="c84d3-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c84d3-116">Megadja az Azure Resource Manager- vagy RDFE-végpontokra vonatkozó kérelmeket hitelesítésseló jogkivonatok célközönségét.</span><span class="sxs-lookup"><span data-stu-id="c84d3-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="c84d3-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c84d3-117">-AdTenant</span></span>
<span data-ttu-id="c84d3-118">Az alapértelmezett Active Directory-bérlő.</span><span class="sxs-lookup"><span data-stu-id="c84d3-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="c84d3-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-119">-ARMEndpoint</span></span>
<span data-ttu-id="c84d3-120">Az Azure Resource Manager végpontja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="c84d3-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="c84d3-122">Az Azure Analysis Services erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c84d3-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="c84d3-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="c84d3-124">Az Azure Log Analytics API-val való kommunikáció során használt végpont.</span><span class="sxs-lookup"><span data-stu-id="c84d3-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c84d3-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="c84d3-126">Az Azure Attestation szolgáltatás erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c84d3-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84d3-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="c84d3-128">Az Azure Attestation szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84d3-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="c84d3-130">Az Azure Data Lake Analytics-feladat- és katalógusszolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="c84d3-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="c84d3-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="c84d3-132">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="c84d3-133">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="c84d3-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="c84d3-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="c84d3-135">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="c84d3-136">Példa erre: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="c84d3-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="c84d3-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="c84d3-138">Az Azure Key Vault adatszolgáltatásának erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c84d3-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c84d3-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="c84d3-140">Az Azure Log Analytics API-val való kommunikáció során használt végpont.</span><span class="sxs-lookup"><span data-stu-id="c84d3-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c84d3-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="c84d3-142">Az Azure Log Analytics API-val hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="c84d3-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c84d3-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="c84d3-144">Az Azure Synapse Analytics erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c84d3-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84d3-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="c84d3-146">Az Azure Synapse Analytics DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84d3-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c84d3-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="c84d3-148">A kért jogkivonat címzettjeként megadott Azure Batch szolgáltatás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c84d3-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="c84d3-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="c84d3-150">Az Azure Container Registry utótagja.</span><span class="sxs-lookup"><span data-stu-id="c84d3-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c84d3-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="c84d3-151">-DataLakeAudience</span></span>
<span data-ttu-id="c84d3-152">Az AD Data Lake services Végponttal hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="c84d3-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="c84d3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c84d3-153">-DefaultProfile</span></span>
<span data-ttu-id="c84d3-154">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c84d3-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c84d3-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c84d3-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="c84d3-156">Azt jelzi, hogy az Active Directory összevonási szolgáltatások (ADFS) a helyeken való hitelesítés engedélyezett.</span><span class="sxs-lookup"><span data-stu-id="c84d3-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="c84d3-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-157">-GalleryEndpoint</span></span>
<span data-ttu-id="c84d3-158">Az Azure Resource Manager üzembe helyezési sablonjainak végpontját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="c84d3-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="c84d3-159">-GraphAudience</span></span>
<span data-ttu-id="c84d3-160">Az AD Graph-végponttal hitelesítő tokenek célközönsége.</span><span class="sxs-lookup"><span data-stu-id="c84d3-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="c84d3-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-161">-GraphEndpoint</span></span>
<span data-ttu-id="c84d3-162">A Graph -(Active Directory-metaadat-) kérelmek URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="c84d3-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c84d3-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="c84d3-164">Az felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="c84d3-165">-Name</span><span class="sxs-lookup"><span data-stu-id="c84d3-165">-Name</span></span>
<span data-ttu-id="c84d3-166">A módosítani szükséges környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="c84d3-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c84d3-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c84d3-168">Azt az URL-címet adja meg, amelyből a .publishsettings fájlok letölthetők.</span><span class="sxs-lookup"><span data-stu-id="c84d3-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="c84d3-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c84d3-170">Az Azure Resource Manager-kérelmek URL-címe.</span><span class="sxs-lookup"><span data-stu-id="c84d3-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="c84d3-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="c84d3-171">-Scope</span></span>
<span data-ttu-id="c84d3-172">Meghatározza a környezetváltozások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre vonatkoznak-e.</span><span class="sxs-lookup"><span data-stu-id="c84d3-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c84d3-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-173">-ServiceEndpoint</span></span>
<span data-ttu-id="c84d3-174">Az RDFE-kérelmek végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="c84d3-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="c84d3-176">Az Azure SQL-adatbáziskiszolgálók tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="c84d3-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c84d3-177">-StorageEndpoint</span></span>
<span data-ttu-id="c84d3-178">A tárterület-hozzáférés (blob, tábla, várólista és fájl) végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="c84d3-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c84d3-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="c84d3-180">Az Azure Traffic Manager-szolgáltatások tartománynév-utótagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c84d3-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="c84d3-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c84d3-181">-Confirm</span></span>
<span data-ttu-id="c84d3-182">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c84d3-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c84d3-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c84d3-183">-WhatIf</span></span>
<span data-ttu-id="c84d3-184">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c84d3-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c84d3-185">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c84d3-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c84d3-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c84d3-186">CommonParameters</span></span>
<span data-ttu-id="c84d3-187">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c84d3-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c84d3-188">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c84d3-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c84d3-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c84d3-189">INPUTS</span></span>

### <span data-ttu-id="c84d3-190">System.String</span><span class="sxs-lookup"><span data-stu-id="c84d3-190">System.String</span></span>

### <span data-ttu-id="c84d3-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c84d3-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c84d3-192">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c84d3-192">OUTPUTS</span></span>

### <span data-ttu-id="c84d3-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c84d3-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c84d3-194">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c84d3-194">NOTES</span></span>

## <span data-ttu-id="c84d3-195">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c84d3-195">RELATED LINKS</span></span>

[<span data-ttu-id="c84d3-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c84d3-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c84d3-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c84d3-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c84d3-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c84d3-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

