---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C6E65138-CD14-4A54-A901-8E944201F2AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 2e89186c98540886ef46365e3f099292231d148a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470153"
---
# <span data-ttu-id="d6a43-101">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6a43-101">New-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d6a43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6a43-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a43-103">IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="d6a43-103">Creates an IP Configuration for a Virtual Network Gateway</span></span>

## <span data-ttu-id="d6a43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d6a43-104">SYNTAX</span></span>

### <span data-ttu-id="d6a43-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6a43-105">SetByResourceId</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6a43-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d6a43-106">SetByResource</span></span>
```
New-AzVirtualNetworkGatewayIpConfig -Name <String> [-PrivateIpAddress <String>] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6a43-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d6a43-107">DESCRIPTION</span></span>
<span data-ttu-id="d6a43-108">A **New-AzVirtualNetworkGatewayIpConfig** parancsmag létrehoz egy olyan konfigurációt, amely egy (korábban létrehozott) nyilvános IP-címmel van hozzárendelve egy virtuális hálózati átjáróhoz alhálózati azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="d6a43-108">The **New-AzVirtualNetworkGatewayIpConfig** cmdlet creates a configuration assigned to a Virtual Network Gateway with a (previously created) Public IP Address based on Subnet ID.</span></span>

## <span data-ttu-id="d6a43-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d6a43-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a43-110">1: IP-konfiguráció létrehozása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="d6a43-110">1: Create an IP Configuration for a Virtual Network Gateway</span></span>
```
$gwIpConfig = New-AzVirtualNetworkGatewayIpConfig -Name myGWIpConfig -SubnetId $myGWsubnet.Id -PublicIpAddressId $myGWpip.Id
```

<span data-ttu-id="d6a43-111">Konfigurál egy virtuális hálózati átjárót nyilvános IP-címmel.</span><span class="sxs-lookup"><span data-stu-id="d6a43-111">Configures a Virtual Network Gateway with a Public IP Address.</span></span> <span data-ttu-id="d6a43-112">Az $myGWsubnet változót a virtuális hálózat létrehozásához használni kívánt virtuális hálózat "GatewaySubnet" átjárója **Get-AzVirtualNetworkSubnetConfig** parancsmagját használva lehet beszerezni.</span><span class="sxs-lookup"><span data-stu-id="d6a43-112">The variable $myGWsubnet is obtained using the **Get-AzVirtualNetworkSubnetConfig** cmdlet on the "GatewaySubnet" within the Virtual Network you intend to create a Virtual Network Gateway.</span></span> <span data-ttu-id="d6a43-113">A $myGWpip a **New-AzPublicIpAddress** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d6a43-113">The variable $myGWpip is obtained using the **New-AzPublicIpAddress** cmdlet.</span></span>

## <span data-ttu-id="d6a43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6a43-114">PARAMETERS</span></span>

### <span data-ttu-id="d6a43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a43-115">-DefaultProfile</span></span>
<span data-ttu-id="d6a43-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6a43-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6a43-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d6a43-117">-Name</span></span>
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

### <span data-ttu-id="d6a43-118">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6a43-118">-PrivateIpAddress</span></span>
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

### <span data-ttu-id="d6a43-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d6a43-119">-PublicIpAddress</span></span>
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

### <span data-ttu-id="d6a43-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d6a43-120">-PublicIpAddressId</span></span>
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

### <span data-ttu-id="d6a43-121">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="d6a43-121">-Subnet</span></span>
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

### <span data-ttu-id="d6a43-122">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d6a43-122">-SubnetId</span></span>
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

### <span data-ttu-id="d6a43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a43-123">CommonParameters</span></span>
<span data-ttu-id="d6a43-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6a43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a43-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a43-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a43-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6a43-126">INPUTS</span></span>

### <span data-ttu-id="d6a43-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="d6a43-127">None</span></span>

## <span data-ttu-id="d6a43-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6a43-128">OUTPUTS</span></span>

### <span data-ttu-id="d6a43-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6a43-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration</span></span>

## <span data-ttu-id="d6a43-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d6a43-130">NOTES</span></span>

## <span data-ttu-id="d6a43-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6a43-131">RELATED LINKS</span></span>

[<span data-ttu-id="d6a43-132">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6a43-132">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d6a43-133">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d6a43-133">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
