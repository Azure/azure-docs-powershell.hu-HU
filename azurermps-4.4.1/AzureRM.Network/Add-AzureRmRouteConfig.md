---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501759"
---
# <span data-ttu-id="72c1c-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72c1c-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="72c1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="72c1c-103">Útvonalat ad az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="72c1c-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72c1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72c1c-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72c1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="72c1c-106">Az **Add-AzureRmRouteConfig** parancsmag az Azure Route-táblázathoz ad hozzá útvonalat.</span><span class="sxs-lookup"><span data-stu-id="72c1c-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="72c1c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="72c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="72c1c-108">1. példa: útvonal felvétele az útválasztási táblázatba</span><span class="sxs-lookup"><span data-stu-id="72c1c-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="72c1c-109">Az első parancs az Get-AzureRmRouteTable parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="72c1c-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="72c1c-110">A parancs a táblázatot a $RouteTable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="72c1c-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="72c1c-111">A második parancs hozzáadja a Route13 nevű útvonalat a $RouteTableban tárolt útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="72c1c-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="72c1c-112">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="72c1c-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="72c1c-113">2. példa: útvonal hozzáadása az útválasztási táblázathoz a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="72c1c-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="72c1c-114">Ez a parancs a **Get-AzureRmRouteTable** segítségével a RouteTable01 nevű útválasztási táblázatot kapja</span><span class="sxs-lookup"><span data-stu-id="72c1c-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="72c1c-115">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="72c1c-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="72c1c-116">Az aktuális parancsmag hozzáadja a Route02 nevű útvonalat, majd átadja az eredményt a **set-AzureRmRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="72c1c-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="72c1c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72c1c-117">PARAMETERS</span></span>

### <span data-ttu-id="72c1c-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="72c1c-118">-AddressPrefix</span></span>
<span data-ttu-id="72c1c-119">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="72c1c-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="72c1c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72c1c-120">-Name</span></span>
<span data-ttu-id="72c1c-121">Annak az útvonalnak a neve, amelyet fel szeretne venni az útvonal táblájába.</span><span class="sxs-lookup"><span data-stu-id="72c1c-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="72c1c-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="72c1c-122">-NextHopIpAddress</span></span>
<span data-ttu-id="72c1c-123">Az Azure virtuális hálózatához hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72c1c-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="72c1c-124">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="72c1c-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="72c1c-125">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="72c1c-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="72c1c-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="72c1c-126">-NextHopType</span></span>
<span data-ttu-id="72c1c-127">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="72c1c-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="72c1c-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="72c1c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="72c1c-129">Internet.</span><span class="sxs-lookup"><span data-stu-id="72c1c-129">Internet.</span></span>
<span data-ttu-id="72c1c-130">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="72c1c-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="72c1c-131">Nincs.</span><span class="sxs-lookup"><span data-stu-id="72c1c-131">None.</span></span>
<span data-ttu-id="72c1c-132">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="72c1c-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="72c1c-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="72c1c-133">VirtualAppliance.</span></span>
<span data-ttu-id="72c1c-134">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="72c1c-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="72c1c-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="72c1c-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="72c1c-136">Az Azure Server-to-Server virtuális magánhálózati átjárója.</span><span class="sxs-lookup"><span data-stu-id="72c1c-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="72c1c-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="72c1c-137">VnetLocal.</span></span>
<span data-ttu-id="72c1c-138">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="72c1c-138">The local virtual network.</span></span>
<span data-ttu-id="72c1c-139">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="72c1c-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="72c1c-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="72c1c-140">-RouteTable</span></span>
<span data-ttu-id="72c1c-141">Annak az útvonalnak a táblázatát adja meg, amelyre a parancsmag hozzáadja az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="72c1c-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72c1c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c1c-142">-DefaultProfile</span></span>
<span data-ttu-id="72c1c-143">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72c1c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72c1c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c1c-144">CommonParameters</span></span>
<span data-ttu-id="72c1c-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72c1c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c1c-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c1c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c1c-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72c1c-147">INPUTS</span></span>

### <span data-ttu-id="72c1c-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="72c1c-148">PSRouteTable</span></span>
<span data-ttu-id="72c1c-149">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="72c1c-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="72c1c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72c1c-150">OUTPUTS</span></span>

### <span data-ttu-id="72c1c-151">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="72c1c-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="72c1c-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72c1c-152">NOTES</span></span>

## <span data-ttu-id="72c1c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72c1c-153">RELATED LINKS</span></span>

[<span data-ttu-id="72c1c-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72c1c-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="72c1c-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72c1c-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="72c1c-156">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72c1c-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="72c1c-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72c1c-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="72c1c-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="72c1c-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="72c1c-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="72c1c-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


