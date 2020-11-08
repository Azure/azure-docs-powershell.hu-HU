---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: c1df1917a4133cf43f7cf0db89f1d59ad2c9c151
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013042"
---
# <span data-ttu-id="117e7-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="117e7-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="117e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="117e7-102">SYNOPSIS</span></span>
<span data-ttu-id="117e7-103">Végpontokat és metaadatokat ad az Azure Resource Manager egy példányához.</span><span class="sxs-lookup"><span data-stu-id="117e7-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="117e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="117e7-104">SYNTAX</span></span>

### <span data-ttu-id="117e7-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="117e7-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="117e7-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="117e7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="117e7-107">DESCRIPTION</span></span>
<span data-ttu-id="117e7-108">Az Add-AzEnvironment parancsmag végpontokat és metaadatokat ad hozzá az Azure Resource Manager parancsmagok számára az Azure Resource Manager új példányához való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="117e7-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="117e7-109">A beépített környezetek AzureCloud és AzureChinaCloud az Azure Resource Manager meglévő nyilvános példányainak megcélzására.</span><span class="sxs-lookup"><span data-stu-id="117e7-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="117e7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="117e7-110">EXAMPLES</span></span>

### <span data-ttu-id="117e7-111">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="117e7-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="117e7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="117e7-112">PARAMETERS</span></span>

### <span data-ttu-id="117e7-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="117e7-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="117e7-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="117e7-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="117e7-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="117e7-117">-AdTenant</span></span>
<span data-ttu-id="117e7-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="117e7-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-119">-ARMEndpoint</span></span>
<span data-ttu-id="117e7-120">Az Azure Resource Manager végpontja</span><span class="sxs-lookup"><span data-stu-id="117e7-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="117e7-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="117e7-122">Az Azure Analysis Services-erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="117e7-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="117e7-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="117e7-124">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="117e7-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="117e7-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="117e7-126">Annak az Azure tanúsítvány-szolgáltatásnak az erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="117e7-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="117e7-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="117e7-128">Az Azure tanúsítási szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="117e7-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="117e7-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="117e7-130">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="117e7-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="117e7-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="117e7-132">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="117e7-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="117e7-133">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="117e7-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="117e7-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="117e7-135">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="117e7-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="117e7-136">Példa a vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="117e7-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="117e7-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="117e7-138">Az Azure Key Vault-adatszolgáltatások erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="117e7-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="117e7-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="117e7-140">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="117e7-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="117e7-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="117e7-142">Az Azure log Analytics API-t hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="117e7-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="117e7-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="117e7-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="117e7-144">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="117e7-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="117e7-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="117e7-145">-DataLakeAudience</span></span>
<span data-ttu-id="117e7-146">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="117e7-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="117e7-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117e7-147">-DefaultProfile</span></span>
<span data-ttu-id="117e7-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="117e7-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="117e7-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="117e7-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="117e7-150">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="117e7-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="117e7-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-151">-GalleryEndpoint</span></span>
<span data-ttu-id="117e7-152">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="117e7-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="117e7-153">-GraphAudience</span></span>
<span data-ttu-id="117e7-154">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="117e7-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="117e7-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-155">-GraphEndpoint</span></span>
<span data-ttu-id="117e7-156">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="117e7-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="117e7-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="117e7-158">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="117e7-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="117e7-159">-Name</span></span>
<span data-ttu-id="117e7-160">A hozzáadni kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="117e7-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="117e7-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="117e7-162">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="117e7-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="117e7-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="117e7-164">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="117e7-165">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="117e7-165">-Scope</span></span>
<span data-ttu-id="117e7-166">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="117e7-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="117e7-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-167">-ServiceEndpoint</span></span>
<span data-ttu-id="117e7-168">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="117e7-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="117e7-170">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="117e7-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="117e7-171">-StorageEndpoint</span></span>
<span data-ttu-id="117e7-172">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="117e7-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="117e7-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="117e7-174">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="117e7-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="117e7-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="117e7-175">-Confirm</span></span>
<span data-ttu-id="117e7-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="117e7-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117e7-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117e7-177">-WhatIf</span></span>
<span data-ttu-id="117e7-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="117e7-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="117e7-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="117e7-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117e7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117e7-180">CommonParameters</span></span>
<span data-ttu-id="117e7-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="117e7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117e7-182">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117e7-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117e7-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="117e7-183">INPUTS</span></span>

### <span data-ttu-id="117e7-184">System. String</span><span class="sxs-lookup"><span data-stu-id="117e7-184">System.String</span></span>

### <span data-ttu-id="117e7-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="117e7-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="117e7-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="117e7-186">OUTPUTS</span></span>

### <span data-ttu-id="117e7-187">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="117e7-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="117e7-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="117e7-188">NOTES</span></span>

## <span data-ttu-id="117e7-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="117e7-189">RELATED LINKS</span></span>

[<span data-ttu-id="117e7-190">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="117e7-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="117e7-191">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="117e7-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="117e7-192">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="117e7-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

