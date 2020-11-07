---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 8793da5f73ba1b6891d3522c171c167753188c1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837154"
---
# <span data-ttu-id="be6ec-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="be6ec-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="be6ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="be6ec-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="be6ec-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="be6ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be6ec-104">SYNTAX</span></span>

### <span data-ttu-id="be6ec-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="be6ec-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be6ec-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="be6ec-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be6ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be6ec-107">DESCRIPTION</span></span>
<span data-ttu-id="be6ec-108">A **New-AzVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel rendelkező virtuális hálózati átjáróhoz van társítva az alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="be6ec-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="be6ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be6ec-109">EXAMPLES</span></span>

### <span data-ttu-id="be6ec-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="be6ec-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="be6ec-111">Virtuális hálózati átjárót konfigurál egy nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="be6ec-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="be6ec-112">A $myGWsubnet változót a **Get-AzVirtualNetworkSubnetConfig** parancsmag használatával kapjuk a virtuális hálózati átjárót létrehozni kívánt virtuális hálózat "GatewaySubnet".</span><span class="sxs-lookup"><span data-stu-id="be6ec-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="be6ec-113">A $myGWpip változó a **New-AzPublicIpAddress** parancsmag használatával szerezhető be.</span><span class="sxs-lookup"><span data-stu-id="be6ec-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="be6ec-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be6ec-114">PARAMETERS</span></span>

### <span data-ttu-id="be6ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be6ec-115">-DefaultProfile</span></span>
<span data-ttu-id="be6ec-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be6ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be6ec-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be6ec-117">-Name</span></span>
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

### <span data-ttu-id="be6ec-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="be6ec-118">-PrivateIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6ec-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be6ec-119">-PublicIpAddress</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be6ec-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="be6ec-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="be6ec-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="be6ec-121">-Subnet</span></span>
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

### <span data-ttu-id="be6ec-122">– NetI</span><span class="sxs-lookup"><span data-stu-id="be6ec-122">-SubnetId</span></span>
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

### <span data-ttu-id="be6ec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be6ec-123">CommonParameters</span></span>
<span data-ttu-id="be6ec-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be6ec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be6ec-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be6ec-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be6ec-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be6ec-126">INPUTS</span></span>

### <span data-ttu-id="be6ec-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="be6ec-127">None</span></span>

## <span data-ttu-id="be6ec-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be6ec-128">OUTPUTS</span></span>

### <span data-ttu-id="be6ec-129">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="be6ec-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="be6ec-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be6ec-130">NOTES</span></span>

## <span data-ttu-id="be6ec-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be6ec-131">RELATED LINKS</span></span>

[<span data-ttu-id="be6ec-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="be6ec-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="be6ec-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="be6ec-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
