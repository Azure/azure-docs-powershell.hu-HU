---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRoute.md
ms.openlocfilehash: 84a1de629e983e78531faa9f33c33f43df4c5372
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339402"
---
# <span data-ttu-id="acbb0-101">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="acbb0-101">Add-AzVirtualHubRoute</span></span>

## <span data-ttu-id="acbb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="acbb0-103">VirtualHubRoute-objektumot hoz létre, amely paraméterként továbbkalmazható a Add-AzVirtualHubRouteTable parancsnak.</span><span class="sxs-lookup"><span data-stu-id="acbb0-103">Creates a VirtualHubRoute object which can be passed as parameter to the Add-AzVirtualHubRouteTable command.</span></span> 

## <span data-ttu-id="acbb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acbb0-104">SYNTAX</span></span>

```
Add-AzVirtualHubRoute -Destination <String[]> -DestinationType <String> -NextHop <String[]>
 -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acbb0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acbb0-105">DESCRIPTION</span></span>
<span data-ttu-id="acbb0-106">VirtualHubRoute-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="acbb0-106">Creates a VirtualHubRoute object.</span></span>

## <span data-ttu-id="acbb0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acbb0-107">EXAMPLES</span></span>

### <span data-ttu-id="acbb0-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="acbb0-108">Example 1</span></span>
```powershell
PS C:\> Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")

AddressPrefixes  : {10.4.0.0/16, 10.5.0.0/16}
NextHopIpAddress : 10.0.0.68
DestinationType  : CIDR
Destinations     : {10.4.0.0/16, 10.5.0.0/16}
NextHopType      : IPAddress
NextHops         : {10.0.0.68}
```

<span data-ttu-id="acbb0-109">A fenti parancs létrehoz egy VirtualHubRoute-objektumot, amelyet aztán hozzá lehet adni egy VirtualHubRouteTable erőforráshoz, és virtualhubra lehet állítani.</span><span class="sxs-lookup"><span data-stu-id="acbb0-109">The above command will create a VirtualHubRoute object which can then be added to a VirtualHubRouteTable resource and set to a VirtualHub.</span></span>

## <span data-ttu-id="acbb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acbb0-110">PARAMETERS</span></span>

### <span data-ttu-id="acbb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbb0-111">-DefaultProfile</span></span>
<span data-ttu-id="acbb0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acbb0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acbb0-113">-Destination</span><span class="sxs-lookup"><span data-stu-id="acbb0-113">-Destination</span></span>
<span data-ttu-id="acbb0-114">A célországok listája.</span><span class="sxs-lookup"><span data-stu-id="acbb0-114">List of Destinations.</span></span>

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

### <span data-ttu-id="acbb0-115">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="acbb0-115">-DestinationType</span></span>
<span data-ttu-id="acbb0-116">A célhely típusa.</span><span class="sxs-lookup"><span data-stu-id="acbb0-116">Type of Destinations.</span></span>

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

### <span data-ttu-id="acbb0-117">-NextHop</span><span class="sxs-lookup"><span data-stu-id="acbb0-117">-NextHop</span></span>
<span data-ttu-id="acbb0-118">A következő ugrások listája.</span><span class="sxs-lookup"><span data-stu-id="acbb0-118">List of Next hops.</span></span>

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

### <span data-ttu-id="acbb0-119">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="acbb0-119">-NextHopType</span></span>
<span data-ttu-id="acbb0-120">A következő ugrás típusa</span><span class="sxs-lookup"><span data-stu-id="acbb0-120">The Next Hop type.</span></span>

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

### <span data-ttu-id="acbb0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbb0-121">CommonParameters</span></span>
<span data-ttu-id="acbb0-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbb0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbb0-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acbb0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbb0-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acbb0-124">INPUTS</span></span>

### <span data-ttu-id="acbb0-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="acbb0-125">None</span></span>

## <span data-ttu-id="acbb0-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acbb0-126">OUTPUTS</span></span>

### <span data-ttu-id="acbb0-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="acbb0-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="acbb0-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acbb0-128">NOTES</span></span>

## <span data-ttu-id="acbb0-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acbb0-129">RELATED LINKS</span></span>
