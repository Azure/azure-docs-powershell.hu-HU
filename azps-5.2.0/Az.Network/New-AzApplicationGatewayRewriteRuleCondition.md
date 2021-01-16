---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriterulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleCondition.md
ms.openlocfilehash: 5bf255e104b065d601dba0a29c3b47b3fa126e0e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358201"
---
# <span data-ttu-id="d2adf-101">New-AzApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d2adf-101">New-AzApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d2adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2adf-103">Hozzáad egy feltételt egy alkalmazás-átjáró RewriteRule-hez.</span><span class="sxs-lookup"><span data-stu-id="d2adf-103">Adds a condition to the RewriteRule for an application gateway.</span></span>

## <span data-ttu-id="d2adf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2adf-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleCondition -Variable <String> [-Pattern <String>] [-IgnoreCase] [-Negate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2adf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2adf-105">DESCRIPTION</span></span>
<span data-ttu-id="d2adf-106">**AzApplicationGatewayRewriteRuleCondition** parancsmag létrehoz egy újraírási szabályt egy Azure-alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d2adf-106">**The AzApplicationGatewayRewriteRuleCondition** cmdlet creates a rewrite rule condition for an Azure application gateway.</span></span>

## <span data-ttu-id="d2adf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2adf-107">EXAMPLES</span></span>

### <span data-ttu-id="d2adf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d2adf-108">Example 1</span></span>
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
<span data-ttu-id="d2adf-109">Ez a parancs létrehoz egy feltételt egy újraírási szabályban, és az eredményt a következő nevű változóban $condition.</span><span class="sxs-lookup"><span data-stu-id="d2adf-109">This command creates a condition in a rewrite rule and stores the result in the variable named $condition.</span></span>

## <span data-ttu-id="d2adf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2adf-110">PARAMETERS</span></span>

### <span data-ttu-id="d2adf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2adf-111">-DefaultProfile</span></span>
<span data-ttu-id="d2adf-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2adf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2adf-113">-IgnoreCase</span><span class="sxs-lookup"><span data-stu-id="d2adf-113">-IgnoreCase</span></span>
<span data-ttu-id="d2adf-114">A jelölő beállítása a mintán a kis- és</span><span class="sxs-lookup"><span data-stu-id="d2adf-114">Set this flag to ignore case on the pattern</span></span>

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

### <span data-ttu-id="d2adf-115">-Negate</span><span class="sxs-lookup"><span data-stu-id="d2adf-115">-Negate</span></span>
<span data-ttu-id="d2adf-116">A jelölő beállítása a feltételérvényesítést nem érvényesítő jelölőre</span><span class="sxs-lookup"><span data-stu-id="d2adf-116">Set this flag to negate the condition validation</span></span>

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

### <span data-ttu-id="d2adf-117">-Pattern</span><span class="sxs-lookup"><span data-stu-id="d2adf-117">-Pattern</span></span>
<span data-ttu-id="d2adf-118">A változófejlécen keresve keresve</span><span class="sxs-lookup"><span data-stu-id="d2adf-118">Pattern to look for in the Variable Header</span></span>

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

### <span data-ttu-id="d2adf-119">-Variable</span><span class="sxs-lookup"><span data-stu-id="d2adf-119">-Variable</span></span>
<span data-ttu-id="d2adf-120">A feltételt megszállító fejléc neve</span><span class="sxs-lookup"><span data-stu-id="d2adf-120">Name of the Header to set condition on it</span></span>

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

### <span data-ttu-id="d2adf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2adf-121">CommonParameters</span></span>
<span data-ttu-id="d2adf-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2adf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d2adf-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2adf-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2adf-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2adf-124">INPUTS</span></span>

### <span data-ttu-id="d2adf-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="d2adf-125">None</span></span>

## <span data-ttu-id="d2adf-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2adf-126">OUTPUTS</span></span>

### <span data-ttu-id="d2adf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span><span class="sxs-lookup"><span data-stu-id="d2adf-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleCondition</span></span>

## <span data-ttu-id="d2adf-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2adf-128">NOTES</span></span>

## <span data-ttu-id="d2adf-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2adf-129">RELATED LINKS</span></span>
[<span data-ttu-id="d2adf-130">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-130">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2adf-131">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-131">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2adf-132">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-132">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2adf-133">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-133">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2adf-134">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-134">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="d2adf-135">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="d2adf-135">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="d2adf-136">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="d2adf-136">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
