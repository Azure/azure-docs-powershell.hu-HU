---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494803"
---
# <span data-ttu-id="c34d2-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c34d2-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="c34d2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c34d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c34d2-103">Az útvonal cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="c34d2-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c34d2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c34d2-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c34d2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c34d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c34d2-106">A **set-AzureRmRouteConfig** parancsmag az Azure-útvonalak cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="c34d2-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="c34d2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c34d2-107">EXAMPLES</span></span>

### <span data-ttu-id="c34d2-108">Példa 1: útvonal módosítása</span><span class="sxs-lookup"><span data-stu-id="c34d2-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="c34d2-109">Ez a parancs a RouteTable01 nevű útválasztási táblázatot a Get-AzureRmRouteTable parancsmag használatával kapja.</span><span class="sxs-lookup"><span data-stu-id="c34d2-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="c34d2-110">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="c34d2-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c34d2-111">Az aktuális parancsmag módosítja a Route02 nevű útvonalat, majd átadja az eredményt a **set-AzureRmRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="c34d2-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="c34d2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c34d2-112">PARAMETERS</span></span>

### <span data-ttu-id="c34d2-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c34d2-113">-AddressPrefix</span></span>
<span data-ttu-id="c34d2-114">Annak a célhelynek a meghatározása, amelynek a többosztályos tartományok közötti útválasztási (CIDR) formátumában az útvonal érvényes.</span><span class="sxs-lookup"><span data-stu-id="c34d2-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="c34d2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c34d2-115">-Name</span></span>
<span data-ttu-id="c34d2-116">A parancsmag által módosított útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c34d2-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c34d2-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="c34d2-117">-NextHopIpAddress</span></span>
<span data-ttu-id="c34d2-118">Az Azure virtuális hálózatához hozzáadott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c34d2-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="c34d2-119">Ez az útvonal továbbítja a csomagokat a címre.</span><span class="sxs-lookup"><span data-stu-id="c34d2-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="c34d2-120">Csak akkor adja meg ezt a paramétert, ha a *NextHopType* paraméter VirtualAppliance értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c34d2-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="c34d2-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="c34d2-121">-NextHopType</span></span>
<span data-ttu-id="c34d2-122">Azt adja meg, hogy az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="c34d2-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="c34d2-123">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c34d2-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c34d2-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="c34d2-124">Internet.</span></span>
<span data-ttu-id="c34d2-125">Az Azure által biztosított alapértelmezett internetátjáró.</span><span class="sxs-lookup"><span data-stu-id="c34d2-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="c34d2-126">Nincs.</span><span class="sxs-lookup"><span data-stu-id="c34d2-126">None.</span></span>
<span data-ttu-id="c34d2-127">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="c34d2-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="c34d2-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="c34d2-128">VirtualAppliance.</span></span>
<span data-ttu-id="c34d2-129">Az Azure virtuális hálózatához hozzáadott virtuális készülék.</span><span class="sxs-lookup"><span data-stu-id="c34d2-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="c34d2-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="c34d2-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="c34d2-131">Egy Azureserver-to-Server Virtual Private hálózati átjáró.</span><span class="sxs-lookup"><span data-stu-id="c34d2-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="c34d2-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="c34d2-132">VnetLocal.</span></span>
<span data-ttu-id="c34d2-133">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="c34d2-133">The local virtual network.</span></span>
<span data-ttu-id="c34d2-134">Ha két alhálózata van, akkor a 10.1.0.0/16 és a 10.2.0.0/16 ugyanazon a virtuális hálózaton belül válassza ki az egyes alhálózatok VnetLocal értékét, és továbbítsa a másik alhálózatra.</span><span class="sxs-lookup"><span data-stu-id="c34d2-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="c34d2-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="c34d2-135">-RouteTable</span></span>
<span data-ttu-id="c34d2-136">Annak az útvonalnak a táblázatát adja meg, amelyen az útvonal van társítva.</span><span class="sxs-lookup"><span data-stu-id="c34d2-136">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="c34d2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34d2-137">-DefaultProfile</span></span>
<span data-ttu-id="c34d2-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c34d2-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c34d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34d2-139">CommonParameters</span></span>
<span data-ttu-id="c34d2-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c34d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34d2-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34d2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34d2-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c34d2-142">INPUTS</span></span>

### <span data-ttu-id="c34d2-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c34d2-143">PSRouteTable</span></span>
<span data-ttu-id="c34d2-144">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c34d2-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="c34d2-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c34d2-145">OUTPUTS</span></span>

### <span data-ttu-id="c34d2-146">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c34d2-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c34d2-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c34d2-147">NOTES</span></span>

## <span data-ttu-id="c34d2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c34d2-148">RELATED LINKS</span></span>

[<span data-ttu-id="c34d2-149">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c34d2-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="c34d2-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c34d2-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="c34d2-151">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c34d2-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="c34d2-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="c34d2-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


