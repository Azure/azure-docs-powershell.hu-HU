---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014802"
---
# <span data-ttu-id="943f6-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="943f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="943f6-102">SYNOPSIS</span></span>
<span data-ttu-id="943f6-103">IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="943f6-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="943f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="943f6-104">SYNTAX</span></span>

### <span data-ttu-id="943f6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="943f6-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="943f6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="943f6-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="943f6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="943f6-107">DESCRIPTION</span></span>
<span data-ttu-id="943f6-108">A **New-AzApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="943f6-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="943f6-109">Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="943f6-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="943f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="943f6-110">EXAMPLES</span></span>

### <span data-ttu-id="943f6-111">Példa 1: IP-konfiguráció létrehozása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="943f6-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="943f6-112">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="943f6-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="943f6-113">A második parancs beilleszti annak az alhálózatnak az alhálózatának konfigurációját, amely az előző parancs virtuális hálózata, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="943f6-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="943f6-114">A harmadik parancs az IP-konfigurációt az $Subnet használatával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="943f6-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="943f6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="943f6-115">PARAMETERS</span></span>

### <span data-ttu-id="943f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943f6-116">-DefaultProfile</span></span>
<span data-ttu-id="943f6-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="943f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="943f6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="943f6-118">-Name</span></span>
<span data-ttu-id="943f6-119">A létrehozandó IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="943f6-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="943f6-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="943f6-120">-Subnet</span></span>
<span data-ttu-id="943f6-121">Az alhálózat-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="943f6-121">Specifies the subnet object.</span></span>
<span data-ttu-id="943f6-122">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="943f6-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="943f6-123">– NetI</span><span class="sxs-lookup"><span data-stu-id="943f6-123">-SubnetId</span></span>
<span data-ttu-id="943f6-124">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="943f6-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="943f6-125">Ez az az alhálózat, amelyben az alkalmazás-átjárót telepítették.</span><span class="sxs-lookup"><span data-stu-id="943f6-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="943f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943f6-126">CommonParameters</span></span>
<span data-ttu-id="943f6-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="943f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943f6-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="943f6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943f6-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="943f6-129">INPUTS</span></span>

### <span data-ttu-id="943f6-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="943f6-130">None</span></span>

## <span data-ttu-id="943f6-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="943f6-131">OUTPUTS</span></span>

### <span data-ttu-id="943f6-132">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="943f6-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="943f6-133">NOTES</span></span>

## <span data-ttu-id="943f6-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="943f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="943f6-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="943f6-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="943f6-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="943f6-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="943f6-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


