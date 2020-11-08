---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194034"
---
# <span data-ttu-id="50e0e-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="50e0e-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="50e0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50e0e-102">SYNOPSIS</span></span>
<span data-ttu-id="50e0e-103">Az IP-címek telefonszámok a virtuális központi tűzfalon</span><span class="sxs-lookup"><span data-stu-id="50e0e-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="50e0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50e0e-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50e0e-105">DESCRIPTION</span></span>
<span data-ttu-id="50e0e-106">Az IP-címek telefonszámok a virtuális központi tűzfalon.</span><span class="sxs-lookup"><span data-stu-id="50e0e-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="50e0e-107">Ezek lehetnek nyilvános és privát címek is</span><span class="sxs-lookup"><span data-stu-id="50e0e-107">These can be public and private addresses</span></span>

## <span data-ttu-id="50e0e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="50e0e-108">EXAMPLES</span></span>

### <span data-ttu-id="50e0e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="50e0e-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="50e0e-110">Ez a példa egy központi IP-cím objektumot hoz létre, amelyben 2 nyilvános IP-cím szerepel.</span><span class="sxs-lookup"><span data-stu-id="50e0e-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="50e0e-111">A HubIPAddress objektum a virtuális ssociated lévő tűzfalon van.</span><span class="sxs-lookup"><span data-stu-id="50e0e-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="50e0e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50e0e-112">PARAMETERS</span></span>

### <span data-ttu-id="50e0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e0e-113">-DefaultProfile</span></span>
<span data-ttu-id="50e0e-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50e0e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50e0e-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="50e0e-115">-PrivateIPAddress</span></span>
<span data-ttu-id="50e0e-116">A hub-hoz rendelt tűzfal privát IP-címe</span><span class="sxs-lookup"><span data-stu-id="50e0e-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="50e0e-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="50e0e-117">-PublicIPs</span></span>
<span data-ttu-id="50e0e-118">A hub-hoz csatlakoztatott tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="50e0e-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="50e0e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50e0e-119">-Confirm</span></span>
<span data-ttu-id="50e0e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50e0e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e0e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e0e-121">-WhatIf</span></span>
<span data-ttu-id="50e0e-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50e0e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50e0e-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50e0e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50e0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e0e-124">CommonParameters</span></span>
<span data-ttu-id="50e0e-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50e0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e0e-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="50e0e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e0e-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e0e-127">INPUTS</span></span>

### <span data-ttu-id="50e0e-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="50e0e-128">None</span></span>

## <span data-ttu-id="50e0e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50e0e-129">OUTPUTS</span></span>

### <span data-ttu-id="50e0e-130">Microsoft. Azure. commands. Network. models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="50e0e-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="50e0e-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50e0e-131">NOTES</span></span>

## <span data-ttu-id="50e0e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50e0e-132">RELATED LINKS</span></span>