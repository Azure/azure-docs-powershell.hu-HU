---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3504e4fbdb74fffc41e3f6424540dec71bb209e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495026"
---
# <span data-ttu-id="2c1ef-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c1ef-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="2c1ef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c1ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ef-103">Eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c1ef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c1ef-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c1ef-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c1ef-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1ef-106">Az Remove-AzureRmApplicationGatewaySslPolicy parancsmag eltávolítja az SSL-házirendet egy Azure Application Gateway-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="2c1ef-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c1ef-107">EXAMPLES</span></span>

### <span data-ttu-id="2c1ef-108">1. példa: az SSL-házirendek eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="2c1ef-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="2c1ef-109">Ez a parancs eltávolítja az SSL-házirendet a ApplicationGateway01 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="2c1ef-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c1ef-110">PARAMETERS</span></span>

### <span data-ttu-id="2c1ef-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c1ef-111">-ApplicationGateway</span></span>
<span data-ttu-id="2c1ef-112">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja az SSL-házirendet.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="2c1ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ef-113">-DefaultProfile</span></span>
<span data-ttu-id="2c1ef-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c1ef-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2c1ef-115">-Force</span></span>
<span data-ttu-id="2c1ef-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c1ef-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c1ef-117">-Confirm</span></span>
<span data-ttu-id="2c1ef-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1ef-119">-WhatIf</span></span>
<span data-ttu-id="2c1ef-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c1ef-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c1ef-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ef-122">CommonParameters</span></span>
<span data-ttu-id="2c1ef-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c1ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1ef-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c1ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ef-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c1ef-125">INPUTS</span></span>

### <span data-ttu-id="2c1ef-126">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c1ef-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="2c1ef-127">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c1ef-127">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="2c1ef-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c1ef-128">OUTPUTS</span></span>

### <span data-ttu-id="2c1ef-129">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c1ef-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2c1ef-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c1ef-130">NOTES</span></span>
<span data-ttu-id="2c1ef-131">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, hálózat, hálózat</span><span class="sxs-lookup"><span data-stu-id="2c1ef-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="2c1ef-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c1ef-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c1ef-133">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c1ef-133">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="2c1ef-134">Új – AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c1ef-134">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="2c1ef-135">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="2c1ef-135">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

