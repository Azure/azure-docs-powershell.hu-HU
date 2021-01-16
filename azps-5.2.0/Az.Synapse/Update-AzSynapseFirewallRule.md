---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334337"
---
# <span data-ttu-id="09220-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="09220-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="09220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09220-102">SYNOPSIS</span></span>
<span data-ttu-id="09220-103">Frissíti a Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="09220-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="09220-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09220-104">SYNTAX</span></span>

### <span data-ttu-id="09220-105">UpdateByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09220-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09220-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09220-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09220-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09220-107">DESCRIPTION</span></span>
<span data-ttu-id="09220-108">Az **Update-AzSynapseFirewallRule parancsmag** módosítja az Azure Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="09220-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="09220-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09220-109">EXAMPLES</span></span>

### <span data-ttu-id="09220-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="09220-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="09220-111">Ez a parancs frissíti a ContosoFirewallRule nevű tűzfalszabályt a ContosoWorkspace munkaterületen ContosoFirewallRule néven.</span><span class="sxs-lookup"><span data-stu-id="09220-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="09220-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="09220-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="09220-113">Ez a parancs frissíti a ContosoFirewallRule nevű tűzfalszabályt egy munkaterületen keresztüli folyamaton keresztül.</span><span class="sxs-lookup"><span data-stu-id="09220-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="09220-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09220-114">PARAMETERS</span></span>

### <span data-ttu-id="09220-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09220-115">-AsJob</span></span>
<span data-ttu-id="09220-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="09220-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09220-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09220-117">-DefaultProfile</span></span>
<span data-ttu-id="09220-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="09220-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09220-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="09220-119">-EndIpAddress</span></span>
<span data-ttu-id="09220-120">A tűzfalszabály ip-címe.</span><span class="sxs-lookup"><span data-stu-id="09220-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="09220-121">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="09220-121">Must be IPv4 format.</span></span>
<span data-ttu-id="09220-122">A startIpAddress értéknél nem kisebbnek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="09220-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="09220-123">-Name</span><span class="sxs-lookup"><span data-stu-id="09220-123">-Name</span></span>
<span data-ttu-id="09220-124">A munkaterület firerwall-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="09220-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="09220-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09220-125">-ResourceGroupName</span></span>
<span data-ttu-id="09220-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09220-126">Resource group name.</span></span>

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

### <span data-ttu-id="09220-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="09220-127">-StartIpAddress</span></span>
<span data-ttu-id="09220-128">A tűzfalszabály kezdő IP-címe.</span><span class="sxs-lookup"><span data-stu-id="09220-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="09220-129">IPv4 formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="09220-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="09220-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09220-130">-WorkspaceName</span></span>
<span data-ttu-id="09220-131">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="09220-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="09220-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09220-132">-WorkspaceObject</span></span>
<span data-ttu-id="09220-133">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="09220-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="09220-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09220-134">-Confirm</span></span>
<span data-ttu-id="09220-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09220-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09220-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09220-136">-WhatIf</span></span>
<span data-ttu-id="09220-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09220-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09220-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09220-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09220-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09220-139">CommonParameters</span></span>
<span data-ttu-id="09220-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09220-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09220-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09220-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09220-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09220-142">INPUTS</span></span>

### <span data-ttu-id="09220-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="09220-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="09220-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09220-144">OUTPUTS</span></span>

### <span data-ttu-id="09220-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="09220-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="09220-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09220-146">NOTES</span></span>

## <span data-ttu-id="09220-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09220-147">RELATED LINKS</span></span>
