---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: ac48531402f474db07ed811b6c2dac2f9a1f233f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303151"
---
# <span data-ttu-id="5daed-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5daed-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5daed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5daed-102">SYNOPSIS</span></span>
<span data-ttu-id="5daed-103">Eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="5daed-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="5daed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5daed-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5daed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5daed-105">DESCRIPTION</span></span>
<span data-ttu-id="5daed-106">Az Remove-AzApplicationGatewaySslPolicy parancsmag eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="5daed-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="5daed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5daed-107">EXAMPLES</span></span>

### <span data-ttu-id="5daed-108">1. példa: az SSL-házirendek eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="5daed-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="5daed-109">Ez a parancs eltávolítja az SSL-házirendet a ApplicationGateway01 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="5daed-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="5daed-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5daed-110">PARAMETERS</span></span>

### <span data-ttu-id="5daed-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5daed-111">-ApplicationGateway</span></span>
<span data-ttu-id="5daed-112">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="5daed-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="5daed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5daed-113">-DefaultProfile</span></span>
<span data-ttu-id="5daed-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5daed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5daed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5daed-115">-Force</span></span>
<span data-ttu-id="5daed-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5daed-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5daed-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5daed-117">-Confirm</span></span>
<span data-ttu-id="5daed-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5daed-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5daed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5daed-119">-WhatIf</span></span>
<span data-ttu-id="5daed-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5daed-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5daed-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5daed-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5daed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5daed-122">CommonParameters</span></span>
<span data-ttu-id="5daed-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5daed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5daed-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5daed-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5daed-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5daed-125">INPUTS</span></span>

### <span data-ttu-id="5daed-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5daed-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5daed-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5daed-127">OUTPUTS</span></span>

### <span data-ttu-id="5daed-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5daed-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5daed-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5daed-129">NOTES</span></span>
<span data-ttu-id="5daed-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="5daed-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5daed-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5daed-131">RELATED LINKS</span></span>

[<span data-ttu-id="5daed-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5daed-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5daed-133">Új – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5daed-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5daed-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5daed-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

