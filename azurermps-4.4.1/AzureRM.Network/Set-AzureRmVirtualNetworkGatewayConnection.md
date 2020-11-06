---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494792"
---
# <span data-ttu-id="3ac2c-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3ac2c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ac2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac2c-103">Virtuális hálózati átjáró kapcsolatának beállítása.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ac2c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ac2c-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ac2c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ac2c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac2c-106">A **set-AzureRmVirtualNetworkGatewayConnection** parancsmag a virtuális hálózati átjáró kapcsolatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="3ac2c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ac2c-107">EXAMPLES</span></span>

## <span data-ttu-id="3ac2c-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ac2c-108">PARAMETERS</span></span>

### <span data-ttu-id="3ac2c-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="3ac2c-109">-EnableBgp</span></span>
<span data-ttu-id="3ac2c-110">Szeretné-e, hogy a BGP-munkamenetet egy S2S VPN-alagúton keresztül használja</span><span class="sxs-lookup"><span data-stu-id="3ac2c-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3ac2c-111">-Force</span></span>
<span data-ttu-id="3ac2c-112">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="3ac2c-113">-IpsecPolicies</span></span>
<span data-ttu-id="3ac2c-114">Az IPSec-házirendek listája.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="3ac2c-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="3ac2c-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="3ac2c-116">A S2S-kapcsolatokhoz használható házirend-alapú forgalom kiválasztása</span><span class="sxs-lookup"><span data-stu-id="3ac2c-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="3ac2c-118">Azt a PSVirtualNetworkGatewayConnection-objektumot adja meg, amelyre a parancsmag a virtuális hálózati átjáró kapcsolatának módosítását használja.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3ac2c-119">-Confirm</span></span>
<span data-ttu-id="3ac2c-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac2c-121">-WhatIf</span></span>
<span data-ttu-id="3ac2c-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac2c-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac2c-124">-DefaultProfile</span></span>
<span data-ttu-id="3ac2c-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ac2c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac2c-126">CommonParameters</span></span>
<span data-ttu-id="3ac2c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ac2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac2c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac2c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac2c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ac2c-129">INPUTS</span></span>

### <span data-ttu-id="3ac2c-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="3ac2c-131">A ' VirtualNetworkGatewayConnection ' paraméter az "PSVirtualNetworkGatewayConnection" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3ac2c-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="3ac2c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ac2c-132">OUTPUTS</span></span>

### <span data-ttu-id="3ac2c-133">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="3ac2c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ac2c-134">NOTES</span></span>

## <span data-ttu-id="3ac2c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ac2c-135">RELATED LINKS</span></span>

[<span data-ttu-id="3ac2c-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3ac2c-137">Új – AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="3ac2c-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3ac2c-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


