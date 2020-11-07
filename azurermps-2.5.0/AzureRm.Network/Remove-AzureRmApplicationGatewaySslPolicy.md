---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 383ad627ff7a633d508daccde70e3de395e4ad57
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848742"
---
# <span data-ttu-id="a6871-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a6871-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="a6871-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6871-102">SYNOPSIS</span></span>
<span data-ttu-id="a6871-103">Eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a6871-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6871-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6871-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6871-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6871-105">DESCRIPTION</span></span>
<span data-ttu-id="a6871-106">Az Remove-AzureRmApplicationGatewaySslPolicy parancsmag eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="a6871-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="a6871-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6871-107">EXAMPLES</span></span>

### <span data-ttu-id="a6871-108">1. példa: az SSL-házirendek eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="a6871-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="a6871-109">Ez a parancs eltávolítja az SSL-házirendet a ApplicationGateway01 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a6871-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="a6871-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6871-110">PARAMETERS</span></span>

### <span data-ttu-id="a6871-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6871-111">-ApplicationGateway</span></span>
<span data-ttu-id="a6871-112">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="a6871-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="a6871-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6871-113">-DefaultProfile</span></span>
<span data-ttu-id="a6871-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6871-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6871-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a6871-115">-Force</span></span>
<span data-ttu-id="a6871-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6871-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6871-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6871-117">-Confirm</span></span>
<span data-ttu-id="a6871-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6871-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6871-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6871-119">-WhatIf</span></span>
<span data-ttu-id="a6871-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6871-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6871-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6871-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6871-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6871-122">CommonParameters</span></span>
<span data-ttu-id="a6871-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6871-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6871-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6871-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6871-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6871-125">INPUTS</span></span>

### <span data-ttu-id="a6871-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a6871-126">System.String</span></span>

## <span data-ttu-id="a6871-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6871-127">OUTPUTS</span></span>

### <span data-ttu-id="a6871-128">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6871-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a6871-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6871-129">NOTES</span></span>
<span data-ttu-id="a6871-130">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="a6871-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a6871-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6871-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6871-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a6871-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="a6871-133">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a6871-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="a6871-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="a6871-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

