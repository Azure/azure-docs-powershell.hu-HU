---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzRouteTable.md
ms.openlocfilehash: 531c2724289e90f92bf14347518d53b6208be932
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843569"
---
# <span data-ttu-id="99c79-101">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-101">Set-AzRouteTable</span></span>

## <span data-ttu-id="99c79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99c79-102">SYNOPSIS</span></span>
<span data-ttu-id="99c79-103">Az útvonaltervezés cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="99c79-103">Sets the goal state for a route table.</span></span>

## <span data-ttu-id="99c79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99c79-104">SYNTAX</span></span>

```
Set-AzRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c79-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99c79-105">DESCRIPTION</span></span>
<span data-ttu-id="99c79-106">A **set-AzRouteTable** parancsmag az Azure Route-táblázatok cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="99c79-106">The **Set-AzRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="99c79-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99c79-107">EXAMPLES</span></span>

### <span data-ttu-id="99c79-108">1. példa: útvonal hozzáadása, majd az útválasztási táblázat cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="99c79-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/RouteTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "Route13",
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

<span data-ttu-id="99c79-109">Ez a parancs Get-AzRouteTable parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="99c79-109">This command gets the route table named RouteTable01 by using Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="99c79-110">A parancs a táblázatot átadja a Add-AzRouteConfig parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="99c79-110">The command passes that table to the Add-AzRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="99c79-111">A **Add-AzRouteConfig** hozzáadja a Route07 nevű útvonalat, majd átadja az eredményt az aktuális parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="99c79-111">**Add-AzRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="99c79-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99c79-112">PARAMETERS</span></span>

### <span data-ttu-id="99c79-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99c79-113">-AsJob</span></span>
<span data-ttu-id="99c79-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99c79-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99c79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c79-115">-DefaultProfile</span></span>
<span data-ttu-id="99c79-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99c79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c79-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-117">-RouteTable</span></span>
<span data-ttu-id="99c79-118">Megadja a Route Table-objektumot, amely azt a célt adja meg, amelyre a parancsmag az útválasztási táblázatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="99c79-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99c79-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99c79-119">-Confirm</span></span>
<span data-ttu-id="99c79-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99c79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c79-121">-WhatIf</span></span>
<span data-ttu-id="99c79-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99c79-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99c79-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99c79-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c79-124">CommonParameters</span></span>
<span data-ttu-id="99c79-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99c79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c79-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99c79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c79-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c79-127">INPUTS</span></span>

### <span data-ttu-id="99c79-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-128">PSRouteTable</span></span>
<span data-ttu-id="99c79-129">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="99c79-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="99c79-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99c79-130">OUTPUTS</span></span>

### <span data-ttu-id="99c79-131">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="99c79-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99c79-132">NOTES</span></span>

## <span data-ttu-id="99c79-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99c79-133">RELATED LINKS</span></span>

[<span data-ttu-id="99c79-134">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="99c79-134">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="99c79-135">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-135">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="99c79-136">Új – AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-136">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="99c79-137">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="99c79-137">Remove-AzRouteTable</span></span>](./Remove-AzRouteTable.md)


