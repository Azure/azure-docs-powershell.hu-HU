---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013284"
---
# <span data-ttu-id="0ad6b-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0ad6b-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="0ad6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ad6b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad6b-103">Az Azure VirtualHub név és ResourceGroupName alapján kapja meg, vagy felsorolja az összes virtuális hub-ot ResourceGroupName/előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="0ad6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ad6b-104">SYNTAX</span></span>

### <span data-ttu-id="0ad6b-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ad6b-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad6b-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad6b-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad6b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ad6b-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad6b-108">Az Azure VirtualHub név és ResourceGroupName alapján kapja meg, vagy felsorolja az összes virtuális hub-ot ResourceGroupName/előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="0ad6b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0ad6b-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad6b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ad6b-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0ad6b-111">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="0ad6b-112">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="0ad6b-113">Ezután a virtuális hubot a ResourceGroupName és a ResourceName segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="0ad6b-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="0ad6b-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="0ad6b-115">Ez a parancsmag a virtuális hubot szűréssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="0ad6b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ad6b-116">PARAMETERS</span></span>

### <span data-ttu-id="0ad6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad6b-117">-DefaultProfile</span></span>
<span data-ttu-id="0ad6b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad6b-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0ad6b-119">-Name</span></span>
<span data-ttu-id="0ad6b-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0ad6b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad6b-121">-ResourceGroupName</span></span>
<span data-ttu-id="0ad6b-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0ad6b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad6b-123">CommonParameters</span></span>
<span data-ttu-id="0ad6b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ad6b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad6b-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ad6b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad6b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad6b-126">INPUTS</span></span>

### <span data-ttu-id="0ad6b-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ad6b-127">None</span></span>

## <span data-ttu-id="0ad6b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ad6b-128">OUTPUTS</span></span>

### <span data-ttu-id="0ad6b-129">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0ad6b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0ad6b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ad6b-130">NOTES</span></span>

## <span data-ttu-id="0ad6b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ad6b-131">RELATED LINKS</span></span>

[<span data-ttu-id="0ad6b-132">Új – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0ad6b-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="0ad6b-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0ad6b-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="0ad6b-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0ad6b-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
