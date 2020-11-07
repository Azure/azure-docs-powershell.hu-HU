---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: d4945c93fdfb402e56e1822229a1bb9592951d20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670490"
---
# <span data-ttu-id="5bc38-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bc38-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="5bc38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bc38-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc38-103">Az Azure VirtualHub név és ResourceGroupName alapján kapja meg, vagy felsorolja az összes virtuális hub-ot ResourceGroupName/előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="5bc38-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="5bc38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bc38-104">SYNTAX</span></span>

### <span data-ttu-id="5bc38-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5bc38-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bc38-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc38-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bc38-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bc38-107">DESCRIPTION</span></span>
<span data-ttu-id="5bc38-108">Az Azure VirtualHub név és ResourceGroupName alapján kapja meg, vagy felsorolja az összes virtuális hub-ot ResourceGroupName/előfizetéssel.</span><span class="sxs-lookup"><span data-stu-id="5bc38-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="5bc38-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5bc38-109">EXAMPLES</span></span>

### <span data-ttu-id="5bc38-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5bc38-110">Example 1</span></span>

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

<span data-ttu-id="5bc38-111">A fenti létrehoz egy erőforráscsoport "testRG", egy virtuális WAN és egy virtuális hub a West US-ben az Azure-beli erőforrás-csoportban.</span><span class="sxs-lookup"><span data-stu-id="5bc38-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="5bc38-112">A virtuális hub a "10.0.1.0/24" címterületet fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="5bc38-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="5bc38-113">Ezután a virtuális hubot a ResourceGroupName és a ResourceName segítségével kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5bc38-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="5bc38-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="5bc38-114">Example 2</span></span>

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

<span data-ttu-id="5bc38-115">Ez a parancsmag a virtuális hubot szűréssel kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5bc38-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="5bc38-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bc38-116">PARAMETERS</span></span>

### <span data-ttu-id="5bc38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc38-117">-DefaultProfile</span></span>
<span data-ttu-id="5bc38-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bc38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc38-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bc38-119">-Name</span></span>
<span data-ttu-id="5bc38-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="5bc38-120">The resource name.</span></span>

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

### <span data-ttu-id="5bc38-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc38-121">-ResourceGroupName</span></span>
<span data-ttu-id="5bc38-122">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5bc38-122">The resource group name.</span></span>

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

### <span data-ttu-id="5bc38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc38-123">CommonParameters</span></span>
<span data-ttu-id="5bc38-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bc38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc38-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5bc38-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc38-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bc38-126">INPUTS</span></span>

### <span data-ttu-id="5bc38-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="5bc38-127">None</span></span>

## <span data-ttu-id="5bc38-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bc38-128">OUTPUTS</span></span>

### <span data-ttu-id="5bc38-129">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bc38-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="5bc38-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bc38-130">NOTES</span></span>

## <span data-ttu-id="5bc38-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bc38-131">RELATED LINKS</span></span>

[<span data-ttu-id="5bc38-132">Új – AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bc38-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="5bc38-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bc38-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="5bc38-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="5bc38-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
