---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298247"
---
# <span data-ttu-id="f73f5-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f73f5-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f73f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f73f5-102">SYNOPSIS</span></span>
<span data-ttu-id="f73f5-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="f73f5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="f73f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f73f5-104">SYNTAX</span></span>

### <span data-ttu-id="f73f5-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f73f5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f73f5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f73f5-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73f5-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f73f5-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73f5-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f73f5-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73f5-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f73f5-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f73f5-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f73f5-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f73f5-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="f73f5-111">DESCRIPTION</span></span>
<span data-ttu-id="f73f5-112">A Set-AzDataFactoryV2IntegrationRuntime parancsmag meghatározott paraméterekkel frissíti az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="f73f5-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="f73f5-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f73f5-113">EXAMPLES</span></span>

### <span data-ttu-id="f73f5-114">1. példa: az integrációs futtatókörnyezet frissítésének leírása.</span><span class="sxs-lookup"><span data-stu-id="f73f5-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="f73f5-115">A parancsmag frissíti a "teszt-selfhost – IR" nevű integrációs futtatókörnyezet leírását.</span><span class="sxs-lookup"><span data-stu-id="f73f5-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="f73f5-116">2. példa: az önálló, önállóan működtetett integrációs futtatókörnyezet megosztása.</span><span class="sxs-lookup"><span data-stu-id="f73f5-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="f73f5-117">A parancsmag hozzáadja az ADF-t a megosztott integrációs futtatókörnyezet használatához.</span><span class="sxs-lookup"><span data-stu-id="f73f5-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="f73f5-118">`-SharedIntegrationRuntimeResourceId`A paraméter használata esetén az is szerepelnie `-Type` kell.</span><span class="sxs-lookup"><span data-stu-id="f73f5-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="f73f5-119">Felhívjuk a figyelmét arra, hogy az adatfeldolgozónak engedélyt kell adni az integrációs futtatókörnyezet használatához a parancsmag futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="f73f5-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="f73f5-120">3. példa: a Self-Hosted IR beállítása az Azure-SSIS infravörös kapcsolatának beállítása ADF-ben.</span><span class="sxs-lookup"><span data-stu-id="f73f5-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="f73f5-121">A parancsmag az Azure-SSIS-integrációs futtatókörnyezetet használja az önálló, önállóan működtetett integrációs futtatókörnyezethez adatproxyként.</span><span class="sxs-lookup"><span data-stu-id="f73f5-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="f73f5-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f73f5-122">PARAMETERS</span></span>

### <span data-ttu-id="f73f5-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="f73f5-123">-AuthKey</span></span>
<span data-ttu-id="f73f5-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="f73f5-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="f73f5-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="f73f5-126">Az integrációs futtatókörnyezethez tartozó katalógus-adatbázis-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="f73f5-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="f73f5-127">-CatalogPricingTier</span></span>
<span data-ttu-id="f73f5-128">Az integrációs futtatókörnyezet katalógus-adatbázis árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="f73f5-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f73f5-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="f73f5-130">Az integrációs futtatókörnyezet katalógus Database Server végpontja.</span><span class="sxs-lookup"><span data-stu-id="f73f5-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f73f5-131">-DataFactoryName</span></span>
<span data-ttu-id="f73f5-132">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="f73f5-132">The data factory name.</span></span>

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

