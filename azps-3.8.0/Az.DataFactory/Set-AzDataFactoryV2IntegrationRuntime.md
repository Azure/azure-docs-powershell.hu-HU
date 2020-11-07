---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 020a492ddab075d121025623f5c731bdc71c440b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847137"
---
# <span data-ttu-id="df4d1-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df4d1-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="df4d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="df4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="df4d1-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="df4d1-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="df4d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="df4d1-104">SYNTAX</span></span>

### <span data-ttu-id="df4d1-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df4d1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] 
 [-PublicIPs <String[]>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="df4d1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df4d1-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>] [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="df4d1-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="df4d1-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4d1-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="df4d1-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4d1-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="df4d1-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="df4d1-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="df4d1-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4d1-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="df4d1-111">DESCRIPTION</span></span>
<span data-ttu-id="df4d1-112">A Set-AzDataFactoryV2IntegrationRuntime parancsmag meghatározott paraméterekkel frissíti az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="df4d1-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="df4d1-113">Példák</span><span class="sxs-lookup"><span data-stu-id="df4d1-113">EXAMPLES</span></span>

### <span data-ttu-id="df4d1-114">1. példa: az integrációs futtatókörnyezet frissítésének leírása.</span><span class="sxs-lookup"><span data-stu-id="df4d1-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="df4d1-115">A parancsmag frissíti a "teszt-selfhost – IR" nevű integrációs futtatókörnyezet leírását.</span><span class="sxs-lookup"><span data-stu-id="df4d1-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="df4d1-116">2. példa: az önálló, önállóan működtetett integrációs futtatókörnyezet megosztása.</span><span class="sxs-lookup"><span data-stu-id="df4d1-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="df4d1-117">A parancsmag hozzáadja az ADF-t a megosztott integrációs futtatókörnyezet használatához.</span><span class="sxs-lookup"><span data-stu-id="df4d1-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="df4d1-118">`-SharedIntegrationRuntimeResourceId`A paraméter használata esetén az is szerepelnie `-Type` kell.</span><span class="sxs-lookup"><span data-stu-id="df4d1-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="df4d1-119">Felhívjuk a figyelmét arra, hogy az adatfeldolgozónak engedélyt kell adni az integrációs futtatókörnyezet használatához a parancsmag futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="df4d1-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="df4d1-120">3. példa: a Self-Hosted IR beállítása az Azure-SSIS infravörös kapcsolatának beállítása ADF-ben.</span><span class="sxs-lookup"><span data-stu-id="df4d1-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    PublicIPs                         : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="df4d1-121">A parancsmag az Azure-SSIS-integrációs futtatókörnyezetet használja az önálló, önállóan működtetett integrációs futtatókörnyezethez adatproxyként.</span><span class="sxs-lookup"><span data-stu-id="df4d1-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="df4d1-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="df4d1-122">PARAMETERS</span></span>

### <span data-ttu-id="df4d1-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="df4d1-123">-AuthKey</span></span>
<span data-ttu-id="df4d1-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="df4d1-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="df4d1-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="df4d1-126">Az integrációs futtatókörnyezethez tartozó katalógus-adatbázis-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="df4d1-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="df4d1-127">-CatalogPricingTier</span></span>
<span data-ttu-id="df4d1-128">Az integrációs futtatókörnyezet katalógus-adatbázis árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="df4d1-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="df4d1-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="df4d1-130">Az integrációs futtatókörnyezet katalógus Database Server végpontja.</span><span class="sxs-lookup"><span data-stu-id="df4d1-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="df4d1-131">-DataFactoryName</span></span>
<span data-ttu-id="df4d1-132">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="df4d1-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="df4d1-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="df4d1-134">A proxyként használt Self-Hosted-integrációs futásidejű név</span><span class="sxs-lookup"><span data-stu-id="df4d1-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="df4d1-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="df4d1-136">A Self-Hosted és az Azure-SSIS integrációs futtatókörnyezete között az adatok áthelyezésekor használandó átmeneti adattárolóra hivatkozó Azure Blob Storage kapcsolt szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="df4d1-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="df4d1-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="df4d1-138">Az adattárolási útvonal az Self-Hosted és az Azure-SSIS integrációs futtatókörnyezete közötti adatáthelyezéskor használatos az alapértelmezett tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="df4d1-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4d1-139">-DefaultProfile</span></span>
<span data-ttu-id="df4d1-140">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df4d1-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df4d1-141">-Leírás</span><span class="sxs-lookup"><span data-stu-id="df4d1-141">-Description</span></span>
<span data-ttu-id="df4d1-142">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="df4d1-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="df4d1-143">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="df4d1-143">-Edition</span></span>
<span data-ttu-id="df4d1-144">Az SSIS-integrációs futásidejű verzió, amely a standard vagy a nagyvállalati lehet, az alapértelmezett érték a normál, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="df4d1-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-145">-Force</span><span class="sxs-lookup"><span data-stu-id="df4d1-145">-Force</span></span>
<span data-ttu-id="df4d1-146">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="df4d1-146">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df4d1-147">-InputObject</span></span>
<span data-ttu-id="df4d1-148">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="df4d1-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="df4d1-149">-LicenseType</span></span>
<span data-ttu-id="df4d1-150">Az SSIS-infravörös beállításhoz használni kívánt licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="df4d1-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="df4d1-151">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="df4d1-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="df4d1-152">Ha jogosult az Azure hibrid használati előnyeinek (AHUB) árazására, kérjük, válassza a BasePrice.</span><span class="sxs-lookup"><span data-stu-id="df4d1-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="df4d1-153">Ha nem, akkor válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="df4d1-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-154">-Hely</span><span class="sxs-lookup"><span data-stu-id="df4d1-154">-Location</span></span>
<span data-ttu-id="df4d1-155">Az integrációs futtatókörnyezet helye.</span><span class="sxs-lookup"><span data-stu-id="df4d1-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="df4d1-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="df4d1-157">A csomópontok maximális párhuzamos végrehajtásának száma egy felügyelt, dedikált integrációs futtatókörnyezet esetében.</span><span class="sxs-lookup"><span data-stu-id="df4d1-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-158">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="df4d1-158">-Name</span></span>
<span data-ttu-id="df4d1-159">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="df4d1-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="df4d1-160">-NodeCount</span></span>
<span data-ttu-id="df4d1-161">A fürtcsomópontok száma az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="df4d1-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="df4d1-162">-NodeSize</span></span>
<span data-ttu-id="df4d1-163">Az integrációs futtatókörnyezet csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="df4d1-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-164">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="df4d1-164">-PublicIPs</span></span>
<span data-ttu-id="df4d1-165">A statikus nyilvános IP-címek, amelyek az integrációs futtatókörnyezetet fogják használni.</span><span class="sxs-lookup"><span data-stu-id="df4d1-165">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4d1-166">-ResourceGroupName</span></span>
<span data-ttu-id="df4d1-167">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="df4d1-167">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-168">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4d1-168">-ResourceId</span></span>
<span data-ttu-id="df4d1-169">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="df4d1-169">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-170">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="df4d1-170">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="df4d1-171">Az egyéni beállítási parancsfájlt tartalmazó Azure Blob-tároló SAS-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df4d1-171">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-172">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="df4d1-172">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="df4d1-173">A megosztott önkiszolgáló integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="df4d1-173">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-174">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="df4d1-174">-Subnet</span></span>
<span data-ttu-id="df4d1-175">Az alhálózat neve a VNet.</span><span class="sxs-lookup"><span data-stu-id="df4d1-175">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-176">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="df4d1-176">-Type</span></span>
<span data-ttu-id="df4d1-177">Az integrációs futtatókörnyezet típusa.</span><span class="sxs-lookup"><span data-stu-id="df4d1-177">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-178">-VNetId</span><span class="sxs-lookup"><span data-stu-id="df4d1-178">-VNetId</span></span>
<span data-ttu-id="df4d1-179">Annak az VNet az azonosítója, amelyhez az integrációs futtatókörnyezet csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="df4d1-179">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-180">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="df4d1-180">-Confirm</span></span>
<span data-ttu-id="df4d1-181">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="df4d1-181">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4d1-182">-WhatIf</span></span>
<span data-ttu-id="df4d1-183">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="df4d1-183">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4d1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4d1-184">CommonParameters</span></span>
<span data-ttu-id="df4d1-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="df4d1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4d1-186">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df4d1-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4d1-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4d1-187">INPUTS</span></span>

### <span data-ttu-id="df4d1-188">System. String</span><span class="sxs-lookup"><span data-stu-id="df4d1-188">System.String</span></span>

### <span data-ttu-id="df4d1-189">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df4d1-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="df4d1-190">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df4d1-190">OUTPUTS</span></span>

### <span data-ttu-id="df4d1-191">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df4d1-191">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="df4d1-192">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="df4d1-192">NOTES</span></span>

## <span data-ttu-id="df4d1-193">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df4d1-193">RELATED LINKS</span></span>

[<span data-ttu-id="df4d1-194">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="df4d1-194">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()