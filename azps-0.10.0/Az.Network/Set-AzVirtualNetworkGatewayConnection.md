---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843570"
---
# <span data-ttu-id="ca692-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ca692-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca692-102">SYNOPSIS</span></span>
<span data-ttu-id="ca692-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="ca692-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ca692-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca692-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca692-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca692-105">DESCRIPTION</span></span>
<span data-ttu-id="ca692-106">A **set-AzVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca692-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="ca692-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca692-107">EXAMPLES</span></span>

### <span data-ttu-id="ca692-108">1:</span><span class="sxs-lookup"><span data-stu-id="ca692-108">1:</span></span>
```

```

## <span data-ttu-id="ca692-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca692-109">PARAMETERS</span></span>

### <span data-ttu-id="ca692-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca692-110">-AsJob</span></span>
<span data-ttu-id="ca692-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ca692-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca692-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca692-112">-DefaultProfile</span></span>
<span data-ttu-id="ca692-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca692-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca692-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="ca692-114">-EnableBgp</span></span>
<span data-ttu-id="ca692-115">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="ca692-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="ca692-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ca692-116">-Force</span></span>
<span data-ttu-id="ca692-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ca692-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca692-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="ca692-118">-IpsecPolicies</span></span>
<span data-ttu-id="ca692-119">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="ca692-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="ca692-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="ca692-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="ca692-121">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="ca692-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="ca692-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ca692-123">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="ca692-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="ca692-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca692-124">-Confirm</span></span>
<span data-ttu-id="ca692-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca692-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca692-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca692-126">-WhatIf</span></span>
<span data-ttu-id="ca692-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca692-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca692-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca692-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca692-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca692-129">CommonParameters</span></span>
<span data-ttu-id="ca692-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca692-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca692-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca692-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca692-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca692-132">INPUTS</span></span>

### <span data-ttu-id="ca692-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="ca692-134">A ' VirtualNetworkGatewayConnection ' paraméter az "PSVirtualNetworkGatewayConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ca692-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="ca692-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca692-135">OUTPUTS</span></span>

### <span data-ttu-id="ca692-136">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="ca692-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca692-137">NOTES</span></span>

## <span data-ttu-id="ca692-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca692-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca692-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ca692-140">Új – AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="ca692-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ca692-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


