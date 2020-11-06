---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteTable.md
ms.openlocfilehash: f4ef683b65967fe694713b7990d23eb173f02163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494825"
---
# <span data-ttu-id="2011e-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2011e-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="2011e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2011e-102">SYNOPSIS</span></span>
<span data-ttu-id="2011e-103">Útválasztási táblázat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="2011e-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2011e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2011e-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -Name <String> -ResourceGroupName <String> -Location <String>
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2011e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2011e-105">DESCRIPTION</span></span>
<span data-ttu-id="2011e-106">A **New-AzureRmRouteTable** parancsmag egy Azure Route-táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2011e-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="2011e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2011e-107">EXAMPLES</span></span>

### <span data-ttu-id="2011e-108">1. példa: útvonalat tartalmazó útvonalkártya létrehozása</span><span class="sxs-lookup"><span data-stu-id="2011e-108">Example 1: Create a route table that contains a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> New-AzureRmRouteTable -Name "RouteTable01" -ResourceGroupName "ResourceGroup11" -Location "EASTUS" -Route $Route
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

<span data-ttu-id="2011e-109">Az első parancs az New-AzureRmRouteConfig parancsmag segítségével létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2011e-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="2011e-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="2011e-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="2011e-111">A második parancs létrehoz egy RouteTable01 nevű útvonalkártya-táblázatot, és a $Routeban tárolt útvonalat hozzáadja az új táblához.</span><span class="sxs-lookup"><span data-stu-id="2011e-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="2011e-112">A parancs azt az erőforráscsoportot adja meg, amelyhez a táblázat tartozik, valamint a tábla helyét.</span><span class="sxs-lookup"><span data-stu-id="2011e-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="2011e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2011e-113">PARAMETERS</span></span>

### <span data-ttu-id="2011e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2011e-114">-Force</span></span>
<span data-ttu-id="2011e-115">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="2011e-115">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

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

### <span data-ttu-id="2011e-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="2011e-116">-Location</span></span>
<span data-ttu-id="2011e-117">Azt az Azure-területet adja meg, amelyben ez a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2011e-117">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="2011e-118">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions/)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="2011e-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

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

### <span data-ttu-id="2011e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2011e-119">-Name</span></span>
<span data-ttu-id="2011e-120">Az útvonal-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2011e-120">Specifies a name for the route table.</span></span>

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

### <span data-ttu-id="2011e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2011e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2011e-122">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="2011e-122">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

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

### <span data-ttu-id="2011e-123">– Útvonal</span><span class="sxs-lookup"><span data-stu-id="2011e-123">-Route</span></span>
<span data-ttu-id="2011e-124">Az útválasztási táblázathoz társítandó **útvonali** objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2011e-124">Specifies an array of **Route** objects to associate with the route table.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2011e-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="2011e-125">-Tag</span></span>
<span data-ttu-id="2011e-126">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="2011e-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2011e-127">Példa:</span><span class="sxs-lookup"><span data-stu-id="2011e-127">For example:</span></span>

<span data-ttu-id="2011e-128">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="2011e-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2011e-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2011e-129">-Confirm</span></span>
<span data-ttu-id="2011e-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2011e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2011e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2011e-131">-WhatIf</span></span>
<span data-ttu-id="2011e-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2011e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2011e-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2011e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2011e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2011e-134">-DefaultProfile</span></span>
<span data-ttu-id="2011e-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2011e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2011e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2011e-136">CommonParameters</span></span>
<span data-ttu-id="2011e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2011e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2011e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2011e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2011e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2011e-139">INPUTS</span></span>

## <span data-ttu-id="2011e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2011e-140">OUTPUTS</span></span>

### <span data-ttu-id="2011e-141">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2011e-141">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2011e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2011e-142">NOTES</span></span>

## <span data-ttu-id="2011e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2011e-143">RELATED LINKS</span></span>

[<span data-ttu-id="2011e-144">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2011e-144">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="2011e-145">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2011e-145">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2011e-146">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2011e-146">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="2011e-147">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="2011e-147">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
