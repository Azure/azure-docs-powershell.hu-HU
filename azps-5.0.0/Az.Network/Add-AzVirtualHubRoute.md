---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195597"
---
# <span data-ttu-id="74870-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="74870-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="74870-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74870-102">SYNOPSIS</span></span>
<span data-ttu-id="74870-103">Létrehoz egy VirtualHubRoute objektumot, amely paraméterként átadható a Add-AzVirtualHubRouteTable parancshoz.</span><span class="sxs-lookup"><span data-stu-id="74870-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="74870-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74870-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74870-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="74870-105">DESCRIPTION</span></span>
<span data-ttu-id="74870-106">VirtualHubRoute objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="74870-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="74870-107">Példák</span><span class="sxs-lookup"><span data-stu-id="74870-107">EXAMPLES</span></span>

### <span data-ttu-id="74870-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74870-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="74870-109">A fenti parancs létrehoz egy VirtualHubRoute objektumot, amelyet azután hozzáadhat egy VirtualHubRouteTable-erőforráshoz, és beállíthatja egy VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="74870-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="74870-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74870-110">PARAMETERS</span></span>

### <span data-ttu-id="74870-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74870-111">-DefaultProfile</span></span>
<span data-ttu-id="74870-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74870-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74870-113">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="74870-113">-Destination</span></span>
<span data-ttu-id="74870-114">A célhelyek listája.</span><span class="sxs-lookup"><span data-stu-id="74870-114">List of Destinations.</span></span>

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

### <span data-ttu-id="74870-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="74870-115">-DestinationType</span></span>
<span data-ttu-id="74870-116">A rendeltetési hely típusa.</span><span class="sxs-lookup"><span data-stu-id="74870-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="74870-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="74870-117">-NextHop</span></span>
<span data-ttu-id="74870-118">A következő ugrások listája.</span><span class="sxs-lookup"><span data-stu-id="74870-118">List of Next hops.</span></span>

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

### <span data-ttu-id="74870-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="74870-119">-NextHopType</span></span>
<span data-ttu-id="74870-120">A következő ugrás típusa</span><span class="sxs-lookup"><span data-stu-id="74870-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="74870-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74870-121">CommonParameters</span></span>
<span data-ttu-id="74870-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74870-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74870-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74870-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74870-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74870-124">INPUTS</span></span>

### <span data-ttu-id="74870-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="74870-125">None</span></span>

## <span data-ttu-id="74870-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74870-126">OUTPUTS</span></span>

### <span data-ttu-id="74870-127">Microsoft. Azure. commands. Network. models. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="74870-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="74870-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74870-128">NOTES</span></span>

## <span data-ttu-id="74870-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74870-129">RELATED LINKS</span></span>
