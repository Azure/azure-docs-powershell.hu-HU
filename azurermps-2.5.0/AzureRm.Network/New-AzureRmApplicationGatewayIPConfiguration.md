---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 4928df8bd24769e0ebb3eb60728a30a5c55f36fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848145"
---
# <span data-ttu-id="80432-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="80432-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80432-102">SYNOPSIS</span></span>
<span data-ttu-id="80432-103">IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="80432-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80432-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80432-104">SYNTAX</span></span>

### <span data-ttu-id="80432-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="80432-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80432-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="80432-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80432-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="80432-107">DESCRIPTION</span></span>
<span data-ttu-id="80432-108">A **New-AzureRmApplicationGatewayIPConfiguration** parancsmag IP-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="80432-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="80432-109">Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="80432-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="80432-110">Példák</span><span class="sxs-lookup"><span data-stu-id="80432-110">EXAMPLES</span></span>

### <span data-ttu-id="80432-111">Példa 1: IP-konfiguráció létrehozása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="80432-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="80432-112">Az első parancs a VNet01 nevű virtuális hálózatot kapja, amely az ResourceGroup01 nevű erőforráscsoport csoportjába tartozik.</span><span class="sxs-lookup"><span data-stu-id="80432-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="80432-113">A második parancs beilleszti annak az alhálózatnak az alhálózatának konfigurációját, amely az előző parancs virtuális hálózata, és a $Subnet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="80432-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="80432-114">A harmadik parancs az IP-konfigurációt az $Subnet használatával hozza létre.</span><span class="sxs-lookup"><span data-stu-id="80432-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="80432-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80432-115">PARAMETERS</span></span>

### <span data-ttu-id="80432-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80432-116">-DefaultProfile</span></span>
<span data-ttu-id="80432-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80432-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80432-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80432-118">-Name</span></span>
<span data-ttu-id="80432-119">A létrehozandó IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80432-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="80432-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="80432-120">-Subnet</span></span>
<span data-ttu-id="80432-121">Az alhálózat-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="80432-121">Specifies the subnet object.</span></span>
<span data-ttu-id="80432-122">Ez az az alhálózat, amelyben az alkalmazás átjárója van telepítve.</span><span class="sxs-lookup"><span data-stu-id="80432-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="80432-123">– NetI</span><span class="sxs-lookup"><span data-stu-id="80432-123">-SubnetId</span></span>
<span data-ttu-id="80432-124">Az alhálózati azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="80432-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="80432-125">Ez az az alhálózat, amelyben az alkalmazás-átjárót telepítették.</span><span class="sxs-lookup"><span data-stu-id="80432-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="80432-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80432-126">CommonParameters</span></span>
<span data-ttu-id="80432-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80432-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80432-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80432-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80432-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80432-129">INPUTS</span></span>

### <span data-ttu-id="80432-130">System. String</span><span class="sxs-lookup"><span data-stu-id="80432-130">System.String</span></span>

## <span data-ttu-id="80432-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80432-131">OUTPUTS</span></span>

### <span data-ttu-id="80432-132">Microsoft. Azure. commands. Network. models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="80432-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80432-133">NOTES</span></span>

## <span data-ttu-id="80432-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80432-134">RELATED LINKS</span></span>

[<span data-ttu-id="80432-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="80432-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="80432-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="80432-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80432-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


