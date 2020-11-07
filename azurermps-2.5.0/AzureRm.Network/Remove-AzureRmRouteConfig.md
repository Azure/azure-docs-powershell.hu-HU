---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: c5117fc961a93395991055eff2d404b5b8c6c051
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850621"
---
# <span data-ttu-id="2d096-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2d096-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="2d096-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d096-102">SYNOPSIS</span></span>
<span data-ttu-id="2d096-103">Egy útvonal eltávolítása az útvonal-táblázatból.</span><span class="sxs-lookup"><span data-stu-id="2d096-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d096-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d096-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -RouteTable <PSRouteTable> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d096-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d096-105">DESCRIPTION</span></span>
<span data-ttu-id="2d096-106">A **Remove-AzureRmRouteConfig** parancsmag az Azure Route-táblázatból távolítja el az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="2d096-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="2d096-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2d096-107">EXAMPLES</span></span>

### <span data-ttu-id="2d096-108">1. példa: útvonal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2d096-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="2d096-109">Ez a parancs a **Get-AzureRmRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="2d096-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="2d096-110">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="2d096-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2d096-111">Az aktuális parancsmag eltávolítja a Route02 nevű útvonalat, és az eredményt átadja a **set-AzureRmRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="2d096-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="2d096-112">A táblázat már nem tartalmazza a Route02 nevű útvonalat.</span><span class="sxs-lookup"><span data-stu-id="2d096-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="2d096-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d096-113">PARAMETERS</span></span>

### <span data-ttu-id="2d096-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d096-114">-DefaultProfile</span></span>
<span data-ttu-id="2d096-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d096-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d096-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d096-116">-Name</span></span>
<span data-ttu-id="2d096-117">A parancsmag által eltávolított útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d096-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2d096-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2d096-118">-RouteTable</span></span>
<span data-ttu-id="2d096-119">Annak az útvonalnak a táblázatát adja meg, amely a parancsmag által törölt útvonalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2d096-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="2d096-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d096-120">-Confirm</span></span>
<span data-ttu-id="2d096-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d096-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d096-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d096-122">-WhatIf</span></span>
<span data-ttu-id="2d096-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d096-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d096-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d096-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d096-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d096-125">CommonParameters</span></span>
<span data-ttu-id="2d096-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d096-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d096-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d096-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d096-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d096-128">INPUTS</span></span>

### <span data-ttu-id="2d096-129">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d096-129">PSRouteTable</span></span>
<span data-ttu-id="2d096-130">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2d096-130">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="2d096-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d096-131">OUTPUTS</span></span>

### <span data-ttu-id="2d096-132">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d096-132">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2d096-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d096-133">NOTES</span></span>

## <span data-ttu-id="2d096-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d096-134">RELATED LINKS</span></span>

[<span data-ttu-id="2d096-135">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2d096-135">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="2d096-136">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2d096-136">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="2d096-137">Új – AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2d096-137">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="2d096-138">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2d096-138">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


