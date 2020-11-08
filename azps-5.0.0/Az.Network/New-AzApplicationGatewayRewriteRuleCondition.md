---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194272"
---
# <span data-ttu-id="9330e-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="9330e-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="9330e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9330e-102">SYNOPSIS</span></span>
<span data-ttu-id="9330e-103">Feltételt ad az RewriteRule.</span><span class="sxs-lookup"><span data-stu-id="9330e-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="9330e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9330e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9330e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9330e-105">DESCRIPTION</span></span>
<span data-ttu-id="9330e-106">**Az AzApplicationGatewayRewriteRuleCondition** parancsmag az Azure-alkalmazások átjárójának Újraírási szabályának feltételeit hozza létre.</span><span class="sxs-lookup"><span data-stu-id="9330e-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="9330e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9330e-107">EXAMPLES</span></span>

### <span data-ttu-id="9330e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9330e-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayRewriteRuleCondition -Variable "var_request_uri" -Pattern "http" -IgnoreCase
PS C:\> $condition

Variable   : var_request_uri
Pattern    : http
IgnoreCase : True
Negate     : False

PS C:\> $condition | Format-Table

Variable        Pattern IgnoreCase Negate
--------        ------- ---------- ------
var_request_uri http          True  False
```
<span data-ttu-id="9330e-109">A parancs új feltételt hoz létre egy Újraírási szabályban, és az eredményt az $condition nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9330e-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="9330e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9330e-110">PARAMETERS</span></span>

### <span data-ttu-id="9330e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9330e-111">-DefaultProfile</span></span>
<span data-ttu-id="9330e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9330e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9330e-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="9330e-113">-IgnoreCase</span></span>
<span data-ttu-id="9330e-114">A jelölő beállítása a minta kihagyása esetére</span><span class="sxs-lookup"><span data-stu-id="9330e-114">Set this flag to ignore case on the pattern</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9330e-115">-Tagadás</span><span class="sxs-lookup"><span data-stu-id="9330e-115">-Negate</span></span>
<span data-ttu-id="9330e-116">A feltétel érvényesítésének eltagadására szolgáló beállítás beállítása</span><span class="sxs-lookup"><span data-stu-id="9330e-116">Set this flag to negate the condition validation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9330e-117">-Minta</span><span class="sxs-lookup"><span data-stu-id="9330e-117">-Pattern</span></span>
<span data-ttu-id="9330e-118">Minta a változó fejlécen való kereséshez</span><span class="sxs-lookup"><span data-stu-id="9330e-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="9330e-119">-Változó</span><span class="sxs-lookup"><span data-stu-id="9330e-119">-Variable</span></span>
<span data-ttu-id="9330e-120">Annak a fejlécnek a neve, amelyre feltételt szeretne beállítani</span><span class="sxs-lookup"><span data-stu-id="9330e-120">Name of the Header to set condition on it</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9330e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9330e-121">CommonParameters</span></span>
<span data-ttu-id="9330e-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9330e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9330e-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9330e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9330e-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9330e-124">INPUTS</span></span>

### <span data-ttu-id="9330e-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="9330e-125">None</span></span>

## <span data-ttu-id="9330e-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9330e-126">OUTPUTS</span></span>

### <span data-ttu-id="9330e-127">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="9330e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="9330e-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9330e-128">NOTES</span></span>

## <span data-ttu-id="9330e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9330e-129">RELATED LINKS</span></span>
[<span data-ttu-id="9330e-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9330e-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9330e-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9330e-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9330e-132">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9330e-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9330e-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9330e-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9330e-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9330e-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="9330e-135">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="9330e-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="9330e-136">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="9330e-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)