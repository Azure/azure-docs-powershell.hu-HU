---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: c5f1c3f2d1a23a06286cdbf7fb54915d33b1e3d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208983"
---
# <span data-ttu-id="71716-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="71716-101">Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="71716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71716-102">SYNOPSIS</span></span>
<span data-ttu-id="71716-103">Eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait egy SQL-készletből.</span><span class="sxs-lookup"><span data-stu-id="71716-103">Removes the advanced threat protection settings from a SQL pool.</span></span>

## <span data-ttu-id="71716-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71716-104">SYNTAX</span></span>

### <span data-ttu-id="71716-105">ClearByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71716-105">ClearByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71716-106">ClearByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71716-106">ClearByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71716-107">ClearByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71716-107">ClearByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71716-108">ClearByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71716-108">ClearByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71716-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71716-109">DESCRIPTION</span></span>
<span data-ttu-id="71716-110">A **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** parancsmag eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait az Azure Synapse Analytics SQL-készletből.</span><span class="sxs-lookup"><span data-stu-id="71716-110">The **Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="71716-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71716-111">EXAMPLES</span></span>

### <span data-ttu-id="71716-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="71716-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="71716-113">Ez a parancs eltávolítja a komplex veszélyforrások elleni védelem speciális beállításait egy ContosoSqlPool nevű SQL-készletből a ContosoWorkspace nevű munkaterület alatt.</span><span class="sxs-lookup"><span data-stu-id="71716-113">This command removes the advanced threat protection settings from a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="71716-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71716-114">PARAMETERS</span></span>

### <span data-ttu-id="71716-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71716-115">-AsJob</span></span>
<span data-ttu-id="71716-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71716-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71716-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71716-117">-DefaultProfile</span></span>
<span data-ttu-id="71716-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71716-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71716-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71716-119">-InputObject</span></span>
<span data-ttu-id="71716-120">SQL-készlet bemeneti objektuma, amely általában a folyamaton keresztül áthalad.</span><span class="sxs-lookup"><span data-stu-id="71716-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71716-121">-Name</span><span class="sxs-lookup"><span data-stu-id="71716-121">-Name</span></span>
<span data-ttu-id="71716-122">A Synapse SQL-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="71716-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet, ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71716-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71716-123">-PassThru</span></span>
<span data-ttu-id="71716-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="71716-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="71716-125">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="71716-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="71716-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71716-126">-ResourceGroupName</span></span>
<span data-ttu-id="71716-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71716-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71716-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71716-128">-ResourceId</span></span>
<span data-ttu-id="71716-129">A Synapse SQL-készlet erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="71716-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71716-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71716-130">-WorkspaceName</span></span>
<span data-ttu-id="71716-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="71716-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71716-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="71716-132">-WorkspaceObject</span></span>
<span data-ttu-id="71716-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="71716-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71716-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71716-134">-Confirm</span></span>
<span data-ttu-id="71716-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="71716-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71716-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71716-136">-WhatIf</span></span>
<span data-ttu-id="71716-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="71716-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71716-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71716-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71716-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71716-139">CommonParameters</span></span>
<span data-ttu-id="71716-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71716-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71716-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71716-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71716-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71716-142">INPUTS</span></span>

### <span data-ttu-id="71716-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="71716-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="71716-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="71716-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="71716-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71716-145">OUTPUTS</span></span>

### <span data-ttu-id="71716-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71716-146">System.Boolean</span></span>

## <span data-ttu-id="71716-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71716-147">NOTES</span></span>

## <span data-ttu-id="71716-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71716-148">RELATED LINKS</span></span>
