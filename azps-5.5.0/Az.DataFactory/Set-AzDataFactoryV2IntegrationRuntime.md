---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204431"
---
# <span data-ttu-id="b4e2e-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4e2e-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="b4e2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e2e-103">Egy integrációs futási idő frissítése.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="b4e2e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4e2e-104">SYNTAX</span></span>

### <span data-ttu-id="b4e2e-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4e2e-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="b4e2e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e2e-106">ByResourceId</span></span>
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

### <span data-ttu-id="b4e2e-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e2e-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e2e-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b4e2e-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e2e-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b4e2e-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="b4e2e-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b4e2e-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e2e-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4e2e-111">DESCRIPTION</span></span>
<span data-ttu-id="b4e2e-112">A Set-AzDataFactoryV2IntegrationRuntime parancsmag adott paraméterekkel frissíti az integrációs futásiidőt.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="b4e2e-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4e2e-113">EXAMPLES</span></span>

### <span data-ttu-id="b4e2e-114">1. példa: Az integráció futásidejű leírásának frissítése.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="b4e2e-115">A parancsmag frissíti a "test-selfhost-ir" nevű integrációs futási idő leírását.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="b4e2e-116">2. példa: Önkiszolgáló integrációs futásidejű megosztás.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="b4e2e-117">A parancsmag hozzáadja az ADF-et a megosztott integrációs futásidejű használathoz.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="b4e2e-118">Paraméter használata `-SharedIntegrationRuntimeResourceId` esetén az `-Type` értéknek is szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="b4e2e-119">Ne feledje, hogy a parancsmag futtatása előtt az adat factorynak engedélyt kell adni az integrációs futtatókörnyezet használatára.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="b4e2e-120">3. példa: Az Self-Hosted IR konfigurálása az Azure-SSIS IR proxyjaként az ADF-ben.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="b4e2e-121">A parancsmag frissítése az Azure-SSIS-integráció futásidejére, hogy önkiszolgáló integrációs futásiidőt használjon adatproxyként.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="b4e2e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4e2e-122">PARAMETERS</span></span>

### <span data-ttu-id="b4e2e-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="b4e2e-123">-AuthKey</span></span>
<span data-ttu-id="b4e2e-124">Az önkiszolgáló integráció futásidejű futásidejű hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="b4e2e-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="b4e2e-126">Az integrációs futásidejű katalógus-adatbázis rendszergazdájának hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="b4e2e-127">-CatalogPricingTier</span></span>
<span data-ttu-id="b4e2e-128">Az integrációs futásidejű katalógus-adatbázis árazási rétege.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b4e2e-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="b4e2e-130">Az integrációs futásidő katalógus-adatbázis-kiszolgálójának végpontja.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4e2e-131">-DataFactoryName</span></span>
<span data-ttu-id="b4e2e-132">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-132">The data factory name.</span></span>

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

