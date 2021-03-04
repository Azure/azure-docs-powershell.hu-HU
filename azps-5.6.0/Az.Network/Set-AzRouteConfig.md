---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: a4cdcbf52dfb20f0282347d5dc1ce9a5aec14da0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938545"
---
# <span data-ttu-id="4acf5-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4acf5-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="4acf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4acf5-102">SYNOPSIS</span></span>
<span data-ttu-id="4acf5-103">Frissíti az útvonal-konfigurációt egy útvonaltáblához.</span><span class="sxs-lookup"><span data-stu-id="4acf5-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="4acf5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4acf5-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4acf5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4acf5-105">DESCRIPTION</span></span>
<span data-ttu-id="4acf5-106">A **Set-AzRouteConfig** parancsmag frissíti az útvonal-konfigurációt egy útvonaltáblához.</span><span class="sxs-lookup"><span data-stu-id="4acf5-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="4acf5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4acf5-107">EXAMPLES</span></span>

### <span data-ttu-id="4acf5-108">1. példa: Útvonal módosítása</span><span class="sxs-lookup"><span data-stu-id="4acf5-108">Example 1: Modify a route</span></span>
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

<span data-ttu-id="4acf5-109">Ez a parancs a RouteTable01 nevű útválasztási táblát a Get-AzRouteTable parancsmag használatával kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4acf5-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="4acf5-110">A parancs a folyamat műveleti operátorával átadja a táblát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="4acf5-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4acf5-111">Az aktuális parancsmag módosítja az Route02 nevű útvonalat, majd átadja az eredményt a **Set-AzRouteTable** parancsmagnak, amely a módosításoknak megfelelően frissíti a táblát.</span><span class="sxs-lookup"><span data-stu-id="4acf5-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="4acf5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4acf5-112">PARAMETERS</span></span>

### <span data-ttu-id="4acf5-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4acf5-113">-AddressPrefix</span></span>
<span data-ttu-id="4acf5-114">Az útvonal célhelyét adja meg Classless Interdomain Routing (CIDR) formátumban.</span><span class="sxs-lookup"><span data-stu-id="4acf5-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="4acf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acf5-115">-DefaultProfile</span></span>
<span data-ttu-id="4acf5-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4acf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4acf5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4acf5-117">-Name</span></span>
<span data-ttu-id="4acf5-118">Annak az útvonalnak a nevét adja meg, amely módosítja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4acf5-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4acf5-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="4acf5-119">-NextHopIpAddress</span></span>
<span data-ttu-id="4acf5-120">Az Azure virtuális hálózatához adott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4acf5-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="4acf5-121">Ez az útvonal csomagokat továbbít erre a címre.</span><span class="sxs-lookup"><span data-stu-id="4acf5-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="4acf5-122">Ezt a paramétert csak akkor adja meg, ha a VirtualAppliance értéket adja meg a *NextHopType paraméterhez.*</span><span class="sxs-lookup"><span data-stu-id="4acf5-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="4acf5-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="4acf5-123">-NextHopType</span></span>
<span data-ttu-id="4acf5-124">Meghatározza, hogy ez az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="4acf5-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="4acf5-125">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="4acf5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4acf5-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="4acf5-126">Internet.</span></span>
<span data-ttu-id="4acf5-127">Az Azure által biztosított alapértelmezett internetes átjáró.</span><span class="sxs-lookup"><span data-stu-id="4acf5-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="4acf5-128">Nincs.</span><span class="sxs-lookup"><span data-stu-id="4acf5-128">None.</span></span>
<span data-ttu-id="4acf5-129">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="4acf5-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="4acf5-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4acf5-130">VirtualAppliance.</span></span>
<span data-ttu-id="4acf5-131">Egy virtuális eszköz, amely hozzáadva az Azure virtuális hálózatához.</span><span class="sxs-lookup"><span data-stu-id="4acf5-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="4acf5-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="4acf5-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="4acf5-133">Azureserver-to-server virtual private network gateway.</span><span class="sxs-lookup"><span data-stu-id="4acf5-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="4acf5-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="4acf5-134">VnetLocal.</span></span>
<span data-ttu-id="4acf5-135">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="4acf5-135">The local virtual network.</span></span>
<span data-ttu-id="4acf5-136">Ha két alhálózata van: 10.1.0.0/16 és 10.2.0.0/16 ugyanabban a virtuális hálózatban, válassza ki az egyes alhálózatok VnetLocal-értékét a másik alhálózatra való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="4acf5-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="4acf5-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="4acf5-137">-RouteTable</span></span>
<span data-ttu-id="4acf5-138">Azt az útvonaltáblát adja meg, amelyhez az útvonal társítva van.</span><span class="sxs-lookup"><span data-stu-id="4acf5-138">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="4acf5-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4acf5-139">-Confirm</span></span>
<span data-ttu-id="4acf5-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4acf5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4acf5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4acf5-141">-WhatIf</span></span>
<span data-ttu-id="4acf5-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4acf5-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4acf5-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4acf5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4acf5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acf5-144">CommonParameters</span></span>
<span data-ttu-id="4acf5-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acf5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acf5-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4acf5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acf5-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4acf5-147">INPUTS</span></span>

### <span data-ttu-id="4acf5-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4acf5-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="4acf5-149">System.String</span><span class="sxs-lookup"><span data-stu-id="4acf5-149">System.String</span></span>

## <span data-ttu-id="4acf5-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4acf5-150">OUTPUTS</span></span>

### <span data-ttu-id="4acf5-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="4acf5-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="4acf5-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4acf5-152">NOTES</span></span>

## <span data-ttu-id="4acf5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4acf5-153">RELATED LINKS</span></span>

[<span data-ttu-id="4acf5-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4acf5-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="4acf5-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4acf5-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="4acf5-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4acf5-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="4acf5-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="4acf5-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


