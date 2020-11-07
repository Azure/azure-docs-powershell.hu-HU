---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 1a043b14ef957eed6ac4983c4a30edf6fc72521f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850657"
---
# <span data-ttu-id="451fe-101">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="451fe-101">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="451fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="451fe-102">SYNOPSIS</span></span>
<span data-ttu-id="451fe-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="451fe-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="451fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="451fe-104">SYNTAX</span></span>

### <span data-ttu-id="451fe-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="451fe-105">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="451fe-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="451fe-106">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="451fe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="451fe-107">DESCRIPTION</span></span>
<span data-ttu-id="451fe-108">A **New-AzureRmVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel rendelkező virtuális hálózati átjáróhoz van társítva az alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="451fe-108">The **New-AzureRmVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="451fe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="451fe-109">EXAMPLES</span></span>

### <span data-ttu-id="451fe-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="451fe-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzureRmVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="451fe-111">Virtuális hálózati átjárót konfigurál egy nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="451fe-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="451fe-112">A $myGWsubnet változót a **Get-AzureRmVirtualNetworkSubnetConfig** parancsmag használatával kapjuk a virtuális hálózati átjárót létrehozni kívánt virtuális hálózat "GatewaySubnet".</span><span class="sxs-lookup"><span data-stu-id="451fe-112">The variable $myGWsubnet is obtained using the **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="451fe-113">A $myGWpip változó a **New-AzureRmPublicIpAddress** parancsmag használatával szerezhető be.</span><span class="sxs-lookup"><span data-stu-id="451fe-113">The variable $myGWpip is obtained using the **New-AzureRmPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="451fe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="451fe-114">PARAMETERS</span></span>

### <span data-ttu-id="451fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451fe-115">-DefaultProfile</span></span>
<span data-ttu-id="451fe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="451fe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="451fe-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="451fe-117">-Name</span></span>
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

### <span data-ttu-id="451fe-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="451fe-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="451fe-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="451fe-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="451fe-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="451fe-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="451fe-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="451fe-121">-Subnet</span></span>
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

### <span data-ttu-id="451fe-122">– NetI</span><span class="sxs-lookup"><span data-stu-id="451fe-122">-SubnetId</span></span>
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

### <span data-ttu-id="451fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451fe-123">CommonParameters</span></span>
<span data-ttu-id="451fe-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="451fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451fe-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451fe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451fe-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="451fe-126">INPUTS</span></span>

## <span data-ttu-id="451fe-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="451fe-127">OUTPUTS</span></span>

### <span data-ttu-id="451fe-128">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="451fe-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="451fe-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="451fe-129">NOTES</span></span>

## <span data-ttu-id="451fe-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="451fe-130">RELATED LINKS</span></span>