### <span data-ttu-id="b4e2e-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="b4e2e-133">-DataFlowComputeType</span></span>
<span data-ttu-id="b4e2e-134">Az adatfolyam-fürt típusának kiszámítása, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b4e2e-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="b4e2e-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="b4e2e-136">Az adatfolyam-fürt alapszáma, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b4e2e-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b4e2e-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="b4e2e-138">Az adatfolyam-fürtnek az adatfolyam-fürtnek az adatfolyam-feladat végrehajtására (percben) vonatkozó beállítása.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="b4e2e-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b4e2e-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="b4e2e-140">Az Self-Hosted-integrációs futásidejű név, amely proxyként használatos</span><span class="sxs-lookup"><span data-stu-id="b4e2e-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="b4e2e-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b4e2e-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="b4e2e-142">Az Azure Blob Storage Csatolt szolgáltatás neve, amely az átmeneti adattárra hivatkozik, és amely az adatok Self-Hosted és az Azure-SSIS integration Runtime között való adatokat mozgatja</span><span class="sxs-lookup"><span data-stu-id="b4e2e-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="b4e2e-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="b4e2e-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="b4e2e-144">A Self-Hosted és az Azure-SSIS Integration Runtimes közötti adatáthelyezéshez használt adattár elérési útja, ha nincs megadva az alapértelmezett tároló.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="b4e2e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e2e-145">-DefaultProfile</span></span>
<span data-ttu-id="b4e2e-146">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4e2e-147">-Leírás</span><span class="sxs-lookup"><span data-stu-id="b4e2e-147">-Description</span></span>
<span data-ttu-id="b4e2e-148">Az integráció futásidejű leírása.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="b4e2e-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="b4e2e-149">-Edition</span></span>
<span data-ttu-id="b4e2e-150">Az SSIS-integráció futásidejű változata, amely lehet Standard vagy Enterprise, alapérték, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="b4e2e-151">-Force</span><span class="sxs-lookup"><span data-stu-id="b4e2e-151">-Force</span></span>
<span data-ttu-id="b4e2e-152">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b4e2e-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4e2e-153">-InputObject</span></span>
<span data-ttu-id="b4e2e-154">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="b4e2e-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b4e2e-155">-LicenseType</span></span>
<span data-ttu-id="b4e2e-156">Az SSIS IR-hez kiválasztani kívánt licenctípus.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="b4e2e-157">Kétféle típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="b4e2e-158">Ha Jogosult az Azure Hybrid Use Benefit (AHUB) árára, válassza a BasePrice lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="b4e2e-159">Ha nem, válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="b4e2e-160">-Location</span><span class="sxs-lookup"><span data-stu-id="b4e2e-160">-Location</span></span>
<span data-ttu-id="b4e2e-161">Az integráció futásidejű helye.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="b4e2e-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="b4e2e-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="b4e2e-163">Csomópontonkénti maximális párhuzamos végrehajtások száma felügyelt dedikált integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-164">-Name</span><span class="sxs-lookup"><span data-stu-id="b4e2e-164">-Name</span></span>
<span data-ttu-id="b4e2e-165">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="b4e2e-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b4e2e-166">-NodeCount</span></span>
<span data-ttu-id="b4e2e-167">Az integrációs futásidejű célcsomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="b4e2e-168">-NodeSize</span></span>
<span data-ttu-id="b4e2e-169">Az integráció futásidejű csomópontmérete.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="b4e2e-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="b4e2e-170">-PublicIPs</span></span>
<span data-ttu-id="b4e2e-171">Az integrációs futásidejű statikus nyilvános IP-címek.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="b4e2e-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e2e-172">-ResourceGroupName</span></span>
<span data-ttu-id="b4e2e-173">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-173">The resource group name.</span></span>

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

### <span data-ttu-id="b4e2e-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e2e-174">-ResourceId</span></span>
<span data-ttu-id="b4e2e-175">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4e2e-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="b4e2e-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="b4e2e-177">Az egyéni beállítási parancsfájlt tartalmazó Azure blobtároló SAS URI-ja.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="b4e2e-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e2e-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="b4e2e-179">A megosztott önkiszolgáló integráció futásidejű futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="b4e2e-180">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="b4e2e-180">-Subnet</span></span>
<span data-ttu-id="b4e2e-181">A VNetben található alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="b4e2e-182">-Type</span><span class="sxs-lookup"><span data-stu-id="b4e2e-182">-Type</span></span>
<span data-ttu-id="b4e2e-183">Az integráció futásidejű típusa.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="b4e2e-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="b4e2e-184">-VNetId</span></span>
<span data-ttu-id="b4e2e-185">Annak a VNetnek az azonosítója, amelyhez az integrációs futásidejű futási idő csatlakozik.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="b4e2e-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4e2e-186">-Confirm</span></span>
<span data-ttu-id="b4e2e-187">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e2e-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e2e-188">-WhatIf</span></span>
<span data-ttu-id="b4e2e-189">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b4e2e-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e2e-190">CommonParameters</span></span>
<span data-ttu-id="b4e2e-191">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e2e-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e2e-192">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e2e-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e2e-193">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4e2e-193">INPUTS</span></span>

### <span data-ttu-id="b4e2e-194">System.String</span><span class="sxs-lookup"><span data-stu-id="b4e2e-194">System.String</span></span>

### <span data-ttu-id="b4e2e-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4e2e-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b4e2e-196">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4e2e-196">OUTPUTS</span></span>

### <span data-ttu-id="b4e2e-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4e2e-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b4e2e-198">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4e2e-198">NOTES</span></span>

## <span data-ttu-id="b4e2e-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4e2e-199">RELATED LINKS</span></span>

[<span data-ttu-id="b4e2e-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b4e2e-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
