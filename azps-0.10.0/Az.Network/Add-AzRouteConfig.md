---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 1afd855be89f83e9591bbd180b1357e1b03952eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841802"
---
# <span data-ttu-id="76e22-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76e22-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="76e22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76e22-102">SYNOPSIS</span></span>
<span data-ttu-id="76e22-103">Útvonalat ad az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="76e22-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="76e22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76e22-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76e22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76e22-105">DESCRIPTION</span></span>
<span data-ttu-id="76e22-106">Az **Add-AzRouteConfig** parancsmag az Azure Route-táblázathoz ad hozzá útvonalat.</span><span class="sxs-lookup"><span data-stu-id="76e22-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="76e22-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76e22-107">EXAMPLES</span></span>

### <span data-ttu-id="76e22-108">1. példa: útvonal felvétele az útválasztási táblázatba</span><span class="sxs-lookup"><span data-stu-id="76e22-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="76e22-109">Az első parancs az Get-AzRouteTable parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="76e22-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="76e22-110">A parancs a táblázatot a $RouteTable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="76e22-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="76e22-111">A második parancs hozzáadja a Route13 nevű útvonalat a $RouteTableban tárolt útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="76e22-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="76e22-112">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="76e22-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="76e22-113">2. példa: útvonal hozzáadása az útválasztási táblázathoz a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="76e22-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="76e22-114">Ez a parancs a **Get-AzRouteTable** segítségével a RouteTable01 nevű útválasztási táblázatot kapja</span><span class="sxs-lookup"><span data-stu-id="76e22-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="76e22-115">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="76e22-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="76e22-116">Az aktuális parancsmag hozzáadja a Route02 nevű útvonalat, majd átadja az eredményt a **set-AzRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="76e22-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="76e22-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76e22-117">PARAMETERS</span></span>

### <span data-ttu-id="76e22-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="76e22-118">-AddressPrefix</span></span>
<span data-ttu-id="76e22-119">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="76e22-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="76e22-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76e22-120">-DefaultProfile</span></span>
<span data-ttu-id="76e22-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76e22-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76e22-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76e22-122">-Name</span></span>
<span data-ttu-id="76e22-123">Annak az útvonalnak a neve, amelyet fel szeretne venni az útvonal táblájába.</span><span class="sxs-lookup"><span data-stu-id="76e22-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="76e22-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="76e22-124">-NextHopIpAddress</span></span>
<span data-ttu-id="76e22-125">Az Azure virtuális hálózatához hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e22-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="76e22-126">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="76e22-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="76e22-127">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76e22-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="76e22-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="76e22-128">-NextHopType</span></span>
<span data-ttu-id="76e22-129">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="76e22-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="76e22-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76e22-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76e22-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="76e22-131">Internet.</span></span>
<span data-ttu-id="76e22-132">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="76e22-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="76e22-133">Nincs.</span><span class="sxs-lookup"><span data-stu-id="76e22-133">None.</span></span>
<span data-ttu-id="76e22-134">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="76e22-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="76e22-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="76e22-135">VirtualAppliance.</span></span>
<span data-ttu-id="76e22-136">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="76e22-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="76e22-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="76e22-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="76e22-138">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="76e22-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="76e22-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="76e22-139">VnetLocal.</span></span>
<span data-ttu-id="76e22-140">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="76e22-140">The local virtual network.</span></span>
<span data-ttu-id="76e22-141">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="76e22-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="76e22-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="76e22-142">-RouteTable</span></span>
<span data-ttu-id="76e22-143">Annak az útvonalnak a táblázatát adja meg, amelyre a parancsmag hozzáadja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="76e22-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76e22-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="76e22-144">-Confirm</span></span>
<span data-ttu-id="76e22-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="76e22-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76e22-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76e22-146">-WhatIf</span></span>
<span data-ttu-id="76e22-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="76e22-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76e22-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="76e22-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76e22-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76e22-149">CommonParameters</span></span>
<span data-ttu-id="76e22-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76e22-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76e22-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76e22-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76e22-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e22-152">INPUTS</span></span>

### <span data-ttu-id="76e22-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76e22-153">PSRouteTable</span></span>
<span data-ttu-id="76e22-154">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="76e22-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="76e22-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76e22-155">OUTPUTS</span></span>

### <span data-ttu-id="76e22-156">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="76e22-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="76e22-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76e22-157">NOTES</span></span>

## <span data-ttu-id="76e22-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76e22-158">RELATED LINKS</span></span>

[<span data-ttu-id="76e22-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76e22-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="76e22-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76e22-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="76e22-161">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76e22-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="76e22-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76e22-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="76e22-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="76e22-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="76e22-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="76e22-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


