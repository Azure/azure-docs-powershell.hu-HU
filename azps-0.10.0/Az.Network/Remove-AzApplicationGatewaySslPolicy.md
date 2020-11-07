---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 455ee170ffba9f601cd8e3034e0c774966f92eba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841186"
---
# <span data-ttu-id="e1373-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e1373-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e1373-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1373-102">SYNOPSIS</span></span>
<span data-ttu-id="e1373-103">Eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="e1373-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e1373-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1373-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1373-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1373-105">DESCRIPTION</span></span>
<span data-ttu-id="e1373-106">Az Remove-AzApplicationGatewaySslPolicy parancsmag eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="e1373-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="e1373-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e1373-107">EXAMPLES</span></span>

### <span data-ttu-id="e1373-108">1. példa: az SSL-házirendek eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="e1373-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="e1373-109">Ez a parancs eltávolítja az SSL-házirendet a ApplicationGateway01 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="e1373-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="e1373-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1373-110">PARAMETERS</span></span>

### <span data-ttu-id="e1373-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1373-111">-ApplicationGateway</span></span>
<span data-ttu-id="e1373-112">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="e1373-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1373-113">-DefaultProfile</span></span>
<span data-ttu-id="e1373-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1373-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1373-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e1373-115">-Force</span></span>
<span data-ttu-id="e1373-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1373-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e1373-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e1373-117">-Confirm</span></span>
<span data-ttu-id="e1373-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e1373-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1373-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1373-119">-WhatIf</span></span>
<span data-ttu-id="e1373-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e1373-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1373-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e1373-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1373-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1373-122">CommonParameters</span></span>
<span data-ttu-id="e1373-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1373-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1373-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1373-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1373-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1373-125">INPUTS</span></span>

### <span data-ttu-id="e1373-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e1373-126">System.String</span></span>

## <span data-ttu-id="e1373-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1373-127">OUTPUTS</span></span>

### <span data-ttu-id="e1373-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1373-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1373-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1373-129">NOTES</span></span>
<span data-ttu-id="e1373-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="e1373-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e1373-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1373-131">RELATED LINKS</span></span>

[<span data-ttu-id="e1373-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e1373-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e1373-133">Új – AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e1373-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e1373-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e1373-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

