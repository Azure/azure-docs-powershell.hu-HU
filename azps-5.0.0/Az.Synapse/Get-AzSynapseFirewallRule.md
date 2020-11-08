---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186498"
---
# <span data-ttu-id="bf07d-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bf07d-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="bf07d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf07d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf07d-103">Megkapja a szinapszis-elemzési tűzfalszabályok szabályát.</span><span class="sxs-lookup"><span data-stu-id="bf07d-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="bf07d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf07d-104">SYNTAX</span></span>

### <span data-ttu-id="bf07d-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf07d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf07d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf07d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf07d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf07d-107">DESCRIPTION</span></span>
<span data-ttu-id="bf07d-108">A **Get-AzSynapseFirewallRule** parancsmag az Azure szinapszis Analytics-tűzfal szabályát kapja.</span><span class="sxs-lookup"><span data-stu-id="bf07d-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="bf07d-109">Ha nem adja meg a szabály nevét, a parancsmag minden szabályt beilleszt.</span><span class="sxs-lookup"><span data-stu-id="bf07d-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="bf07d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf07d-110">EXAMPLES</span></span>

### <span data-ttu-id="bf07d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bf07d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="bf07d-112">Ez a parancs beilleszti az összes tűzfal-szabályt egy munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="bf07d-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="bf07d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="bf07d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="bf07d-114">Ez a parancs a tűzfal szabályait a munkaterület ContosoWorkspace a name ContosoFirewallRule-ban kapja.</span><span class="sxs-lookup"><span data-stu-id="bf07d-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="bf07d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="bf07d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="bf07d-116">Ez a parancs minden tűzfal szabályait átveszi egy munkaterületre a csővezetékek között.</span><span class="sxs-lookup"><span data-stu-id="bf07d-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="bf07d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf07d-117">PARAMETERS</span></span>

### <span data-ttu-id="bf07d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf07d-118">-DefaultProfile</span></span>
<span data-ttu-id="bf07d-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf07d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf07d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf07d-120">-Name</span></span>
<span data-ttu-id="bf07d-121">A firerwall szabály neve a munkaterülethez.</span><span class="sxs-lookup"><span data-stu-id="bf07d-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf07d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf07d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf07d-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="bf07d-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf07d-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf07d-124">-WorkspaceName</span></span>
<span data-ttu-id="bf07d-125">A szinapszis munkaterületének neve.</span><span class="sxs-lookup"><span data-stu-id="bf07d-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf07d-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="bf07d-126">-WorkSpaceObject</span></span>
<span data-ttu-id="bf07d-127">munkaterület bemeneti objektuma, amely általában áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="bf07d-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf07d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf07d-128">CommonParameters</span></span>
<span data-ttu-id="bf07d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf07d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf07d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf07d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf07d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf07d-131">INPUTS</span></span>

### <span data-ttu-id="bf07d-132">Microsoft. Azure. commands. szinapszis. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf07d-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bf07d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf07d-133">OUTPUTS</span></span>

### <span data-ttu-id="bf07d-134">Microsoft. Azure. commands. szinapszis. models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bf07d-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="bf07d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf07d-135">NOTES</span></span>

## <span data-ttu-id="bf07d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf07d-136">RELATED LINKS</span></span>
