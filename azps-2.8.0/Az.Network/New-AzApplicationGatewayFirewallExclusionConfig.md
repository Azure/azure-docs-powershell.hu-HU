---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 58060c488e778510822d9bc86a21de216447e0f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837512"
---
# <span data-ttu-id="7c1b2-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="7c1b2-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="7c1b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c1b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1b2-103">Új kizárási szabály lista létrehozása az alkalmazás-átjáró WAF</span><span class="sxs-lookup"><span data-stu-id="7c1b2-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="7c1b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c1b2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c1b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c1b2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1b2-106">A **New-AzApplicationGatewayFirewallExclusionConfig** parancsmag új kizáró szabály lista az Application Gateway WAF.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="7c1b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7c1b2-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1b2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7c1b2-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="7c1b2-109">Ez a parancs létrehoz egy új kizárási szabályt, amely a RequestHeaderNames és az StartsWith nevű és az XYZ nevű operátort tartalmazó változó konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="7c1b2-110">A kizárási lista konfigurációját a program az 1 $exclusion menti.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="7c1b2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c1b2-111">PARAMETERS</span></span>

### <span data-ttu-id="7c1b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1b2-112">-DefaultProfile</span></span>
<span data-ttu-id="7c1b2-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c1b2-114">-Operátor</span><span class="sxs-lookup"><span data-stu-id="7c1b2-114">-Operator</span></span>
<span data-ttu-id="7c1b2-115">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemei érvényesek.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="7c1b2-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="7c1b2-116">-Selector</span></span>
<span data-ttu-id="7c1b2-117">Ha a változó egy gyűjtemény, az operátor a gyűjteményben szereplő elemek meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="7c1b2-118">-Változó</span><span class="sxs-lookup"><span data-stu-id="7c1b2-118">-Variable</span></span>
<span data-ttu-id="7c1b2-119">A kizárni kívánt változó.</span><span class="sxs-lookup"><span data-stu-id="7c1b2-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="7c1b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1b2-120">CommonParameters</span></span>
<span data-ttu-id="7c1b2-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c1b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1b2-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1b2-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c1b2-123">INPUTS</span></span>

### <span data-ttu-id="7c1b2-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="7c1b2-124">None</span></span>

## <span data-ttu-id="7c1b2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c1b2-125">OUTPUTS</span></span>

### <span data-ttu-id="7c1b2-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="7c1b2-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="7c1b2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c1b2-127">NOTES</span></span>

## <span data-ttu-id="7c1b2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c1b2-128">RELATED LINKS</span></span>
