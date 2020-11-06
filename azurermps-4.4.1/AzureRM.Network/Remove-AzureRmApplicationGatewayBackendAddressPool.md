---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5655272afa9ddc9c0ff4c1873a0fac7a0e1f50dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493420"
---
# <span data-ttu-id="73275-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="73275-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73275-102">SYNOPSIS</span></span>
<span data-ttu-id="73275-103">Eltávolítja a háttérbeli címkészletet egy alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="73275-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73275-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73275-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73275-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="73275-105">DESCRIPTION</span></span>
<span data-ttu-id="73275-106">A **Remove-AzureRmApplicationGatewayBackendAddressPool** parancsmag az Azure Application Gateway-től eltávolítja a háttér-végpontot.</span><span class="sxs-lookup"><span data-stu-id="73275-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="73275-107">Példák</span><span class="sxs-lookup"><span data-stu-id="73275-107">EXAMPLES</span></span>

### <span data-ttu-id="73275-108">1. példa: a back-end Address Pool eltávolítása egy alkalmazás-átjáróról</span><span class="sxs-lookup"><span data-stu-id="73275-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="73275-109">Az első parancs a ResourceGroup01 nevű ApplicationGateway01 tartozó alkalmazás-átjárót kapja meg, és a $AppGw változóban menti.</span><span class="sxs-lookup"><span data-stu-id="73275-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="73275-110">A második parancs eltávolítja a BackEndPool02 nevű back-end-címkészletet az alkalmazás-átjáróról.</span><span class="sxs-lookup"><span data-stu-id="73275-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="73275-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73275-111">PARAMETERS</span></span>

### <span data-ttu-id="73275-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73275-112">-ApplicationGateway</span></span>
<span data-ttu-id="73275-113">Annak az alkalmazásnak az átjáróját adja meg, amelyből a parancsmag eltávolítja a háttér-címkészletet.</span><span class="sxs-lookup"><span data-stu-id="73275-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="73275-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73275-114">-Name</span></span>
<span data-ttu-id="73275-115">A parancsmag által eltávolított back-end-címkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="73275-115">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="73275-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73275-116">-Confirm</span></span>
<span data-ttu-id="73275-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73275-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73275-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73275-118">-WhatIf</span></span>
<span data-ttu-id="73275-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73275-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73275-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73275-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73275-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73275-121">-DefaultProfile</span></span>
<span data-ttu-id="73275-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73275-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73275-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73275-123">CommonParameters</span></span>
<span data-ttu-id="73275-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73275-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73275-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73275-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73275-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73275-126">INPUTS</span></span>

### <span data-ttu-id="73275-127">System. String</span><span class="sxs-lookup"><span data-stu-id="73275-127">System.String</span></span>

## <span data-ttu-id="73275-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73275-128">OUTPUTS</span></span>

### <span data-ttu-id="73275-129">Microsoft. Azure. commands. Network. models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="73275-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73275-130">NOTES</span></span>

## <span data-ttu-id="73275-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73275-131">RELATED LINKS</span></span>

[<span data-ttu-id="73275-132">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="73275-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="73275-134">Új – AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="73275-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="73275-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


