---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193971"
---
# <span data-ttu-id="db224-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db224-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="db224-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db224-102">SYNOPSIS</span></span>
<span data-ttu-id="db224-103">Ez annak az IP-címnek a helyőrzője, amelyet az Azure tűzfalon több pip-hez használhat.</span><span class="sxs-lookup"><span data-stu-id="db224-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="db224-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db224-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db224-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db224-105">DESCRIPTION</span></span>
<span data-ttu-id="db224-106">Ez annak az IP-címnek a helyőrzője, amelyet az Azure tűzfalon több pip-hez használhat.</span><span class="sxs-lookup"><span data-stu-id="db224-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="db224-107">Példák</span><span class="sxs-lookup"><span data-stu-id="db224-107">EXAMPLES</span></span>

### <span data-ttu-id="db224-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db224-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="db224-109">a $publicIp az IP-cím 20.2.3.4 helyőrzője lesz</span><span class="sxs-lookup"><span data-stu-id="db224-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="db224-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db224-110">PARAMETERS</span></span>

### <span data-ttu-id="db224-111">-Address (cím)</span><span class="sxs-lookup"><span data-stu-id="db224-111">-Address</span></span>
<span data-ttu-id="db224-112">A hub-hoz csatlakoztatott tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="db224-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="db224-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db224-113">-DefaultProfile</span></span>
<span data-ttu-id="db224-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db224-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db224-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db224-115">-Confirm</span></span>
<span data-ttu-id="db224-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db224-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db224-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db224-117">-WhatIf</span></span>
<span data-ttu-id="db224-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db224-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db224-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db224-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db224-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db224-120">CommonParameters</span></span>
<span data-ttu-id="db224-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db224-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db224-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db224-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db224-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db224-123">INPUTS</span></span>

### <span data-ttu-id="db224-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="db224-124">None</span></span>

## <span data-ttu-id="db224-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db224-125">OUTPUTS</span></span>

### <span data-ttu-id="db224-126">Microsoft. Azure. commands. Network. models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db224-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="db224-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db224-127">NOTES</span></span>

## <span data-ttu-id="db224-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db224-128">RELATED LINKS</span></span>
