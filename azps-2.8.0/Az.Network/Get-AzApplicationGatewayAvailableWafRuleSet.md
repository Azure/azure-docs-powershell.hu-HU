---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837388"
---
# <span data-ttu-id="4783d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="4783d-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="4783d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4783d-102">SYNOPSIS</span></span>
<span data-ttu-id="4783d-103">Bekapcsolja az összes elérhető webalkalmazási tűzfalszabály-készletet.</span><span class="sxs-lookup"><span data-stu-id="4783d-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="4783d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4783d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4783d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4783d-105">DESCRIPTION</span></span>
<span data-ttu-id="4783d-106">A **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag minden elérhető webalkalmazási tűzfalszabály-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="4783d-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="4783d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4783d-107">EXAMPLES</span></span>

### <span data-ttu-id="4783d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4783d-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="4783d-109">Ez a parancs az összes elérhető webalkalmazási tűzfalszabály-készletet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="4783d-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="4783d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4783d-110">PARAMETERS</span></span>

### <span data-ttu-id="4783d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4783d-111">-DefaultProfile</span></span>
<span data-ttu-id="4783d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4783d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4783d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4783d-113">CommonParameters</span></span>
<span data-ttu-id="4783d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4783d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4783d-115">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4783d-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4783d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4783d-116">INPUTS</span></span>

### <span data-ttu-id="4783d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="4783d-117">None</span></span>

## <span data-ttu-id="4783d-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4783d-118">OUTPUTS</span></span>

### <span data-ttu-id="4783d-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="4783d-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="4783d-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4783d-120">NOTES</span></span>
<span data-ttu-id="4783d-121">**Lista – a AzApplicationGatewayAvailableWafRuleSets** a **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="4783d-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="4783d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4783d-122">RELATED LINKS</span></span>
