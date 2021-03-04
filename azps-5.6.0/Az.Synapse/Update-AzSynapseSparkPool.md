---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: f8657a8a9b8f4c4c15606e70f632e6ad0b29a33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939121"
---
# <span data-ttu-id="c9b7b-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c9b7b-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="c9b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b7b-103">Frissíti a Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c9b7b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-104">SYNTAX</span></span>

### <span data-ttu-id="c9b7b-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9b7b-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b7b-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b7b-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b7b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b7b-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9b7b-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9b7b-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9b7b-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-109">DESCRIPTION</span></span>
<span data-ttu-id="c9b7b-110">Az **Update-AzSynapseSparkPool** parancsmag frissíti az Azure Synapse Analytics Spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c9b7b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-111">EXAMPLES</span></span>

### <span data-ttu-id="c9b7b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="c9b7b-113">Ez a parancs frissíti az Azure Synapse Analytics spark-készletet.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c9b7b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="c9b7b-115">Ez a parancs egy Azure Synapse Analytics spark-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="c9b7b-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="c9b7b-117">Ez a parancs egy Azure Synapse Analytics spark-készletet frissíti folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="c9b7b-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="c9b7b-119">Ez a parancs frissíti az Azure Synapse Analytics spark-készletet erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="c9b7b-120">5. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="c9b7b-121">Ez a parancs lehetővé teszi az Azure Synapse Analytics Spark-készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c9b7b-122">6. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="c9b7b-123">Ez a parancs letiltja az Azure Synapse Analytics Spark-készlet automatikus méretezését.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c9b7b-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="c9b7b-125">Ez a parancs lehetővé teszi az Azure Synapse Analytics Spark-készlet automatikus szüneteltetését.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="c9b7b-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="c9b7b-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="c9b7b-127">Ez a parancs letiltja az Azure Synapse Analytics Spark-készlet automatikus szüneteltetését.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="c9b7b-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-128">PARAMETERS</span></span>

### <span data-ttu-id="c9b7b-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9b7b-129">-AsJob</span></span>
<span data-ttu-id="c9b7b-130">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c9b7b-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9b7b-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="c9b7b-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="c9b7b-132">Az üresjárati percek száma.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-132">Number of minutes idle.</span></span> <span data-ttu-id="c9b7b-133">Ezt a paramétert az automatikus szüneteltetés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-133">This parameter must be specified when Auto-pause is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="c9b7b-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="c9b7b-135">A megadott értékkészletben lefoglalandó csomópontok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c9b7b-136">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-136">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="c9b7b-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="c9b7b-138">A megadott értékkészletben kiosztandó csomópontok minimális száma.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c9b7b-139">Ezt a paramétert az automatikus méretezés engedélyezésekor kell megadni.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-139">This parameter must be specified when Auto-scale is enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b7b-140">-DefaultProfile</span></span>
<span data-ttu-id="c9b7b-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9b7b-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="c9b7b-142">-EnableAutoPause</span></span>
<span data-ttu-id="c9b7b-143">Azt jelzi, hogy engedélyezve kell-e lennie az automatikus szüneteltetésnek.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-143">Indicates whether Auto-pause should be enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="c9b7b-144">-EnableAutoScale</span></span>
<span data-ttu-id="c9b7b-145">Azt jelzi, hogy engedélyezve kell-e lennie az automatikus méretezésnek</span><span class="sxs-lookup"><span data-stu-id="c9b7b-145">Indicates whether Auto-scale should be enabled</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9b7b-146">-InputObject</span></span>
<span data-ttu-id="c9b7b-147">Spark pool input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-147">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="c9b7b-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="c9b7b-149">Környezetkonfigurációs fájl ("PIP freeze" kimenet).</span><span class="sxs-lookup"><span data-stu-id="c9b7b-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="c9b7b-150">-Name</span><span class="sxs-lookup"><span data-stu-id="c9b7b-150">-Name</span></span>
<span data-ttu-id="c9b7b-151">A Synapse spark-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-151">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c9b7b-152">-NodeCount</span></span>
<span data-ttu-id="c9b7b-153">A megadott értékkészletben kiosztandó csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c9b7b-154">-NodeSize</span></span>
<span data-ttu-id="c9b7b-155">A megadott értékkészletben kiosztott csomópontokhoz használt alapértékek és memória száma.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="c9b7b-156">Ezt a paramétert az automatikus méretezés letiltása esetén kell megadni.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-156">This parameter must be specified when Auto-scale is disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b7b-157">-ResourceGroupName</span></span>
<span data-ttu-id="c9b7b-158">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9b7b-159">-ResourceId</span></span>
<span data-ttu-id="c9b7b-160">A Synapse Spark készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-160">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="c9b7b-161">-SparkVersion</span></span>
<span data-ttu-id="c9b7b-162">Spark-verzió.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-162">Apache Spark version.</span></span>
<span data-ttu-id="c9b7b-163">Engedélyezett értékek: 2,4</span><span class="sxs-lookup"><span data-stu-id="c9b7b-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="c9b7b-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9b7b-164">-Tag</span></span>
<span data-ttu-id="c9b7b-165">Az erőforráshoz társított címkék karakterlánc-karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-165">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c9b7b-166">-WorkspaceName</span></span>
<span data-ttu-id="c9b7b-167">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-167">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c9b7b-168">-WorkspaceObject</span></span>
<span data-ttu-id="c9b7b-169">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-169">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b7b-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9b7b-170">-Confirm</span></span>
<span data-ttu-id="c9b7b-171">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b7b-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b7b-172">-WhatIf</span></span>
<span data-ttu-id="c9b7b-173">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b7b-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b7b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b7b-175">CommonParameters</span></span>
<span data-ttu-id="c9b7b-176">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b7b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b7b-177">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9b7b-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b7b-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9b7b-178">INPUTS</span></span>

### <span data-ttu-id="c9b7b-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9b7b-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c9b7b-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c9b7b-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c9b7b-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-181">OUTPUTS</span></span>

### <span data-ttu-id="c9b7b-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c9b7b-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="c9b7b-183">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-183">NOTES</span></span>

## <span data-ttu-id="c9b7b-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9b7b-184">RELATED LINKS</span></span>
