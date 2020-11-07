---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteConfig.md
ms.openlocfilehash: b8ace5d38878e9acbdbfaa25e3bfd4ebfc185260
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670126"
---
# <span data-ttu-id="dc3c7-101">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c7-101">Remove-AzRouteConfig</span></span>

## <span data-ttu-id="dc3c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3c7-103">Egy útvonal eltávolítása az útvonal-táblázatból.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-103">Removes a route from a route table.</span></span>

## <span data-ttu-id="dc3c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc3c7-104">SYNTAX</span></span>

```
Remove-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc3c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc3c7-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3c7-106">A **Remove-AzRouteConfig** parancsmag az Azure Route-táblázatból távolítja el az útvonalat.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-106">The **Remove-AzRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="dc3c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dc3c7-107">EXAMPLES</span></span>

### <span data-ttu-id="dc3c7-108">1. példa: útvonal eltávolítása</span><span class="sxs-lookup"><span data-stu-id="dc3c7-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzRouteConfig -Name "Route02" | Set-AzRouteTable
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

<span data-ttu-id="dc3c7-109">Ez a parancs a **Get-AzRouteTable** parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-109">This command gets the route table named RouteTable01 by using the **Get-AzRouteTable** cmdlet.</span></span>
<span data-ttu-id="dc3c7-110">A parancs átadja az adott táblát az aktuális parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc3c7-111">Az aktuális parancsmag eltávolítja a Route02 nevű útvonalat, és az eredményt átadja a **set-AzRouteTable** parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="dc3c7-112">A táblázat már nem tartalmazza a Route02 nevű útvonalat.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="dc3c7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc3c7-113">PARAMETERS</span></span>

### <span data-ttu-id="dc3c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3c7-114">-DefaultProfile</span></span>
<span data-ttu-id="dc3c7-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3c7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc3c7-116">-Name</span></span>
<span data-ttu-id="dc3c7-117">A parancsmag által eltávolított útvonal nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-117">Specifies the name of the route that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dc3c7-118">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dc3c7-118">-RouteTable</span></span>
<span data-ttu-id="dc3c7-119">Annak az útvonalnak a táblázatát adja meg, amely a parancsmag által törölt útvonalat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-119">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="dc3c7-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dc3c7-120">-Confirm</span></span>
<span data-ttu-id="dc3c7-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3c7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3c7-122">-WhatIf</span></span>
<span data-ttu-id="dc3c7-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc3c7-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dc3c7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3c7-125">CommonParameters</span></span>
<span data-ttu-id="dc3c7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc3c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3c7-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3c7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3c7-128">INPUTS</span></span>

### <span data-ttu-id="dc3c7-129">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc3c7-129">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="dc3c7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc3c7-130">OUTPUTS</span></span>

### <span data-ttu-id="dc3c7-131">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dc3c7-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="dc3c7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc3c7-132">NOTES</span></span>

## <span data-ttu-id="dc3c7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc3c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="dc3c7-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c7-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="dc3c7-135">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c7-135">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="dc3c7-136">Új – AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c7-136">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="dc3c7-137">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c7-137">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


