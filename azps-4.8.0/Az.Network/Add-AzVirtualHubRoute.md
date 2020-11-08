---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024653"
---
# <span data-ttu-id="5e9b1-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5e9b1-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="5e9b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9b1-103">Létrehoz egy VirtualHubRoute objektumot, amely paraméterként átadható a Add-AzVirtualHubRouteTable parancshoz.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="5e9b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e9b1-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e9b1-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9b1-106">VirtualHubRoute objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="5e9b1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5e9b1-107">EXAMPLES</span></span>

### <span data-ttu-id="5e9b1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e9b1-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="5e9b1-109">A fenti parancs létrehoz egy VirtualHubRoute objektumot, amelyet azután hozzáadhat egy VirtualHubRouteTable-erőforráshoz, és beállíthatja egy VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="5e9b1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e9b1-110">PARAMETERS</span></span>

### <span data-ttu-id="5e9b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9b1-111">-DefaultProfile</span></span>
<span data-ttu-id="5e9b1-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e9b1-113">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="5e9b1-113">-Destination</span></span>
<span data-ttu-id="5e9b1-114">A célhelyek listája.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-114">List of Destinations.</span></span>

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

### <span data-ttu-id="5e9b1-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="5e9b1-115">-DestinationType</span></span>
<span data-ttu-id="5e9b1-116">A rendeltetési hely típusa.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="5e9b1-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="5e9b1-117">-NextHop</span></span>
<span data-ttu-id="5e9b1-118">A következő ugrások listája.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-118">List of Next hops.</span></span>

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

### <span data-ttu-id="5e9b1-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="5e9b1-119">-NextHopType</span></span>
<span data-ttu-id="5e9b1-120">A következő ugrás típusa</span><span class="sxs-lookup"><span data-stu-id="5e9b1-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="5e9b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9b1-121">CommonParameters</span></span>
<span data-ttu-id="5e9b1-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e9b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9b1-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5e9b1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9b1-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e9b1-124">INPUTS</span></span>

### <span data-ttu-id="5e9b1-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="5e9b1-125">None</span></span>

## <span data-ttu-id="5e9b1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e9b1-126">OUTPUTS</span></span>

### <span data-ttu-id="5e9b1-127">Microsoft. Azure. commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="5e9b1-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="5e9b1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e9b1-128">NOTES</span></span>

## <span data-ttu-id="5e9b1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e9b1-129">RELATED LINKS</span></span>
