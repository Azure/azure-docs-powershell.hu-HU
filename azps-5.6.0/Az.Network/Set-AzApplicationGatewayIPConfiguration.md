---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: b8a38bd16fcd08104f678752d03dbc4a6d1f054b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003478"
---
# <span data-ttu-id="5aaaf-101">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-101">Set-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="5aaaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aaaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5aaaf-103">Módosítja egy alkalmazás-átjáró IP-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-103">Modifies an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="5aaaf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5aaaf-104">SYNTAX</span></span>

### <span data-ttu-id="5aaaf-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5aaaf-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aaaf-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5aaaf-106">SetByResource</span></span>
```
Set-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aaaf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5aaaf-107">DESCRIPTION</span></span>
<span data-ttu-id="5aaaf-108">A **Set-AzApplicationGatewayIPConfiguration** parancsmag módosítja az IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-108">The **Set-AzApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="5aaaf-109">Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyen az alkalmazás-átjárót üzembe kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="5aaaf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5aaaf-110">EXAMPLES</span></span>

### <span data-ttu-id="5aaaf-111">1. példa: Alkalmazás-átjáró IP-konfigurációjának frissítése</span><span class="sxs-lookup"><span data-stu-id="5aaaf-111">Example 1: Update an IP configuration for an application gateway</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="5aaaf-112">Az első parancs a VNet01 nevű virtuális hálózatot kapja meg, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $VNet tárolja.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>
<span data-ttu-id="5aaaf-113">A második parancs az Alhálózat01 nevű alhálózati konfigurációt kapja $VNet alhálózati változóban $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="5aaaf-114">A harmadik parancs egy ApplicationGateway01 nevű alkalmazás-átjárót kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5aaaf-115">A "oda" parancs a $AppGw alhálózati konfigurációra állítja be az $Subnet.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="5aaaf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aaaf-116">PARAMETERS</span></span>

### <span data-ttu-id="5aaaf-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aaaf-117">-ApplicationGateway</span></span>
<span data-ttu-id="5aaaf-118">Azt az alkalmazás-átjáróobjektumot adja meg, amellyel ez a parancsmag IP-konfigurációt társít.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

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

### <span data-ttu-id="5aaaf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aaaf-119">-DefaultProfile</span></span>
<span data-ttu-id="5aaaf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aaaf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5aaaf-121">-Name</span></span>
<span data-ttu-id="5aaaf-122">Az IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="5aaaf-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="5aaaf-123">-Subnet</span></span>
<span data-ttu-id="5aaaf-124">Az alhálózatot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-124">Specifies the subnet.</span></span>
<span data-ttu-id="5aaaf-125">Ez az az alhálózat, amelyben az alkalmazás átjárója üzembe van telepítve.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="5aaaf-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5aaaf-126">-SubnetId</span></span>
<span data-ttu-id="5aaaf-127">Az alhálózat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="5aaaf-128">Ez az az alhálózat, amelyben az alkalmazás átjárója üzembe van telepítve.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="5aaaf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aaaf-129">CommonParameters</span></span>
<span data-ttu-id="5aaaf-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aaaf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aaaf-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aaaf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aaaf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5aaaf-132">INPUTS</span></span>

### <span data-ttu-id="5aaaf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aaaf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5aaaf-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5aaaf-134">OUTPUTS</span></span>

### <span data-ttu-id="5aaaf-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5aaaf-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5aaaf-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5aaaf-136">NOTES</span></span>

## <span data-ttu-id="5aaaf-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5aaaf-137">RELATED LINKS</span></span>

[<span data-ttu-id="5aaaf-138">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-138">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5aaaf-139">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-139">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5aaaf-140">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-140">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5aaaf-141">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-141">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="5aaaf-142">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5aaaf-142">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)


