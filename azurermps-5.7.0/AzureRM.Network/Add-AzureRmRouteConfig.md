---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: ecd5df4728e963e8bcf4614a6acb554fdbf17788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499792"
---
# <span data-ttu-id="0cd52-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0cd52-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="0cd52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0cd52-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd52-103">Útvonalat ad az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="0cd52-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0cd52-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cd52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0cd52-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd52-106">Az **Add-AzureRmRouteConfig** parancsmag az Azure Route-táblázathoz ad hozzá útvonalat.</span><span class="sxs-lookup"><span data-stu-id="0cd52-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="0cd52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0cd52-107">EXAMPLES</span></span>

### <span data-ttu-id="0cd52-108">1. példa: útvonal felvétele az útválasztási táblázatba</span><span class="sxs-lookup"><span data-stu-id="0cd52-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="0cd52-109">Az első parancs az Get-AzureRmRouteTable parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="0cd52-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="0cd52-110">A parancs a táblázatot a $RouteTable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0cd52-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="0cd52-111">A második parancs hozzáadja a Route13 nevű útvonalat a $RouteTableban tárolt útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="0cd52-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="0cd52-112">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="0cd52-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="0cd52-113">2. példa: útvonal hozzáadása az útválasztási táblázathoz a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="0cd52-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="0cd52-114">Ez a parancs a **Get-AzureRmRouteTable** segítségével a RouteTable01 nevű útválasztási táblázatot kapja</span><span class="sxs-lookup"><span data-stu-id="0cd52-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="0cd52-115">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="0cd52-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0cd52-116">Az aktuális parancsmag hozzáadja a Route02 nevű útvonalat, majd átadja az eredményt a **set-AzureRmRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="0cd52-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="0cd52-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0cd52-117">PARAMETERS</span></span>

### <span data-ttu-id="0cd52-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0cd52-118">-AddressPrefix</span></span>
<span data-ttu-id="0cd52-119">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="0cd52-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="0cd52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd52-120">-DefaultProfile</span></span>
<span data-ttu-id="0cd52-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cd52-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cd52-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0cd52-122">-Name</span></span>
<span data-ttu-id="0cd52-123">Annak az útvonalnak a neve, amelyet fel szeretne venni az útvonal táblájába.</span><span class="sxs-lookup"><span data-stu-id="0cd52-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="0cd52-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="0cd52-124">-NextHopIpAddress</span></span>
<span data-ttu-id="0cd52-125">Az Azure virtuális hálózatához hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0cd52-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="0cd52-126">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="0cd52-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="0cd52-127">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0cd52-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="0cd52-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="0cd52-128">-NextHopType</span></span>
<span data-ttu-id="0cd52-129">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="0cd52-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="0cd52-130">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0cd52-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0cd52-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="0cd52-131">Internet.</span></span>
<span data-ttu-id="0cd52-132">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="0cd52-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="0cd52-133">Nincs.</span><span class="sxs-lookup"><span data-stu-id="0cd52-133">None.</span></span>
<span data-ttu-id="0cd52-134">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="0cd52-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="0cd52-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="0cd52-135">VirtualAppliance.</span></span>
<span data-ttu-id="0cd52-136">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="0cd52-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="0cd52-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0cd52-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="0cd52-138">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="0cd52-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="0cd52-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="0cd52-139">VnetLocal.</span></span>
<span data-ttu-id="0cd52-140">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="0cd52-140">The local virtual network.</span></span>
<span data-ttu-id="0cd52-141">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="0cd52-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="0cd52-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0cd52-142">-RouteTable</span></span>
<span data-ttu-id="0cd52-143">Annak az útvonalnak a táblázatát adja meg, amelyre a parancsmag hozzáadja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="0cd52-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="0cd52-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0cd52-144">-Confirm</span></span>
<span data-ttu-id="0cd52-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0cd52-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cd52-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd52-146">-WhatIf</span></span>
<span data-ttu-id="0cd52-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0cd52-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cd52-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cd52-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cd52-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd52-149">CommonParameters</span></span>
<span data-ttu-id="0cd52-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0cd52-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd52-151">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd52-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd52-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cd52-152">INPUTS</span></span>

### <span data-ttu-id="0cd52-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0cd52-153">PSRouteTable</span></span>
<span data-ttu-id="0cd52-154">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0cd52-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="0cd52-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cd52-155">OUTPUTS</span></span>

### <span data-ttu-id="0cd52-156">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0cd52-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0cd52-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0cd52-157">NOTES</span></span>

## <span data-ttu-id="0cd52-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cd52-158">RELATED LINKS</span></span>

[<span data-ttu-id="0cd52-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0cd52-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="0cd52-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0cd52-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0cd52-161">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0cd52-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="0cd52-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0cd52-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="0cd52-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0cd52-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="0cd52-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0cd52-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


