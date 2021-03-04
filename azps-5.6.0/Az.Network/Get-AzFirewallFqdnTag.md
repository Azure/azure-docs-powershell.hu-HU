---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: ff5dee9a4e072cea7f1ee5bd46898857233ed0d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921089"
---
# <span data-ttu-id="5ac20-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5ac20-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="5ac20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac20-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac20-103">A rendelkezésre álló Azure Firewall Fqdn-címkéket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ac20-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="5ac20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5ac20-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ac20-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5ac20-105">DESCRIPTION</span></span>
<span data-ttu-id="5ac20-106">A **Get-AzFirewallFqdnTag** parancsmag megkapja az Azure tűzfal alkalmazásszabályzához használható FQDN-címkék listáját.</span><span class="sxs-lookup"><span data-stu-id="5ac20-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="5ac20-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5ac20-107">EXAMPLES</span></span>

### <span data-ttu-id="5ac20-108">1: Az összes elérhető teljes tartománycímcédulának beolvasása</span><span class="sxs-lookup"><span data-stu-id="5ac20-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="5ac20-109">Ez a példa beolvassa az összes elérhető teljes tartománycímkét.</span><span class="sxs-lookup"><span data-stu-id="5ac20-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="5ac20-110">2: Az első elérhető FQDN-címke használata alkalmazásszabályban</span><span class="sxs-lookup"><span data-stu-id="5ac20-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="5ac20-111">Ebben a példában az első elérhető teljes tartománycímke használatával tűzfalalkalmazási szabályt hoz létre</span><span class="sxs-lookup"><span data-stu-id="5ac20-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="5ac20-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ac20-112">PARAMETERS</span></span>

### <span data-ttu-id="5ac20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac20-113">-DefaultProfile</span></span>
<span data-ttu-id="5ac20-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ac20-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ac20-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac20-115">CommonParameters</span></span>
<span data-ttu-id="5ac20-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac20-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac20-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ac20-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac20-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ac20-118">INPUTS</span></span>

### <span data-ttu-id="5ac20-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="5ac20-119">None</span></span>

## <span data-ttu-id="5ac20-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ac20-120">OUTPUTS</span></span>

### <span data-ttu-id="5ac20-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="5ac20-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="5ac20-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5ac20-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5ac20-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5ac20-123">NOTES</span></span>

## <span data-ttu-id="5ac20-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ac20-124">RELATED LINKS</span></span>

[<span data-ttu-id="5ac20-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="5ac20-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="5ac20-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="5ac20-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
