---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147011"
---
# <span data-ttu-id="f2770-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="f2770-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="f2770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2770-102">SYNOPSIS</span></span>
<span data-ttu-id="f2770-103">Új kivételszabálylista létrehozása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="f2770-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="f2770-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f2770-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2770-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f2770-105">DESCRIPTION</span></span>
<span data-ttu-id="f2770-106">The **New-AzApplicationGatewayFirewallExclusionConfig cmdlet** a new exclusion rule list for application gateway waf.</span><span class="sxs-lookup"><span data-stu-id="f2770-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="f2770-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f2770-107">EXAMPLES</span></span>

### <span data-ttu-id="f2770-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f2770-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="f2770-109">Ez a parancs létrehoz egy új kivételszabályt, amely felsorolja a RequestHeaderNames nevű változó és a StartsWith és a Selector nevű xyz nevű operátor konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f2770-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="f2770-110">A kivétellista-konfigurációt a rendszer a $exclusion 1 fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="f2770-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="f2770-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2770-111">PARAMETERS</span></span>

### <span data-ttu-id="f2770-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2770-112">-DefaultProfile</span></span>
<span data-ttu-id="f2770-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2770-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2770-114">-Operátor</span><span class="sxs-lookup"><span data-stu-id="f2770-114">-Operator</span></span>
<span data-ttu-id="f2770-115">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="f2770-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="f2770-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="f2770-116">-Selector</span></span>
<span data-ttu-id="f2770-117">Ha a változó egy gyűjtemény, az operátor azt határozza meg, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="f2770-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="f2770-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="f2770-118">-Variable</span></span>
<span data-ttu-id="f2770-119">Az a változó, amelyből ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="f2770-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="f2770-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2770-120">CommonParameters</span></span>
<span data-ttu-id="f2770-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2770-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2770-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2770-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2770-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2770-123">INPUTS</span></span>

### <span data-ttu-id="f2770-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="f2770-124">None</span></span>

## <span data-ttu-id="f2770-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2770-125">OUTPUTS</span></span>

### <span data-ttu-id="f2770-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="f2770-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="f2770-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f2770-127">NOTES</span></span>

## <span data-ttu-id="f2770-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2770-128">RELATED LINKS</span></span>
