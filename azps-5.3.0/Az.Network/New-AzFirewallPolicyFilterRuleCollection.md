---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469006"
---
# <span data-ttu-id="6e48d-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="6e48d-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="6e48d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e48d-102">SYNOPSIS</span></span>
<span data-ttu-id="6e48d-103">Új Azure tűzfal házirendszűrési szabálygyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="6e48d-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="6e48d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e48d-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e48d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e48d-105">DESCRIPTION</span></span>
<span data-ttu-id="6e48d-106">A **New-AzFirewallPolicyFilterRuleCollection** parancsmag létrehoz egy szűrőszabálygyűjteményt egy Azure tűzfalházi házirendhez.</span><span class="sxs-lookup"><span data-stu-id="6e48d-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="6e48d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e48d-107">EXAMPLES</span></span>

### <span data-ttu-id="6e48d-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6e48d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="6e48d-109">Ebben a példában egy szűrőszabályt hoz létre 2 szabályfeltételekkel</span><span class="sxs-lookup"><span data-stu-id="6e48d-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="6e48d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e48d-110">PARAMETERS</span></span>

### <span data-ttu-id="6e48d-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="6e48d-111">-ActionType</span></span>
<span data-ttu-id="6e48d-112">A szabálygyűjtemény művelete</span><span class="sxs-lookup"><span data-stu-id="6e48d-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e48d-113">-DefaultProfile</span></span>
<span data-ttu-id="6e48d-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e48d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e48d-115">-Name</span></span>
<span data-ttu-id="6e48d-116">Az alkalmazásszabály-gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="6e48d-116">The name of the Application Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="6e48d-117">-Priority</span></span>
<span data-ttu-id="6e48d-118">A szabálygyűjtemény prioritása</span><span class="sxs-lookup"><span data-stu-id="6e48d-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-119">-Rule</span><span class="sxs-lookup"><span data-stu-id="6e48d-119">-Rule</span></span>
<span data-ttu-id="6e48d-120">Az alkalmazásszabályok listája</span><span class="sxs-lookup"><span data-stu-id="6e48d-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e48d-121">-Confirm</span></span>
<span data-ttu-id="6e48d-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e48d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e48d-123">-WhatIf</span></span>
<span data-ttu-id="6e48d-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e48d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e48d-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e48d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e48d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e48d-126">CommonParameters</span></span>
<span data-ttu-id="6e48d-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e48d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e48d-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e48d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e48d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e48d-129">INPUTS</span></span>

### <span data-ttu-id="6e48d-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="6e48d-130">None</span></span>

## <span data-ttu-id="6e48d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e48d-131">OUTPUTS</span></span>

### <span data-ttu-id="6e48d-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="6e48d-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="6e48d-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e48d-133">NOTES</span></span>

## <span data-ttu-id="6e48d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e48d-134">RELATED LINKS</span></span>
