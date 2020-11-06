---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494834"
---
# <span data-ttu-id="69769-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="69769-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="69769-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69769-102">SYNOPSIS</span></span>
<span data-ttu-id="69769-103">Útvonalat hoz létre az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="69769-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69769-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69769-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69769-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69769-105">DESCRIPTION</span></span>
<span data-ttu-id="69769-106">A **New-AzureRmRouteConfig** parancsmag az Azure Route-táblázatok útvonalát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="69769-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="69769-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69769-107">EXAMPLES</span></span>

### <span data-ttu-id="69769-108">1. példa: útvonal létrehozása</span><span class="sxs-lookup"><span data-stu-id="69769-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="69769-109">Az első parancs létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="69769-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="69769-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="69769-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="69769-111">A második parancs az útvonal tulajdonságait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="69769-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="69769-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69769-112">PARAMETERS</span></span>

### <span data-ttu-id="69769-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="69769-113">-AddressPrefix</span></span>
<span data-ttu-id="69769-114">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="69769-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="69769-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69769-115">-Name</span></span>
<span data-ttu-id="69769-116">Az útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69769-116">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="69769-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="69769-117">-NextHopIpAddress</span></span>
<span data-ttu-id="69769-118">A Azurevirtual-hálózathoz hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69769-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="69769-119">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="69769-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="69769-120">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69769-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="69769-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="69769-121">-NextHopType</span></span>
<span data-ttu-id="69769-122">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="69769-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="69769-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="69769-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69769-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="69769-124">Internet.</span></span>
<span data-ttu-id="69769-125">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="69769-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="69769-126">Nincs.</span><span class="sxs-lookup"><span data-stu-id="69769-126">None.</span></span>
<span data-ttu-id="69769-127">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="69769-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="69769-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="69769-128">VirtualAppliance.</span></span>
<span data-ttu-id="69769-129">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="69769-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="69769-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="69769-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="69769-131">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="69769-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="69769-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="69769-132">VnetLocal.</span></span>
<span data-ttu-id="69769-133">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="69769-133">The local virtual network.</span></span>
<span data-ttu-id="69769-134">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="69769-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69769-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69769-135">-DefaultProfile</span></span>
<span data-ttu-id="69769-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="69769-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69769-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69769-137">CommonParameters</span></span>
<span data-ttu-id="69769-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69769-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69769-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69769-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69769-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69769-140">INPUTS</span></span>

## <span data-ttu-id="69769-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69769-141">OUTPUTS</span></span>

### <span data-ttu-id="69769-142">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="69769-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="69769-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69769-143">NOTES</span></span>

## <span data-ttu-id="69769-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69769-144">RELATED LINKS</span></span>

[<span data-ttu-id="69769-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="69769-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="69769-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="69769-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="69769-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="69769-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="69769-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="69769-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


