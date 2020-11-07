---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a9346f3ff990007ed1033032d111e5851a2ac534
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841229"
---
# <span data-ttu-id="b9c46-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b9c46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b9c46-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c46-103">Eltávolítja a háttérbeli címkészletet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b9c46-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="b9c46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b9c46-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c46-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b9c46-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c46-106">A **Remove-AzApplicationGatewayBackendAddressPool** parancsmag az Azure Application Gateway-től eltávolítja a háttér-végpontot.</span><span class="sxs-lookup"><span data-stu-id="b9c46-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="b9c46-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b9c46-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c46-108">1. példa: a back-end Address Pool eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="b9c46-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="b9c46-109">Az első parancs a ResourceGroup01 nevű ApplicationGateway01 tartozó alkalmazás-átjárót kapja meg, és a $AppGw változóban menti.</span><span class="sxs-lookup"><span data-stu-id="b9c46-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="b9c46-110">A második parancs eltávolítja a BackEndPool02 nevű back-end-címkészletet az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="b9c46-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="b9c46-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b9c46-111">PARAMETERS</span></span>

### <span data-ttu-id="b9c46-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9c46-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9c46-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a háttér-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="b9c46-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="b9c46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c46-114">-DefaultProfile</span></span>
<span data-ttu-id="b9c46-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b9c46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c46-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b9c46-116">-Name</span></span>
<span data-ttu-id="b9c46-117">A parancsmag által eltávolított back-end-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="b9c46-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c46-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b9c46-118">-Confirm</span></span>
<span data-ttu-id="b9c46-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b9c46-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c46-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c46-120">-WhatIf</span></span>
<span data-ttu-id="b9c46-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b9c46-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c46-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b9c46-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c46-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c46-123">CommonParameters</span></span>
<span data-ttu-id="b9c46-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b9c46-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c46-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c46-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c46-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9c46-126">INPUTS</span></span>

### <span data-ttu-id="b9c46-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c46-127">System.String</span></span>

## <span data-ttu-id="b9c46-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b9c46-128">OUTPUTS</span></span>

### <span data-ttu-id="b9c46-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b9c46-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b9c46-130">NOTES</span></span>

## <span data-ttu-id="b9c46-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b9c46-131">RELATED LINKS</span></span>

[<span data-ttu-id="b9c46-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9c46-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9c46-134">Új – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9c46-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9c46-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


