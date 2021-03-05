---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: a76731c52de32f8b92ed244f82c6afd69bab32d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007493"
---
# <span data-ttu-id="33997-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33997-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="33997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33997-102">SYNOPSIS</span></span>
<span data-ttu-id="33997-103">Egy integrációs futási idő frissítése.</span><span class="sxs-lookup"><span data-stu-id="33997-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="33997-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33997-104">SYNTAX</span></span>

### <span data-ttu-id="33997-105">SetByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33997-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="33997-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="33997-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="33997-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="33997-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="33997-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="33997-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33997-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="33997-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33997-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33997-113">DESCRIPTION</span></span>
<span data-ttu-id="33997-114">A **Set-AzSynapseIntegrationRuntime parancsmag** adott paraméterekkel frissíti az integrációs runtime-t.</span><span class="sxs-lookup"><span data-stu-id="33997-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="33997-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33997-115">EXAMPLES</span></span>

### <span data-ttu-id="33997-116">1. példa</span><span class="sxs-lookup"><span data-stu-id="33997-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="33997-117">A parancsmag frissíti a "test-selfhost-ir" nevű integrációs futási idő leírását.</span><span class="sxs-lookup"><span data-stu-id="33997-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="33997-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="33997-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="33997-119">A parancsmag hozzáadja a munkaterületet a megosztott integrációs futásidejű használathoz.</span><span class="sxs-lookup"><span data-stu-id="33997-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="33997-120">Paraméter használata `-SharedIntegrationRuntimeResourceId` esetén az `-Type` értéknek is szerepelnie kell.</span><span class="sxs-lookup"><span data-stu-id="33997-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="33997-121">Ne feledje, hogy a munkaterületnek engedélyt kell adni az integráció futásidejű használatára a parancsmag futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="33997-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="33997-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33997-122">PARAMETERS</span></span>

