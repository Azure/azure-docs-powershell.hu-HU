---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d3ca233ba82d1ee485e93a898726087f5cc69415
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837891"
---
# <span data-ttu-id="011e4-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="011e4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="011e4-102">SYNOPSIS</span></span>
<span data-ttu-id="011e4-103">Eltávolítja a háttérbeli címkészletet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="011e4-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="011e4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="011e4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="011e4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="011e4-105">DESCRIPTION</span></span>
<span data-ttu-id="011e4-106">A **Remove-AzApplicationGatewayBackendAddressPool** parancsmag az Azure Application Gateway-től eltávolítja a háttér-végpontot.</span><span class="sxs-lookup"><span data-stu-id="011e4-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="011e4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="011e4-107">EXAMPLES</span></span>

### <span data-ttu-id="011e4-108">1. példa: a back-end Address Pool eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="011e4-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="011e4-109">Az első parancs a ResourceGroup01 nevű ApplicationGateway01 tartozó alkalmazás-átjárót kapja meg, és a $AppGw változóban menti.</span><span class="sxs-lookup"><span data-stu-id="011e4-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="011e4-110">A második parancs eltávolítja a BackEndPool02 nevű back-end-címkészletet az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="011e4-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="011e4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="011e4-111">PARAMETERS</span></span>

### <span data-ttu-id="011e4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="011e4-112">-ApplicationGateway</span></span>
<span data-ttu-id="011e4-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a háttér-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="011e4-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="011e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="011e4-114">-DefaultProfile</span></span>
<span data-ttu-id="011e4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="011e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="011e4-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="011e4-116">-Name</span></span>
<span data-ttu-id="011e4-117">A parancsmag által eltávolított back-end-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="011e4-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="011e4-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="011e4-118">-Confirm</span></span>
<span data-ttu-id="011e4-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="011e4-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011e4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="011e4-120">-WhatIf</span></span>
<span data-ttu-id="011e4-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="011e4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="011e4-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="011e4-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="011e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="011e4-123">CommonParameters</span></span>
<span data-ttu-id="011e4-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="011e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="011e4-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="011e4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="011e4-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="011e4-126">INPUTS</span></span>

### <span data-ttu-id="011e4-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="011e4-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="011e4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="011e4-128">OUTPUTS</span></span>

### <span data-ttu-id="011e4-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="011e4-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="011e4-130">NOTES</span></span>

## <span data-ttu-id="011e4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="011e4-131">RELATED LINKS</span></span>

[<span data-ttu-id="011e4-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="011e4-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="011e4-134">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="011e4-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="011e4-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


