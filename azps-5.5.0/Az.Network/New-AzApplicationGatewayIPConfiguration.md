---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146962"
---
# <span data-ttu-id="b5603-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b5603-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5603-102">SYNOPSIS</span></span>
<span data-ttu-id="b5603-103">Ip-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b5603-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="b5603-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5603-104">SYNTAX</span></span>

### <span data-ttu-id="b5603-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5603-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5603-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b5603-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5603-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5603-107">DESCRIPTION</span></span>
<span data-ttu-id="b5603-108">A **New-AzApplicationGatewayIPConfiguration** parancsmag ip-konfigurációt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b5603-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="b5603-109">Az IP-konfiguráció tartalmazza azt az alhálózatot, amelyen az alkalmazás-átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="b5603-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="b5603-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5603-110">EXAMPLES</span></span>

### <span data-ttu-id="b5603-111">1. példa: IP-konfiguráció létrehozása alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b5603-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="b5603-112">Az első parancs egy VNet01 nevű virtuális hálózatot kap, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="b5603-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="b5603-113">A második parancs annak az alhálózatnak az alhálózati konfigurációját kapja meg, amelyhez az előző parancs virtuális hálózata tartozik, és azt a $Subnet tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5603-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="b5603-114">A harmadik parancs létrehozza az IP-konfigurációt a $Subnet.</span><span class="sxs-lookup"><span data-stu-id="b5603-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="b5603-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5603-115">PARAMETERS</span></span>

### <span data-ttu-id="b5603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5603-116">-DefaultProfile</span></span>
<span data-ttu-id="b5603-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5603-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5603-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b5603-118">-Name</span></span>
<span data-ttu-id="b5603-119">A létrehozni szükséges IP-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5603-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="b5603-120">-Alhálózat</span><span class="sxs-lookup"><span data-stu-id="b5603-120">-Subnet</span></span>
<span data-ttu-id="b5603-121">Az alhálózati objektumot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b5603-121">Specifies the subnet object.</span></span>
<span data-ttu-id="b5603-122">Ez az az alhálózat, amelyben az alkalmazás-átjáró telepítve van.</span><span class="sxs-lookup"><span data-stu-id="b5603-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="b5603-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b5603-123">-SubnetId</span></span>
<span data-ttu-id="b5603-124">Az alhálózat azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5603-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="b5603-125">Ez az az alhálózat, amelyben az alkalmazás-átjárót üzembe kell helyezni.</span><span class="sxs-lookup"><span data-stu-id="b5603-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="b5603-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5603-126">CommonParameters</span></span>
<span data-ttu-id="b5603-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5603-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5603-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5603-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5603-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5603-129">INPUTS</span></span>

### <span data-ttu-id="b5603-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5603-130">None</span></span>

## <span data-ttu-id="b5603-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5603-131">OUTPUTS</span></span>

### <span data-ttu-id="b5603-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b5603-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5603-133">NOTES</span></span>

## <span data-ttu-id="b5603-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5603-134">RELATED LINKS</span></span>

[<span data-ttu-id="b5603-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b5603-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b5603-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b5603-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5603-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


