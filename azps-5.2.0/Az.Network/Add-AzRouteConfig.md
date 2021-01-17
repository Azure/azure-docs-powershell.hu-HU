---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 326baa91b8da8f9bae67cf47dcc69246549d7c06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359727"
---
# <span data-ttu-id="b5204-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b5204-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="b5204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5204-102">SYNOPSIS</span></span>
<span data-ttu-id="b5204-103">Útvonal hozzáadása egy útvonaltáblához.</span><span class="sxs-lookup"><span data-stu-id="b5204-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="b5204-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5204-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5204-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5204-105">DESCRIPTION</span></span>
<span data-ttu-id="b5204-106">Az **Add-AzRouteConfig** parancsmag hozzáad egy útvonalat egy Azure-útvonaltáblához.</span><span class="sxs-lookup"><span data-stu-id="b5204-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="b5204-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5204-107">EXAMPLES</span></span>

### <span data-ttu-id="b5204-108">1. példa: Útvonal hozzáadása útvonaltáblához</span><span class="sxs-lookup"><span data-stu-id="b5204-108">Example 1: Add a route to a route table</span></span>
```powershell
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="b5204-109">Az első parancs egy RouteTable01 nevű útvonaltáblát kap a Get-AzRouteTable parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b5204-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="b5204-110">A parancs a táblát a $RouteTable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5204-110">The command stores the table in the $RouteTable variable.</span></span>
<span data-ttu-id="b5204-111">A második parancs hozzáad egy Route13 nevű útvonalat a $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="b5204-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="b5204-112">Ez az útvonal csomagokat továbbít a helyi virtuális hálózatra.</span><span class="sxs-lookup"><span data-stu-id="b5204-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="b5204-113">2. példa: Útvonal hozzáadása útvonaltáblához a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="b5204-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```powershell
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

<span data-ttu-id="b5204-114">Ez a parancs a RouteTable01 nevű útválasztási táblát a **Get-AzRouteTable segítségével kapja meg.**</span><span class="sxs-lookup"><span data-stu-id="b5204-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="b5204-115">A parancs a folyamat műveleti operátorával átadja a táblát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="b5204-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b5204-116">Az aktuális parancsmag hozzáadja az Route02 nevű útvonalat, majd átadja az eredményt a **Set-AzRouteTable** parancsmagnak, amely frissíti a táblát a módosításoknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="b5204-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="b5204-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5204-117">PARAMETERS</span></span>

### <span data-ttu-id="b5204-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b5204-118">-AddressPrefix</span></span>
<span data-ttu-id="b5204-119">Az útvonal célhelyét adja meg Classless Interdomain Routing (CIDR) formátumban.</span><span class="sxs-lookup"><span data-stu-id="b5204-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="b5204-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5204-120">-DefaultProfile</span></span>
<span data-ttu-id="b5204-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5204-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5204-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b5204-122">-Name</span></span>
<span data-ttu-id="b5204-123">Megadja az útvonaltáblához hozzáadni tervezett útvonal nevét.</span><span class="sxs-lookup"><span data-stu-id="b5204-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="b5204-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b5204-124">-NextHopIpAddress</span></span>
<span data-ttu-id="b5204-125">Az Azure virtuális hálózatához adott virtuális készülék IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b5204-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="b5204-126">Ez az útvonal csomagokat továbbít erre a címre.</span><span class="sxs-lookup"><span data-stu-id="b5204-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="b5204-127">Ezt a paramétert csak akkor adja meg, ha a VirtualAppliance értéket adja meg a *NextHopType paraméterhez.*</span><span class="sxs-lookup"><span data-stu-id="b5204-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="b5204-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b5204-128">-NextHopType</span></span>
<span data-ttu-id="b5204-129">Meghatározza, hogy ez az útvonal hogyan továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="b5204-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="b5204-130">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b5204-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5204-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="b5204-131">Internet.</span></span>
<span data-ttu-id="b5204-132">Az Azure által biztosított alapértelmezett internetes átjáró.</span><span class="sxs-lookup"><span data-stu-id="b5204-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="b5204-133">Nincs.</span><span class="sxs-lookup"><span data-stu-id="b5204-133">None.</span></span>
<span data-ttu-id="b5204-134">Ha ezt az értéket adja meg, az útvonal nem továbbítja a csomagokat.</span><span class="sxs-lookup"><span data-stu-id="b5204-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="b5204-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b5204-135">VirtualAppliance.</span></span>
<span data-ttu-id="b5204-136">Egy virtuális eszköz, amely hozzáadva az Azure virtuális hálózatához.</span><span class="sxs-lookup"><span data-stu-id="b5204-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="b5204-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b5204-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="b5204-138">Azure server-to-server virtual private network gateway.</span><span class="sxs-lookup"><span data-stu-id="b5204-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="b5204-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="b5204-139">VnetLocal.</span></span>
<span data-ttu-id="b5204-140">A helyi virtuális hálózat.</span><span class="sxs-lookup"><span data-stu-id="b5204-140">The local virtual network.</span></span>
<span data-ttu-id="b5204-141">Ha két alhálózata van: 10.1.0.0/16 és 10.2.0.0/16 ugyanabban a virtuális hálózatban, válassza ki az egyes alhálózatok VnetLocal-értékét a másik alhálózatra való továbbításhoz.</span><span class="sxs-lookup"><span data-stu-id="b5204-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="b5204-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="b5204-142">-RouteTable</span></span>
<span data-ttu-id="b5204-143">Azt az útvonaltáblát adja meg, amelyhez ez a parancsmag útvonalat ad.</span><span class="sxs-lookup"><span data-stu-id="b5204-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="b5204-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5204-144">-Confirm</span></span>
<span data-ttu-id="b5204-145">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b5204-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5204-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5204-146">-WhatIf</span></span>
<span data-ttu-id="b5204-147">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b5204-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5204-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b5204-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5204-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5204-149">CommonParameters</span></span>
<span data-ttu-id="b5204-150">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5204-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5204-151">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5204-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5204-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5204-152">INPUTS</span></span>

### <span data-ttu-id="b5204-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5204-153">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="b5204-154">System.String</span><span class="sxs-lookup"><span data-stu-id="b5204-154">System.String</span></span>

## <span data-ttu-id="b5204-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5204-155">OUTPUTS</span></span>

### <span data-ttu-id="b5204-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5204-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="b5204-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5204-157">NOTES</span></span>

## <span data-ttu-id="b5204-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5204-158">RELATED LINKS</span></span>

[<span data-ttu-id="b5204-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b5204-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="b5204-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5204-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="b5204-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b5204-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="b5204-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b5204-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="b5204-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b5204-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="b5204-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5204-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


