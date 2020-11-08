---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186603"
---
# <span data-ttu-id="4b7ab-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="4b7ab-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="4b7ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4b7ab-103">Törli a szinapszis-elemzési tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="4b7ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b7ab-104">SYNTAX</span></span>

### <span data-ttu-id="4b7ab-105">DeleteByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4b7ab-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b7ab-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b7ab-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b7ab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b7ab-107">DESCRIPTION</span></span>
<span data-ttu-id="4b7ab-108">A **Remove-AzSynapseFirewallRule** parancsmag véglegesen törli az Azure szinapszis Analytics-tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="4b7ab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4b7ab-109">EXAMPLES</span></span>

### <span data-ttu-id="4b7ab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4b7ab-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="4b7ab-111">Ez a parancs törli a ContosoFirewallRule nevű tűzfal-szabályt a ContosoFirewallRule nevű munkaterület-ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="4b7ab-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4b7ab-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="4b7ab-113">Ez a parancs törli a ContosoFirewallRule nevű tűzfal-szabályt a munkaterületen a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="4b7ab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b7ab-114">PARAMETERS</span></span>

### <span data-ttu-id="4b7ab-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b7ab-115">-AsJob</span></span>
<span data-ttu-id="4b7ab-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4b7ab-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b7ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b7ab-117">-DefaultProfile</span></span>
<span data-ttu-id="4b7ab-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b7ab-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4b7ab-119">-Name</span></span>
<span data-ttu-id="4b7ab-120">A firerwall szabály neve a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="4b7ab-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b7ab-121">-PassThru</span></span>
<span data-ttu-id="4b7ab-122">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4b7ab-123">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4b7ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b7ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b7ab-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-125">Resource group name.</span></span>

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

### <span data-ttu-id="4b7ab-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4b7ab-126">-WorkspaceName</span></span>
<span data-ttu-id="4b7ab-127">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4b7ab-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4b7ab-128">-WorkspaceObject</span></span>
<span data-ttu-id="4b7ab-129">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4b7ab-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b7ab-130">-Confirm</span></span>
<span data-ttu-id="4b7ab-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b7ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b7ab-132">-WhatIf</span></span>
<span data-ttu-id="4b7ab-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b7ab-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b7ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b7ab-135">CommonParameters</span></span>
<span data-ttu-id="4b7ab-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b7ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b7ab-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4b7ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b7ab-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b7ab-138">INPUTS</span></span>

### <span data-ttu-id="4b7ab-139">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4b7ab-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4b7ab-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b7ab-140">OUTPUTS</span></span>

### <span data-ttu-id="4b7ab-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b7ab-141">System.Boolean</span></span>

## <span data-ttu-id="4b7ab-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b7ab-142">NOTES</span></span>

## <span data-ttu-id="4b7ab-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b7ab-143">RELATED LINKS</span></span>
