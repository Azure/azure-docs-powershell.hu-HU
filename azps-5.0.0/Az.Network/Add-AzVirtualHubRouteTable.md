---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303737"
---
# <span data-ttu-id="591af-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="591af-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="591af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="591af-102">SYNOPSIS</span></span>
<span data-ttu-id="591af-103">Létrehoz egy virtuális hub Route Table-erőforrást, amely a VirtualHub gyermeke.</span><span class="sxs-lookup"><span data-stu-id="591af-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="591af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="591af-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="591af-105">DESCRIPTION</span></span>
<span data-ttu-id="591af-106">A virtuális hub Route Table (virtuális hub) erőforrás az útvonalak listáját tartalmazza, és azokat a kapcsolatokat sorolja fel, amelyekhez hozzá lehet rendelni, és a forgalmat egy virtuális központban kell átirányítani.</span><span class="sxs-lookup"><span data-stu-id="591af-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="591af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="591af-107">EXAMPLES</span></span>

### <span data-ttu-id="591af-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="591af-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="591af-109">A fenti parancs létrehozza a virtuális hub Route Table-erőforrást az átadott útvonalon, és ezt az objektumot a virtuális központ útválasztási forgalmához használhatja.</span><span class="sxs-lookup"><span data-stu-id="591af-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="591af-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="591af-110">PARAMETERS</span></span>

### <span data-ttu-id="591af-111">-Kapcsolat</span><span class="sxs-lookup"><span data-stu-id="591af-111">-Connection</span></span>
<span data-ttu-id="591af-112">Azon kapcsolatok listája, amelyekhez az útválasztási táblázat van csatolva.</span><span class="sxs-lookup"><span data-stu-id="591af-112">List of connections this route table is attached to.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591af-113">-DefaultProfile</span></span>
<span data-ttu-id="591af-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="591af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591af-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="591af-115">-Name</span></span>
<span data-ttu-id="591af-116">Az útválasztási táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="591af-116">Name of the route table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591af-117">– Útvonal</span><span class="sxs-lookup"><span data-stu-id="591af-117">-Route</span></span>
<span data-ttu-id="591af-118">A virtuális hub-útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="591af-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591af-119">CommonParameters</span></span>
<span data-ttu-id="591af-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="591af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591af-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="591af-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591af-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="591af-122">INPUTS</span></span>

### <span data-ttu-id="591af-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="591af-123">None</span></span>

## <span data-ttu-id="591af-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="591af-124">OUTPUTS</span></span>

### <span data-ttu-id="591af-125">Microsoft. Azure. commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="591af-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="591af-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="591af-126">NOTES</span></span>

## <span data-ttu-id="591af-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="591af-127">RELATED LINKS</span></span>
