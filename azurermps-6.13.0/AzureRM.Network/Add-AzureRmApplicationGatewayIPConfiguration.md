---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 2ce0cb130e6c4d25d4b076d06224364011ced2b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503576"
---
# <span data-ttu-id="61f24-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f24-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="61f24-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61f24-102">SYNOPSIS</span></span>
<span data-ttu-id="61f24-103">IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="61f24-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f24-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61f24-104">SYNTAX</span></span>

### <span data-ttu-id="61f24-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="61f24-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61f24-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="61f24-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f24-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="61f24-107">DESCRIPTION</span></span>
<span data-ttu-id="61f24-108">Az **Add-AzureRmApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="61f24-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="61f24-109">Az IP-konfigurációk tartalmazzák azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="61f24-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="61f24-110">Példák</span><span class="sxs-lookup"><span data-stu-id="61f24-110">EXAMPLES</span></span>

### <span data-ttu-id="61f24-111">1. példa: virtuális hálózati konfiguráció felvétele az alkalmazás-átjáróba</span><span class="sxs-lookup"><span data-stu-id="61f24-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="61f24-112">Az első parancs virtuális hálózatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="61f24-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="61f24-113">A második parancs a korábban létrehozott virtuális hálózat segítségével hoz létre alhálózatot.</span><span class="sxs-lookup"><span data-stu-id="61f24-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="61f24-114">A harmadik parancs beolvassa az Application Gatewayt, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="61f24-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="61f24-115">A Fouth parancs hozzáadja az IP-konfigurációt a $AppGwban tárolt alkalmazási átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="61f24-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="61f24-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61f24-116">PARAMETERS</span></span>

### <span data-ttu-id="61f24-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f24-117">-ApplicationGateway</span></span>
<span data-ttu-id="61f24-118">Annak az alkalmazásnak az átjáróját adja meg, amelyre a parancsmag IP-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="61f24-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="61f24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f24-119">-DefaultProfile</span></span>
<span data-ttu-id="61f24-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61f24-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f24-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61f24-121">-Name</span></span>
<span data-ttu-id="61f24-122">A hozzáadni kívánt IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61f24-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="61f24-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="61f24-123">-Subnet</span></span>
<span data-ttu-id="61f24-124">Az alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="61f24-124">Specifies a subnet.</span></span>
<span data-ttu-id="61f24-125">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="61f24-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="61f24-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="61f24-126">-SubnetId</span></span>
<span data-ttu-id="61f24-127">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="61f24-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="61f24-128">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="61f24-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="61f24-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f24-129">CommonParameters</span></span>
<span data-ttu-id="61f24-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61f24-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f24-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f24-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f24-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61f24-132">INPUTS</span></span>

### <span data-ttu-id="61f24-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f24-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="61f24-134">Paraméterek: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="61f24-134">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="61f24-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61f24-135">OUTPUTS</span></span>

### <span data-ttu-id="61f24-136">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="61f24-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="61f24-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61f24-137">NOTES</span></span>

## <span data-ttu-id="61f24-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61f24-138">RELATED LINKS</span></span>

[<span data-ttu-id="61f24-139">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f24-139">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="61f24-140">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f24-140">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="61f24-141">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f24-141">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="61f24-142">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="61f24-142">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


