---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c8dd9faf54d92f34b523292a8b25465978074ad5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670740"
---
# <span data-ttu-id="7db66-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7db66-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="7db66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7db66-102">SYNOPSIS</span></span>
<span data-ttu-id="7db66-103">IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7db66-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="7db66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7db66-104">SYNTAX</span></span>

### <span data-ttu-id="7db66-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7db66-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7db66-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7db66-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7db66-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7db66-107">DESCRIPTION</span></span>
<span data-ttu-id="7db66-108">Az **Add-AzApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7db66-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="7db66-109">Az IP-konfigurációk tartalmazzák azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="7db66-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="7db66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7db66-110">EXAMPLES</span></span>

### <span data-ttu-id="7db66-111">1. példa: virtuális hálózati konfiguráció felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="7db66-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="7db66-112">Az első parancs virtuális hálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="7db66-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="7db66-113">A második parancs a korábban létrehozott virtuális hálózat segítségével kapja meg az alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="7db66-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="7db66-114">A harmadik parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7db66-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7db66-115">A Fouth parancs hozzáadja az IP-konfigurációt a $AppGwban tárolt alkalmazási átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7db66-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7db66-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7db66-116">PARAMETERS</span></span>

### <span data-ttu-id="7db66-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7db66-117">-ApplicationGateway</span></span>
<span data-ttu-id="7db66-118">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag IP-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="7db66-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="7db66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db66-119">-DefaultProfile</span></span>
<span data-ttu-id="7db66-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7db66-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7db66-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7db66-121">-Name</span></span>
<span data-ttu-id="7db66-122">A hozzáadni kívánt IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7db66-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="7db66-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="7db66-123">-Subnet</span></span>
<span data-ttu-id="7db66-124">Az alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7db66-124">Specifies a subnet.</span></span>
<span data-ttu-id="7db66-125">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="7db66-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7db66-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="7db66-126">-SubnetId</span></span>
<span data-ttu-id="7db66-127">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="7db66-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="7db66-128">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="7db66-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="7db66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db66-129">CommonParameters</span></span>
<span data-ttu-id="7db66-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7db66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db66-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db66-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db66-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7db66-132">INPUTS</span></span>

### <span data-ttu-id="7db66-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7db66-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7db66-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7db66-134">OUTPUTS</span></span>

### <span data-ttu-id="7db66-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7db66-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7db66-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7db66-136">NOTES</span></span>

## <span data-ttu-id="7db66-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7db66-137">RELATED LINKS</span></span>

[<span data-ttu-id="7db66-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7db66-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7db66-139">Új – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7db66-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7db66-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7db66-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="7db66-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="7db66-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


