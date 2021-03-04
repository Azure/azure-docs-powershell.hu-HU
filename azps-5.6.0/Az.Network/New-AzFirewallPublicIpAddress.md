---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: 2e7c1b0468ed3faf37c8f11bc0cb1eca707195bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921889"
---
# <span data-ttu-id="50c1b-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="50c1b-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="50c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="50c1b-103">Ez az Ip-cím helyőrzője, amely használható az Azure tűzfalon a több pipával való használathoz.</span><span class="sxs-lookup"><span data-stu-id="50c1b-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="50c1b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="50c1b-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c1b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="50c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="50c1b-106">Ez az Ip-cím helyőrzője, amely használható az Azure tűzfalon a több pipával való használathoz.</span><span class="sxs-lookup"><span data-stu-id="50c1b-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="50c1b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="50c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="50c1b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="50c1b-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="50c1b-109">$publicIp 20.2.3.4-es IP-cím helyőrzője lesz</span><span class="sxs-lookup"><span data-stu-id="50c1b-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="50c1b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c1b-110">PARAMETERS</span></span>

### <span data-ttu-id="50c1b-111">-Address</span><span class="sxs-lookup"><span data-stu-id="50c1b-111">-Address</span></span>
<span data-ttu-id="50c1b-112">A központhoz csatolt tűzfal IP-címei</span><span class="sxs-lookup"><span data-stu-id="50c1b-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="50c1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c1b-113">-DefaultProfile</span></span>
<span data-ttu-id="50c1b-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50c1b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50c1b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50c1b-115">-Confirm</span></span>
<span data-ttu-id="50c1b-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="50c1b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c1b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c1b-117">-WhatIf</span></span>
<span data-ttu-id="50c1b-118">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="50c1b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50c1b-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50c1b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c1b-120">CommonParameters</span></span>
<span data-ttu-id="50c1b-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c1b-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50c1b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c1b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50c1b-123">INPUTS</span></span>

### <span data-ttu-id="50c1b-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="50c1b-124">None</span></span>

## <span data-ttu-id="50c1b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50c1b-125">OUTPUTS</span></span>

### <span data-ttu-id="50c1b-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="50c1b-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="50c1b-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="50c1b-127">NOTES</span></span>

## <span data-ttu-id="50c1b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50c1b-128">RELATED LINKS</span></span>
