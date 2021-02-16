---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161099"
---
# <span data-ttu-id="ba5fa-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="ba5fa-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="ba5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5fa-103">A rendelkezésre álló Azure Firewall Fqdn-címkéket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba5fa-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="ba5fa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba5fa-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba5fa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ba5fa-106">A **Get-AzFirewallFqdnTag** parancsmag lekérése az Azure tűzfal alkalmazásszabályzához használható teljes tartománynévi címkék listájához</span><span class="sxs-lookup"><span data-stu-id="ba5fa-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="ba5fa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ba5fa-108">1: Az összes elérhető teljes tartománycímcédulának beolvasása</span><span class="sxs-lookup"><span data-stu-id="ba5fa-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="ba5fa-109">Ez a példa beolvassa az összes elérhető teljes tartománycímkét.</span><span class="sxs-lookup"><span data-stu-id="ba5fa-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="ba5fa-110">2: Az első elérhető FQDN-címke használata alkalmazásszabályban</span><span class="sxs-lookup"><span data-stu-id="ba5fa-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="ba5fa-111">Ebben a példában az első elérhető teljes tartománycímke használatával tűzfalalkalmazási szabályt hoz létre</span><span class="sxs-lookup"><span data-stu-id="ba5fa-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="ba5fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba5fa-112">PARAMETERS</span></span>

### <span data-ttu-id="ba5fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5fa-113">-DefaultProfile</span></span>
<span data-ttu-id="ba5fa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba5fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba5fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5fa-115">CommonParameters</span></span>
<span data-ttu-id="ba5fa-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba5fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5fa-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba5fa-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5fa-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba5fa-118">INPUTS</span></span>

### <span data-ttu-id="ba5fa-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="ba5fa-119">None</span></span>

## <span data-ttu-id="ba5fa-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba5fa-120">OUTPUTS</span></span>

### <span data-ttu-id="ba5fa-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="ba5fa-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="ba5fa-122">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="ba5fa-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ba5fa-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba5fa-123">NOTES</span></span>

## <span data-ttu-id="ba5fa-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba5fa-124">RELATED LINKS</span></span>

[<span data-ttu-id="ba5fa-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="ba5fa-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="ba5fa-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ba5fa-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
