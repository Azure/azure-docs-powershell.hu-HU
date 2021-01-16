---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334937"
---
# <span data-ttu-id="c4c97-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4c97-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="c4c97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4c97-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c97-103">A virtuális központ tűzfalához assoicated IP-címek</span><span class="sxs-lookup"><span data-stu-id="c4c97-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="c4c97-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4c97-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4c97-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4c97-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c97-106">A virtuális központ tűzfalához assoicated IP-címek.</span><span class="sxs-lookup"><span data-stu-id="c4c97-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="c4c97-107">Ezek nyilvános és privát címek is lehetek</span><span class="sxs-lookup"><span data-stu-id="c4c97-107">These can be public and private addresses</span></span>

## <span data-ttu-id="c4c97-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4c97-108">EXAMPLES</span></span>

### <span data-ttu-id="c4c97-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4c97-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="c4c97-110">Ebben a példában egy központi IP-címobjektumot hoz létre, amely 2 nyilvános IP-címet számol.</span><span class="sxs-lookup"><span data-stu-id="c4c97-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="c4c97-111">A HubIPAddress objektum társítva van a virtuális központ tűzfalához.</span><span class="sxs-lookup"><span data-stu-id="c4c97-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="c4c97-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4c97-112">PARAMETERS</span></span>

### <span data-ttu-id="c4c97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c97-113">-DefaultProfile</span></span>
<span data-ttu-id="c4c97-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4c97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c97-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4c97-115">-PrivateIPAddress</span></span>
<span data-ttu-id="c4c97-116">A központhoz csatlakoztatott tűzfal privát IP-címe</span><span class="sxs-lookup"><span data-stu-id="c4c97-116">The private Ip Address of the Firewall attached to a Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c97-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="c4c97-117">-PublicIPs</span></span>
<span data-ttu-id="c4c97-118">A központhoz csatolt tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="c4c97-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c97-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4c97-119">-Confirm</span></span>
<span data-ttu-id="c4c97-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c4c97-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c97-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c97-121">-WhatIf</span></span>
<span data-ttu-id="c4c97-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c4c97-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4c97-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4c97-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c97-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c97-124">CommonParameters</span></span>
<span data-ttu-id="c4c97-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c97-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c97-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4c97-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c97-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4c97-127">INPUTS</span></span>

### <span data-ttu-id="c4c97-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="c4c97-128">None</span></span>

## <span data-ttu-id="c4c97-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c97-129">OUTPUTS</span></span>

### <span data-ttu-id="c4c97-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="c4c97-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="c4c97-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4c97-131">NOTES</span></span>

## <span data-ttu-id="c4c97-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4c97-132">RELATED LINKS</span></span>
