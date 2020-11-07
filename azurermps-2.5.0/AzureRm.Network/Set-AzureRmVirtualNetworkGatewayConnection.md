---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849930"
---
# <span data-ttu-id="2f4f7-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2f4f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4f7-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f4f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f4f7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f4f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2f4f7-106">A **set-AzureRmVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="2f4f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="2f4f7-108">1:</span><span class="sxs-lookup"><span data-stu-id="2f4f7-108">1:</span></span>
```

```

## <span data-ttu-id="2f4f7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f4f7-109">PARAMETERS</span></span>

### <span data-ttu-id="2f4f7-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f4f7-110">-AsJob</span></span>
<span data-ttu-id="2f4f7-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2f4f7-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4f7-112">-DefaultProfile</span></span>
<span data-ttu-id="2f4f7-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f4f7-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="2f4f7-114">-EnableBgp</span></span>
<span data-ttu-id="2f4f7-115">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="2f4f7-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2f4f7-116">-Force</span></span>
<span data-ttu-id="2f4f7-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="2f4f7-118">-IpsecPolicies</span></span>
<span data-ttu-id="2f4f7-119">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="2f4f7-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="2f4f7-121">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="2f4f7-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="2f4f7-123">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f4f7-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f4f7-124">-Confirm</span></span>
<span data-ttu-id="2f4f7-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f4f7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f4f7-126">-WhatIf</span></span>
<span data-ttu-id="2f4f7-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f4f7-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f4f7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f4f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4f7-129">CommonParameters</span></span>
<span data-ttu-id="2f4f7-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f4f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4f7-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f4f7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4f7-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4f7-132">INPUTS</span></span>

### <span data-ttu-id="2f4f7-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="2f4f7-134">A ' VirtualNetworkGatewayConnection ' paraméter az "PSVirtualNetworkGatewayConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2f4f7-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="2f4f7-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f4f7-135">OUTPUTS</span></span>

### <span data-ttu-id="2f4f7-136">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="2f4f7-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f4f7-137">NOTES</span></span>

## <span data-ttu-id="2f4f7-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f4f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="2f4f7-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2f4f7-140">Új – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="2f4f7-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2f4f7-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


