---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleheaderconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleHeaderConfiguration.md
ms.openlocfilehash: ed8cda03debbb69c2fa65d7c209889c4cd3d2446
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358887"
---
# <span data-ttu-id="99f02-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="99f02-101">New-AzApplicationGatewayRewriteRuleHeaderConfiguration</span></span>

## <span data-ttu-id="99f02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f02-102">SYNOPSIS</span></span>
<span data-ttu-id="99f02-103">Újraírt szabályfejléc-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="99f02-103">Creates a rewrite rule header configuration for an application gateway.</span></span>

## <span data-ttu-id="99f02-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99f02-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName <String> [-HeaderValue <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f02-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99f02-105">DESCRIPTION</span></span>
<span data-ttu-id="99f02-106">**AzApplicationGatewayRewriteRuleHeaderConfiguration parancsmag** létrehoz egy újraírási szabály műveletkészletet egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="99f02-106">**The AzApplicationGatewayRewriteRuleHeaderConfiguration** cmdlet creates a rewrite rule action set for an Azure application gateway.</span></span>

## <span data-ttu-id="99f02-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99f02-107">EXAMPLES</span></span>

### <span data-ttu-id="99f02-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="99f02-108">Example 1</span></span>
```powershell
PS C:\> $hc = New-AzApplicationGatewayRewriteRuleHeaderConfiguration -HeaderName abc -HeaderValue def
```

<span data-ttu-id="99f02-109">Ez a parancs egy újraírási szabályfejléc-konfigurációt hoz létre, és az eredményt a következő nevű változóban $hc.</span><span class="sxs-lookup"><span data-stu-id="99f02-109">This command creates a rewrite rule header configuration and stores the result in the variable named $hc.</span></span>

## <span data-ttu-id="99f02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99f02-110">PARAMETERS</span></span>

### <span data-ttu-id="99f02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f02-111">-DefaultProfile</span></span>
<span data-ttu-id="99f02-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99f02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f02-113">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="99f02-113">-HeaderName</span></span>
<span data-ttu-id="99f02-114">Az újraírni megfelelő fejléc neve</span><span class="sxs-lookup"><span data-stu-id="99f02-114">Name of the Header to rewrite</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f02-115">-HeaderValue</span><span class="sxs-lookup"><span data-stu-id="99f02-115">-HeaderValue</span></span>
<span data-ttu-id="99f02-116">A fejléc értéke a megadott fejlécnév halmazában.</span><span class="sxs-lookup"><span data-stu-id="99f02-116">Header value to the set for the given header name.</span></span>
<span data-ttu-id="99f02-117">A fejléc törlődik, ha ez nincs megadva</span><span class="sxs-lookup"><span data-stu-id="99f02-117">Header will be deleted if this is omitted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f02-118">CommonParameters</span></span>
<span data-ttu-id="99f02-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f02-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99f02-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f02-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99f02-121">INPUTS</span></span>

### <span data-ttu-id="99f02-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="99f02-122">None</span></span>

## <span data-ttu-id="99f02-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99f02-123">OUTPUTS</span></span>

### <span data-ttu-id="99f02-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="99f02-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHeaderConfiguration</span></span>

## <span data-ttu-id="99f02-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99f02-125">NOTES</span></span>

## <span data-ttu-id="99f02-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99f02-126">RELATED LINKS</span></span>

[<span data-ttu-id="99f02-127">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f02-127">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="99f02-128">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f02-128">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="99f02-129">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f02-129">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="99f02-130">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f02-130">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="99f02-131">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="99f02-131">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="99f02-132">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="99f02-132">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="99f02-133">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="99f02-133">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)
