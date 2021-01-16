---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369206"
---
# <span data-ttu-id="fd17a-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="fd17a-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="fd17a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd17a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd17a-103">Törli a Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fd17a-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="fd17a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd17a-104">SYNTAX</span></span>

### <span data-ttu-id="fd17a-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd17a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd17a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd17a-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd17a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd17a-107">DESCRIPTION</span></span>
<span data-ttu-id="fd17a-108">A **Remove-AzSynapseFirewallRule** parancsmag véglegesen törli az Azure Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="fd17a-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="fd17a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd17a-109">EXAMPLES</span></span>

### <span data-ttu-id="fd17a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd17a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="fd17a-111">Ez a parancs törli a ContosoFirewallRule nevű tűzfalszabályt a ContosoWorkspace munkaterületen ContosoFirewallRule néven.</span><span class="sxs-lookup"><span data-stu-id="fd17a-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="fd17a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="fd17a-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="fd17a-113">Ez a parancs törli a ContosoFirewallRule nevű tűzfalszabályt egy munkaterületen keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="fd17a-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="fd17a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd17a-114">PARAMETERS</span></span>

### <span data-ttu-id="fd17a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd17a-115">-AsJob</span></span>
<span data-ttu-id="fd17a-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fd17a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd17a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd17a-117">-DefaultProfile</span></span>
<span data-ttu-id="fd17a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd17a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd17a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fd17a-119">-Force</span></span>
<span data-ttu-id="fd17a-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd17a-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fd17a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fd17a-121">-Name</span></span>
<span data-ttu-id="fd17a-122">A munkaterület firerwall-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="fd17a-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd17a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd17a-123">-PassThru</span></span>
<span data-ttu-id="fd17a-124">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="fd17a-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fd17a-125">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="fd17a-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fd17a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd17a-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd17a-127">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fd17a-127">Resource group name.</span></span>

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

### <span data-ttu-id="fd17a-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd17a-128">-WorkspaceName</span></span>
<span data-ttu-id="fd17a-129">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="fd17a-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fd17a-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd17a-130">-WorkspaceObject</span></span>
<span data-ttu-id="fd17a-131">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="fd17a-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fd17a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd17a-132">-Confirm</span></span>
<span data-ttu-id="fd17a-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fd17a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd17a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd17a-134">-WhatIf</span></span>
<span data-ttu-id="fd17a-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fd17a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd17a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd17a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd17a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd17a-137">CommonParameters</span></span>
<span data-ttu-id="fd17a-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd17a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd17a-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd17a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd17a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd17a-140">INPUTS</span></span>

### <span data-ttu-id="fd17a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd17a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fd17a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd17a-142">OUTPUTS</span></span>

### <span data-ttu-id="fd17a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd17a-143">System.Boolean</span></span>

## <span data-ttu-id="fd17a-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd17a-144">NOTES</span></span>

## <span data-ttu-id="fd17a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd17a-145">RELATED LINKS</span></span>
