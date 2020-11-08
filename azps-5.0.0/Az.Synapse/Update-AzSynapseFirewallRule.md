---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185143"
---
# <span data-ttu-id="3f1fd-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f1fd-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="3f1fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1fd-103">A szinapszis Analytics-tűzfal szabályának frissítése</span><span class="sxs-lookup"><span data-stu-id="3f1fd-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3f1fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f1fd-104">SYNTAX</span></span>

### <span data-ttu-id="3f1fd-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f1fd-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f1fd-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f1fd-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f1fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f1fd-107">DESCRIPTION</span></span>
<span data-ttu-id="3f1fd-108">Az **Update-AzSynapseFirewallRule** parancsmag az Azure szinapszis Analytics-tűzfal szabályát módosítja.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="3f1fd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3f1fd-109">EXAMPLES</span></span>

### <span data-ttu-id="3f1fd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3f1fd-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3f1fd-111">Ez a parancs frissíti a ContosoFirewallRule nevű tűzfal-szabályt a ContosoFirewallRule nevű munkaterület-ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="3f1fd-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3f1fd-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="3f1fd-113">Ez a parancs frissíti a ContosoFirewallRule nevű tűzfal-szabályt a munkaterületen, a csővezetéken keresztül.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="3f1fd-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f1fd-114">PARAMETERS</span></span>

### <span data-ttu-id="3f1fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f1fd-115">-AsJob</span></span>
<span data-ttu-id="3f1fd-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3f1fd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f1fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1fd-117">-DefaultProfile</span></span>
<span data-ttu-id="3f1fd-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1fd-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f1fd-119">-EndIpAddress</span></span>
<span data-ttu-id="3f1fd-120">A tűzfalszabály záró IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="3f1fd-121">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-121">Must be IPv4 format.</span></span>
<span data-ttu-id="3f1fd-122">Nagyobbnak vagy egyenlőnek kell lennie a startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="3f1fd-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f1fd-123">-Name</span></span>
<span data-ttu-id="3f1fd-124">A firerwall szabály neve a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="3f1fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="3f1fd-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1fd-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3f1fd-127">-StartIpAddress</span></span>
<span data-ttu-id="3f1fd-128">A tűzfalszabály kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="3f1fd-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="3f1fd-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f1fd-130">-WorkspaceName</span></span>
<span data-ttu-id="3f1fd-131">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1fd-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f1fd-132">-WorkspaceObject</span></span>
<span data-ttu-id="3f1fd-133">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1fd-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f1fd-134">-Confirm</span></span>
<span data-ttu-id="3f1fd-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1fd-136">-WhatIf</span></span>
<span data-ttu-id="3f1fd-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1fd-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1fd-139">CommonParameters</span></span>
<span data-ttu-id="3f1fd-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f1fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1fd-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3f1fd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1fd-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1fd-142">INPUTS</span></span>

### <span data-ttu-id="3f1fd-143">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f1fd-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f1fd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1fd-144">OUTPUTS</span></span>

### <span data-ttu-id="3f1fd-145">Microsoft. Azure. commands. szinapszis. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3f1fd-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="3f1fd-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f1fd-146">NOTES</span></span>

## <span data-ttu-id="3f1fd-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f1fd-147">RELATED LINKS</span></span>
