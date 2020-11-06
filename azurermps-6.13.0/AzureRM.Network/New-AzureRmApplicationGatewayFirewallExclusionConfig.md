---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498319"
---
# <span data-ttu-id="b4f0b-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="b4f0b-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="b4f0b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f0b-103">Új kizárási szabály lista létrehozása az alkalmazás-átjáró WAF</span><span class="sxs-lookup"><span data-stu-id="b4f0b-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4f0b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4f0b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f0b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f0b-106">A **New-AzureRmApplicationGatewayFirewallExclusionConfig** parancsmag új kizáró szabály lista az Application Gateway WAF.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="b4f0b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b4f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f0b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b4f0b-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="b4f0b-109">Ez a parancs létrehoz egy új kizárási szabályt, amely a RequestHeaderNames és az StartsWith nevű és az XYZ nevű operátort tartalmazó változó konfigurációját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="b4f0b-110">A kizárási lista konfigurációját a program az 1 $exclusion menti.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="b4f0b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4f0b-111">PARAMETERS</span></span>

### <span data-ttu-id="b4f0b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f0b-112">-DefaultProfile</span></span>
<span data-ttu-id="b4f0b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4f0b-114">-Operátor</span><span class="sxs-lookup"><span data-stu-id="b4f0b-114">-Operator</span></span>
<span data-ttu-id="b4f0b-115">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemei érvényesek.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b4f0b-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="b4f0b-116">-Selector</span></span>
<span data-ttu-id="b4f0b-117">Ha a változó egy gyűjtemény, az operátor a gyűjteményben szereplő elemek meghatározására szolgál.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="b4f0b-118">-Változó</span><span class="sxs-lookup"><span data-stu-id="b4f0b-118">-Variable</span></span>
<span data-ttu-id="b4f0b-119">A kizárni kívánt változó.</span><span class="sxs-lookup"><span data-stu-id="b4f0b-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="b4f0b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f0b-120">CommonParameters</span></span>
<span data-ttu-id="b4f0b-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4f0b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f0b-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f0b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f0b-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f0b-123">INPUTS</span></span>

### <span data-ttu-id="b4f0b-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="b4f0b-124">None</span></span>

## <span data-ttu-id="b4f0b-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4f0b-125">OUTPUTS</span></span>

### <span data-ttu-id="b4f0b-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="b4f0b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="b4f0b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4f0b-127">NOTES</span></span>

## <span data-ttu-id="b4f0b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4f0b-128">RELATED LINKS</span></span>
