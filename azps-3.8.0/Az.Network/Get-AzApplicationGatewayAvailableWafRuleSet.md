---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013582"
---
# <span data-ttu-id="a0678-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="a0678-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="a0678-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0678-102">SYNOPSIS</span></span>
<span data-ttu-id="a0678-103">Bekapcsolja az összes elérhető webalkalmazási tűzfalszabály-készletet.</span><span class="sxs-lookup"><span data-stu-id="a0678-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="a0678-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0678-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0678-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0678-105">DESCRIPTION</span></span>
<span data-ttu-id="a0678-106">A **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag minden elérhető webalkalmazási tűzfalszabály-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="a0678-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="a0678-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0678-107">EXAMPLES</span></span>

### <span data-ttu-id="a0678-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a0678-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="a0678-109">Ez a parancs az összes elérhető webalkalmazási tűzfalszabály-készletet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="a0678-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="a0678-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0678-110">PARAMETERS</span></span>

### <span data-ttu-id="a0678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0678-111">-DefaultProfile</span></span>
<span data-ttu-id="a0678-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a0678-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0678-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0678-113">CommonParameters</span></span>
<span data-ttu-id="a0678-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0678-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0678-115">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a0678-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0678-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0678-116">INPUTS</span></span>

### <span data-ttu-id="a0678-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="a0678-117">None</span></span>

## <span data-ttu-id="a0678-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0678-118">OUTPUTS</span></span>

### <span data-ttu-id="a0678-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="a0678-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="a0678-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0678-120">NOTES</span></span>
<span data-ttu-id="a0678-121">**Lista – a AzApplicationGatewayAvailableWafRuleSets** a **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="a0678-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="a0678-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0678-122">RELATED LINKS</span></span>
