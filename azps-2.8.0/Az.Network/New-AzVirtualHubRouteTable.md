---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 3ccf321a089dbb519293fe6407581aecf32b8157
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837158"
---
# <span data-ttu-id="3760d-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3760d-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="3760d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3760d-102">SYNOPSIS</span></span>
<span data-ttu-id="3760d-103">Azure Virtual hub Route Table-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3760d-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="3760d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3760d-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3760d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3760d-105">DESCRIPTION</span></span>
<span data-ttu-id="3760d-106">Azure Virtual hub Route Table-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3760d-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="3760d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3760d-107">EXAMPLES</span></span>

### <span data-ttu-id="3760d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3760d-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"
PS C:\> $route2 = New-AzVirtualHubRoute -AddressPrefix @("13.0.0.0/16") -NextHopIpAddress "14.0.0.5"
PS C:\> $routeTable = New-AzVirtualHubRouteTable -Route @($route1, $route2)
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWanId $virtualWan.Id -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24" -RouteTable $routeTable

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="3760d-109">A fenti táblázat létrehoz egy több útvonalból álló, új virtuális hub-hoz csatolt útvonalat.</span><span class="sxs-lookup"><span data-stu-id="3760d-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="3760d-110">Ez a memória-objektum, amellyel új vagy meglévő VirtualHub adhat hozzá az útválasztási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="3760d-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="3760d-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3760d-111">PARAMETERS</span></span>

### <span data-ttu-id="3760d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3760d-112">-DefaultProfile</span></span>
<span data-ttu-id="3760d-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3760d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3760d-114">– Útvonal</span><span class="sxs-lookup"><span data-stu-id="3760d-114">-Route</span></span>
<span data-ttu-id="3760d-115">A virtuális hub-útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="3760d-115">List of virtual hub routes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3760d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3760d-116">CommonParameters</span></span>
<span data-ttu-id="3760d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3760d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3760d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3760d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3760d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3760d-119">INPUTS</span></span>

### <span data-ttu-id="3760d-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="3760d-120">None</span></span>

## <span data-ttu-id="3760d-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3760d-121">OUTPUTS</span></span>

### <span data-ttu-id="3760d-122">Microsoft. Azure. commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3760d-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="3760d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3760d-123">NOTES</span></span>

## <span data-ttu-id="3760d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3760d-124">RELATED LINKS</span></span>

[<span data-ttu-id="3760d-125">Új – AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="3760d-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
