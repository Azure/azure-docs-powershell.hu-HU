---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 4b157dfd7e7ac47a8161c9f36f9b52bbaaa61869
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493767"
---
# <span data-ttu-id="a605a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a605a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="a605a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a605a-102">SYNOPSIS</span></span>
<span data-ttu-id="a605a-103">IP-konfigurációt ad hozzá egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a605a-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a605a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a605a-104">SYNTAX</span></span>

### <span data-ttu-id="a605a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a605a-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a605a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a605a-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a605a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a605a-107">DESCRIPTION</span></span>
<span data-ttu-id="a605a-108">Az **Add-AzureRmVirtualNetworkGatewayIpConfig** parancsmag IP-konfigurációt ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="a605a-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="a605a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a605a-109">EXAMPLES</span></span>

## <span data-ttu-id="a605a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a605a-110">PARAMETERS</span></span>

### <span data-ttu-id="a605a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a605a-111">-DefaultProfile</span></span>
<span data-ttu-id="a605a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a605a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a605a-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a605a-113">-Name</span></span>
<span data-ttu-id="a605a-114">A hozzáadni kívánt átjáró IP-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-114">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="a605a-115">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a605a-115">-PrivateIpAddress</span></span>
<span data-ttu-id="a605a-116">A magánjellegű IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-116">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="a605a-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a605a-117">-PublicIpAddress</span></span>
<span data-ttu-id="a605a-118">Adja meg a nyilvános IP-címet.</span><span class="sxs-lookup"><span data-stu-id="a605a-118">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="a605a-119">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="a605a-119">-PublicIpAddressId</span></span>
<span data-ttu-id="a605a-120">A nyilvános IP-cím AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-120">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="a605a-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="a605a-121">-Subnet</span></span>
<span data-ttu-id="a605a-122">Egy **PSSubnet** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-122">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="a605a-123">– NetI</span><span class="sxs-lookup"><span data-stu-id="a605a-123">-SubnetId</span></span>
<span data-ttu-id="a605a-124">Az alhálózat AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-124">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="a605a-125">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a605a-125">-VirtualNetworkGateway</span></span>
<span data-ttu-id="a605a-126">Egy **PSVirtualNetworkGateway** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a605a-126">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="a605a-127">Ez a parancsmag módosítja a megadott **PSVirtualNetworkGateway** objektumot.</span><span class="sxs-lookup"><span data-stu-id="a605a-127">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="a605a-128">A **PSVirtualNetworkGateway** -objektumok a Get-AzureRmVirtualNetworkGateway parancsmag használatával is beolvashatók.</span><span class="sxs-lookup"><span data-stu-id="a605a-128">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="a605a-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a605a-129">-Confirm</span></span>
<span data-ttu-id="a605a-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a605a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a605a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a605a-131">-WhatIf</span></span>
<span data-ttu-id="a605a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a605a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a605a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a605a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a605a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a605a-134">CommonParameters</span></span>
<span data-ttu-id="a605a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a605a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a605a-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a605a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a605a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a605a-137">INPUTS</span></span>

### <span data-ttu-id="a605a-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a605a-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="a605a-139">A ' VirtualNetworkGateway ' paraméter az "PSVirtualNetworkGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a605a-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="a605a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a605a-140">OUTPUTS</span></span>

### <span data-ttu-id="a605a-141">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a605a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a605a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a605a-142">NOTES</span></span>

## <span data-ttu-id="a605a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a605a-143">RELATED LINKS</span></span>

[<span data-ttu-id="a605a-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a605a-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a605a-145">Új – AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a605a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="a605a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="a605a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


