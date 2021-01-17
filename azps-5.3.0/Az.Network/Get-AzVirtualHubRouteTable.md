---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHubRouteTable.md
ms.openlocfilehash: bc93ba739a622a97f418dd7e01d4bbdc7d6824dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480335"
---
# <span data-ttu-id="94f2f-101">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="94f2f-101">Get-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="94f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="94f2f-103">Virtuális központi útválasztási táblát kap egy virtuális központban, vagy egy virtuális központban felsorolja az összes útválasztási táblát.</span><span class="sxs-lookup"><span data-stu-id="94f2f-103">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="94f2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="94f2f-104">SYNTAX</span></span>

### <span data-ttu-id="94f2f-105">ByVirtualHubName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94f2f-105">ByVirtualHubName (Default)</span></span>
```
Get-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f2f-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="94f2f-106">ByVirtualHubObject</span></span>
```
Get-AzVirtualHubRouteTable -VirtualHub <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94f2f-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="94f2f-107">ByVirtualHubResourceId</span></span>
```
Get-AzVirtualHubRouteTable -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94f2f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="94f2f-108">DESCRIPTION</span></span>
<span data-ttu-id="94f2f-109">Virtuális központi útválasztási táblát kap egy virtuális központban, vagy felsorolja egy virtuális központ összes útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="94f2f-109">Gets a Virtual Hub Route Table in a virtual hub or lists all route tables in a virtual hub.</span></span>

## <span data-ttu-id="94f2f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="94f2f-110">EXAMPLES</span></span>

### <span data-ttu-id="94f2f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="94f2f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"

Name                : routeTable1
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/westushub/routeTables/routeTable1
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   : Succeeded
```

<span data-ttu-id="94f2f-112">Ez a parancsmag beolvassa az útvonaltábla-erőforrást az erőforráscsoport neve, a központ neve és az útvonaltábla neve használatával.</span><span class="sxs-lookup"><span data-stu-id="94f2f-112">This cmdlet retrieves a route table resource using resource group name, hub name and the route table name.</span></span>

### <span data-ttu-id="94f2f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="94f2f-113">Example 2</span></span>
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

<span data-ttu-id="94f2f-114">Ez a parancsmag felsorolja a virtuális központban található összes útvonaltáblát, az erőforráscsoport nevét és a központi nevet használva.</span><span class="sxs-lookup"><span data-stu-id="94f2f-114">This cmdlet lists all route tables present in a virtual hub using resource group name and the hub name.</span></span>

## <span data-ttu-id="94f2f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f2f-115">PARAMETERS</span></span>

### <span data-ttu-id="94f2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f2f-116">-DefaultProfile</span></span>
<span data-ttu-id="94f2f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94f2f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f2f-118">-HubName</span><span class="sxs-lookup"><span data-stu-id="94f2f-118">-HubName</span></span>
<span data-ttu-id="94f2f-119">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="94f2f-119">The parent resource name.</span></span>

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

### <span data-ttu-id="94f2f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94f2f-120">-Name</span></span>
<span data-ttu-id="94f2f-121">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="94f2f-121">The resource name.</span></span>

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

### <span data-ttu-id="94f2f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="94f2f-122">-ParentResourceId</span></span>
<span data-ttu-id="94f2f-123">A szülőerőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94f2f-123">The parent resource id.</span></span>

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

### <span data-ttu-id="94f2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="94f2f-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="94f2f-125">The resource group name.</span></span>

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

### <span data-ttu-id="94f2f-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f2f-126">-VirtualHub</span></span>
<span data-ttu-id="94f2f-127">A szülőerőforrás.</span><span class="sxs-lookup"><span data-stu-id="94f2f-127">The parent resource.</span></span>

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

### <span data-ttu-id="94f2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f2f-128">CommonParameters</span></span>
<span data-ttu-id="94f2f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f2f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94f2f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f2f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94f2f-131">INPUTS</span></span>

### <span data-ttu-id="94f2f-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="94f2f-132">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="94f2f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="94f2f-133">System.String</span></span>

## <span data-ttu-id="94f2f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94f2f-134">OUTPUTS</span></span>

### <span data-ttu-id="94f2f-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="94f2f-135">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="94f2f-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="94f2f-136">NOTES</span></span>

## <span data-ttu-id="94f2f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94f2f-137">RELATED LINKS</span></span>
