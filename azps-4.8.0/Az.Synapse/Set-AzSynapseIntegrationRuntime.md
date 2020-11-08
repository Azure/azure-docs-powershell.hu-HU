---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017468"
---
# <span data-ttu-id="052e5-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="052e5-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="052e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="052e5-102">SYNOPSIS</span></span>
<span data-ttu-id="052e5-103">Az integrációs futtatókörnyezet frissítése</span><span class="sxs-lookup"><span data-stu-id="052e5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="052e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="052e5-104">SYNTAX</span></span>

### <span data-ttu-id="052e5-105">SetByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="052e5-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="052e5-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="052e5-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e5-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="052e5-107">SetByParentObject</span></span>
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

### <span data-ttu-id="052e5-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="052e5-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e5-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="052e5-109">SetByResourceId</span></span>
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

### <span data-ttu-id="052e5-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="052e5-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="052e5-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="052e5-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="052e5-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="052e5-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="052e5-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="052e5-113">DESCRIPTION</span></span>
<span data-ttu-id="052e5-114">A **set-AzSynapseIntegrationRuntime** parancsmag meghatározott paraméterekkel frissíti az integrációs futtatókörnyezetet.</span><span class="sxs-lookup"><span data-stu-id="052e5-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="052e5-115">Példák</span><span class="sxs-lookup"><span data-stu-id="052e5-115">EXAMPLES</span></span>

### <span data-ttu-id="052e5-116">Példa 1</span><span class="sxs-lookup"><span data-stu-id="052e5-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="052e5-117">A parancsmag frissíti a "teszt-selfhost – IR" nevű integrációs futtatókörnyezet leírását.</span><span class="sxs-lookup"><span data-stu-id="052e5-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="052e5-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="052e5-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="052e5-119">A parancsmag hozzáadja a munkaterületet a megosztott integrációs futtatókörnyezet használatához.</span><span class="sxs-lookup"><span data-stu-id="052e5-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="052e5-120">`-SharedIntegrationRuntimeResourceId`A paraméter használata esetén az is szerepelnie `-Type` kell.</span><span class="sxs-lookup"><span data-stu-id="052e5-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="052e5-121">Felhívjuk a figyelmét arra, hogy a munkaterületnek engedélyt kell adni az integrációs futtatókörnyezet használatához a parancsmag futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="052e5-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="052e5-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="052e5-122">PARAMETERS</span></span>

