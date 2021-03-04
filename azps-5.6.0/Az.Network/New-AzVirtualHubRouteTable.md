---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRouteTable.md
ms.openlocfilehash: 5451a38b90f8903ef816a75ba7d7a27dd3aec5fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007718"
---
# <span data-ttu-id="77dbf-101">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="77dbf-101">New-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="77dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="77dbf-103">Létrehoz egy Azure Virtual Hub Útvonaltábla-objektumot.</span><span class="sxs-lookup"><span data-stu-id="77dbf-103">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="77dbf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77dbf-104">SYNTAX</span></span>

```
New-AzVirtualHubRouteTable -Route <PSVirtualHubRoute[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77dbf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77dbf-105">DESCRIPTION</span></span>
<span data-ttu-id="77dbf-106">Létrehoz egy Azure Virtual Hub Útvonaltábla-objektumot.</span><span class="sxs-lookup"><span data-stu-id="77dbf-106">Creates an Azure Virtual Hub Route Table object.</span></span>

## <span data-ttu-id="77dbf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77dbf-107">EXAMPLES</span></span>

### <span data-ttu-id="77dbf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="77dbf-108">Example 1</span></span>

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

<span data-ttu-id="77dbf-109">A fenti egy több útvonalból álló és egy új virtuális központhoz csatolt útvonaltáblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="77dbf-109">The above will create a route table composed of multiple routes and attached to a new virtual hub.</span></span>

<span data-ttu-id="77dbf-110">Ez egy olyan memóriában lévő objektum, amely egy Útvonal tábla új vagy meglévő VirtualHubhoz való hozzáadására használható.</span><span class="sxs-lookup"><span data-stu-id="77dbf-110">This is an in-memory object that can be used to add a Route table to a new or an existing VirtualHub.</span></span>

## <span data-ttu-id="77dbf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77dbf-111">PARAMETERS</span></span>

### <span data-ttu-id="77dbf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77dbf-112">-DefaultProfile</span></span>
<span data-ttu-id="77dbf-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77dbf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77dbf-114">-Útvonal</span><span class="sxs-lookup"><span data-stu-id="77dbf-114">-Route</span></span>
<span data-ttu-id="77dbf-115">A virtuális központi útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="77dbf-115">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="77dbf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dbf-116">CommonParameters</span></span>
<span data-ttu-id="77dbf-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dbf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dbf-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dbf-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dbf-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77dbf-119">INPUTS</span></span>

### <span data-ttu-id="77dbf-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="77dbf-120">None</span></span>

## <span data-ttu-id="77dbf-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77dbf-121">OUTPUTS</span></span>

### <span data-ttu-id="77dbf-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="77dbf-122">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="77dbf-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77dbf-123">NOTES</span></span>

## <span data-ttu-id="77dbf-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77dbf-124">RELATED LINKS</span></span>

[<span data-ttu-id="77dbf-125">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="77dbf-125">New-AzVirtualHubRoute</span></span>](./New-AzVirtualHubRoute.md)
