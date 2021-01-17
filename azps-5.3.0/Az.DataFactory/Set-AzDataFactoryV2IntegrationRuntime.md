---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477070"
---
# <span data-ttu-id="c97d2-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c97d2-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c97d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c97d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c97d2-103">Egy integrációs futási idő frissítése.</span><span class="sxs-lookup"><span data-stu-id="c97d2-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c97d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c97d2-104">SYNTAX</span></span>

### <span data-ttu-id="c97d2-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c97d2-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="c97d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c97d2-106">ByResourceId</span></span>
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

### <span data-ttu-id="c97d2-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c97d2-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97d2-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c97d2-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c97d2-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c97d2-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="c97d2-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c97d2-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97d2-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c97d2-111">DESCRIPTION</span></span>
<span data-ttu-id="c97d2-112">A Set-AzDataFactoryV2IntegrationRuntime parancsmag adott paraméterekkel frissíti az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="c97d2-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="c97d2-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c97d2-113">EXAMPLES</span></span>

### <span data-ttu-id="c97d2-114">1. példa: Az integráció futásidejű leírásának frissítése.</span><span class="sxs-lookup"><span data-stu-id="c97d2-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="c97d2-115">A parancsmag frissíti a "test-selfhost-ir" nevű integrációs futási idő leírását.</span><span class="sxs-lookup"><span data-stu-id="c97d2-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="c97d2-116">2. példa: Önkiszolgáló integrációs futásidejű megosztás.</span><span class="sxs-lookup"><span data-stu-id="c97d2-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="c97d2-117">A parancsmag hozzáadja az ADF-et a megosztott integrációs futásidejű használathoz.</span><span class="sxs-lookup"><span data-stu-id="c97d2-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="c97d2-118">Paraméter használata `-SharedIntegrationRuntimeResourceId` esetén az `-Type` értéknek is szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="c97d2-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="c97d2-119">Ne feledje, hogy a parancsmag futtatása előtt az adat factorynak engedélyt kell adni az integrációs futtatókörnyezet használatára.</span><span class="sxs-lookup"><span data-stu-id="c97d2-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="c97d2-120">3. példa: Konfigurálja az Self-Hosted IR-t proxyként az Azure-SSIS IR számára az ADF-ben.</span><span class="sxs-lookup"><span data-stu-id="c97d2-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="c97d2-121">A parancsmag frissítése az Azure-SSIS-integráció futásidejére, hogy önkiszolgáló integrációs futásiidőt használjon adatproxyként.</span><span class="sxs-lookup"><span data-stu-id="c97d2-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="c97d2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c97d2-122">PARAMETERS</span></span>

### <span data-ttu-id="c97d2-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="c97d2-123">-AuthKey</span></span>
<span data-ttu-id="c97d2-124">Az önkiszolgáló integráció futásidejű futásidejű hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="c97d2-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="c97d2-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="c97d2-126">Az integrációs futásidejű katalógus-adatbázis rendszergazdájának hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="c97d2-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="c97d2-127">-CatalogPricingTier</span></span>
<span data-ttu-id="c97d2-128">Az integrációs futásidejű katalógus-adatbázis árazási rétege.</span><span class="sxs-lookup"><span data-stu-id="c97d2-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c97d2-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="c97d2-130">Az integrációs futásidő katalógus-adatbázis-kiszolgálójának végpontja.</span><span class="sxs-lookup"><span data-stu-id="c97d2-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c97d2-131">-DataFactoryName</span></span>
<span data-ttu-id="c97d2-132">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="c97d2-132">The data factory name.</span></span>

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