### <span data-ttu-id="052e5-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="052e5-123">-AuthKey</span></span>
<span data-ttu-id="052e5-124">Az önkiszolgáló integrációs futtatókörnyezet hitelesítési kulcsa.</span><span class="sxs-lookup"><span data-stu-id="052e5-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="052e5-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="052e5-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="052e5-126">Az integrációs futtatókörnyezethez tartozó katalógus-adatbázis-rendszergazdai hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="052e5-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="052e5-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="052e5-127">-CatalogPricingTier</span></span>
<span data-ttu-id="052e5-128">Az integrációs futtatókörnyezet katalógus-adatbázis árazási szintje.</span><span class="sxs-lookup"><span data-stu-id="052e5-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="052e5-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="052e5-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="052e5-130">Az integrációs futtatókörnyezet katalógus Database Server végpontja.</span><span class="sxs-lookup"><span data-stu-id="052e5-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="052e5-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="052e5-131">-DataFlowComputeType</span></span>
<span data-ttu-id="052e5-132">Az adatfolyam-feladatot végrehajtó adatfolyam-fürt számítási típusa.</span><span class="sxs-lookup"><span data-stu-id="052e5-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="052e5-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="052e5-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="052e5-134">Az adatfolyam-feladatot elindító adatfolyam-fürt alapvető száma.</span><span class="sxs-lookup"><span data-stu-id="052e5-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="052e5-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="052e5-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="052e5-136">Az adatfolyam-feladatot elindító adatfolyam-fürt (percben) az idő (percben) beállítása.</span><span class="sxs-lookup"><span data-stu-id="052e5-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="052e5-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="052e5-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="052e5-138">A proxyként használt Self-Hosted-integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="052e5-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="052e5-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="052e5-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="052e5-140">Az Azure Blob Storage nevű hivatkozott szolgáltatás neve, amely a Self-Hosted és az Azure-SSIS integrációs futtatókörnyezet közötti adatok áthelyezésekor használatos adatmegőrzési adattárolóra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="052e5-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="052e5-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="052e5-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="052e5-142">A Self-Hosted és az Azure-SSIS-integrációs futtatókörnyezetek közötti adatáthelyezéshez használt adattároló elérési útját a program akkor használja, ha meg van adva egy alapértelmezett tároló.</span><span class="sxs-lookup"><span data-stu-id="052e5-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="052e5-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052e5-143">-DefaultProfile</span></span>
<span data-ttu-id="052e5-144">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="052e5-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="052e5-145">-Leírás</span><span class="sxs-lookup"><span data-stu-id="052e5-145">-Description</span></span>
<span data-ttu-id="052e5-146">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="052e5-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="052e5-147">– Kiadás</span><span class="sxs-lookup"><span data-stu-id="052e5-147">-Edition</span></span>
<span data-ttu-id="052e5-148">Az SSIS-integrációs futásidejű verzió, amely a standard vagy a nagyvállalati lehet, az alapértelmezett érték a normál, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="052e5-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="052e5-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="052e5-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="052e5-150">A SSIS-integrációs futtatókörnyezet Express egyéni beállítása, amely az egyéni beállítási parancsfájl nélkül használható a konfigurációk és külső gyártók összetevőinek beállításához.</span><span class="sxs-lookup"><span data-stu-id="052e5-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="052e5-151">-Force</span><span class="sxs-lookup"><span data-stu-id="052e5-151">-Force</span></span>
<span data-ttu-id="052e5-152">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="052e5-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="052e5-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="052e5-153">-InputObject</span></span>
<span data-ttu-id="052e5-154">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="052e5-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="052e5-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="052e5-155">-LicenseType</span></span>
<span data-ttu-id="052e5-156">Az SSIS-infravörös beállításhoz használni kívánt licenc típusa.</span><span class="sxs-lookup"><span data-stu-id="052e5-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="052e5-157">Két típus létezik: LicenseIncluded vagy BasePrice.</span><span class="sxs-lookup"><span data-stu-id="052e5-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="052e5-158">Ha jogosult az Azure hibrid használati előnyeinek (AHUB) árazására, kérjük, válassza a BasePrice.</span><span class="sxs-lookup"><span data-stu-id="052e5-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="052e5-159">Ha nem, akkor válassza a LicenseIncluded lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="052e5-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="052e5-160">-Hely</span><span class="sxs-lookup"><span data-stu-id="052e5-160">-Location</span></span>
<span data-ttu-id="052e5-161">Az integrációs futtatókörnyezet leírása.</span><span class="sxs-lookup"><span data-stu-id="052e5-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="052e5-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="052e5-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="052e5-163">A csomópontok maximális párhuzamos végrehajtásának száma egy felügyelt, dedikált integrációs futtatókörnyezet esetében.</span><span class="sxs-lookup"><span data-stu-id="052e5-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="052e5-164">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="052e5-164">-Name</span></span>
<span data-ttu-id="052e5-165">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="052e5-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="052e5-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="052e5-166">-NodeCount</span></span>
<span data-ttu-id="052e5-167">A fürtcsomópontok száma az integrációs futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="052e5-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="052e5-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="052e5-168">-NodeSize</span></span>
<span data-ttu-id="052e5-169">Az integrációs futtatókörnyezet csomópontjának mérete.</span><span class="sxs-lookup"><span data-stu-id="052e5-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="052e5-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="052e5-170">-PublicIP</span></span>
<span data-ttu-id="052e5-171">A statikus nyilvános IP-címek, amelyek az integrációs futtatókörnyezetet fogják használni.</span><span class="sxs-lookup"><span data-stu-id="052e5-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="052e5-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052e5-172">-ResourceGroupName</span></span>
<span data-ttu-id="052e5-173">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="052e5-173">Resource group name.</span></span>

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

### <span data-ttu-id="052e5-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="052e5-174">-ResourceId</span></span>
<span data-ttu-id="052e5-175">A szinapszis-integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="052e5-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="052e5-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="052e5-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="052e5-177">Az egyéni beállítási parancsfájlt tartalmazó Azure Blob-tároló SAS-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="052e5-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="052e5-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="052e5-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="052e5-179">A megosztott önkiszolgáló integrációs futtatókörnyezet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="052e5-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="052e5-180">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="052e5-180">-Subnet</span></span>
<span data-ttu-id="052e5-181">Az alhálózat neve a VNet.</span><span class="sxs-lookup"><span data-stu-id="052e5-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="052e5-182">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="052e5-182">-Type</span></span>
<span data-ttu-id="052e5-183">Az integrációs futtatókörnyezet típusa.</span><span class="sxs-lookup"><span data-stu-id="052e5-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="052e5-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="052e5-184">-VNetId</span></span>
<span data-ttu-id="052e5-185">Annak az VNet az azonosítója, amelyhez az integrációs futtatókörnyezet csatlakozni fog.</span><span class="sxs-lookup"><span data-stu-id="052e5-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="052e5-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="052e5-186">-WorkspaceName</span></span>
<span data-ttu-id="052e5-187">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="052e5-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="052e5-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="052e5-188">-WorkspaceObject</span></span>
<span data-ttu-id="052e5-189">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="052e5-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="052e5-190">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="052e5-190">-Confirm</span></span>
<span data-ttu-id="052e5-191">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="052e5-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="052e5-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="052e5-192">-WhatIf</span></span>
<span data-ttu-id="052e5-193">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="052e5-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="052e5-194">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="052e5-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="052e5-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052e5-195">CommonParameters</span></span>
<span data-ttu-id="052e5-196">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="052e5-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052e5-197">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="052e5-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052e5-198">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="052e5-198">INPUTS</span></span>

### <span data-ttu-id="052e5-199">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="052e5-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="052e5-200">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="052e5-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="052e5-201">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="052e5-201">OUTPUTS</span></span>

### <span data-ttu-id="052e5-202">Microsoft. Azure. commands. szinapszis. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="052e5-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="052e5-203">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="052e5-203">NOTES</span></span>

## <span data-ttu-id="052e5-204">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="052e5-204">RELATED LINKS</span></span>
