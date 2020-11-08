---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: fef045417a9c6cb22cd3ec3651a5b27b127b3b9f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185163"
---
# <span data-ttu-id="53676-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="53676-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="53676-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53676-102">SYNOPSIS</span></span>
<span data-ttu-id="53676-103">Felfüggeszti a szinapszis-Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="53676-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="53676-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53676-104">SYNTAX</span></span>

### <span data-ttu-id="53676-105">SuspendByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53676-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53676-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53676-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53676-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53676-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53676-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53676-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53676-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="53676-109">DESCRIPTION</span></span>
<span data-ttu-id="53676-110">A **felfüggesztés – AzSynapseSqlPool** parancsmag felfüggeszti az Azure SZINAPSZIS Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="53676-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="53676-111">Példák</span><span class="sxs-lookup"><span data-stu-id="53676-111">EXAMPLES</span></span>

### <span data-ttu-id="53676-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="53676-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="53676-113">Ez a parancs felfüggeszti az aktív Azure szinapszis-Analytics SQL-készletét.</span><span class="sxs-lookup"><span data-stu-id="53676-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="53676-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53676-114">PARAMETERS</span></span>

### <span data-ttu-id="53676-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53676-115">-AsJob</span></span>
<span data-ttu-id="53676-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="53676-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53676-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53676-117">-DefaultProfile</span></span>
<span data-ttu-id="53676-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53676-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53676-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53676-119">-InputObject</span></span>
<span data-ttu-id="53676-120">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="53676-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53676-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53676-121">-Name</span></span>
<span data-ttu-id="53676-122">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="53676-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53676-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53676-123">-PassThru</span></span>
<span data-ttu-id="53676-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="53676-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="53676-125">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="53676-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="53676-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53676-126">-ResourceGroupName</span></span>
<span data-ttu-id="53676-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="53676-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53676-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53676-128">-ResourceId</span></span>
<span data-ttu-id="53676-129">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="53676-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53676-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="53676-130">-WorkspaceName</span></span>
<span data-ttu-id="53676-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="53676-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53676-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="53676-132">-WorkspaceObject</span></span>
<span data-ttu-id="53676-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="53676-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53676-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53676-134">-Confirm</span></span>
<span data-ttu-id="53676-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53676-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53676-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53676-136">-WhatIf</span></span>
<span data-ttu-id="53676-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53676-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53676-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53676-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53676-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53676-139">CommonParameters</span></span>
<span data-ttu-id="53676-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53676-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53676-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="53676-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53676-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53676-142">INPUTS</span></span>

### <span data-ttu-id="53676-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="53676-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="53676-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="53676-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="53676-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53676-145">OUTPUTS</span></span>

### <span data-ttu-id="53676-146">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="53676-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="53676-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53676-147">NOTES</span></span>

## <span data-ttu-id="53676-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53676-148">RELATED LINKS</span></span>
