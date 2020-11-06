---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE2A30A-6DF8-4C4C-8348-C3C1CD4D0146
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteTable.md
ms.openlocfilehash: 6848b00d090b8d365b0c26fb3948a4eec3ad047d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505439"
---
# <span data-ttu-id="bc5cb-101">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-101">Set-AzureRmRouteTable</span></span>

## <span data-ttu-id="bc5cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bc5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5cb-103">Az útvonaltervezés cél állapotának beállítása.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-103">Sets the goal state for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc5cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bc5cb-104">SYNTAX</span></span>

```
Set-AzureRmRouteTable -RouteTable <PSRouteTable> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bc5cb-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5cb-106">A **set-AzureRmRouteTable** parancsmag az Azure Route-táblázatok cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-106">The **Set-AzureRmRouteTable** cmdlet sets the goal state for an Azure route table.</span></span>

## <span data-ttu-id="bc5cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bc5cb-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5cb-108">1. példa: útvonal hozzáadása, majd az útválasztási táblázat cél állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="bc5cb-108">Example 1: Add a route and then set the goal state of the route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.2.0.0/16 -NextHopType "VnetLocal" | Set-AzureRmRouteTable
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

<span data-ttu-id="bc5cb-109">Ez a parancs Get-AzureRmRouteTable parancsmag segítségével a RouteTable01 nevű útválasztási táblázatot kapja.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-109">This command gets the route table named RouteTable01 by using Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="bc5cb-110">A parancs a táblázatot átadja a Add-AzureRmRouteConfig parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-110">The command passes that table to the Add-AzureRmRouteConfig cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bc5cb-111">A **Add-AzureRmRouteConfig** hozzáadja a Route07 nevű útvonalat, majd átadja az eredményt az aktuális parancsmagnak, amely frissíti a táblázatot a módosítások tükrözése érdekében.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-111">**Add-AzureRmRouteConfig** adds the route named Route07, and then passes the result to the current cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="bc5cb-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bc5cb-112">PARAMETERS</span></span>

### <span data-ttu-id="bc5cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc5cb-113">-AsJob</span></span>
<span data-ttu-id="bc5cb-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bc5cb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc5cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5cb-115">-DefaultProfile</span></span>
<span data-ttu-id="bc5cb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc5cb-117">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-117">-RouteTable</span></span>
<span data-ttu-id="bc5cb-118">Megadja a Route Table-objektumot, amely azt a célt adja meg, amelyre a parancsmag az útválasztási táblázatot állítja be.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-118">Specifies a route table object that represents the goal state to which this cmdlet sets the route table.</span></span>

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

### <span data-ttu-id="bc5cb-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bc5cb-119">-Confirm</span></span>
<span data-ttu-id="bc5cb-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5cb-121">-WhatIf</span></span>
<span data-ttu-id="bc5cb-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc5cb-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc5cb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5cb-124">CommonParameters</span></span>
<span data-ttu-id="bc5cb-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bc5cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5cb-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc5cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5cb-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc5cb-127">INPUTS</span></span>

### <span data-ttu-id="bc5cb-128">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-128">PSRouteTable</span></span>
<span data-ttu-id="bc5cb-129">A ' RouteTable ' paraméter az "PSRouteTable" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="bc5cb-129">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="bc5cb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc5cb-130">OUTPUTS</span></span>

### <span data-ttu-id="bc5cb-131">Microsoft. Azure. commands. Network. models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-131">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="bc5cb-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bc5cb-132">NOTES</span></span>

## <span data-ttu-id="bc5cb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc5cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc5cb-134">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="bc5cb-134">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="bc5cb-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="bc5cb-136">Új – AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="bc5cb-137">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="bc5cb-137">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)


