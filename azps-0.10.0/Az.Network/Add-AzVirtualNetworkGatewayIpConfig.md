---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841797"
---
# <span data-ttu-id="46f3e-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="46f3e-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="46f3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="46f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="46f3e-103">IP-konfigurációt ad hozzá egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="46f3e-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="46f3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="46f3e-104">SYNTAX</span></span>

### <span data-ttu-id="46f3e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="46f3e-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46f3e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="46f3e-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46f3e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="46f3e-107">DESCRIPTION</span></span>
<span data-ttu-id="46f3e-108">Az **Add-AzVirtualNetworkGatewayIpConfig** parancsmag IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="46f3e-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="46f3e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="46f3e-109">EXAMPLES</span></span>

### <span data-ttu-id="46f3e-110">1:</span><span class="sxs-lookup"><span data-stu-id="46f3e-110">1:</span></span>
```

```

## <span data-ttu-id="46f3e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="46f3e-111">PARAMETERS</span></span>

### <span data-ttu-id="46f3e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f3e-112">-DefaultProfile</span></span>
<span data-ttu-id="46f3e-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="46f3e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f3e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="46f3e-114">-Name</span></span>
<span data-ttu-id="46f3e-115">A hozzáadni kívánt átjáró IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="46f3e-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="46f3e-116">-PrivateIpAddress</span></span>
<span data-ttu-id="46f3e-117">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="46f3e-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="46f3e-118">-PublicIpAddress</span></span>
<span data-ttu-id="46f3e-119">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="46f3e-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="46f3e-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="46f3e-120">-PublicIpAddressId</span></span>
<span data-ttu-id="46f3e-121">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="46f3e-122">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="46f3e-122">-Subnet</span></span>
<span data-ttu-id="46f3e-123">Egy **PSSubnet** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="46f3e-124">– NetI</span><span class="sxs-lookup"><span data-stu-id="46f3e-124">-SubnetId</span></span>
<span data-ttu-id="46f3e-125">Az alhálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="46f3e-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46f3e-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="46f3e-127">Egy **PSVirtualNetworkGateway** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="46f3e-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="46f3e-128">Ez a parancsmag módosítja a megadott **PSVirtualNetworkGateway** objektumot.</span><span class="sxs-lookup"><span data-stu-id="46f3e-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="46f3e-129">A **PSVirtualNetworkGateway** -objektumok a Get-AzVirtualNetworkGateway parancsmag használatával is beolvashatók.</span><span class="sxs-lookup"><span data-stu-id="46f3e-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="46f3e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="46f3e-130">-Confirm</span></span>
<span data-ttu-id="46f3e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="46f3e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46f3e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46f3e-132">-WhatIf</span></span>
<span data-ttu-id="46f3e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="46f3e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46f3e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="46f3e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46f3e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f3e-135">CommonParameters</span></span>
<span data-ttu-id="46f3e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="46f3e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f3e-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f3e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f3e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="46f3e-138">INPUTS</span></span>

### <span data-ttu-id="46f3e-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46f3e-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="46f3e-140">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="46f3e-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="46f3e-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="46f3e-141">OUTPUTS</span></span>

### <span data-ttu-id="46f3e-142">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46f3e-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="46f3e-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="46f3e-143">NOTES</span></span>

## <span data-ttu-id="46f3e-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="46f3e-144">RELATED LINKS</span></span>

[<span data-ttu-id="46f3e-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="46f3e-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="46f3e-146">Új – AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="46f3e-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="46f3e-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="46f3e-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


