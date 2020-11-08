---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194298"
---
# <span data-ttu-id="733b1-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="733b1-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="733b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="733b1-102">SYNOPSIS</span></span>
<span data-ttu-id="733b1-103">IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="733b1-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="733b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="733b1-104">SYNTAX</span></span>

### <span data-ttu-id="733b1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="733b1-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="733b1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="733b1-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="733b1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="733b1-107">DESCRIPTION</span></span>
<span data-ttu-id="733b1-108">Az **Add-AzApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="733b1-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="733b1-109">Az IP-konfigurációk tartalmazzák azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="733b1-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="733b1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="733b1-110">EXAMPLES</span></span>

### <span data-ttu-id="733b1-111">1. példa: virtuális hálózati konfiguráció felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="733b1-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="733b1-112">Az első parancs virtuális hálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="733b1-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="733b1-113">A második parancs a korábban létrehozott virtuális hálózat segítségével kapja meg az alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="733b1-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="733b1-114">A harmadik parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="733b1-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="733b1-115">A negyedik parancs hozzáadja az IP-konfigurációt a $AppGwban tárolt alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="733b1-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="733b1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="733b1-116">PARAMETERS</span></span>

### <span data-ttu-id="733b1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="733b1-117">-ApplicationGateway</span></span>
<span data-ttu-id="733b1-118">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag IP-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="733b1-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="733b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733b1-119">-DefaultProfile</span></span>
<span data-ttu-id="733b1-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="733b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="733b1-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="733b1-121">-Name</span></span>
<span data-ttu-id="733b1-122">A hozzáadni kívánt IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="733b1-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="733b1-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="733b1-123">-Subnet</span></span>
<span data-ttu-id="733b1-124">Az alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="733b1-124">Specifies a subnet.</span></span>
<span data-ttu-id="733b1-125">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="733b1-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="733b1-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="733b1-126">-SubnetId</span></span>
<span data-ttu-id="733b1-127">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="733b1-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="733b1-128">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="733b1-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="733b1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733b1-129">CommonParameters</span></span>
<span data-ttu-id="733b1-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="733b1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733b1-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733b1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733b1-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="733b1-132">INPUTS</span></span>

### <span data-ttu-id="733b1-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="733b1-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="733b1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="733b1-134">OUTPUTS</span></span>

### <span data-ttu-id="733b1-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="733b1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="733b1-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="733b1-136">NOTES</span></span>

## <span data-ttu-id="733b1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="733b1-137">RELATED LINKS</span></span>

[<span data-ttu-id="733b1-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="733b1-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="733b1-139">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="733b1-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="733b1-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="733b1-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="733b1-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="733b1-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


