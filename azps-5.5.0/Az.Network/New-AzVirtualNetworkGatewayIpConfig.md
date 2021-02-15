---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202703"
---
# <span data-ttu-id="f0bc6-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0bc6-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f0bc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="f0bc6-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="f0bc6-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="f0bc6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f0bc6-104">SYNTAX</span></span>

### <span data-ttu-id="f0bc6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0bc6-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0bc6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f0bc6-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0bc6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f0bc6-107">DESCRIPTION</span></span>
<span data-ttu-id="f0bc6-108">A **New-AzVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel van hozzárendelve egy virtuális hálózati átjáróhoz alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="f0bc6-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f0bc6-109">EXAMPLES</span></span>

### <span data-ttu-id="f0bc6-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="f0bc6-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="f0bc6-111">Konfigurál egy virtuális hálózati átjárót nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="f0bc6-112">Az $myGWsubnet változót a virtuális hálózat létrehozásához használni kívánt virtuális hálózat "GatewaySubnet" átjárója **Get-AzVirtualNetworkSubnetConfig** parancsmagját használva lehet beszerezni.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="f0bc6-113">A $myGWpip a **New-AzPublicIpAddress** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="f0bc6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0bc6-114">PARAMETERS</span></span>

### <span data-ttu-id="f0bc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0bc6-115">-DefaultProfile</span></span>
<span data-ttu-id="f0bc6-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0bc6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f0bc6-117">-Name</span></span>
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

### <span data-ttu-id="f0bc6-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0bc6-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="f0bc6-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f0bc6-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="f0bc6-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f0bc6-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="f0bc6-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="f0bc6-121">-Subnet</span></span>
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

### <span data-ttu-id="f0bc6-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f0bc6-122">-SubnetId</span></span>
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

### <span data-ttu-id="f0bc6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0bc6-123">CommonParameters</span></span>
<span data-ttu-id="f0bc6-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0bc6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0bc6-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0bc6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0bc6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0bc6-126">INPUTS</span></span>

### <span data-ttu-id="f0bc6-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="f0bc6-127">None</span></span>

## <span data-ttu-id="f0bc6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0bc6-128">OUTPUTS</span></span>

### <span data-ttu-id="f0bc6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0bc6-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="f0bc6-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f0bc6-130">NOTES</span></span>

## <span data-ttu-id="f0bc6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0bc6-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0bc6-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0bc6-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="f0bc6-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f0bc6-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
