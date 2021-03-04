---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 71622fbfa60a8961f10346aa9197b2c019f31bec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933529"
---
# <span data-ttu-id="6f954-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f954-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="6f954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f954-102">SYNOPSIS</span></span>
<span data-ttu-id="6f954-103">Synapse Analytics tűzfalszabályt kap.</span><span class="sxs-lookup"><span data-stu-id="6f954-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="6f954-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6f954-104">SYNTAX</span></span>

### <span data-ttu-id="6f954-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f954-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f954-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f954-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f954-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6f954-107">DESCRIPTION</span></span>
<span data-ttu-id="6f954-108">A **Get-AzSynapseFirewallRule parancsmag** megkapja az Azure Synapse Analytics tűzfalszabályt.</span><span class="sxs-lookup"><span data-stu-id="6f954-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="6f954-109">Ha nem ad meg szabálynevet, ez a parancsmag az összes szabályt megkapja.</span><span class="sxs-lookup"><span data-stu-id="6f954-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="6f954-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6f954-110">EXAMPLES</span></span>

### <span data-ttu-id="6f954-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6f954-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6f954-112">Ez a parancs az összes tűzfalszabályt egy munkaterületen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f954-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="6f954-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6f954-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="6f954-114">Ez a parancs a ContosoWorkspace munkaterületre írja be a tűzfalszabályt ContosoFirewallRule néven.</span><span class="sxs-lookup"><span data-stu-id="6f954-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="6f954-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="6f954-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="6f954-116">Ez a parancs az összes tűzfalszabályt egy munkaterületen keresztül kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6f954-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="6f954-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f954-117">PARAMETERS</span></span>

### <span data-ttu-id="6f954-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f954-118">-DefaultProfile</span></span>
<span data-ttu-id="6f954-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f954-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f954-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6f954-120">-Name</span></span>
<span data-ttu-id="6f954-121">A munkaterület firerwall-szabályának neve.</span><span class="sxs-lookup"><span data-stu-id="6f954-121">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="6f954-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f954-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f954-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f954-123">Resource group name.</span></span>

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

### <span data-ttu-id="6f954-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f954-124">-WorkspaceName</span></span>
<span data-ttu-id="6f954-125">A Synapse-munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6f954-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6f954-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="6f954-126">-WorkSpaceObject</span></span>
<span data-ttu-id="6f954-127">workspace input object, usually passed through the pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f954-127">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6f954-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f954-128">CommonParameters</span></span>
<span data-ttu-id="6f954-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f954-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f954-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f954-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f954-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f954-131">INPUTS</span></span>

### <span data-ttu-id="6f954-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6f954-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6f954-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f954-133">OUTPUTS</span></span>

### <span data-ttu-id="6f954-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6f954-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="6f954-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6f954-135">NOTES</span></span>

## <span data-ttu-id="6f954-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f954-136">RELATED LINKS</span></span>
