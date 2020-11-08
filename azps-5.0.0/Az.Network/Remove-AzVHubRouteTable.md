---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188102"
---
# <span data-ttu-id="c81f1-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c81f1-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="c81f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c81f1-102">SYNOPSIS</span></span>
<span data-ttu-id="c81f1-103">A VirtualHub társított hub Route Table-erőforrás törlése</span><span class="sxs-lookup"><span data-stu-id="c81f1-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="c81f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c81f1-104">SYNTAX</span></span>

### <span data-ttu-id="c81f1-105">ByVHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c81f1-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81f1-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="c81f1-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81f1-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="c81f1-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c81f1-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="c81f1-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c81f1-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c81f1-109">DESCRIPTION</span></span>
<span data-ttu-id="c81f1-110">Törli a megadott virtuális központtal társított központi útválasztási táblázatot.</span><span class="sxs-lookup"><span data-stu-id="c81f1-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="c81f1-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c81f1-111">EXAMPLES</span></span>

### <span data-ttu-id="c81f1-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c81f1-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="c81f1-113">Ez a parancs törli a virtuális hub központi útválasztási táblázatát.</span><span class="sxs-lookup"><span data-stu-id="c81f1-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="c81f1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c81f1-114">PARAMETERS</span></span>

### <span data-ttu-id="c81f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c81f1-115">-AsJob</span></span>
<span data-ttu-id="c81f1-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c81f1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c81f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81f1-117">-DefaultProfile</span></span>
<span data-ttu-id="c81f1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c81f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81f1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c81f1-119">-Force</span></span>
<span data-ttu-id="c81f1-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c81f1-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c81f1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c81f1-121">-InputObject</span></span>
<span data-ttu-id="c81f1-122">Az eltávolítandó vhubroutetable-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="c81f1-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c81f1-123">-Name</span></span>
<span data-ttu-id="c81f1-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c81f1-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c81f1-125">-ParentObject</span></span>
<span data-ttu-id="c81f1-126">Az erőforrás fölérendelt virtuális hub objektuma.</span><span class="sxs-lookup"><span data-stu-id="c81f1-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c81f1-127">-ParentResourceName</span></span>
<span data-ttu-id="c81f1-128">A szülő-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c81f1-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c81f1-129">-PassThru</span></span>
<span data-ttu-id="c81f1-130">Egy olyan objektumot ad eredményül, amely azt az elemet jeleníti meg, amelyen a művelet végre van hajtva.</span><span class="sxs-lookup"><span data-stu-id="c81f1-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c81f1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81f1-131">-ResourceGroupName</span></span>
<span data-ttu-id="c81f1-132">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c81f1-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c81f1-133">-ResourceId</span></span>
<span data-ttu-id="c81f1-134">Az eltávolítandó vhubroutetable erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c81f1-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c81f1-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c81f1-135">-Confirm</span></span>
<span data-ttu-id="c81f1-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c81f1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81f1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81f1-137">-WhatIf</span></span>
<span data-ttu-id="c81f1-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c81f1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81f1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c81f1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81f1-140">CommonParameters</span></span>
<span data-ttu-id="c81f1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c81f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81f1-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c81f1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81f1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c81f1-143">INPUTS</span></span>

### <span data-ttu-id="c81f1-144">Microsoft. Azure. commands. Network. models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c81f1-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c81f1-145">Microsoft. Azure. commands. Network. models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c81f1-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="c81f1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c81f1-146">System.String</span></span>

## <span data-ttu-id="c81f1-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c81f1-147">OUTPUTS</span></span>

### <span data-ttu-id="c81f1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c81f1-148">System.Boolean</span></span>

## <span data-ttu-id="c81f1-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c81f1-149">NOTES</span></span>

## <span data-ttu-id="c81f1-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c81f1-150">RELATED LINKS</span></span>

[<span data-ttu-id="c81f1-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c81f1-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="c81f1-152">Új – AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="c81f1-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="c81f1-153">Új – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c81f1-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="c81f1-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="c81f1-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)