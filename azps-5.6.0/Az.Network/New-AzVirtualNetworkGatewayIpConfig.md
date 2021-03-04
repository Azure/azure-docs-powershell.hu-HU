---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: cfbfd8df28cf4f0d9c11e654694172b86a549141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924682"
---
# <span data-ttu-id="0aec7-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0aec7-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="0aec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aec7-102">SYNOPSIS</span></span>
<span data-ttu-id="0aec7-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="0aec7-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="0aec7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0aec7-104">SYNTAX</span></span>

### <span data-ttu-id="0aec7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0aec7-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0aec7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0aec7-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0aec7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0aec7-107">DESCRIPTION</span></span>
<span data-ttu-id="0aec7-108">A **New-AzVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel van hozzárendelve egy virtuális hálózati átjáróhoz alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="0aec7-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="0aec7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0aec7-109">EXAMPLES</span></span>

### <span data-ttu-id="0aec7-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="0aec7-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="0aec7-111">Konfigurál egy virtuális hálózati átjárót nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="0aec7-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="0aec7-112">Az $myGWsubnet változót a virtuális hálózat létrehozásához használni kívánt virtuális hálózat "GatewaySubnet" átjárója **Get-AzVirtualNetworkSubnetConfig** parancsmagját használva lehet beszerezni.</span><span class="sxs-lookup"><span data-stu-id="0aec7-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="0aec7-113">A $myGWpip a **New-AzPublicIpAddress** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="0aec7-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="0aec7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aec7-114">PARAMETERS</span></span>

### <span data-ttu-id="0aec7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aec7-115">-DefaultProfile</span></span>
<span data-ttu-id="0aec7-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0aec7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aec7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0aec7-117">-Name</span></span>
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

### <span data-ttu-id="0aec7-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="0aec7-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="0aec7-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0aec7-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="0aec7-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="0aec7-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="0aec7-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="0aec7-121">-Subnet</span></span>
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

### <span data-ttu-id="0aec7-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0aec7-122">-SubnetId</span></span>
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

### <span data-ttu-id="0aec7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aec7-123">CommonParameters</span></span>
<span data-ttu-id="0aec7-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aec7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aec7-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aec7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aec7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0aec7-126">INPUTS</span></span>

### <span data-ttu-id="0aec7-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0aec7-127">None</span></span>

## <span data-ttu-id="0aec7-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0aec7-128">OUTPUTS</span></span>

### <span data-ttu-id="0aec7-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0aec7-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="0aec7-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0aec7-130">NOTES</span></span>

## <span data-ttu-id="0aec7-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0aec7-131">RELATED LINKS</span></span>

[<span data-ttu-id="0aec7-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0aec7-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="0aec7-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="0aec7-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
