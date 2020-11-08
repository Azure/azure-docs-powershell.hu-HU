---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194287"
---
# <span data-ttu-id="73562-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73562-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="73562-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73562-102">SYNOPSIS</span></span>
<span data-ttu-id="73562-103">Virtuális hub-útválasztót kap egy virtuális központban, vagy felsorolja az összes útválasztási táblázatot egy virtuális központban.</span><span class="sxs-lookup"><span data-stu-id="73562-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="73562-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73562-104">SYNTAX</span></span>

### <span data-ttu-id="73562-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73562-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73562-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="73562-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73562-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="73562-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73562-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="73562-108">DESCRIPTION</span></span>
<span data-ttu-id="73562-109">Virtuális hub-útválasztót kap egy virtuális központban, vagy felsorolja az összes útválasztási táblázatot egy virtuális központban.</span><span class="sxs-lookup"><span data-stu-id="73562-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="73562-110">Példák</span><span class="sxs-lookup"><span data-stu-id="73562-110">EXAMPLES</span></span>

### <span data-ttu-id="73562-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="73562-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="73562-112">Ez a parancsmag az útvonalcsoport-erőforrást az erőforrás csoport neve, a hub neve és az útvonalkártya neve segítségével veszi át.</span><span class="sxs-lookup"><span data-stu-id="73562-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="73562-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="73562-113">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded

Name                : routeTable2
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable2
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Branches}
ProvisioningState   : Succeeded
```

<span data-ttu-id="73562-114">Ez a parancsmag a virtuális hub-ban található összes útválasztási táblázatot felsorolja az erőforráscsoport neve és a hub neve segítségével.</span><span class="sxs-lookup"><span data-stu-id="73562-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="73562-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73562-115">PARAMETERS</span></span>

### <span data-ttu-id="73562-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73562-116">-DefaultProfile</span></span>
<span data-ttu-id="73562-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73562-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73562-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="73562-118">-HubName</span></span>
<span data-ttu-id="73562-119">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="73562-119">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73562-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="73562-120">-Name</span></span>
<span data-ttu-id="73562-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="73562-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualHubRouteTableName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73562-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73562-122">-ParentResourceId</span></span>
<span data-ttu-id="73562-123">A szülő erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="73562-123">The parent resource id.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73562-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73562-124">-ResourceGroupName</span></span>
<span data-ttu-id="73562-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="73562-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73562-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="73562-126">-VirtualHub</span></span>
<span data-ttu-id="73562-127">A fölérendelt erőforrás.</span><span class="sxs-lookup"><span data-stu-id="73562-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentObject, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73562-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73562-128">CommonParameters</span></span>
<span data-ttu-id="73562-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73562-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73562-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73562-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73562-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73562-131">INPUTS</span></span>

### <span data-ttu-id="73562-132">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="73562-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="73562-133">System. String</span><span class="sxs-lookup"><span data-stu-id="73562-133">System.String</span></span>

## <span data-ttu-id="73562-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73562-134">OUTPUTS</span></span>

### <span data-ttu-id="73562-135">Microsoft. Azure. commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="73562-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="73562-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73562-136">NOTES</span></span>

## <span data-ttu-id="73562-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73562-137">RELATED LINKS</span></span>