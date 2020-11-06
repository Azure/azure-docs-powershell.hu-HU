---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: faf242ea76e5985b0b8544e889fdc3240c87afb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493432"
---
# <span data-ttu-id="9b5ce-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="9b5ce-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="9b5ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9b5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5ce-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="9b5ce-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b5ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9b5ce-104">SYNTAX</span></span>

### <span data-ttu-id="9b5ce-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b5ce-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b5ce-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9b5ce-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b5ce-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9b5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="9b5ce-108">A **New-AzureRmVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel rendelkező virtuális hálózati átjáróhoz van társítva az alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="9b5ce-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9b5ce-109">EXAMPLES</span></span>

### <span data-ttu-id="9b5ce-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="9b5ce-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="9b5ce-111">Virtuális hálózati átjárót konfigurál egy nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="9b5ce-112">A $myGWsubnet változót a **Get-AzureRmVirtualNetworkSubnetConfig** parancsmag használatával kapjuk a virtuális hálózati átjárót létrehozni kívánt virtuális hálózat "GatewaySubnet".</span><span class="sxs-lookup"><span data-stu-id="9b5ce-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="9b5ce-113">A $myGWpip változó a **New-AzureRmPublicIpAddress** parancsmag használatával szerezhető be.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="9b5ce-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9b5ce-114">PARAMETERS</span></span>

### <span data-ttu-id="9b5ce-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9b5ce-115">-Name</span></span>
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

### <span data-ttu-id="9b5ce-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b5ce-116">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="9b5ce-117">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b5ce-117">-PublicIpAddress</span></span>
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

### <span data-ttu-id="9b5ce-118">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="9b5ce-118">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="9b5ce-119">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="9b5ce-119">-Subnet</span></span>
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

### <span data-ttu-id="9b5ce-120">– NetI</span><span class="sxs-lookup"><span data-stu-id="9b5ce-120">-SubnetId</span></span>
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

### <span data-ttu-id="9b5ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5ce-121">-DefaultProfile</span></span>
<span data-ttu-id="9b5ce-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b5ce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b5ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5ce-123">CommonParameters</span></span>
<span data-ttu-id="9b5ce-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9b5ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5ce-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5ce-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5ce-126">INPUTS</span></span>

## <span data-ttu-id="9b5ce-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b5ce-127">OUTPUTS</span></span>

### <span data-ttu-id="9b5ce-128">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b5ce-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="9b5ce-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9b5ce-129">NOTES</span></span>

## <span data-ttu-id="9b5ce-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b5ce-130">RELATED LINKS</span></span>

