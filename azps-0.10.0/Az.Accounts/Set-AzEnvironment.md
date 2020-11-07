---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 7ec08296fe88b7d5b7d7825c3a3078b1e85ce81c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840998"
---
# <span data-ttu-id="b6e52-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6e52-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="b6e52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6e52-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e52-103">Az Azure-környezet tulajdonságainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="b6e52-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="b6e52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6e52-104">SYNTAX</span></span>

### <span data-ttu-id="b6e52-105">Név (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6e52-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6e52-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6e52-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6e52-107">DESCRIPTION</span></span>
<span data-ttu-id="b6e52-108">Az Set-AzEnvironment parancsmag végpontokat és metaadatokat állít be az Azure-példányhoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="b6e52-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="b6e52-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b6e52-109">EXAMPLES</span></span>

### <span data-ttu-id="b6e52-110">1. példa: új környezet létrehozása és módosítása</span><span class="sxs-lookup"><span data-stu-id="b6e52-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="b6e52-111">Ebben a példában egy új Azure-környezetet hozunk létre a minta végpontokkal az Add-AzEnvironment használatával, és a ActiveDirectoryEndpoint és a GraphEndpoint attribútum értékét az-as parancsmag set-AzEnvironment segítségével változtatjuk meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="b6e52-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6e52-112">PARAMETERS</span></span>

### <span data-ttu-id="b6e52-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="b6e52-114">Az Azure Active Directory-hitelesítéshez az alapszintű szervezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="b6e52-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="b6e52-116">Az Azure Resource Manager vagy a Service Management (RDFE) végpontokra vonatkozó kérelmeket hitelesítő tokenek közönségét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="b6e52-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="b6e52-117">-AdTenant</span></span>
<span data-ttu-id="b6e52-118">Az alapértelmezett Active Directory-bérlőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="b6e52-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-119">-ARMEndpoint</span></span>
<span data-ttu-id="b6e52-120">Az Azure Resource Manager végpontja.</span><span class="sxs-lookup"><span data-stu-id="b6e52-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="b6e52-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="b6e52-122">Az Azure Analysis Services-erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b6e52-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="b6e52-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="b6e52-124">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="b6e52-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="b6e52-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="b6e52-126">Annak az Azure tanúsítvány-szolgáltatásnak az erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="b6e52-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="b6e52-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="b6e52-128">Az Azure tanúsítási szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="b6e52-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="b6e52-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="b6e52-130">Azure Data Lake – az Azure Data Lake Analytics munka-és katalógus-szolgáltatások DNS-utótagja</span><span class="sxs-lookup"><span data-stu-id="b6e52-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="b6e52-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="b6e52-132">Az Azure Data Lake Store FileSystem DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="b6e52-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="b6e52-133">Példa: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="b6e52-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="b6e52-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="b6e52-135">Az Azure Key Vault szolgáltatás DNS-utótagja.</span><span class="sxs-lookup"><span data-stu-id="b6e52-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="b6e52-136">Példa a vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="b6e52-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="b6e52-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="b6e52-138">Az Azure Key Vault-adatszolgáltatások erőforrás-azonosítója, amely a kért jogkivonat címzettje.</span><span class="sxs-lookup"><span data-stu-id="b6e52-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="b6e52-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="b6e52-140">Az Azure log Analytics API-val való kommunikáció során használandó végpont.</span><span class="sxs-lookup"><span data-stu-id="b6e52-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="b6e52-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="b6e52-142">Az Azure log Analytics API-t hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="b6e52-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="b6e52-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6e52-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="b6e52-144">Annak az Azure-kötegnek az erőforrás-azonosítója, amely a kért jogkivonat címzettje</span><span class="sxs-lookup"><span data-stu-id="b6e52-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="b6e52-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="b6e52-145">-DataLakeAudience</span></span>
<span data-ttu-id="b6e52-146">Az AD Data Lake Services végponttal hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="b6e52-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="b6e52-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e52-147">-DefaultProfile</span></span>
<span data-ttu-id="b6e52-148">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6e52-148">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6e52-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="b6e52-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="b6e52-150">Azt jelzi, hogy engedélyezve van az Active Directory összevonási szolgáltatások helyi hitelesítése.</span><span class="sxs-lookup"><span data-stu-id="b6e52-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="b6e52-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-151">-GalleryEndpoint</span></span>
<span data-ttu-id="b6e52-152">A központi telepítő sablonok Azure Resource Manager-gyűjteményének végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="b6e52-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="b6e52-153">-GraphAudience</span></span>
<span data-ttu-id="b6e52-154">Az AD gráf végpontját hitelesítő tokenek közönsége.</span><span class="sxs-lookup"><span data-stu-id="b6e52-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="b6e52-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-155">-GraphEndpoint</span></span>
<span data-ttu-id="b6e52-156">A Graph (Active Directory metadata) kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="b6e52-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="b6e52-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="b6e52-158">A felügyeleti portál URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="b6e52-159">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6e52-159">-Name</span></span>
<span data-ttu-id="b6e52-160">A módosítani kívánt környezet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-160">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="b6e52-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="b6e52-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="b6e52-162">Azt az URL-címet adja meg, amelyből a. publishsettings fájlokat le lehet tölteni.</span><span class="sxs-lookup"><span data-stu-id="b6e52-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="b6e52-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b6e52-164">Az Azure Resource Manager-kérések URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="b6e52-165">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="b6e52-165">-Scope</span></span>
<span data-ttu-id="b6e52-166">Meghatározza a környezeti változások hatókörét, például hogy a módosítások csak az aktuális folyamatra vagy a felhasználó által indított összes munkamenetre érvényesek-e.</span><span class="sxs-lookup"><span data-stu-id="b6e52-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b6e52-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-167">-ServiceEndpoint</span></span>
<span data-ttu-id="b6e52-168">A Service Management (RDFE) kérések végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="b6e52-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="b6e52-170">Az Azure SQL-adatbázis kiszolgálóihoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="b6e52-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6e52-171">-StorageEndpoint</span></span>
<span data-ttu-id="b6e52-172">A tárterület (blob, táblázat, várólista és fájl) elérési végpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="b6e52-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6e52-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="b6e52-174">Az Azure Traffic Manager Services szolgáltatáshoz tartozó tartománynév-utótagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6e52-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="b6e52-175">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6e52-175">-Confirm</span></span>
<span data-ttu-id="b6e52-176">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6e52-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6e52-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e52-177">-WhatIf</span></span>
<span data-ttu-id="b6e52-178">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6e52-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6e52-179">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6e52-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6e52-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e52-180">CommonParameters</span></span>
<span data-ttu-id="b6e52-181">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6e52-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e52-182">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6e52-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e52-183">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e52-183">INPUTS</span></span>

### <span data-ttu-id="b6e52-184">System. String</span><span class="sxs-lookup"><span data-stu-id="b6e52-184">System.String</span></span>

### <span data-ttu-id="b6e52-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6e52-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6e52-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6e52-186">OUTPUTS</span></span>

### <span data-ttu-id="b6e52-187">Microsoft. Azure. Command. profil. models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6e52-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b6e52-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6e52-188">NOTES</span></span>

## <span data-ttu-id="b6e52-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6e52-189">RELATED LINKS</span></span>

[<span data-ttu-id="b6e52-190">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6e52-190">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="b6e52-191">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6e52-191">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="b6e52-192">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6e52-192">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

