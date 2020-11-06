---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 996a2c17b6283e967eaca8462f4d703aed60d19c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495034"
---
# <span data-ttu-id="e45fe-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e45fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e45fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e45fe-103">Eltávolítja a háttérbeli címkészletet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="e45fe-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e45fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e45fe-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e45fe-105">DESCRIPTION</span></span>
<span data-ttu-id="e45fe-106">A **Remove-AzureRmApplicationGatewayBackendAddressPool** parancsmag az Azure Application Gateway-től eltávolítja a háttér-végpontot.</span><span class="sxs-lookup"><span data-stu-id="e45fe-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="e45fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e45fe-107">EXAMPLES</span></span>

### <span data-ttu-id="e45fe-108">1. példa: a back-end Address Pool eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="e45fe-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="e45fe-109">Az első parancs a ResourceGroup01 nevű ApplicationGateway01 tartozó alkalmazás-átjárót kapja meg, és a $AppGw változóban menti.</span><span class="sxs-lookup"><span data-stu-id="e45fe-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="e45fe-110">A második parancs eltávolítja a BackEndPool02 nevű back-end-címkészletet az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="e45fe-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="e45fe-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e45fe-111">PARAMETERS</span></span>

### <span data-ttu-id="e45fe-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e45fe-112">-ApplicationGateway</span></span>
<span data-ttu-id="e45fe-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a háttér-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="e45fe-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="e45fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45fe-114">-DefaultProfile</span></span>
<span data-ttu-id="e45fe-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e45fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e45fe-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e45fe-116">-Name</span></span>
<span data-ttu-id="e45fe-117">A parancsmag által eltávolított back-end-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="e45fe-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e45fe-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e45fe-118">-Confirm</span></span>
<span data-ttu-id="e45fe-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e45fe-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45fe-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45fe-120">-WhatIf</span></span>
<span data-ttu-id="e45fe-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e45fe-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45fe-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e45fe-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45fe-123">CommonParameters</span></span>
<span data-ttu-id="e45fe-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e45fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45fe-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45fe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45fe-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e45fe-126">INPUTS</span></span>

### <span data-ttu-id="e45fe-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e45fe-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="e45fe-128">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e45fe-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="e45fe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e45fe-129">OUTPUTS</span></span>

### <span data-ttu-id="e45fe-130">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e45fe-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e45fe-131">NOTES</span></span>

## <span data-ttu-id="e45fe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e45fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="e45fe-133">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-133">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e45fe-134">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-134">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e45fe-135">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-135">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e45fe-136">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e45fe-136">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


