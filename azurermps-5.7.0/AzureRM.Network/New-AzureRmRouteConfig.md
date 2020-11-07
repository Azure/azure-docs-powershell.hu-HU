---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: 98e3bf7f76475b451d3a8f6509e311d9d861f691
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680141"
---
# <span data-ttu-id="007f6-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="007f6-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="007f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="007f6-102">SYNOPSIS</span></span>
<span data-ttu-id="007f6-103">Útvonalat hoz létre az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="007f6-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="007f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="007f6-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-AddressPrefix <String>] [-NextHopType <String>] [-NextHopIpAddress <String>]
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="007f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="007f6-105">DESCRIPTION</span></span>
<span data-ttu-id="007f6-106">A **New-AzureRmRouteConfig** parancsmag az Azure Route-táblázatok útvonalát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="007f6-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="007f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="007f6-107">EXAMPLES</span></span>

### <span data-ttu-id="007f6-108">1. példa: útvonal létrehozása</span><span class="sxs-lookup"><span data-stu-id="007f6-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="007f6-109">Az első parancs létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="007f6-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="007f6-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="007f6-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="007f6-111">A második parancs az útvonal tulajdonságait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="007f6-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="007f6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="007f6-112">PARAMETERS</span></span>

### <span data-ttu-id="007f6-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="007f6-113">-AddressPrefix</span></span>
<span data-ttu-id="007f6-114">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="007f6-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="007f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007f6-115">-DefaultProfile</span></span>
<span data-ttu-id="007f6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="007f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="007f6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="007f6-117">-Name</span></span>
<span data-ttu-id="007f6-118">Az útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="007f6-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="007f6-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="007f6-119">-NextHopIpAddress</span></span>
<span data-ttu-id="007f6-120">A Azurevirtual-hálózathoz hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="007f6-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="007f6-121">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="007f6-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="007f6-122">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="007f6-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="007f6-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="007f6-123">-NextHopType</span></span>
<span data-ttu-id="007f6-124">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="007f6-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="007f6-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="007f6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="007f6-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="007f6-126">Internet.</span></span>
<span data-ttu-id="007f6-127">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="007f6-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="007f6-128">Nincs.</span><span class="sxs-lookup"><span data-stu-id="007f6-128">None.</span></span>
<span data-ttu-id="007f6-129">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="007f6-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="007f6-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="007f6-130">VirtualAppliance.</span></span>
<span data-ttu-id="007f6-131">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="007f6-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="007f6-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="007f6-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="007f6-133">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="007f6-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="007f6-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="007f6-134">VnetLocal.</span></span>
<span data-ttu-id="007f6-135">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="007f6-135">The local virtual network.</span></span>
<span data-ttu-id="007f6-136">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="007f6-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="007f6-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="007f6-137">-Confirm</span></span>
<span data-ttu-id="007f6-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="007f6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="007f6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="007f6-139">-WhatIf</span></span>
<span data-ttu-id="007f6-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="007f6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="007f6-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="007f6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="007f6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007f6-142">CommonParameters</span></span>
<span data-ttu-id="007f6-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="007f6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007f6-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007f6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007f6-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="007f6-145">INPUTS</span></span>

### <span data-ttu-id="007f6-146">Nincs</span><span class="sxs-lookup"><span data-stu-id="007f6-146">None</span></span>
<span data-ttu-id="007f6-147">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="007f6-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="007f6-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="007f6-148">OUTPUTS</span></span>

### <span data-ttu-id="007f6-149">Microsoft. Azure. commands. Network. models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="007f6-149">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="007f6-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="007f6-150">NOTES</span></span>

## <span data-ttu-id="007f6-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="007f6-151">RELATED LINKS</span></span>

[<span data-ttu-id="007f6-152">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="007f6-152">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="007f6-153">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="007f6-153">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="007f6-154">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="007f6-154">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="007f6-155">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="007f6-155">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


