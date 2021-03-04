---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ac18c96353e247c721f95acf83e174e18a578b2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938578"
---
# <span data-ttu-id="d48b3-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d48b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d48b3-102">SYNOPSIS</span></span>
<span data-ttu-id="d48b3-103">Eltávolít egy kéréstovábbító szabályt egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="d48b3-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="d48b3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d48b3-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d48b3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d48b3-105">DESCRIPTION</span></span>
<span data-ttu-id="d48b3-106">A **Remove-AzApplicationGatewayRequestRoutingRule** parancsmag eltávolít egy kéréstovábbítási szabályt egy Azure-alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="d48b3-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="d48b3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d48b3-107">EXAMPLES</span></span>

### <span data-ttu-id="d48b3-108">1. példa: Kéréstovábbító szabály eltávolítása egy alkalmazás-átjáróból</span><span class="sxs-lookup"><span data-stu-id="d48b3-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="d48b3-109">Az első parancs egy alkalmazás-átjárót kap, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="d48b3-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d48b3-110">A második parancs eltávolítja a Szabály02 nevű útválasztási szabályt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d48b3-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d48b3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d48b3-111">PARAMETERS</span></span>

### <span data-ttu-id="d48b3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d48b3-112">-ApplicationGateway</span></span>
<span data-ttu-id="d48b3-113">Azt az alkalmazás-átjárót adja meg, amelyből el szeretné távolítani a kéréstovábbító szabályt.</span><span class="sxs-lookup"><span data-stu-id="d48b3-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d48b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d48b3-114">-DefaultProfile</span></span>
<span data-ttu-id="d48b3-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d48b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d48b3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d48b3-116">-Name</span></span>
<span data-ttu-id="d48b3-117">Annak a kérés-útválasztási szabálynak a nevét adja meg, amelynek a parancsmagja eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d48b3-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="d48b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d48b3-118">CommonParameters</span></span>
<span data-ttu-id="d48b3-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d48b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d48b3-120">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d48b3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d48b3-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d48b3-121">INPUTS</span></span>

### <span data-ttu-id="d48b3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d48b3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d48b3-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d48b3-123">OUTPUTS</span></span>

### <span data-ttu-id="d48b3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d48b3-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d48b3-125">NOTES</span></span>

## <span data-ttu-id="d48b3-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d48b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="d48b3-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d48b3-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d48b3-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d48b3-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d48b3-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


