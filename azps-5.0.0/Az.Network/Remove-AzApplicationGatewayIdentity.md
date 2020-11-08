---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: d0056cedad180fda8475abae2106aaba3d2ad239
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194230"
---
# <span data-ttu-id="3190b-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="3190b-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="3190b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3190b-102">SYNOPSIS</span></span>
<span data-ttu-id="3190b-103">Eltávolít egy identitást egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="3190b-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="3190b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3190b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3190b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3190b-105">DESCRIPTION</span></span>
<span data-ttu-id="3190b-106">**Remove-AzApplicationGatewayIdentity** parancsmag: eltávolítja az identitást egy alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="3190b-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="3190b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3190b-107">EXAMPLES</span></span>

### <span data-ttu-id="3190b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3190b-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="3190b-109">Ebben a példában egy meglévő alkalmazás-átjáróból távolítjuk el az identitást.</span><span class="sxs-lookup"><span data-stu-id="3190b-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="3190b-110">Megjegyzés: Ha az átjáró a boltozatos titokra hivatkozik, akkor fontos, hogy távolítsa el az SSL-tanúsítvány hivatkozásait a művelettel együtt.</span><span class="sxs-lookup"><span data-stu-id="3190b-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="3190b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3190b-111">PARAMETERS</span></span>

### <span data-ttu-id="3190b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3190b-112">-ApplicationGateway</span></span>
<span data-ttu-id="3190b-113">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="3190b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="3190b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3190b-114">-DefaultProfile</span></span>
<span data-ttu-id="3190b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3190b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3190b-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3190b-116">-Confirm</span></span>
<span data-ttu-id="3190b-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3190b-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3190b-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3190b-118">-WhatIf</span></span>
<span data-ttu-id="3190b-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3190b-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3190b-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3190b-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3190b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3190b-121">CommonParameters</span></span>
<span data-ttu-id="3190b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3190b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3190b-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3190b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3190b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3190b-124">INPUTS</span></span>

### <span data-ttu-id="3190b-125">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3190b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3190b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3190b-126">OUTPUTS</span></span>

### <span data-ttu-id="3190b-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3190b-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3190b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3190b-128">NOTES</span></span>

## <span data-ttu-id="3190b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3190b-129">RELATED LINKS</span></span>
