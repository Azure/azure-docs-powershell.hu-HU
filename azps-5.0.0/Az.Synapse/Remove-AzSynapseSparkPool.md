---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187139"
---
# <span data-ttu-id="24154-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="24154-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="24154-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24154-102">SYNOPSIS</span></span>
<span data-ttu-id="24154-103">Törli a szinapszis-elemző Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="24154-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="24154-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24154-104">SYNTAX</span></span>

### <span data-ttu-id="24154-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24154-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24154-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24154-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24154-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24154-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24154-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24154-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24154-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="24154-109">DESCRIPTION</span></span>
<span data-ttu-id="24154-110">A **Remove-AzSynapseSparkPool** parancsmag véglegesen törli az Azure szinapszis Analytics Spark-medencét.</span><span class="sxs-lookup"><span data-stu-id="24154-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="24154-111">Példák</span><span class="sxs-lookup"><span data-stu-id="24154-111">EXAMPLES</span></span>

### <span data-ttu-id="24154-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24154-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="24154-113">Ez a parancs törli az Azure szinapszis Analytics Spark poolt.</span><span class="sxs-lookup"><span data-stu-id="24154-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="24154-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="24154-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="24154-115">Ez a parancs törli az Azure szinapszis Analytics Spark-medencét csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="24154-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="24154-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="24154-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="24154-117">Ez a parancs törli az Azure szinapszis Analytics Spark-medencét csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="24154-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="24154-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="24154-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="24154-119">Ez a parancs törli az Azure szinapszis Analytics Spark-medencét egy erőforrás-AZONOSÍTÓval.</span><span class="sxs-lookup"><span data-stu-id="24154-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="24154-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24154-120">PARAMETERS</span></span>

### <span data-ttu-id="24154-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24154-121">-AsJob</span></span>
<span data-ttu-id="24154-122">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="24154-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24154-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24154-123">-DefaultProfile</span></span>
<span data-ttu-id="24154-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24154-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24154-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24154-125">-InputObject</span></span>
<span data-ttu-id="24154-126">A szikra medence bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="24154-126">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24154-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24154-127">-Name</span></span>
<span data-ttu-id="24154-128">A szinapszis Spark Pool neve.</span><span class="sxs-lookup"><span data-stu-id="24154-128">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24154-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24154-129">-PassThru</span></span>
<span data-ttu-id="24154-130">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="24154-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="24154-131">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="24154-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="24154-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24154-132">-ResourceGroupName</span></span>
<span data-ttu-id="24154-133">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="24154-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24154-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24154-134">-ResourceId</span></span>
<span data-ttu-id="24154-135">A szinapszis szikra készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="24154-135">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24154-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="24154-136">-WorkspaceName</span></span>
<span data-ttu-id="24154-137">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="24154-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24154-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="24154-138">-WorkspaceObject</span></span>
<span data-ttu-id="24154-139">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="24154-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24154-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24154-140">-Confirm</span></span>
<span data-ttu-id="24154-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24154-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24154-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24154-142">-WhatIf</span></span>
<span data-ttu-id="24154-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24154-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24154-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24154-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24154-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24154-145">CommonParameters</span></span>
<span data-ttu-id="24154-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24154-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24154-147">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="24154-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24154-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24154-148">INPUTS</span></span>

### <span data-ttu-id="24154-149">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="24154-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="24154-150">Microsoft. Azure. commands. szinapszis. models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="24154-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="24154-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24154-151">OUTPUTS</span></span>

### <span data-ttu-id="24154-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24154-152">System.Boolean</span></span>

## <span data-ttu-id="24154-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24154-153">NOTES</span></span>

## <span data-ttu-id="24154-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24154-154">RELATED LINKS</span></span>
