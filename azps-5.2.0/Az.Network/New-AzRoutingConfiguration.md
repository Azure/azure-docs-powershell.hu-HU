---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutingconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRoutingConfiguration.md
ms.openlocfilehash: 31601c93a6979d09dfb3641cac079cba2757d043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327231"
---
# <span data-ttu-id="63a36-101">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a36-101">New-AzRoutingConfiguration</span></span>

## <span data-ttu-id="63a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a36-102">SYNOPSIS</span></span>
<span data-ttu-id="63a36-103">RoutingConfiguration objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a36-103">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="63a36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="63a36-104">SYNTAX</span></span>

```powershell
New-AzRoutingConfiguration -AssociatedRouteTable <String> -Label <String[]> -Id <String[]> [-StaticRoute <PSStaticRoute[]>]  [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63a36-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="63a36-105">DESCRIPTION</span></span>
<span data-ttu-id="63a36-106">RoutingConfiguration objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="63a36-106">Creates a RoutingConfiguration object.</span></span>

## <span data-ttu-id="63a36-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="63a36-107">EXAMPLES</span></span>

### <span data-ttu-id="63a36-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="63a36-108">Example 1</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
```

<span data-ttu-id="63a36-109">A fenti parancs létrehoz egy RoutingConfiguration objektumot, amelyet aztán hozzá lehet adni egy kapcsolaterőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="63a36-109">The above command will create a RoutingConfiguration object which can then be added to a connection resource.</span></span> <span data-ttu-id="63a36-110">A statikus útvonalak csak HubVirtualNetworkConnection objektum esetén engedélyezettek.</span><span class="sxs-lookup"><span data-stu-id="63a36-110">Static routes are only allowed with a HubVirtualNetworkConnection object.</span></span> 

## <span data-ttu-id="63a36-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63a36-111">PARAMETERS</span></span>

### <span data-ttu-id="63a36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63a36-112">-DefaultProfile</span></span>
<span data-ttu-id="63a36-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="63a36-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63a36-114">-AssociatedRouteTable</span><span class="sxs-lookup"><span data-stu-id="63a36-114">-AssociatedRouteTable</span></span>
<span data-ttu-id="63a36-115">Az útválasztási konfigurációhoz társított központi útválasztási tábla.</span><span class="sxs-lookup"><span data-stu-id="63a36-115">The hub route table associated with this routing configuration.</span></span>

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

### <span data-ttu-id="63a36-116">-Id</span><span class="sxs-lookup"><span data-stu-id="63a36-116">-Id</span></span>
<span data-ttu-id="63a36-117">A propagáltRouteTables tulajdonság útvonalait meghirdető összes központi útválasztási tábla erőforrás-azonosítóinak listája.</span><span class="sxs-lookup"><span data-stu-id="63a36-117">The list of resource ids of all the hub route tables to advertise the routes to for the PropagatedRouteTables property.</span></span>

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

### <span data-ttu-id="63a36-118">-Label</span><span class="sxs-lookup"><span data-stu-id="63a36-118">-Label</span></span>
<span data-ttu-id="63a36-119">A PropagáltRouteTables tulajdonság címkéinek listája.</span><span class="sxs-lookup"><span data-stu-id="63a36-119">The list of labels for the PropagatedRouteTables property.</span></span>

```yaml
Type: String[]
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a36-120">-StaticRoute</span><span class="sxs-lookup"><span data-stu-id="63a36-120">-StaticRoute</span></span>
<span data-ttu-id="63a36-121">Azon útvonalak listája, amelyek a VirtualHubról virtuális hálózati kapcsolatra irányítják az átirányítást.</span><span class="sxs-lookup"><span data-stu-id="63a36-121">List of routes that control routing from VirtualHub into a virtual network connection.</span></span>

```yaml
Type: PSStaticRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63a36-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a36-122">CommonParameters</span></span>
<span data-ttu-id="63a36-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63a36-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a36-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63a36-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a36-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63a36-125">INPUTS</span></span>

### <span data-ttu-id="63a36-126">System.String</span><span class="sxs-lookup"><span data-stu-id="63a36-126">System.String</span></span>

### <span data-ttu-id="63a36-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="63a36-127">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="63a36-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63a36-128">OUTPUTS</span></span>

### <span data-ttu-id="63a36-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="63a36-129">Microsoft.Azure.Commands.Network.Models.PSRoutingConfiguration</span></span>

## <span data-ttu-id="63a36-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="63a36-130">NOTES</span></span>

## <span data-ttu-id="63a36-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63a36-131">RELATED LINKS</span></span>

[<span data-ttu-id="63a36-132">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="63a36-132">New-AzStaticRoute</span></span>](./New-AzStaticRoute.md)

[<span data-ttu-id="63a36-133">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-133">New-AzExpressRouteConnection</span></span>](./New-AzExpressRouteConnection.md)

[<span data-ttu-id="63a36-134">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-134">Set-AzExpressRouteConnection</span></span>](./Set-AzExpressRouteConnection.md)

[<span data-ttu-id="63a36-135">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-135">New-AzVirtualHubVnetConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="63a36-136">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-136">Update-AzVirtualHubVnetConnection</span></span>](./Update-AzVpnConnection.md)

[<span data-ttu-id="63a36-137">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63a36-137">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="63a36-138">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="63a36-138">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)

[<span data-ttu-id="63a36-139">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-139">New-AzVpnConnection</span></span>](./New-AzVpnConnection.md)

[<span data-ttu-id="63a36-140">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="63a36-140">Update-AzVpnConnection</span></span>](./Update-AzVpnConnection.md)