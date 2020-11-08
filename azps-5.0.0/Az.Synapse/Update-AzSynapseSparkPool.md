---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSparkPool.md
ms.openlocfilehash: 1ed539f6064d6f99aff632a43cee5f200d735b6d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194163"
---
# <span data-ttu-id="368c0-101">Update-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="368c0-101">Update-AzSynapseSparkPool</span></span>

## <span data-ttu-id="368c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="368c0-102">SYNOPSIS</span></span>
<span data-ttu-id="368c0-103">Frissíti a szinapszis-elemző Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="368c0-103">Updates a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="368c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="368c0-104">SYNTAX</span></span>

### <span data-ttu-id="368c0-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="368c0-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>]
 [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>]
 [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="368c0-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="368c0-106">SetByParentObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-EnableAutoScale <Boolean>] [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>]
 [-EnableAutoPause <Boolean>] [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>]
 [-SparkVersion <String>] [-LibraryRequirementsFilePath <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="368c0-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="368c0-107">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="368c0-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="368c0-108">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseSparkPool -ResourceId <String> [-Tag <Hashtable>] [-EnableAutoScale <Boolean>]
 [-AutoScaleMinNodeCount <Int32>] [-AutoScaleMaxNodeCount <Int32>] [-EnableAutoPause <Boolean>]
 [-AutoPauseDelayInMinute <Int32>] [-NodeCount <Int32>] [-NodeSize <String>] [-SparkVersion <String>]
 [-LibraryRequirementsFilePath <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="368c0-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="368c0-109">DESCRIPTION</span></span>
<span data-ttu-id="368c0-110">Az **Update-AzSynapseSparkPool** parancsmag az Azure szinapszis Analytics Spark-gyűjtőt frissíti.</span><span class="sxs-lookup"><span data-stu-id="368c0-110">The **Update-AzSynapseSparkPool** cmdlet updates an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="368c0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="368c0-111">EXAMPLES</span></span>

### <span data-ttu-id="368c0-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="368c0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool -Tag @{"key" = "value"} -NodeCount 5 -NodeSize Medium
```

<span data-ttu-id="368c0-113">Ez a parancs frissíti az Azure szinapszis-elemző Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="368c0-113">This command updates an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="368c0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
$pool | Update-AzSynapseSparkPool -Tag @{"key" = "value1"}
```

<span data-ttu-id="368c0-115">Ez a parancs frissíti az Azure szinapszis-elemző Spark-medencét csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="368c0-115">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="368c0-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSparkPool -Name ContosoSparkPool -Tag @{"key" = "value2"}
```

<span data-ttu-id="368c0-117">Ez a parancs frissíti az Azure szinapszis-elemző Spark-medencét csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="368c0-117">This command updates an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="368c0-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool -Tag @{"key" = "value3"}
```

<span data-ttu-id="368c0-119">Ez a parancs egy erőforrás-AZONOSÍTÓval frissíti az Azure szinapszis Analytics Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="368c0-119">This command updates an Azure Synapse Analytics Spark pool with resource ID.</span></span>

### <span data-ttu-id="368c0-120">Példa 5</span><span class="sxs-lookup"><span data-stu-id="368c0-120">Example 5</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $true -AutoScaleMinNodeCount 3 -AutoScaleMaxNodeCount 7
```

<span data-ttu-id="368c0-121">Ez a parancs lehetővé teszi, hogy az Azure szinapszis Analytics Spark-készlet automatikus átméretezése.</span><span class="sxs-lookup"><span data-stu-id="368c0-121">This command enables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="368c0-122">6. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-122">Example 6</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoScale $false
```

<span data-ttu-id="368c0-123">Ez a parancs tiltja az automatikus méretezést az Azure szinapszis Analytics Spark poolban.</span><span class="sxs-lookup"><span data-stu-id="368c0-123">This command disables auto-scale for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="368c0-124">7. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-124">Example 7</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $true -AutoPauseDelayInMinute 15
```

<span data-ttu-id="368c0-125">Ez a parancs engedélyezi az Azure szinapszis Analytics Spark-készlet automatikus szüneteltetését.</span><span class="sxs-lookup"><span data-stu-id="368c0-125">This command enables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="368c0-126">8. példa</span><span class="sxs-lookup"><span data-stu-id="368c0-126">Example 8</span></span>
```powershell
PS C:\> Update-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -EnableAutoPause $false
```

<span data-ttu-id="368c0-127">Ez a parancs letiltja az Azure szinapszis Analytics Spark-készlet automatikus szüneteltetését.</span><span class="sxs-lookup"><span data-stu-id="368c0-127">This command disables auto-pause for an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="368c0-128">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="368c0-128">PARAMETERS</span></span>

### <span data-ttu-id="368c0-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="368c0-129">-AsJob</span></span>
<span data-ttu-id="368c0-130">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="368c0-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="368c0-131">-AutoPauseDelayInMinute</span><span class="sxs-lookup"><span data-stu-id="368c0-131">-AutoPauseDelayInMinute</span></span>
<span data-ttu-id="368c0-132">Üresjárati percek száma.</span><span class="sxs-lookup"><span data-stu-id="368c0-132">Number of minutes idle.</span></span> <span data-ttu-id="368c0-133">Ezt a paramétert akkor adja meg, ha az automatikus szünet engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="368c0-133">This parameter must be specified when Auto-pause is enabled.</span></span>

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

### <span data-ttu-id="368c0-134">-AutoScaleMaxNodeCount</span><span class="sxs-lookup"><span data-stu-id="368c0-134">-AutoScaleMaxNodeCount</span></span>
<span data-ttu-id="368c0-135">A megadott Spark-készletben kiosztani kívánt csomópontok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="368c0-135">Maximum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="368c0-136">Ezt a paramétert akkor adja meg, ha az automatikus méretezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="368c0-136">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="368c0-137">-AutoScaleMinNodeCount</span><span class="sxs-lookup"><span data-stu-id="368c0-137">-AutoScaleMinNodeCount</span></span>
<span data-ttu-id="368c0-138">A megadott Spark-készletben kiosztani kívánt csomópontok minimális száma</span><span class="sxs-lookup"><span data-stu-id="368c0-138">Minimum number of nodes to be allocated in the specified Spark pool.</span></span>
<span data-ttu-id="368c0-139">Ezt a paramétert akkor adja meg, ha az automatikus méretezés engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="368c0-139">This parameter must be specified when Auto-scale is enabled.</span></span>

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

### <span data-ttu-id="368c0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368c0-140">-DefaultProfile</span></span>
<span data-ttu-id="368c0-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="368c0-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="368c0-142">-EnableAutoPause</span><span class="sxs-lookup"><span data-stu-id="368c0-142">-EnableAutoPause</span></span>
<span data-ttu-id="368c0-143">Azt jelzi, hogy engedélyezve kell-e az automatikus szüneteltetést.</span><span class="sxs-lookup"><span data-stu-id="368c0-143">Indicates whether Auto-pause should be enabled.</span></span>

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

### <span data-ttu-id="368c0-144">-EnableAutoScale</span><span class="sxs-lookup"><span data-stu-id="368c0-144">-EnableAutoScale</span></span>
<span data-ttu-id="368c0-145">Azt jelzi, hogy engedélyezve van-e az automatikus méretezés</span><span class="sxs-lookup"><span data-stu-id="368c0-145">Indicates whether Auto-scale should be enabled</span></span>

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

### <span data-ttu-id="368c0-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="368c0-146">-InputObject</span></span>
<span data-ttu-id="368c0-147">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="368c0-147">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="368c0-148">-LibraryRequirementsFilePath</span><span class="sxs-lookup"><span data-stu-id="368c0-148">-LibraryRequirementsFilePath</span></span>
<span data-ttu-id="368c0-149">Környezet konfigurációs fájlja ("PIP rögzítése" kimenet)</span><span class="sxs-lookup"><span data-stu-id="368c0-149">Environment configuration file ("PIP freeze" output).</span></span>

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

### <span data-ttu-id="368c0-150">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="368c0-150">-Name</span></span>
<span data-ttu-id="368c0-151">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="368c0-151">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="368c0-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="368c0-152">-NodeCount</span></span>
<span data-ttu-id="368c0-153">A megadott Spark-készletben kiosztani kívánt csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="368c0-153">Number of nodes to be allocated in the specified Spark pool.</span></span>

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

### <span data-ttu-id="368c0-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="368c0-154">-NodeSize</span></span>
<span data-ttu-id="368c0-155">A megadott Spark-készletben kiosztott csomópontok számára használandó alapvető és memória száma.</span><span class="sxs-lookup"><span data-stu-id="368c0-155">Number of core and memory to be used for nodes allocated in the specified Spark pool.</span></span>
<span data-ttu-id="368c0-156">Ezt a paramétert meg kell adni, ha az automatikus méretezés le van tiltva</span><span class="sxs-lookup"><span data-stu-id="368c0-156">This parameter must be specified when Auto-scale is disabled</span></span>

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

### <span data-ttu-id="368c0-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="368c0-157">-ResourceGroupName</span></span>
<span data-ttu-id="368c0-158">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="368c0-158">Resource group name.</span></span>

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

### <span data-ttu-id="368c0-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="368c0-159">-ResourceId</span></span>
<span data-ttu-id="368c0-160">A szinapszis szikra készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="368c0-160">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="368c0-161">-SparkVersion</span><span class="sxs-lookup"><span data-stu-id="368c0-161">-SparkVersion</span></span>
<span data-ttu-id="368c0-162">Apache Spark verzió.</span><span class="sxs-lookup"><span data-stu-id="368c0-162">Apache Spark version.</span></span>
<span data-ttu-id="368c0-163">Engedélyezett értékek: 2,4</span><span class="sxs-lookup"><span data-stu-id="368c0-163">Allowed values: 2.4</span></span>

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

### <span data-ttu-id="368c0-164">-Címke</span><span class="sxs-lookup"><span data-stu-id="368c0-164">-Tag</span></span>
<span data-ttu-id="368c0-165">Az erőforráshoz társított címkék karakterlánca, karakterláncok szótára</span><span class="sxs-lookup"><span data-stu-id="368c0-165">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="368c0-166">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="368c0-166">-WorkspaceName</span></span>
<span data-ttu-id="368c0-167">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="368c0-167">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="368c0-168">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="368c0-168">-WorkspaceObject</span></span>
<span data-ttu-id="368c0-169">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="368c0-169">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="368c0-170">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="368c0-170">-Confirm</span></span>
<span data-ttu-id="368c0-171">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="368c0-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="368c0-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="368c0-172">-WhatIf</span></span>
<span data-ttu-id="368c0-173">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="368c0-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="368c0-174">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="368c0-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="368c0-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368c0-175">CommonParameters</span></span>
<span data-ttu-id="368c0-176">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="368c0-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368c0-177">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="368c0-177">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368c0-178">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="368c0-178">INPUTS</span></span>

### <span data-ttu-id="368c0-179">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="368c0-179">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="368c0-180">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="368c0-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="368c0-181">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="368c0-181">OUTPUTS</span></span>

### <span data-ttu-id="368c0-182">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="368c0-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="368c0-183">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="368c0-183">NOTES</span></span>

## <span data-ttu-id="368c0-184">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="368c0-184">RELATED LINKS</span></span>