### <span data-ttu-id="c97d2-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="c97d2-133">-DataFlowComputeType</span></span>
<span data-ttu-id="c97d2-134">Az adatfolyam-fürt típusának kiszámítása, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="c97d2-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c97d2-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="c97d2-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="c97d2-136">Az adatfolyam-fürt alapszáma, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="c97d2-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c97d2-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="c97d2-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="c97d2-138">Az adatfolyam-fürtnek az adatfolyam-fürtnek az adatfolyam-feladat végrehajtására (percben) vonatkozó beállítása.</span><span class="sxs-lookup"><span data-stu-id="c97d2-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="c97d2-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c97d2-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="c97d2-140">A Self-Hosted-integrációs futásidejű név, amely proxyként használatos</span><span class="sxs-lookup"><span data-stu-id="c97d2-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="c97d2-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c97d2-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="c97d2-142">Az Azure Blob Storage Csatolt szolgáltatás neve, amely az átmeneti adattárra hivatkozik, és amely az adatok Self-Hosted és az Azure-SSIS integration Runtime között való adatokat mozgatja</span><span class="sxs-lookup"><span data-stu-id="c97d2-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="c97d2-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="c97d2-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="c97d2-144">A Self-Hosted és az Azure-SSIS Integration Runtimes közötti adatáthelyezéshez használt adattár elérési útja, ha nincs megadva az alapértelmezett tároló.</span><span class="sxs-lookup"><span data-stu-id="c97d2-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="c97d2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97d2-145">-DefaultProfile</span></span>
<span data-ttu-id="c97d2-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c97d2-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97d2-147">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c97d2-147">-Description</span></span>
<span data-ttu-id="c97d2-148">Az integráció futásidejű leírása.</span><span class="sxs-lookup"><span data-stu-id="c97d2-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="c97d2-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="c97d2-149">-Edition</span></span>
<span data-ttu-id="c97d2-150">Az SSIS-integráció futásidejű változata, amely lehet Standard vagy Enterprise, alapérték, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="c97d2-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="c97d2-151">-Force</span><span class="sxs-lookup"><span data-stu-id="c97d2-151">-Force</span></span>
<span data-ttu-id="c97d2-152">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c97d2-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c97d2-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c97d2-153">-InputObject</span></span>
<span data-ttu-id="c97d2-154">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="c97d2-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="c97d2-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c97d2-155">-LicenseType</span></span>
<span data-ttu-id="c97d2-156">Az SSIS IR-hez kiválasztani kívánt licenctípus.</span><span class="sxs-lookup"><span data-stu-id="c97d2-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="c97d2-157">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="c97d2-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="c97d2-158">Ha Jogosult az Azure Hybrid Use Benefit (AHUB) árára, válassza a BasePrice lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97d2-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="c97d2-159">Ha nem, válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="c97d2-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="c97d2-160">-Location</span><span class="sxs-lookup"><span data-stu-id="c97d2-160">-Location</span></span>
<span data-ttu-id="c97d2-161">Az integráció futásidejű helye.</span><span class="sxs-lookup"><span data-stu-id="c97d2-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="c97d2-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="c97d2-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="c97d2-163">Csomópontonkénti maximális párhuzamos végrehajtások száma felügyelt dedikált integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="c97d2-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-164">-Name</span><span class="sxs-lookup"><span data-stu-id="c97d2-164">-Name</span></span>
<span data-ttu-id="c97d2-165">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="c97d2-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="c97d2-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c97d2-166">-NodeCount</span></span>
<span data-ttu-id="c97d2-167">Az integrációs futásidejű célcsomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="c97d2-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c97d2-168">-NodeSize</span></span>
<span data-ttu-id="c97d2-169">Az integráció futásidejű csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="c97d2-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="c97d2-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="c97d2-170">-PublicIPs</span></span>
<span data-ttu-id="c97d2-171">Az integrációs futásidejű statikus nyilvános IP-címek.</span><span class="sxs-lookup"><span data-stu-id="c97d2-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="c97d2-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c97d2-172">-ResourceGroupName</span></span>
<span data-ttu-id="c97d2-173">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c97d2-173">The resource group name.</span></span>

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

### <span data-ttu-id="c97d2-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c97d2-174">-ResourceId</span></span>
<span data-ttu-id="c97d2-175">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="c97d2-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c97d2-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c97d2-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="c97d2-177">Az egyéni telepítőprogramot tartalmazó Azure blobtároló SAS URI-ja.</span><span class="sxs-lookup"><span data-stu-id="c97d2-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="c97d2-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c97d2-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="c97d2-179">A megosztott önkiszolgáló integráció futásidejű futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c97d2-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c97d2-180">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="c97d2-180">-Subnet</span></span>
<span data-ttu-id="c97d2-181">A VNetben található alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="c97d2-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="c97d2-182">-Type</span><span class="sxs-lookup"><span data-stu-id="c97d2-182">-Type</span></span>
<span data-ttu-id="c97d2-183">Az integráció futásidejű típusa.</span><span class="sxs-lookup"><span data-stu-id="c97d2-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="c97d2-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="c97d2-184">-VNetId</span></span>
<span data-ttu-id="c97d2-185">Annak a VNetnek az azonosítója, amelyhez az integrációs futásidejű futási idő csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="c97d2-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="c97d2-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c97d2-186">-Confirm</span></span>
<span data-ttu-id="c97d2-187">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c97d2-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97d2-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97d2-188">-WhatIf</span></span>
<span data-ttu-id="c97d2-189">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c97d2-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c97d2-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97d2-190">CommonParameters</span></span>
<span data-ttu-id="c97d2-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97d2-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97d2-192">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97d2-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97d2-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c97d2-193">INPUTS</span></span>

### <span data-ttu-id="c97d2-194">System.String</span><span class="sxs-lookup"><span data-stu-id="c97d2-194">System.String</span></span>

### <span data-ttu-id="c97d2-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c97d2-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c97d2-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c97d2-196">OUTPUTS</span></span>

### <span data-ttu-id="c97d2-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c97d2-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c97d2-198">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c97d2-198">NOTES</span></span>

## <span data-ttu-id="c97d2-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c97d2-199">RELATED LINKS</span></span>

[<span data-ttu-id="c97d2-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c97d2-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
