---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480337"
---
# <span data-ttu-id="610d4-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="610d4-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="610d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="610d4-102">SYNOPSIS</span></span>
<span data-ttu-id="610d4-103">Egy Azure VirtualHubot kap név és ResourceGroupName szerint, vagy felsorolja az összes virtuális központot ResourceGroupName/Subscription szerint.</span><span class="sxs-lookup"><span data-stu-id="610d4-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="610d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="610d4-104">SYNTAX</span></span>

### <span data-ttu-id="610d4-105">ListBySubscriptionId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="610d4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="610d4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610d4-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="610d4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="610d4-107">DESCRIPTION</span></span>
<span data-ttu-id="610d4-108">Egy Azure VirtualHubot kap név és ResourceGroupName szerint, vagy felsorolja az összes virtuális központot ResourceGroupName/Subscription szerint.</span><span class="sxs-lookup"><span data-stu-id="610d4-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="610d4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="610d4-109">EXAMPLES</span></span>

### <span data-ttu-id="610d4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="610d4-110">Example 1</span></span>

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

<span data-ttu-id="610d4-111">A fentiekkel létrehoz egy "testRG" erőforráscsoportot, egy virtuális WAN-t és egy virtuális központot az Azure-ban az adott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="610d4-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="610d4-112">A virtuális központ a "10.0.1.0/24" címterületet fogja rendelkezésre álló helyen.</span><span class="sxs-lookup"><span data-stu-id="610d4-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="610d4-113">Ezután a virtuális központ a ResourceGroupName és az ResourceName nevet használja.</span><span class="sxs-lookup"><span data-stu-id="610d4-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="610d4-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="610d4-114">Example 2</span></span>

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

<span data-ttu-id="610d4-115">Ez a parancsmag szűrést használva kapja meg a virtuális központot.</span><span class="sxs-lookup"><span data-stu-id="610d4-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="610d4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="610d4-116">PARAMETERS</span></span>

### <span data-ttu-id="610d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610d4-117">-DefaultProfile</span></span>
<span data-ttu-id="610d4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="610d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="610d4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="610d4-119">-Name</span></span>
<span data-ttu-id="610d4-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="610d4-120">The resource name.</span></span>

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

### <span data-ttu-id="610d4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610d4-121">-ResourceGroupName</span></span>
<span data-ttu-id="610d4-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="610d4-122">The resource group name.</span></span>

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

### <span data-ttu-id="610d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610d4-123">CommonParameters</span></span>
<span data-ttu-id="610d4-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610d4-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="610d4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610d4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="610d4-126">INPUTS</span></span>

### <span data-ttu-id="610d4-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="610d4-127">None</span></span>

## <span data-ttu-id="610d4-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="610d4-128">OUTPUTS</span></span>

### <span data-ttu-id="610d4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="610d4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="610d4-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="610d4-130">NOTES</span></span>

## <span data-ttu-id="610d4-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="610d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="610d4-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="610d4-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="610d4-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="610d4-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="610d4-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="610d4-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
