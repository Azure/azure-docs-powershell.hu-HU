---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: ab528e837f6f2e45db5e68430d973e0d8f019850
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850378"
---
# <span data-ttu-id="72a5f-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72a5f-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="72a5f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="72a5f-103">Útvonalat hoz létre az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="72a5f-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72a5f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72a5f-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72a5f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72a5f-105">DESCRIPTION</span></span>
<span data-ttu-id="72a5f-106">A **New-AzureRmRouteConfig** parancsmag az Azure Route-táblázatok útvonalát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="72a5f-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="72a5f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72a5f-107">EXAMPLES</span></span>

### <span data-ttu-id="72a5f-108">1. példa: útvonal létrehozása</span><span class="sxs-lookup"><span data-stu-id="72a5f-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="72a5f-109">Az első parancs létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72a5f-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="72a5f-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="72a5f-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="72a5f-111">A második parancs az útvonal tulajdonságait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="72a5f-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="72a5f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72a5f-112">PARAMETERS</span></span>

### <span data-ttu-id="72a5f-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72a5f-113">-AddressPrefix</span></span>
<span data-ttu-id="72a5f-114">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="72a5f-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72a5f-115">-DefaultProfile</span></span>
<span data-ttu-id="72a5f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72a5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72a5f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72a5f-117">-Name</span></span>
<span data-ttu-id="72a5f-118">Az útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72a5f-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="72a5f-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="72a5f-119">-NextHopIpAddress</span></span>
<span data-ttu-id="72a5f-120">A Azurevirtual-hálózathoz hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72a5f-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="72a5f-121">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="72a5f-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="72a5f-122">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72a5f-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a5f-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="72a5f-123">-NextHopType</span></span>
<span data-ttu-id="72a5f-124">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="72a5f-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="72a5f-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="72a5f-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72a5f-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="72a5f-126">Internet.</span></span>
<span data-ttu-id="72a5f-127">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="72a5f-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="72a5f-128">Nincs.</span><span class="sxs-lookup"><span data-stu-id="72a5f-128">None.</span></span>
<span data-ttu-id="72a5f-129">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="72a5f-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="72a5f-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="72a5f-130">VirtualAppliance.</span></span>
<span data-ttu-id="72a5f-131">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="72a5f-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="72a5f-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="72a5f-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="72a5f-133">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="72a5f-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="72a5f-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="72a5f-134">VnetLocal.</span></span>
<span data-ttu-id="72a5f-135">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="72a5f-135">The local virtual network.</span></span>
<span data-ttu-id="72a5f-136">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="72a5f-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72a5f-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72a5f-137">-Confirm</span></span>
<span data-ttu-id="72a5f-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72a5f-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a5f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72a5f-139">-WhatIf</span></span>
<span data-ttu-id="72a5f-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72a5f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72a5f-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72a5f-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72a5f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72a5f-142">CommonParameters</span></span>
<span data-ttu-id="72a5f-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72a5f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72a5f-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72a5f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72a5f-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72a5f-145">INPUTS</span></span>

## <span data-ttu-id="72a5f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72a5f-146">OUTPUTS</span></span>

### <span data-ttu-id="72a5f-147">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="72a5f-147">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="72a5f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72a5f-148">NOTES</span></span>

## <span data-ttu-id="72a5f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72a5f-149">RELATED LINKS</span></span>

[<span data-ttu-id="72a5f-150">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72a5f-150">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="72a5f-151">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72a5f-151">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="72a5f-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72a5f-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="72a5f-153">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72a5f-153">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