### <span data-ttu-id="f73f5-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="f73f5-133">-DataFlowComputeType</span></span>
<span data-ttu-id="f73f5-134">Az adatfolyam-feladatot végrehajtó adatfolyam-fürt számítási típusa.</span><span class="sxs-lookup"><span data-stu-id="f73f5-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f73f5-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="f73f5-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="f73f5-136">Az adatfolyam-feladatot elindító adatfolyam-fürt alapvető száma.</span><span class="sxs-lookup"><span data-stu-id="f73f5-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f73f5-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="f73f5-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="f73f5-138">Az adatfolyam-feladatot elindító adatfolyam-fürt (percben) az idő (percben) beállítása.</span><span class="sxs-lookup"><span data-stu-id="f73f5-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="f73f5-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="f73f5-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="f73f5-140">A proxyként használt Self-Hosted-integrációs futásidejű név</span><span class="sxs-lookup"><span data-stu-id="f73f5-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="f73f5-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="f73f5-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="f73f5-142">A Self-Hosted és az Azure-SSIS integrációs futtatókörnyezete között az adatok áthelyezésekor használandó átmeneti adattárolóra hivatkozó Azure Blob Storage kapcsolt szolgáltatás neve</span><span class="sxs-lookup"><span data-stu-id="f73f5-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="f73f5-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="f73f5-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="f73f5-144">Az adattárolási útvonal az Self-Hosted és az Azure-SSIS integrációs futtatókörnyezete közötti adatáthelyezéskor használatos az alapértelmezett tárolóhoz</span><span class="sxs-lookup"><span data-stu-id="f73f5-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="f73f5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73f5-145">-DefaultProfile</span></span>
<span data-ttu-id="f73f5-146">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f73f5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f73f5-147">-Leírás</span><span class="sxs-lookup"><span data-stu-id="f73f5-147">-Description</span></span>
<span data-ttu-id="f73f5-148">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="f73f5-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="f73f5-149">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="f73f5-149">-Edition</span></span>
<span data-ttu-id="f73f5-150">Az SSIS-integrációs futásidejű verzió, amely a standard vagy a nagyvállalati lehet, az alapértelmezett érték a normál, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f73f5-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="f73f5-151">-Force</span><span class="sxs-lookup"><span data-stu-id="f73f5-151">-Force</span></span>
<span data-ttu-id="f73f5-152">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f73f5-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f73f5-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f73f5-153">-InputObject</span></span>
<span data-ttu-id="f73f5-154">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="f73f5-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="f73f5-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f73f5-155">-LicenseType</span></span>
<span data-ttu-id="f73f5-156">Az SSIS-infravörös beállításhoz használni kívánt licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="f73f5-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="f73f5-157">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f73f5-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="f73f5-158">Ha jogosult az Azure hibrid használati előnyeinek (AHUB) árazására, kérjük, válassza a BasePrice.</span><span class="sxs-lookup"><span data-stu-id="f73f5-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="f73f5-159">Ha nem, akkor válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="f73f5-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="f73f5-160">-Hely</span><span class="sxs-lookup"><span data-stu-id="f73f5-160">-Location</span></span>
<span data-ttu-id="f73f5-161">Az integrációs futtatókörnyezet helye.</span><span class="sxs-lookup"><span data-stu-id="f73f5-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="f73f5-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="f73f5-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="f73f5-163">A csomópontok maximális párhuzamos végrehajtásának száma egy felügyelt, dedikált integrációs futtatókörnyezet esetében.</span><span class="sxs-lookup"><span data-stu-id="f73f5-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-164">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f73f5-164">-Name</span></span>
<span data-ttu-id="f73f5-165">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="f73f5-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="f73f5-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="f73f5-166">-NodeCount</span></span>
<span data-ttu-id="f73f5-167">A fürtcsomópontok száma az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="f73f5-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="f73f5-168">-NodeSize</span></span>
<span data-ttu-id="f73f5-169">Az integrációs futtatókörnyezet csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="f73f5-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="f73f5-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="f73f5-170">-PublicIPs</span></span>
<span data-ttu-id="f73f5-171">A statikus nyilvános IP-címek, amelyek az integrációs futtatókörnyezetet fogják használni.</span><span class="sxs-lookup"><span data-stu-id="f73f5-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="f73f5-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73f5-172">-ResourceGroupName</span></span>
<span data-ttu-id="f73f5-173">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f73f5-173">The resource group name.</span></span>

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

### <span data-ttu-id="f73f5-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f73f5-174">-ResourceId</span></span>
<span data-ttu-id="f73f5-175">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f73f5-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f73f5-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="f73f5-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="f73f5-177">Az egyéni beállítási parancsfájlt tartalmazó Azure Blob-tároló SAS-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f73f5-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="f73f5-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="f73f5-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="f73f5-179">A megosztott önkiszolgáló integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f73f5-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="f73f5-180">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="f73f5-180">-Subnet</span></span>
<span data-ttu-id="f73f5-181">Az alhálózat neve a VNet.</span><span class="sxs-lookup"><span data-stu-id="f73f5-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="f73f5-182">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="f73f5-182">-Type</span></span>
<span data-ttu-id="f73f5-183">Az integrációs futtatókörnyezet típusa.</span><span class="sxs-lookup"><span data-stu-id="f73f5-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="f73f5-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="f73f5-184">-VNetId</span></span>
<span data-ttu-id="f73f5-185">Annak az VNet az azonosítója, amelyhez az integrációs futtatókörnyezet csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="f73f5-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="f73f5-186">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f73f5-186">-Confirm</span></span>
<span data-ttu-id="f73f5-187">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f73f5-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f73f5-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f73f5-188">-WhatIf</span></span>
<span data-ttu-id="f73f5-189">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f73f5-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f73f5-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73f5-190">CommonParameters</span></span>
<span data-ttu-id="f73f5-191">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f73f5-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73f5-192">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73f5-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73f5-193">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f73f5-193">INPUTS</span></span>

### <span data-ttu-id="f73f5-194">System. String</span><span class="sxs-lookup"><span data-stu-id="f73f5-194">System.String</span></span>

### <span data-ttu-id="f73f5-195">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f73f5-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f73f5-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f73f5-196">OUTPUTS</span></span>

### <span data-ttu-id="f73f5-197">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f73f5-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f73f5-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f73f5-198">NOTES</span></span>

## <span data-ttu-id="f73f5-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f73f5-199">RELATED LINKS</span></span>

[<span data-ttu-id="f73f5-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f73f5-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
