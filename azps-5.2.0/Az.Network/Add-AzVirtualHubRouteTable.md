---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359699"
---
# <span data-ttu-id="2cf12-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2cf12-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="2cf12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf12-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf12-103">Virtuális központi útválasztási tábla típusú erőforrást hoz létre, amely a VirtualHub gyermeke.</span><span class="sxs-lookup"><span data-stu-id="2cf12-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="2cf12-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2cf12-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf12-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2cf12-105">DESCRIPTION</span></span>
<span data-ttu-id="2cf12-106">A virtuális központi útvonaltábla-erőforrás tartalmazza az útvonalak és kapcsolatok listáját, amelyekhez csatolható, és a virtuális központban lévő forgalom útválasztásához használható.</span><span class="sxs-lookup"><span data-stu-id="2cf12-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="2cf12-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2cf12-107">EXAMPLES</span></span>

### <span data-ttu-id="2cf12-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="2cf12-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="2cf12-109">A fenti parancs létrehoz egy Virtual Hub Route Table erőforrást a neki átadott útvonalakból, és ez az objektum használható a virtuális központban lévő forgalom útválasztására.</span><span class="sxs-lookup"><span data-stu-id="2cf12-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="2cf12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cf12-110">PARAMETERS</span></span>

### <span data-ttu-id="2cf12-111">-Connection</span><span class="sxs-lookup"><span data-stu-id="2cf12-111">-Connection</span></span>
<span data-ttu-id="2cf12-112">Azon kapcsolatok listája, amelyekhez ez az útvonaltábla csatolva van.</span><span class="sxs-lookup"><span data-stu-id="2cf12-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="2cf12-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf12-113">-DefaultProfile</span></span>
<span data-ttu-id="2cf12-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cf12-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf12-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2cf12-115">-Name</span></span>
<span data-ttu-id="2cf12-116">Az útvonaltábla neve.</span><span class="sxs-lookup"><span data-stu-id="2cf12-116">Name of the route table.</span></span>

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

### <span data-ttu-id="2cf12-117">-Útvonal</span><span class="sxs-lookup"><span data-stu-id="2cf12-117">-Route</span></span>
<span data-ttu-id="2cf12-118">A virtuális központi útvonalak listája.</span><span class="sxs-lookup"><span data-stu-id="2cf12-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="2cf12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf12-119">CommonParameters</span></span>
<span data-ttu-id="2cf12-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf12-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cf12-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf12-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cf12-122">INPUTS</span></span>

### <span data-ttu-id="2cf12-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="2cf12-123">None</span></span>

## <span data-ttu-id="2cf12-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf12-124">OUTPUTS</span></span>

### <span data-ttu-id="2cf12-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2cf12-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="2cf12-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2cf12-126">NOTES</span></span>

## <span data-ttu-id="2cf12-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cf12-127">RELATED LINKS</span></span>
