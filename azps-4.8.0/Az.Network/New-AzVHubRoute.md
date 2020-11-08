---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVHubRoute.md
ms.openlocfilehash: 7dce18ce266bbd2e92f09039b1772acfc618dbdd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180504"
---
# <span data-ttu-id="973c7-101">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="973c7-101">New-AzVHubRoute</span></span>

## <span data-ttu-id="973c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="973c7-102">SYNOPSIS</span></span>
<span data-ttu-id="973c7-103">Létrehoz egy VHubRoute objektumot, amely paraméterként átadható a New-AzVHubRouteTable parancshoz.</span><span class="sxs-lookup"><span data-stu-id="973c7-103">Creates a VHubRoute object which can be passed as parameter to the New-AzVHubRouteTable command.</span></span>

## <span data-ttu-id="973c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="973c7-104">SYNTAX</span></span>

```powershell
New-AzVHubRoute -Name <String> -Destination <String[]> -DestinationType <String> -NextHop <String> -NextHopType <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="973c7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="973c7-105">DESCRIPTION</span></span>

<span data-ttu-id="973c7-106">VHubRoute objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="973c7-106">Creates a VHubRoute object.</span></span>

## <span data-ttu-id="973c7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="973c7-107">EXAMPLES</span></span>

### <span data-ttu-id="973c7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="973c7-108">Example 1</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $firewallName = "testFirewall"
PS C:\> $firewall = Get-AzFirewall -Name $firewallName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "private-traffic" -Destination @("10.30.0.0/16", "10.40.0.0/16") -DestinationType "CIDR" -NextHop $firewall.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/azureFirewalls/testFirewall
```

<span data-ttu-id="973c7-109">A fenti parancs egy VHubRoute objektumot hoz létre a nextHop-ban, és a megadott tűzfalon keresztül hozzáadható egy VHubRouteTable-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="973c7-109">The above command will create a VHubRoute object with nextHop as the specified Firewall which can then be added to a VHubRouteTable resource.</span></span>

### <span data-ttu-id="973c7-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="973c7-110">Example 2</span></span>

```powershell
PS C:\> $rgName = "testRg"
PS C:\> $hubName = "testHub"
PS C:\> $hubVnetConnName = "testHubVnetConn"
PS C:\> $hubVnetConnection = Get-AzVirtualHubVnetConnection -Name $hubVnetConnName -ParentResourceName $hubName -ResourceGroupName $rgName
PS C:\> New-AzVHubRoute -Name "nva-traffic" -Destination @("10.20.0.0/16", "10.50.0.0/16") -DestinationType "CIDR" -NextHop $hubVnetConnection.Id -NextHopType "ResourceId"

Name            : private-traffic
DestinationType : CIDR
Destinations    : {10.30.0.0/16, 10.40.0.0/16}
NextHopType     : ResourceId
NextHop         : /subscriptions/testSub/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubVirtualNetworkConnections/testHubVnetConn
```

<span data-ttu-id="973c7-111">A fenti parancs egy VHubRoute objektumot hoz létre a nextHop megadott hubVnetConnection, melyet aztán hozzáadhat egy VHubRouteTable-erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="973c7-111">The above command will create a VHubRoute object with nextHop as the specified hubVnetConnection which can then be added to a VHubRouteTable resource.</span></span>

## <span data-ttu-id="973c7-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="973c7-112">PARAMETERS</span></span>

### <span data-ttu-id="973c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973c7-113">-DefaultProfile</span></span>
<span data-ttu-id="973c7-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="973c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="973c7-115">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="973c7-115">-Destination</span></span>
<span data-ttu-id="973c7-116">A célhelyek listája.</span><span class="sxs-lookup"><span data-stu-id="973c7-116">List of Destinations.</span></span>

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

### <span data-ttu-id="973c7-117">-DestinationType</span><span class="sxs-lookup"><span data-stu-id="973c7-117">-DestinationType</span></span>
<span data-ttu-id="973c7-118">A rendeltetési hely típusa.</span><span class="sxs-lookup"><span data-stu-id="973c7-118">Type of Destinations.</span></span>

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

### <span data-ttu-id="973c7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="973c7-119">-Name</span></span>
<span data-ttu-id="973c7-120">Az útvonal neve.</span><span class="sxs-lookup"><span data-stu-id="973c7-120">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="973c7-121">-NextHop</span><span class="sxs-lookup"><span data-stu-id="973c7-121">-NextHop</span></span>
<span data-ttu-id="973c7-122">A következő Ugrás elemre.</span><span class="sxs-lookup"><span data-stu-id="973c7-122">The next hop.</span></span>

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

### <span data-ttu-id="973c7-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="973c7-123">-NextHopType</span></span>
<span data-ttu-id="973c7-124">A következő ugrás típusa</span><span class="sxs-lookup"><span data-stu-id="973c7-124">The Next Hop type.</span></span>

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

### <span data-ttu-id="973c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973c7-125">CommonParameters</span></span>
<span data-ttu-id="973c7-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="973c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973c7-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="973c7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973c7-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="973c7-128">INPUTS</span></span>

### <span data-ttu-id="973c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="973c7-129">System.String</span></span>

## <span data-ttu-id="973c7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="973c7-130">OUTPUTS</span></span>

### <span data-ttu-id="973c7-131">Microsoft. Azure. commands. Network. models. PSVHubRoute</span><span class="sxs-lookup"><span data-stu-id="973c7-131">Microsoft.Azure.Commands.Network.Models.PSVHubRoute</span></span>

## <span data-ttu-id="973c7-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="973c7-132">NOTES</span></span>

## <span data-ttu-id="973c7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="973c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="973c7-134">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="973c7-134">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="973c7-135">Új – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="973c7-135">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="973c7-136">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="973c7-136">Remove-AzVHubRouteTable</span></span>](./Remove-AzVHubRouteTable.md)

[<span data-ttu-id="973c7-137">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="973c7-137">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)