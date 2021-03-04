---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 029ba60169ee22d86d9e54661296f04bf2242713
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924714"
---
# <span data-ttu-id="5eb18-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="5eb18-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="5eb18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb18-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb18-103">Új kivételszabálylista létrehozása az alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="5eb18-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="5eb18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5eb18-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb18-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5eb18-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb18-106">The **New-AzApplicationGatewayFirewallExclusionConfig cmdlet** a new exclusion rule list for application gateway waf.</span><span class="sxs-lookup"><span data-stu-id="5eb18-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="5eb18-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5eb18-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb18-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5eb18-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="5eb18-109">Ez a parancs létrehoz egy új kivételszabályt, amely felsorolja a RequestHeaderNames nevű változó és a StartsWith és a Selector nevű xyz nevű operátor konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5eb18-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="5eb18-110">A kivétellista-konfigurációt a rendszer a $exclusion 1 fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="5eb18-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="5eb18-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eb18-111">PARAMETERS</span></span>

### <span data-ttu-id="5eb18-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb18-112">-DefaultProfile</span></span>
<span data-ttu-id="5eb18-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5eb18-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb18-114">-Operátor</span><span class="sxs-lookup"><span data-stu-id="5eb18-114">-Operator</span></span>
<span data-ttu-id="5eb18-115">Ha a változó egy gyűjtemény, a választóval megadhatja, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="5eb18-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="5eb18-116">-Választó</span><span class="sxs-lookup"><span data-stu-id="5eb18-116">-Selector</span></span>
<span data-ttu-id="5eb18-117">Ha a változó egy gyűjtemény, az operátor azt határozza meg, hogy a gyűjtemény mely elemeire vonatkozik ez a kivétel.</span><span class="sxs-lookup"><span data-stu-id="5eb18-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

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

### <span data-ttu-id="5eb18-118">-Variable</span><span class="sxs-lookup"><span data-stu-id="5eb18-118">-Variable</span></span>
<span data-ttu-id="5eb18-119">Az a változó, amelyből ki kell zárni.</span><span class="sxs-lookup"><span data-stu-id="5eb18-119">The variable to be excluded.</span></span>

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

### <span data-ttu-id="5eb18-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb18-120">CommonParameters</span></span>
<span data-ttu-id="5eb18-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb18-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb18-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb18-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb18-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb18-123">INPUTS</span></span>

### <span data-ttu-id="5eb18-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="5eb18-124">None</span></span>

## <span data-ttu-id="5eb18-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5eb18-125">OUTPUTS</span></span>

### <span data-ttu-id="5eb18-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="5eb18-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="5eb18-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5eb18-127">NOTES</span></span>

## <span data-ttu-id="5eb18-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5eb18-128">RELATED LINKS</span></span>
