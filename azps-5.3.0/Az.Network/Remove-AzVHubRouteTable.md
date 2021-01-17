---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481192"
---
# <span data-ttu-id="00592-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="00592-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="00592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00592-102">SYNOPSIS</span></span>
<span data-ttu-id="00592-103">Törölje a VirtualHubbal társított központi útvonaltábla-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="00592-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="00592-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00592-104">SYNTAX</span></span>

### <span data-ttu-id="00592-105">ByVHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00592-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00592-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="00592-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00592-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="00592-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00592-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="00592-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00592-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00592-109">DESCRIPTION</span></span>
<span data-ttu-id="00592-110">Törli a megadott virtuális központhoz társított központi útválasztási táblát.</span><span class="sxs-lookup"><span data-stu-id="00592-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="00592-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00592-111">EXAMPLES</span></span>

### <span data-ttu-id="00592-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="00592-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="00592-113">Ez a parancs törli a virtuális központ központi útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="00592-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="00592-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00592-114">PARAMETERS</span></span>

### <span data-ttu-id="00592-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00592-115">-AsJob</span></span>
<span data-ttu-id="00592-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="00592-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00592-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00592-117">-DefaultProfile</span></span>
<span data-ttu-id="00592-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00592-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00592-119">-Force</span><span class="sxs-lookup"><span data-stu-id="00592-119">-Force</span></span>
<span data-ttu-id="00592-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="00592-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="00592-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00592-121">-InputObject</span></span>
<span data-ttu-id="00592-122">Az eltávolítható vhubroutetable erőforrás.</span><span class="sxs-lookup"><span data-stu-id="00592-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="00592-123">-Name</span><span class="sxs-lookup"><span data-stu-id="00592-123">-Name</span></span>
<span data-ttu-id="00592-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="00592-124">The resource name.</span></span>

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

### <span data-ttu-id="00592-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="00592-125">-ParentObject</span></span>
<span data-ttu-id="00592-126">Az erőforrás szülő virtuális központi objektuma.</span><span class="sxs-lookup"><span data-stu-id="00592-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="00592-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="00592-127">-ParentResourceName</span></span>
<span data-ttu-id="00592-128">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="00592-128">The parent resource name.</span></span>

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

### <span data-ttu-id="00592-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00592-129">-PassThru</span></span>
<span data-ttu-id="00592-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="00592-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="00592-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00592-131">-ResourceGroupName</span></span>
<span data-ttu-id="00592-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00592-132">The resource group name.</span></span>

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

### <span data-ttu-id="00592-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00592-133">-ResourceId</span></span>
<span data-ttu-id="00592-134">Az eltávolítható vhubroutetable erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00592-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="00592-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00592-135">-Confirm</span></span>
<span data-ttu-id="00592-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="00592-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00592-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00592-137">-WhatIf</span></span>
<span data-ttu-id="00592-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="00592-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00592-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="00592-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00592-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00592-140">CommonParameters</span></span>
<span data-ttu-id="00592-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00592-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00592-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00592-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00592-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00592-143">INPUTS</span></span>

### <span data-ttu-id="00592-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="00592-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="00592-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="00592-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="00592-146">System.String</span><span class="sxs-lookup"><span data-stu-id="00592-146">System.String</span></span>

## <span data-ttu-id="00592-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00592-147">OUTPUTS</span></span>

### <span data-ttu-id="00592-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00592-148">System.Boolean</span></span>

## <span data-ttu-id="00592-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00592-149">NOTES</span></span>

## <span data-ttu-id="00592-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00592-150">RELATED LINKS</span></span>

[<span data-ttu-id="00592-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="00592-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="00592-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="00592-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="00592-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="00592-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="00592-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="00592-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)