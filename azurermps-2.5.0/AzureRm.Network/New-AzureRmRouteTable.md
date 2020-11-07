---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6A278F91-C078-4DD4-82D0-2E4FA549A089
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutetable
schema: 2.0.0
ms.openlocfilehash: 9ba23a33e82e003413172240264ef8485b12d4e0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850373"
---
# <span data-ttu-id="ff39e-101">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff39e-101">New-AzureRmRouteTable</span></span>

## <span data-ttu-id="ff39e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff39e-102">SYNOPSIS</span></span>
<span data-ttu-id="ff39e-103">Útválasztási táblázat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="ff39e-103">Creates a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff39e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff39e-104">SYNTAX</span></span>

```
New-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Route <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRoute]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff39e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff39e-105">DESCRIPTION</span></span>
<span data-ttu-id="ff39e-106">A **New-AzureRmRouteTable** parancsmag egy Azure Route-táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ff39e-106">The **New-AzureRmRouteTable** cmdlet creates an Azure route table.</span></span>

## <span data-ttu-id="ff39e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff39e-107">EXAMPLES</span></span>

### <span data-ttu-id="ff39e-108">1. példa: útvonalat tartalmazó útvonalkártya létrehozása</span><span class="sxs-lookup"><span data-stu-id="ff39e-108">Example 1: Create a route table that contains a route</span></span>
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

<span data-ttu-id="ff39e-109">Az első parancs az New-AzureRmRouteConfig parancsmag segítségével létrehoz egy Route07 nevű útvonalat, majd a $Route változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ff39e-109">The first command creates a route named Route07 by using the New-AzureRmRouteConfig cmdlet, and then stores it in the $Route variable.</span></span> <span data-ttu-id="ff39e-110">Az útvonal továbbítja a csomagokat a helyi virtuális hálózatba.</span><span class="sxs-lookup"><span data-stu-id="ff39e-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="ff39e-111">A második parancs létrehoz egy RouteTable01 nevű útvonalkártya-táblázatot, és a $Routeban tárolt útvonalat hozzáadja az új táblához.</span><span class="sxs-lookup"><span data-stu-id="ff39e-111">The second command creates a route table named RouteTable01, and adds the route stored in $Route to the new table.</span></span> <span data-ttu-id="ff39e-112">A parancs azt az erőforráscsoportot adja meg, amelyhez a táblázat tartozik, valamint a tábla helyét.</span><span class="sxs-lookup"><span data-stu-id="ff39e-112">The command specifies the resource group to which the table belongs and the location for the table.</span></span>

## <span data-ttu-id="ff39e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff39e-113">PARAMETERS</span></span>

### <span data-ttu-id="ff39e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff39e-114">-AsJob</span></span>
<span data-ttu-id="ff39e-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ff39e-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff39e-116">-DefaultProfile</span></span>
<span data-ttu-id="ff39e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff39e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff39e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ff39e-118">-Force</span></span>
<span data-ttu-id="ff39e-119">Azt jelzi, hogy ez a parancsmag akkor is létrehoz egy útválasztási táblázatot, ha már létezik azonos nevű útválasztási táblázat.</span><span class="sxs-lookup"><span data-stu-id="ff39e-119">Indicates that this cmdlet creates a route table even if a route table that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="ff39e-120">-Location</span></span>
<span data-ttu-id="ff39e-121">Azt az Azure-területet adja meg, amelyben ez a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ff39e-121">Specifies the Azure region in which this cmdlet creates a route table.</span></span>
<span data-ttu-id="ff39e-122">További tudnivalókat az [Azure Regions](https://azure.microsoft.com/en-us/regions/)című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="ff39e-122">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff39e-123">-Name</span></span>
<span data-ttu-id="ff39e-124">Az útvonal-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff39e-124">Specifies a name for the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff39e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ff39e-126">Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehoz egy útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ff39e-126">Specifies the name of the resource group in which this cmdlet creates a route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-127">– Útvonal</span><span class="sxs-lookup"><span data-stu-id="ff39e-127">-Route</span></span>
<span data-ttu-id="ff39e-128">Az útválasztási táblázathoz társítandó **útvonali** objektumok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff39e-128">Specifies an array of **Route** objects to associate with the route table.</span></span>

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

### <span data-ttu-id="ff39e-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="ff39e-129">-Tag</span></span>
<span data-ttu-id="ff39e-130">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="ff39e-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ff39e-131">Példa:</span><span class="sxs-lookup"><span data-stu-id="ff39e-131">For example:</span></span>

<span data-ttu-id="ff39e-132">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="ff39e-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff39e-133">-Confirm</span></span>
<span data-ttu-id="ff39e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff39e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff39e-135">-WhatIf</span></span>
<span data-ttu-id="ff39e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff39e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff39e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff39e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff39e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff39e-138">CommonParameters</span></span>
<span data-ttu-id="ff39e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff39e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff39e-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff39e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff39e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39e-141">INPUTS</span></span>

## <span data-ttu-id="ff39e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff39e-142">OUTPUTS</span></span>

### <span data-ttu-id="ff39e-143">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff39e-143">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ff39e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff39e-144">NOTES</span></span>

## <span data-ttu-id="ff39e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff39e-145">RELATED LINKS</span></span>

[<span data-ttu-id="ff39e-146">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff39e-146">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="ff39e-147">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ff39e-147">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="ff39e-148">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff39e-148">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="ff39e-149">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff39e-149">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)
