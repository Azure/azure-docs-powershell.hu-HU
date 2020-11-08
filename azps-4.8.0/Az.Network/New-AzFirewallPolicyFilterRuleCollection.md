---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184835"
---
# <span data-ttu-id="de4d9-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="de4d9-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="de4d9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="de4d9-103">Új Azure tűzfal házirend-szűrési szabálygyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="de4d9-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="de4d9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de4d9-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de4d9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="de4d9-106">A **New-AzFirewallPolicyFilterRuleCollection** parancsmag létrehoz egy szűrő szabály-gyűjteményt az Azure tűzfal házirendjéhez.</span><span class="sxs-lookup"><span data-stu-id="de4d9-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="de4d9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="de4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="de4d9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de4d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="de4d9-109">Ez a példa egy szűrő szabályt hoz létre 2 szabály feltételével</span><span class="sxs-lookup"><span data-stu-id="de4d9-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="de4d9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de4d9-110">PARAMETERS</span></span>

### <span data-ttu-id="de4d9-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="de4d9-111">-ActionType</span></span>
<span data-ttu-id="de4d9-112">A szabály-gyűjtemény lépései</span><span class="sxs-lookup"><span data-stu-id="de4d9-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="de4d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4d9-113">-DefaultProfile</span></span>
<span data-ttu-id="de4d9-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de4d9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de4d9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de4d9-115">-Name</span></span>
<span data-ttu-id="de4d9-116">Az alkalmazási szabály gyűjteményének neve</span><span class="sxs-lookup"><span data-stu-id="de4d9-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="de4d9-117">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="de4d9-117">-Priority</span></span>
<span data-ttu-id="de4d9-118">A szabály-gyűjtemény prioritása</span><span class="sxs-lookup"><span data-stu-id="de4d9-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="de4d9-119">-Szabály</span><span class="sxs-lookup"><span data-stu-id="de4d9-119">-Rule</span></span>
<span data-ttu-id="de4d9-120">Az alkalmazás szabályainak listája</span><span class="sxs-lookup"><span data-stu-id="de4d9-120">The list of application rules</span></span>

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

### <span data-ttu-id="de4d9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de4d9-121">-Confirm</span></span>
<span data-ttu-id="de4d9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de4d9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4d9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4d9-123">-WhatIf</span></span>
<span data-ttu-id="de4d9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de4d9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de4d9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de4d9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4d9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4d9-126">CommonParameters</span></span>
<span data-ttu-id="de4d9-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de4d9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4d9-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de4d9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4d9-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4d9-129">INPUTS</span></span>

### <span data-ttu-id="de4d9-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="de4d9-130">None</span></span>

## <span data-ttu-id="de4d9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de4d9-131">OUTPUTS</span></span>

### <span data-ttu-id="de4d9-132">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="de4d9-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="de4d9-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de4d9-133">NOTES</span></span>

## <span data-ttu-id="de4d9-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de4d9-134">RELATED LINKS</span></span>
