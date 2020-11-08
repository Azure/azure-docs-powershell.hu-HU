---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 4b3a3303e8ade93b5c6945dae7650f7a9d16bbff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185948"
---
# <span data-ttu-id="15b55-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="15b55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15b55-102">SYNOPSIS</span></span>
<span data-ttu-id="15b55-103">Módosítja az alkalmazás-átjáró IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="15b55-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="15b55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15b55-104">SYNTAX</span></span>

### <span data-ttu-id="15b55-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="15b55-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b55-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="15b55-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15b55-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="15b55-107">DESCRIPTION</span></span>
<span data-ttu-id="15b55-108">A **set-AzApplicationGatewayIPConfiguration** parancsmag módosította az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="15b55-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="15b55-109">Az IP-konfiguráció azt az alhálózatot tartalmazza, amelyben egy alkalmazás-átjáró van telepítve.</span><span class="sxs-lookup"><span data-stu-id="15b55-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="15b55-110">Példák</span><span class="sxs-lookup"><span data-stu-id="15b55-110">EXAMPLES</span></span>

### <span data-ttu-id="15b55-111">Példa 1: az alkalmazás-átjáró IP-konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="15b55-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="15b55-112">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15b55-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="15b55-113">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt a $VNet használatával, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15b55-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="15b55-114">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="15b55-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="15b55-115">A Forth parancs az $AppGw-on tárolt alkalmazás-átjáró IP-konfigurációját a $Subnet tárolt alhálózat-konfigurációra állítja be.</span><span class="sxs-lookup"><span data-stu-id="15b55-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="15b55-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15b55-116">PARAMETERS</span></span>

### <span data-ttu-id="15b55-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b55-117">-ApplicationGateway</span></span>
<span data-ttu-id="15b55-118">Azt az Application Gateway-objektumot adja meg, amelyhez a parancsmag IP-konfigurációt társít.</span><span class="sxs-lookup"><span data-stu-id="15b55-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="15b55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b55-119">-DefaultProfile</span></span>
<span data-ttu-id="15b55-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15b55-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b55-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="15b55-121">-Name</span></span>
<span data-ttu-id="15b55-122">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b55-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="15b55-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="15b55-123">-Subnet</span></span>
<span data-ttu-id="15b55-124">Az alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b55-124">Specifies the subnet.</span></span>
<span data-ttu-id="15b55-125">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="15b55-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b55-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="15b55-126">-SubnetId</span></span>
<span data-ttu-id="15b55-127">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b55-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="15b55-128">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="15b55-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b55-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b55-129">CommonParameters</span></span>
<span data-ttu-id="15b55-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15b55-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b55-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b55-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b55-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b55-132">INPUTS</span></span>

### <span data-ttu-id="15b55-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b55-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15b55-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b55-134">OUTPUTS</span></span>

### <span data-ttu-id="15b55-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15b55-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15b55-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15b55-136">NOTES</span></span>

## <span data-ttu-id="15b55-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15b55-137">RELATED LINKS</span></span>

[<span data-ttu-id="15b55-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="15b55-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="15b55-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="15b55-141">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="15b55-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="15b55-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

