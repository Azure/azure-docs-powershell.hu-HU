---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024585"
---
# <span data-ttu-id="ac467-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac467-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="ac467-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ac467-102">SYNOPSIS</span></span>
<span data-ttu-id="ac467-103">Virtuális hub-hoz tartozó útválasztási táblázat erőforrásának törlése</span><span class="sxs-lookup"><span data-stu-id="ac467-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="ac467-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ac467-104">SYNTAX</span></span>

### <span data-ttu-id="ac467-105">ByVirtualHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac467-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac467-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="ac467-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac467-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="ac467-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac467-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="ac467-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac467-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="ac467-109">DESCRIPTION</span></span>
<span data-ttu-id="ac467-110">Törli a megadott virtuális központhoz társított útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ac467-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="ac467-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ac467-111">EXAMPLES</span></span>

### <span data-ttu-id="ac467-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ac467-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="ac467-113">Ez a parancs törli a virtuális hub-westushub routeTable1.</span><span class="sxs-lookup"><span data-stu-id="ac467-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="ac467-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ac467-114">PARAMETERS</span></span>

### <span data-ttu-id="ac467-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac467-115">-AsJob</span></span>
<span data-ttu-id="ac467-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ac467-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac467-117">-DefaultProfile</span></span>
<span data-ttu-id="ac467-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac467-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac467-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ac467-119">-Force</span></span>
<span data-ttu-id="ac467-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac467-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="ac467-121">-HubName</span></span>
<span data-ttu-id="ac467-122">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ac467-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac467-123">-InputObject</span></span>
<span data-ttu-id="ac467-124">Az eltávolítandó virtualhubroutetable-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ac467-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ac467-125">-Name</span></span>
<span data-ttu-id="ac467-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ac467-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac467-127">-PassThru</span></span>
<span data-ttu-id="ac467-128">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="ac467-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac467-129">-ResourceGroupName</span></span>
<span data-ttu-id="ac467-130">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac467-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac467-131">-ResourceId</span></span>
<span data-ttu-id="ac467-132">Az eltávolítandó virtualhubroutetable erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ac467-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="ac467-133">-VirtualHub</span></span>
<span data-ttu-id="ac467-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="ac467-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ac467-135">-Confirm</span></span>
<span data-ttu-id="ac467-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ac467-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac467-137">-WhatIf</span></span>
<span data-ttu-id="ac467-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ac467-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac467-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac467-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac467-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac467-140">CommonParameters</span></span>
<span data-ttu-id="ac467-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ac467-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac467-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ac467-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac467-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac467-143">INPUTS</span></span>

### <span data-ttu-id="ac467-144">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="ac467-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="ac467-145">Microsoft. Azure. commands. Network. models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="ac467-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="ac467-146">System. String</span><span class="sxs-lookup"><span data-stu-id="ac467-146">System.String</span></span>

## <span data-ttu-id="ac467-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac467-147">OUTPUTS</span></span>

### <span data-ttu-id="ac467-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac467-148">System.Boolean</span></span>

## <span data-ttu-id="ac467-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ac467-149">NOTES</span></span>

## <span data-ttu-id="ac467-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac467-150">RELATED LINKS</span></span>
