---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteTable.md
ms.openlocfilehash: ac7b370a6a10aff5a9524a2536b5f4dedaff5a9f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837920"
---
# <span data-ttu-id="8324e-101">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8324e-101">New-AzRouteTable</span></span>

## <span data-ttu-id="8324e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8324e-102">SYNOPSIS</span></span>
<span data-ttu-id="8324e-103">Útválasztási táblázat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="8324e-103">Creates a route table.</span></span>

## <span data-ttu-id="8324e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8324e-104">SYNTAX</span></span>

```
New-AzRouteTable -ResourceGroupName <String> -Name <String> [-DisableBgpRoutePropagation] -Location <String>
 [-Tag <Hashtable>] [-Route <PSRoute[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8324e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8324e-105">DESCRIPTION</span></span>
<span data-ttu-id="8324e-106">A **New-AzRouteTable** parancsmag egy Azure Route-táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8324e-106">The **New-AzRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="8324e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8324e-107">EXAMPLES</span></span>

### <span data-ttu-id="8324e-108">1. példa: útvonalat tartalmazó útvonalkártya létrehozása</span><span class="sxs-lookup"><span data-stu-id="8324e-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/myroutetable
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              :
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null,
                        "ProvisioningState": "Succeeded"
                      }
                    ]
Subnets           : []
```

<span data-ttu-id="8324e-109">Az első parancs az New-AzRouteConfig parancsmag segítségével létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8324e-109">The first command creates a route named Route07 by using the New-AzRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="8324e-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="8324e-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="8324e-111">A második parancs létrehoz egy RouteTable01 nevű útvonalkártya-táblázatot, és a $Routeban tárolt útvonalat hozzáadja az új táblához.</span><span class="sxs-lookup"><span data-stu-id="8324e-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="8324e-112">A parancs azt az erőforráscsoportot adja meg, amelyhez a táblázat tartozik, valamint a tábla helyét.</span><span class="sxs-lookup"><span data-stu-id="8324e-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="8324e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8324e-113">PARAMETERS</span></span>

### <span data-ttu-id="8324e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8324e-114">-AsJob</span></span>
<span data-ttu-id="8324e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="8324e-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8324e-116">-DefaultProfile</span></span>
<span data-ttu-id="8324e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8324e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8324e-118">-DisableBgpRoutePropagation</span><span class="sxs-lookup"><span data-stu-id="8324e-118">-DisableBgpRoutePropagation</span></span>
<span data-ttu-id="8324e-119">Tiltsa le a BGP útvonal automatikus propagálását.</span><span class="sxs-lookup"><span data-stu-id="8324e-119">Disable BGP Route auto propagation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8324e-120">-Force</span></span>
<span data-ttu-id="8324e-121">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="8324e-121">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="8324e-122">-Location</span></span>
<span data-ttu-id="8324e-123">Azt az Azure-területet adja meg, amelyben ez a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8324e-123">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="8324e-124">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions/)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="8324e-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8324e-125">-Name</span></span>
<span data-ttu-id="8324e-126">Az útvonal-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8324e-126">Specifies a name for the route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8324e-127">-ResourceGroupName</span></span>
<span data-ttu-id="8324e-128">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8324e-128">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-129">– Útvonal</span><span class="sxs-lookup"><span data-stu-id="8324e-129">-Route</span></span>
<span data-ttu-id="8324e-130">Az útválasztási táblázathoz társítandó **útvonali** objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8324e-130">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRoute[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="8324e-131">-Tag</span></span>
<span data-ttu-id="8324e-132">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8324e-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8324e-133">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8324e-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8324e-134">-Confirm</span></span>
<span data-ttu-id="8324e-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8324e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8324e-136">-WhatIf</span></span>
<span data-ttu-id="8324e-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8324e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8324e-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8324e-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8324e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8324e-139">CommonParameters</span></span>
<span data-ttu-id="8324e-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8324e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8324e-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8324e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8324e-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8324e-142">INPUTS</span></span>

### <span data-ttu-id="8324e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8324e-143">System.String</span></span>

### <span data-ttu-id="8324e-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8324e-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8324e-145">Microsoft. Azure. commands. Network. models. PSRoute []</span><span class="sxs-lookup"><span data-stu-id="8324e-145">Microsoft.Azure.Commands.Network.Models.PSRoute[]</span></span>

## <span data-ttu-id="8324e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8324e-146">OUTPUTS</span></span>

### <span data-ttu-id="8324e-147">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="8324e-147">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="8324e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8324e-148">NOTES</span></span>

## <span data-ttu-id="8324e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8324e-149">RELATED LINKS</span></span>

[<span data-ttu-id="8324e-150">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8324e-150">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="8324e-151">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="8324e-151">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="8324e-152">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8324e-152">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)

[<span data-ttu-id="8324e-153">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="8324e-153">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)
