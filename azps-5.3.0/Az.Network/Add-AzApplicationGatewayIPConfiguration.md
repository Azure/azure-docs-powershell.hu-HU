---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 9c8730c1a6430d98567f880e101497ecc1be432d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380266"
---
# <span data-ttu-id="4ddb0-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ddb0-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="4ddb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ddb0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddb0-103">IP-konfigurációt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="4ddb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4ddb0-104">SYNTAX</span></span>

### <span data-ttu-id="4ddb0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ddb0-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ddb0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4ddb0-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ddb0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4ddb0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ddb0-108">Az **Add-AzApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt ad egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="4ddb0-109">Az IP-konfigurációk tartalmazzák azt az alhálózatot, amelyen az alkalmazás-átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="4ddb0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4ddb0-110">EXAMPLES</span></span>

### <span data-ttu-id="4ddb0-111">1. példa: Virtuális hálózati konfiguráció hozzáadása alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="4ddb0-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="4ddb0-112">Az első parancs egy virtuális hálózatot kap.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-112">The first command gets a virtual network.</span></span>
<span data-ttu-id="4ddb0-113">A második parancs egy alhálózatot kap a korábban létrehozott virtuális hálózat használatával.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-113">The second command gets a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="4ddb0-114">A harmadik parancs az alkalmazás átjáróját a $AppGw tárolja.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4ddb0-115">A negyedik parancs hozzáadja az IP-konfigurációt a $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-115">The fourth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4ddb0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ddb0-116">PARAMETERS</span></span>

### <span data-ttu-id="4ddb0-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ddb0-117">-ApplicationGateway</span></span>
<span data-ttu-id="4ddb0-118">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag IP-konfigurációt ad.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="4ddb0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ddb0-119">-DefaultProfile</span></span>
<span data-ttu-id="4ddb0-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ddb0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ddb0-121">-Name</span></span>
<span data-ttu-id="4ddb0-122">A hozzáadni szükséges IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="4ddb0-123">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="4ddb0-123">-Subnet</span></span>
<span data-ttu-id="4ddb0-124">Egy alhálózatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-124">Specifies a subnet.</span></span>
<span data-ttu-id="4ddb0-125">Ez az az alhálózat, amelyben az alkalmazás átjárója telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4ddb0-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4ddb0-126">-SubnetId</span></span>
<span data-ttu-id="4ddb0-127">Egy alhálózati azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="4ddb0-128">Ez az az alhálózat, amelyben az alkalmazás átjárója telepítve van.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="4ddb0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddb0-129">CommonParameters</span></span>
<span data-ttu-id="4ddb0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ddb0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddb0-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddb0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddb0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ddb0-132">INPUTS</span></span>

### <span data-ttu-id="4ddb0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ddb0-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ddb0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ddb0-134">OUTPUTS</span></span>

### <span data-ttu-id="4ddb0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ddb0-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ddb0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4ddb0-136">NOTES</span></span>

## <span data-ttu-id="4ddb0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ddb0-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ddb0-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ddb0-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ddb0-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ddb0-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ddb0-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ddb0-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4ddb0-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ddb0-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


