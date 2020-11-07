---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680328"
---
# <span data-ttu-id="9039b-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="9039b-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="9039b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9039b-102">SYNOPSIS</span></span>
<span data-ttu-id="9039b-103">Az elérhető Azure Firewall FQDN-címkéket kapja.</span><span class="sxs-lookup"><span data-stu-id="9039b-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9039b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9039b-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9039b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9039b-105">DESCRIPTION</span></span>
<span data-ttu-id="9039b-106">A **Get-AzureRmFirewallFqdnTag** parancsmag az Azure Firewall alkalmazás szabályaihoz használható FQDN-címkék listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9039b-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="9039b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9039b-107">EXAMPLES</span></span>

### <span data-ttu-id="9039b-108">1: az összes elérhető FQDN-címke beolvasása</span><span class="sxs-lookup"><span data-stu-id="9039b-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="9039b-109">Ez a példa beolvassa az összes elérhető FQDN-címkét.</span><span class="sxs-lookup"><span data-stu-id="9039b-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="9039b-110">2: az első elérhető FQDN címke használata az alkalmazási szabályokban</span><span class="sxs-lookup"><span data-stu-id="9039b-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="9039b-111">Ez a példa létrehoz egy tűzfal-alkalmazási szabályt az első FQDN címke használatával.</span><span class="sxs-lookup"><span data-stu-id="9039b-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="9039b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9039b-112">PARAMETERS</span></span>

### <span data-ttu-id="9039b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9039b-113">-DefaultProfile</span></span>
<span data-ttu-id="9039b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9039b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9039b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9039b-115">CommonParameters</span></span>
<span data-ttu-id="9039b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9039b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9039b-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9039b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9039b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9039b-118">INPUTS</span></span>

### <span data-ttu-id="9039b-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="9039b-119">None</span></span>
<span data-ttu-id="9039b-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9039b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9039b-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9039b-121">OUTPUTS</span></span>

### <span data-ttu-id="9039b-122">Microsoft. Azure. commands. Network. models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="9039b-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="9039b-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9039b-123">NOTES</span></span>

## <span data-ttu-id="9039b-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9039b-124">RELATED LINKS</span></span>

[<span data-ttu-id="9039b-125">Új – AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="9039b-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="9039b-126">Új – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="9039b-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
