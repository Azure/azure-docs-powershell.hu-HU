---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013353"
---
# <span data-ttu-id="0040a-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="0040a-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="0040a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0040a-102">SYNOPSIS</span></span>
<span data-ttu-id="0040a-103">Az elérhető Azure Firewall FQDN-címkéket kapja.</span><span class="sxs-lookup"><span data-stu-id="0040a-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="0040a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0040a-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0040a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0040a-105">DESCRIPTION</span></span>
<span data-ttu-id="0040a-106">A **Get-AzFirewallFqdnTag** parancsmag az Azure Firewall alkalmazás szabályaihoz használható FQDN-címkék listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0040a-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="0040a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0040a-107">EXAMPLES</span></span>

### <span data-ttu-id="0040a-108">1: az összes elérhető FQDN-címke beolvasása</span><span class="sxs-lookup"><span data-stu-id="0040a-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="0040a-109">Ez a példa beolvassa az összes elérhető FQDN-címkét.</span><span class="sxs-lookup"><span data-stu-id="0040a-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="0040a-110">2: az első elérhető FQDN címke használata az alkalmazási szabályokban</span><span class="sxs-lookup"><span data-stu-id="0040a-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="0040a-111">Ez a példa létrehoz egy tűzfal-alkalmazási szabályt az első FQDN címke használatával.</span><span class="sxs-lookup"><span data-stu-id="0040a-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="0040a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0040a-112">PARAMETERS</span></span>

### <span data-ttu-id="0040a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0040a-113">-DefaultProfile</span></span>
<span data-ttu-id="0040a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0040a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0040a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0040a-115">CommonParameters</span></span>
<span data-ttu-id="0040a-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0040a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0040a-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0040a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0040a-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0040a-118">INPUTS</span></span>

### <span data-ttu-id="0040a-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="0040a-119">None</span></span>

## <span data-ttu-id="0040a-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0040a-120">OUTPUTS</span></span>

### <span data-ttu-id="0040a-121">Microsoft. Azure. commands. Network. models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="0040a-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="0040a-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. parancsmagok. Network, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0040a-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0040a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0040a-123">NOTES</span></span>

## <span data-ttu-id="0040a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0040a-124">RELATED LINKS</span></span>

[<span data-ttu-id="0040a-125">Új – AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="0040a-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="0040a-126">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0040a-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
