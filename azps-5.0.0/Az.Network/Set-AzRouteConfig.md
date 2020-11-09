---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: ca7335abfd8fe2dc9591dcb7d96fb6ca71dda4fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303578"
---
# <span data-ttu-id="0ece3-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0ece3-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="0ece3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ece3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ece3-103">Az útválasztási táblázat útválasztási konfigurációjának frissítése.</span><span class="sxs-lookup"><span data-stu-id="0ece3-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="0ece3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ece3-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ece3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ece3-105">DESCRIPTION</span></span>
<span data-ttu-id="0ece3-106">A **set-AzRouteConfig** parancsmag frissíti az útválasztási táblázat útvonal-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="0ece3-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="0ece3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ece3-107">EXAMPLES</span></span>

### <span data-ttu-id="0ece3-108">Példa 1: útvonal módosítása</span><span class="sxs-lookup"><span data-stu-id="0ece3-108">Example 1: Modify a route</span></span>
```powershell
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="0ece3-109">Ez a parancs a RouteTable01 nevű útválasztási táblázatot a Get-AzRouteTable parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="0ece3-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="0ece3-110">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="0ece3-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0ece3-111">Az aktuális parancsmag módosítja a Route02 nevű útvonalat, majd átadja az eredményt a **set-AzRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="0ece3-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="0ece3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ece3-112">PARAMETERS</span></span>

### <span data-ttu-id="0ece3-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0ece3-113">-AddressPrefix</span></span>
<span data-ttu-id="0ece3-114">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="0ece3-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ece3-115">-DefaultProfile</span></span>
<span data-ttu-id="0ece3-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ece3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ece3-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ece3-117">-Name</span></span>
<span data-ttu-id="0ece3-118">A parancsmag által módosított útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ece3-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0ece3-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="0ece3-119">-NextHopIpAddress</span></span>
<span data-ttu-id="0ece3-120">Az Azure virtuális hálózatához hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ece3-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="0ece3-121">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="0ece3-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="0ece3-122">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ece3-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="0ece3-123">-NextHopType</span></span>
<span data-ttu-id="0ece3-124">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="0ece3-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="0ece3-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0ece3-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0ece3-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="0ece3-126">Internet.</span></span>
<span data-ttu-id="0ece3-127">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="0ece3-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="0ece3-128">Nincs.</span><span class="sxs-lookup"><span data-stu-id="0ece3-128">None.</span></span>
<span data-ttu-id="0ece3-129">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="0ece3-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="0ece3-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="0ece3-130">VirtualAppliance.</span></span>
<span data-ttu-id="0ece3-131">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="0ece3-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="0ece3-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="0ece3-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="0ece3-133">Egy Azureserver-to-Server Virtual Private hálózati átjáró.</span><span class="sxs-lookup"><span data-stu-id="0ece3-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="0ece3-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="0ece3-134">VnetLocal.</span></span>
<span data-ttu-id="0ece3-135">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="0ece3-135">The local virtual network.</span></span>
<span data-ttu-id="0ece3-136">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="0ece3-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="0ece3-137">-RouteTable</span></span>
<span data-ttu-id="0ece3-138">Annak az útvonalnak a táblázatát adja meg, amelyen az útvonal van társítva.</span><span class="sxs-lookup"><span data-stu-id="0ece3-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ece3-139">-Confirm</span></span>
<span data-ttu-id="0ece3-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ece3-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ece3-141">-WhatIf</span></span>
<span data-ttu-id="0ece3-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ece3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ece3-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ece3-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ece3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ece3-144">CommonParameters</span></span>
<span data-ttu-id="0ece3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ece3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ece3-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ece3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ece3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ece3-147">INPUTS</span></span>

### <span data-ttu-id="0ece3-148">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0ece3-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="0ece3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0ece3-149">System.String</span></span>

## <span data-ttu-id="0ece3-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ece3-150">OUTPUTS</span></span>

### <span data-ttu-id="0ece3-151">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="0ece3-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="0ece3-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ece3-152">NOTES</span></span>

## <span data-ttu-id="0ece3-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ece3-153">RELATED LINKS</span></span>

[<span data-ttu-id="0ece3-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0ece3-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="0ece3-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0ece3-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="0ece3-156">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0ece3-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="0ece3-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="0ece3-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


