---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: a749c90a77c486e9e3e75f5a5fdbb48488a23559
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299987"
---
# <span data-ttu-id="c0e3a-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0e3a-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="c0e3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e3a-103">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="c0e3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0e3a-104">SYNTAX</span></span>

### <span data-ttu-id="c0e3a-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-105">Name (Default)</span></span>
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e3a-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e3a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e3a-108">Az Set-AzEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="c0e3a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e3a-110">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="c0e3a-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="c0e3a-111">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="c0e3a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="c0e3a-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c0e3a-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="c0e3a-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="c0e3a-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c0e3a-117">-AdTenant</span></span>
<span data-ttu-id="c0e3a-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="c0e3a-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-119">-ARMEndpoint</span></span>
<span data-ttu-id="c0e3a-120">Az Azure Resource Manager végpontja.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="c0e3a-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-122">Az Azure Analysis Services-erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="c0e3a-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="c0e3a-124">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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
### <span data-ttu-id="c0e3a-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-126">Annak az Azure tanúsítvány-szolgáltatásnak az erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c0e3a-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="c0e3a-128">Az Azure tanúsítási szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="c0e3a-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="c0e3a-130">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="c0e3a-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="c0e3a-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="c0e3a-132">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="c0e3a-133">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="c0e3a-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="c0e3a-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="c0e3a-135">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="c0e3a-136">Példa a vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="c0e3a-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="c0e3a-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-138">Az Azure Key Vault-adatszolgáltatások erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c0e3a-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="c0e3a-140">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c0e3a-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-142">Az Azure log Analytics API-t hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c0e3a-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-144">Az Azure szinapszis-Analytics erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c0e3a-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="c0e3a-146">Az Azure szinapszis-Analytics DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-146">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="c0e3a-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e3a-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="c0e3a-148">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="c0e3a-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="c0e3a-149">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="c0e3a-149">-DataLakeAudience</span></span>
<span data-ttu-id="c0e3a-150">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-150">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="c0e3a-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e3a-151">-DefaultProfile</span></span>
<span data-ttu-id="c0e3a-152">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-152">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e3a-153">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c0e3a-153">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="c0e3a-154">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-154">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="c0e3a-155">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-155">-GalleryEndpoint</span></span>
<span data-ttu-id="c0e3a-156">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-156">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="c0e3a-157">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="c0e3a-157">-GraphAudience</span></span>
<span data-ttu-id="c0e3a-158">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-158">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="c0e3a-159">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-159">-GraphEndpoint</span></span>
<span data-ttu-id="c0e3a-160">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-160">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="c0e3a-161">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="c0e3a-161">-ManagementPortalUrl</span></span>
<span data-ttu-id="c0e3a-162">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-162">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="c0e3a-163">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-163">-Name</span></span>
<span data-ttu-id="c0e3a-164">A módosítani kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-164">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="c0e3a-165">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c0e3a-165">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c0e3a-166">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-166">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="c0e3a-167">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-167">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c0e3a-168">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-168">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="c0e3a-169">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="c0e3a-169">-Scope</span></span>
<span data-ttu-id="c0e3a-170">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-170">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c0e3a-171">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-171">-ServiceEndpoint</span></span>
<span data-ttu-id="c0e3a-172">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-172">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="c0e3a-173">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-173">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="c0e3a-174">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-174">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="c0e3a-175">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0e3a-175">-StorageEndpoint</span></span>
<span data-ttu-id="c0e3a-176">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-176">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="c0e3a-177">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c0e3a-177">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="c0e3a-178">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-178">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="c0e3a-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c0e3a-179">-Confirm</span></span>
<span data-ttu-id="c0e3a-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e3a-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e3a-181">-WhatIf</span></span>
<span data-ttu-id="c0e3a-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-182">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0e3a-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0e3a-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e3a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e3a-184">CommonParameters</span></span>
<span data-ttu-id="c0e3a-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0e3a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e3a-186">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e3a-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e3a-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0e3a-187">INPUTS</span></span>

### <span data-ttu-id="c0e3a-188">System. String</span><span class="sxs-lookup"><span data-stu-id="c0e3a-188">System.String</span></span>

### <span data-ttu-id="c0e3a-189">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c0e3a-189">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c0e3a-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0e3a-190">OUTPUTS</span></span>

### <span data-ttu-id="c0e3a-191">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0e3a-191">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c0e3a-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0e3a-192">NOTES</span></span>

## <span data-ttu-id="c0e3a-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0e3a-193">RELATED LINKS</span></span>

[<span data-ttu-id="c0e3a-194">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0e3a-194">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c0e3a-195">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0e3a-195">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c0e3a-196">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c0e3a-196">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

