---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301688"
---
# <span data-ttu-id="66f45-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66f45-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="66f45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66f45-102">SYNOPSIS</span></span>
<span data-ttu-id="66f45-103">Folytatja a szinapszis-Analytics SQL-készletet.</span><span class="sxs-lookup"><span data-stu-id="66f45-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="66f45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66f45-104">SYNTAX</span></span>

### <span data-ttu-id="66f45-105">ResumeByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66f45-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66f45-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f45-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66f45-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f45-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66f45-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66f45-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66f45-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="66f45-109">DESCRIPTION</span></span>
<span data-ttu-id="66f45-110">A **resume-AzSynapseSqlPool** parancsmag egy Azure szinapszis-Analytics SQL-készletet folytat.</span><span class="sxs-lookup"><span data-stu-id="66f45-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="66f45-111">Példák</span><span class="sxs-lookup"><span data-stu-id="66f45-111">EXAMPLES</span></span>

### <span data-ttu-id="66f45-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66f45-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="66f45-113">A parancs a felfüggesztett Azure szinapszis-Analytics SQL-készletet folytatja.</span><span class="sxs-lookup"><span data-stu-id="66f45-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="66f45-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66f45-114">PARAMETERS</span></span>

### <span data-ttu-id="66f45-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66f45-115">-AsJob</span></span>
<span data-ttu-id="66f45-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="66f45-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66f45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f45-117">-DefaultProfile</span></span>
<span data-ttu-id="66f45-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66f45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66f45-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66f45-119">-InputObject</span></span>
<span data-ttu-id="66f45-120">Az SQL-készlet bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="66f45-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66f45-121">-Name</span></span>
<span data-ttu-id="66f45-122">A szinapszis SQL Pool neve.</span><span class="sxs-lookup"><span data-stu-id="66f45-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66f45-123">-PassThru</span></span>
<span data-ttu-id="66f45-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="66f45-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="66f45-125">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="66f45-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="66f45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f45-126">-ResourceGroupName</span></span>
<span data-ttu-id="66f45-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="66f45-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66f45-128">-ResourceId</span></span>
<span data-ttu-id="66f45-129">A szinapszis SQL Pool erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="66f45-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="66f45-130">-WorkspaceName</span></span>
<span data-ttu-id="66f45-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="66f45-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="66f45-132">-WorkspaceObject</span></span>
<span data-ttu-id="66f45-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="66f45-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f45-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="66f45-134">-Confirm</span></span>
<span data-ttu-id="66f45-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="66f45-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66f45-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f45-136">-WhatIf</span></span>
<span data-ttu-id="66f45-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="66f45-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f45-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66f45-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66f45-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f45-139">CommonParameters</span></span>
<span data-ttu-id="66f45-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66f45-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f45-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66f45-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f45-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f45-142">INPUTS</span></span>

### <span data-ttu-id="66f45-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="66f45-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="66f45-144">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66f45-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="66f45-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66f45-145">OUTPUTS</span></span>

### <span data-ttu-id="66f45-146">Microsoft. Azure. commands. szinapszis. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="66f45-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="66f45-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66f45-147">NOTES</span></span>

## <span data-ttu-id="66f45-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66f45-148">RELATED LINKS</span></span>
