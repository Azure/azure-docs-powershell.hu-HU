---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: b25ca2a026cf5d82aa25f69868ca8605fd75bced
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333821"
---
# <span data-ttu-id="ebc98-101">Reset-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="ebc98-101">Reset-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="ebc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc98-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc98-103">Eltávolítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="ebc98-103">Removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="ebc98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebc98-104">SYNTAX</span></span>

### <span data-ttu-id="ebc98-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebc98-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc98-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc98-106">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc98-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc98-107">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc98-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebc98-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc98-109">A **Reset-AzSynapseSqlAuditSetting** parancsmag eltávolítja az Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="ebc98-109">The **Reset-AzSynapseSqlAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="ebc98-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebc98-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc98-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ebc98-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ebc98-112">Ez a parancs eltávolítja a ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási beállításait.</span><span class="sxs-lookup"><span data-stu-id="ebc98-112">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ebc98-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ebc98-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Reset-AzSynapseSqlAuditSetting
```

<span data-ttu-id="ebc98-114">Ez a parancs eltávolítja a ContosoWorkspace nevű Azure Synapse Analytics Workspace naplózási beállításait a folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="ebc98-114">This command removes the auditing settings of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ebc98-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc98-115">PARAMETERS</span></span>

### <span data-ttu-id="ebc98-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebc98-116">-AsJob</span></span>
<span data-ttu-id="ebc98-117">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ebc98-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebc98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc98-118">-DefaultProfile</span></span>
<span data-ttu-id="ebc98-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebc98-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc98-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc98-120">-InputObject</span></span>
<span data-ttu-id="ebc98-121">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebc98-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ebc98-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebc98-122">-PassThru</span></span>
<span data-ttu-id="ebc98-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="ebc98-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ebc98-124">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="ebc98-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ebc98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc98-125">-ResourceGroupName</span></span>
<span data-ttu-id="ebc98-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ebc98-126">Resource group name.</span></span>

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

### <span data-ttu-id="ebc98-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc98-127">-ResourceId</span></span>
<span data-ttu-id="ebc98-128">A Synapse-munkaterület erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ebc98-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="ebc98-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ebc98-129">-WorkspaceName</span></span>
<span data-ttu-id="ebc98-130">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="ebc98-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ebc98-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc98-131">-Confirm</span></span>
<span data-ttu-id="ebc98-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ebc98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebc98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc98-133">-WhatIf</span></span>
<span data-ttu-id="ebc98-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ebc98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc98-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ebc98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebc98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc98-136">CommonParameters</span></span>
<span data-ttu-id="ebc98-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc98-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebc98-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc98-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc98-139">INPUTS</span></span>

### <span data-ttu-id="ebc98-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ebc98-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ebc98-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc98-141">OUTPUTS</span></span>

### <span data-ttu-id="ebc98-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebc98-142">System.Boolean</span></span>

## <span data-ttu-id="ebc98-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebc98-143">NOTES</span></span>

## <span data-ttu-id="ebc98-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc98-144">RELATED LINKS</span></span>