### <span data-ttu-id="33997-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="33997-123">-AuthKey</span></span>
<span data-ttu-id="33997-124">Az önkiszolgáló integráció futásidejű futásidejű hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="33997-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="33997-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="33997-126">Az integrációs futásidejű katalógus-adatbázis rendszergazdájának hitelesítő adatai.</span><span class="sxs-lookup"><span data-stu-id="33997-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="33997-127">-CatalogPricingTier</span></span>
<span data-ttu-id="33997-128">Az integrációs futásidejű katalógus-adatbázis árazási rétege.</span><span class="sxs-lookup"><span data-stu-id="33997-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33997-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="33997-130">Az integrációs futásidő katalógus-adatbázis-kiszolgálójának végpontja.</span><span class="sxs-lookup"><span data-stu-id="33997-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="33997-131">-DataFlowComputeType</span></span>
<span data-ttu-id="33997-132">Az adatfolyam-fürt típusának kiszámítása, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="33997-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="33997-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="33997-134">Az adatfolyam-fürt alapszáma, amely végrehajtja az adatfolyam-feladatot.</span><span class="sxs-lookup"><span data-stu-id="33997-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="33997-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="33997-136">Az adatfolyam-fürtnek az adatfolyam-fürtnek az adatfolyam-feladat végrehajtására (percben) vonatkozó beállítása.</span><span class="sxs-lookup"><span data-stu-id="33997-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="33997-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="33997-138">Az Self-Hosted-integrációs futásidejű név, amely proxyként használatos.</span><span class="sxs-lookup"><span data-stu-id="33997-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="33997-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="33997-140">Az Azure Blob Storage Csatolt szolgáltatás neve, amely az átmeneti adattárra hivatkozik, és amely az adatok Self-Hosted Azure-SSIS Integration Runtime között történő adatokat mozgatja.</span><span class="sxs-lookup"><span data-stu-id="33997-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="33997-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="33997-142">A Self-Hosted és az Azure-SSIS Integration Runtimes közötti adatáthelyezéshez használt adattár elérési útja, ha nincs megadva, az alapértelmezett tároló lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="33997-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33997-143">-DefaultProfile</span></span>
<span data-ttu-id="33997-144">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33997-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33997-145">-Leírás</span><span class="sxs-lookup"><span data-stu-id="33997-145">-Description</span></span>
<span data-ttu-id="33997-146">Az integráció futásidejű leírása.</span><span class="sxs-lookup"><span data-stu-id="33997-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="33997-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="33997-147">-Edition</span></span>
<span data-ttu-id="33997-148">Az SSIS-integráció futásidejű változata, amely lehet Standard vagy Enterprise, alapértelmezés szerint Normál, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="33997-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="33997-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="33997-150">Az SSIS-integráció futásidejébe való gyors egyéni beállítás, amely egyéni beállítási parancsprogram nélküli konfigurációk és külső összetevők beállításához használható.</span><span class="sxs-lookup"><span data-stu-id="33997-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-151">-Force</span><span class="sxs-lookup"><span data-stu-id="33997-151">-Force</span></span>
<span data-ttu-id="33997-152">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="33997-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="33997-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33997-153">-InputObject</span></span>
<span data-ttu-id="33997-154">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="33997-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33997-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="33997-155">-LicenseType</span></span>
<span data-ttu-id="33997-156">Az SSIS IR-hez kiválasztani kívánt licenctípus.</span><span class="sxs-lookup"><span data-stu-id="33997-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="33997-157">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="33997-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="33997-158">Ha Jogosult az Azure Hybrid Use Benefit (AHUB) árára, válassza a BasePrice lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="33997-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="33997-159">Ha nem, válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="33997-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-160">-Location</span><span class="sxs-lookup"><span data-stu-id="33997-160">-Location</span></span>
<span data-ttu-id="33997-161">Az integráció futásidejű leírása.</span><span class="sxs-lookup"><span data-stu-id="33997-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="33997-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="33997-163">Csomópontonkénti maximális párhuzamos végrehajtások száma felügyelt dedikált integrációs futási időben.</span><span class="sxs-lookup"><span data-stu-id="33997-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-164">-Name</span><span class="sxs-lookup"><span data-stu-id="33997-164">-Name</span></span>
<span data-ttu-id="33997-165">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="33997-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="33997-166">-NodeCount</span></span>
<span data-ttu-id="33997-167">Az integrációs futásidejű célcsomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="33997-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="33997-168">-NodeSize</span></span>
<span data-ttu-id="33997-169">Az integráció futásidejű csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="33997-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="33997-170">-PublicIP</span></span>
<span data-ttu-id="33997-171">Az integrációs futásidejű statikus nyilvános IP-címek.</span><span class="sxs-lookup"><span data-stu-id="33997-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33997-172">-ResourceGroupName</span></span>
<span data-ttu-id="33997-173">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33997-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33997-174">-ResourceId</span></span>
<span data-ttu-id="33997-175">A Synapse-integráció futásideje erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33997-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="33997-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="33997-177">Az egyéni telepítőprogramot tartalmazó Azure blobtároló SAS URI-ja.</span><span class="sxs-lookup"><span data-stu-id="33997-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="33997-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="33997-179">A megosztott önkiszolgáló integrációs futási idő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="33997-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-180">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="33997-180">-Subnet</span></span>
<span data-ttu-id="33997-181">A VNetben található alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="33997-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-182">-Type</span><span class="sxs-lookup"><span data-stu-id="33997-182">-Type</span></span>
<span data-ttu-id="33997-183">Az integráció futásidejű típusa.</span><span class="sxs-lookup"><span data-stu-id="33997-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="33997-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="33997-184">-VNetId</span></span>
<span data-ttu-id="33997-185">Annak a VNetnek az azonosítója, amelyhez az integrációs futásidejű futási idő csatlakozni fog.</span><span class="sxs-lookup"><span data-stu-id="33997-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="33997-186">-WorkspaceName</span></span>
<span data-ttu-id="33997-187">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="33997-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33997-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="33997-188">-WorkspaceObject</span></span>
<span data-ttu-id="33997-189">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="33997-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33997-190">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33997-190">-Confirm</span></span>
<span data-ttu-id="33997-191">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="33997-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33997-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33997-192">-WhatIf</span></span>
<span data-ttu-id="33997-193">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="33997-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33997-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="33997-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33997-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33997-195">CommonParameters</span></span>
<span data-ttu-id="33997-196">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33997-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33997-197">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33997-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33997-198">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33997-198">INPUTS</span></span>

### <span data-ttu-id="33997-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="33997-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="33997-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33997-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33997-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33997-201">OUTPUTS</span></span>

### <span data-ttu-id="33997-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33997-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33997-203">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33997-203">NOTES</span></span>

## <span data-ttu-id="33997-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33997-204">RELATED LINKS</span></span>
