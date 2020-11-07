---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: d3a309d99dff493e2440618d87c20b1a543e2ed9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848698"
---
# <span data-ttu-id="4fc78-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4fc78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fc78-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc78-103">Módosítja az alkalmazás-átjáró IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="4fc78-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fc78-104">SYNTAX</span></span>

### <span data-ttu-id="4fc78-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc78-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fc78-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fc78-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fc78-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fc78-107">DESCRIPTION</span></span>
<span data-ttu-id="4fc78-108">A **set-AzureRmApplicationGatewayIPConfiguration** parancsmag módosította az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="4fc78-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="4fc78-109">Az IP-konfiguráció azt az alhálózatot tartalmazza, amelyben egy alkalmazás-átjáró van telepítve.</span><span class="sxs-lookup"><span data-stu-id="4fc78-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="4fc78-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4fc78-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc78-111">Példa 1: IP-konfiguráció célérték-állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="4fc78-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="4fc78-112">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $VNet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4fc78-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="4fc78-113">A második parancs beolvassa a Subnet01 nevű alhálózat-konfigurációt a $VNet használatával, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4fc78-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="4fc78-114">A harmadik parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4fc78-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4fc78-115">A Forth parancs az $AppGw-on tárolt alkalmazás-átjáró IP-konfigurációját a $Subnet tárolt alhálózat-konfigurációra állítja be.</span><span class="sxs-lookup"><span data-stu-id="4fc78-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="4fc78-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fc78-116">PARAMETERS</span></span>

### <span data-ttu-id="4fc78-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc78-117">-ApplicationGateway</span></span>
<span data-ttu-id="4fc78-118">Azt az Application Gateway-objektumot adja meg, amelyhez a parancsmag IP-konfigurációt társít.</span><span class="sxs-lookup"><span data-stu-id="4fc78-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="4fc78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc78-119">-DefaultProfile</span></span>
<span data-ttu-id="4fc78-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fc78-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc78-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fc78-121">-Name</span></span>
<span data-ttu-id="4fc78-122">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fc78-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="4fc78-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="4fc78-123">-Subnet</span></span>
<span data-ttu-id="4fc78-124">Az alhálózatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fc78-124">Specifies the subnet.</span></span>
<span data-ttu-id="4fc78-125">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="4fc78-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc78-126">– NetI</span><span class="sxs-lookup"><span data-stu-id="4fc78-126">-SubnetId</span></span>
<span data-ttu-id="4fc78-127">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4fc78-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="4fc78-128">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="4fc78-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc78-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc78-129">CommonParameters</span></span>
<span data-ttu-id="4fc78-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fc78-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc78-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc78-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc78-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc78-132">INPUTS</span></span>

### <span data-ttu-id="4fc78-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4fc78-133">System.String</span></span>

## <span data-ttu-id="4fc78-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fc78-134">OUTPUTS</span></span>

### <span data-ttu-id="4fc78-135">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fc78-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fc78-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fc78-136">NOTES</span></span>

## <span data-ttu-id="4fc78-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fc78-137">RELATED LINKS</span></span>

[<span data-ttu-id="4fc78-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc78-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc78-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc78-141">Új – AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4fc78-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc78-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


