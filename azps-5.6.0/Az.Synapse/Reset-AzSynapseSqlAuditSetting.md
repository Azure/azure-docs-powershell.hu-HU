---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 00d9682eb6562cfbfb9d06a4c8a6bac3b149cea1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929466"
---
# <span data-ttu-id="531c2-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="531c2-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="531c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531c2-102">SYNOPSIS</span></span>
<span data-ttu-id="531c2-103">Eltávolítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="531c2-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="531c2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="531c2-104">SYNTAX</span></span>

### <span data-ttu-id="531c2-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="531c2-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531c2-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="531c2-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="531c2-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="531c2-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531c2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="531c2-108">DESCRIPTION</span></span>
<span data-ttu-id="531c2-109">A **Reset-AzSynapseSqlAuditSetting** parancsmag eltávolítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="531c2-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="531c2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="531c2-110">EXAMPLES</span></span>

### <span data-ttu-id="531c2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="531c2-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="531c2-112">Ez a parancs eltávolítja a ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="531c2-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="531c2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="531c2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="531c2-114">Ez a parancs eltávolítja a ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási beállításait a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="531c2-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="531c2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="531c2-115">PARAMETERS</span></span>

### <span data-ttu-id="531c2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="531c2-116">-AsJob</span></span>
<span data-ttu-id="531c2-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="531c2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="531c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531c2-118">-DefaultProfile</span></span>
<span data-ttu-id="531c2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="531c2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="531c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="531c2-120">-InputObject</span></span>
<span data-ttu-id="531c2-121">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="531c2-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="531c2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="531c2-122">-PassThru</span></span>
<span data-ttu-id="531c2-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="531c2-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="531c2-124">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="531c2-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="531c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="531c2-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="531c2-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531c2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="531c2-127">-ResourceId</span></span>
<span data-ttu-id="531c2-128">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="531c2-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531c2-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="531c2-129">-WorkspaceName</span></span>
<span data-ttu-id="531c2-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="531c2-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531c2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="531c2-131">-Confirm</span></span>
<span data-ttu-id="531c2-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="531c2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531c2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531c2-133">-WhatIf</span></span>
<span data-ttu-id="531c2-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="531c2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531c2-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="531c2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531c2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531c2-136">CommonParameters</span></span>
<span data-ttu-id="531c2-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531c2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531c2-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="531c2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531c2-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="531c2-139">INPUTS</span></span>

### <span data-ttu-id="531c2-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="531c2-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="531c2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="531c2-141">OUTPUTS</span></span>

### <span data-ttu-id="531c2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="531c2-142">System.Boolean</span></span>

## <span data-ttu-id="531c2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="531c2-143">NOTES</span></span>

## <span data-ttu-id="531c2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="531c2-144">RELATED LINKS</span></span>
