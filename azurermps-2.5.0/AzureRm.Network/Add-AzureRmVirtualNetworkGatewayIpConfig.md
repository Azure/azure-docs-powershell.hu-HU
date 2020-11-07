---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850785"
---
# <span data-ttu-id="de369-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de369-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="de369-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de369-102">SYNOPSIS</span></span>
<span data-ttu-id="de369-103">IP-konfigurációt ad hozzá egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="de369-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de369-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de369-104">SYNTAX</span></span>

### <span data-ttu-id="de369-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de369-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de369-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="de369-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de369-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de369-107">DESCRIPTION</span></span>
<span data-ttu-id="de369-108">Az **Add-AzureRmVirtualNetworkGatewayIpConfig** parancsmag IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="de369-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="de369-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de369-109">EXAMPLES</span></span>

### <span data-ttu-id="de369-110">1:</span><span class="sxs-lookup"><span data-stu-id="de369-110">1:</span></span>
```

```

## <span data-ttu-id="de369-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de369-111">PARAMETERS</span></span>

### <span data-ttu-id="de369-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de369-112">-DefaultProfile</span></span>
<span data-ttu-id="de369-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de369-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de369-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de369-114">-Name</span></span>
<span data-ttu-id="de369-115">A hozzáadni kívánt átjáró IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de369-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="de369-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="de369-116">-PrivateIpAddress</span></span>
<span data-ttu-id="de369-117">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="de369-117">Specifies the private IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de369-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="de369-118">-PublicIpAddress</span></span>
<span data-ttu-id="de369-119">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="de369-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de369-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="de369-120">-PublicIpAddressId</span></span>
<span data-ttu-id="de369-121">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de369-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="de369-122">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="de369-122">-Subnet</span></span>
<span data-ttu-id="de369-123">Egy **PSSubnet** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="de369-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="de369-124">– NetI</span><span class="sxs-lookup"><span data-stu-id="de369-124">-SubnetId</span></span>
<span data-ttu-id="de369-125">Az alhálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de369-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="de369-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de369-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="de369-127">Egy **PSVirtualNetworkGateway** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="de369-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="de369-128">Ez a parancsmag módosítja a megadott **PSVirtualNetworkGateway** objektumot.</span><span class="sxs-lookup"><span data-stu-id="de369-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="de369-129">A **PSVirtualNetworkGateway** -objektumok a Get-AzureRmVirtualNetworkGateway parancsmag használatával is beolvashatók.</span><span class="sxs-lookup"><span data-stu-id="de369-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de369-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de369-130">-Confirm</span></span>
<span data-ttu-id="de369-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de369-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de369-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de369-132">-WhatIf</span></span>
<span data-ttu-id="de369-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de369-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de369-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de369-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de369-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de369-135">CommonParameters</span></span>
<span data-ttu-id="de369-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de369-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de369-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de369-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de369-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de369-138">INPUTS</span></span>

### <span data-ttu-id="de369-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de369-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="de369-140">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="de369-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="de369-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de369-141">OUTPUTS</span></span>

### <span data-ttu-id="de369-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de369-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="de369-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de369-143">NOTES</span></span>

## <span data-ttu-id="de369-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de369-144">RELATED LINKS</span></span>

[<span data-ttu-id="de369-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="de369-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="de369-146">Új – AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de369-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="de369-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="de369-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


