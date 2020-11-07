---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841758"
---
# <span data-ttu-id="3a35e-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a35e-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="3a35e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3a35e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a35e-103">Bekapcsolja az összes elérhető webalkalmazási tűzfalszabály-készletet.</span><span class="sxs-lookup"><span data-stu-id="3a35e-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="3a35e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3a35e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a35e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3a35e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a35e-106">A **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag minden elérhető webalkalmazási tűzfalszabály-készletet kap.</span><span class="sxs-lookup"><span data-stu-id="3a35e-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="3a35e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3a35e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a35e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3a35e-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="3a35e-109">Ez a parancs az összes elérhető webalkalmazási tűzfalszabály-készletet visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="3a35e-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="3a35e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3a35e-110">PARAMETERS</span></span>

### <span data-ttu-id="3a35e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a35e-111">-DefaultProfile</span></span>
<span data-ttu-id="3a35e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a35e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a35e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a35e-113">CommonParameters</span></span>
<span data-ttu-id="3a35e-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3a35e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a35e-115">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a35e-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a35e-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a35e-116">INPUTS</span></span>

### <span data-ttu-id="3a35e-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a35e-117">None</span></span>

## <span data-ttu-id="3a35e-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a35e-118">OUTPUTS</span></span>

### <span data-ttu-id="3a35e-119">Microsoft. Azure. commands. Network. models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="3a35e-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="3a35e-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3a35e-120">NOTES</span></span>
<span data-ttu-id="3a35e-121">**Lista – a AzApplicationGatewayAvailableWafRuleSet** a **Get-AzApplicationGatewayAvailableWafRuleSet** parancsmag aliasa.</span><span class="sxs-lookup"><span data-stu-id="3a35e-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="3a35e-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a35e-122">RELATED LINKS</span></span>

