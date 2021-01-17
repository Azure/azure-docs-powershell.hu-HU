---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324053"
---
# <span data-ttu-id="2f574-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f574-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="2f574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f574-102">SYNOPSIS</span></span>
<span data-ttu-id="2f574-103">Törölje a VirtualHubbal társított központi útvonaltábla-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="2f574-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="2f574-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2f574-104">SYNTAX</span></span>

### <span data-ttu-id="2f574-105">ByVHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f574-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f574-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="2f574-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f574-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="2f574-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f574-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="2f574-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f574-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2f574-109">DESCRIPTION</span></span>
<span data-ttu-id="2f574-110">Törli a megadott virtuális központhoz társított központi útválasztási táblát.</span><span class="sxs-lookup"><span data-stu-id="2f574-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="2f574-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2f574-111">EXAMPLES</span></span>

### <span data-ttu-id="2f574-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="2f574-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="2f574-113">Ez a parancs törli a virtuális központ központi útvonaltábláját.</span><span class="sxs-lookup"><span data-stu-id="2f574-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="2f574-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f574-114">PARAMETERS</span></span>

### <span data-ttu-id="2f574-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f574-115">-AsJob</span></span>
<span data-ttu-id="2f574-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="2f574-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f574-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f574-117">-DefaultProfile</span></span>
<span data-ttu-id="2f574-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f574-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f574-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2f574-119">-Force</span></span>
<span data-ttu-id="2f574-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="2f574-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2f574-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f574-121">-InputObject</span></span>
<span data-ttu-id="2f574-122">Az eltávolítható vhubroutetable erőforrás.</span><span class="sxs-lookup"><span data-stu-id="2f574-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="2f574-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2f574-123">-Name</span></span>
<span data-ttu-id="2f574-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2f574-124">The resource name.</span></span>

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

### <span data-ttu-id="2f574-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2f574-125">-ParentObject</span></span>
<span data-ttu-id="2f574-126">Az erőforrás szülő virtuális központi objektuma.</span><span class="sxs-lookup"><span data-stu-id="2f574-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="2f574-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="2f574-127">-ParentResourceName</span></span>
<span data-ttu-id="2f574-128">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2f574-128">The parent resource name.</span></span>

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

### <span data-ttu-id="2f574-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f574-129">-PassThru</span></span>
<span data-ttu-id="2f574-130">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="2f574-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2f574-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f574-131">-ResourceGroupName</span></span>
<span data-ttu-id="2f574-132">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2f574-132">The resource group name.</span></span>

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

### <span data-ttu-id="2f574-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f574-133">-ResourceId</span></span>
<span data-ttu-id="2f574-134">Az eltávolítható vhubroutetable erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="2f574-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="2f574-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f574-135">-Confirm</span></span>
<span data-ttu-id="2f574-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2f574-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f574-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f574-137">-WhatIf</span></span>
<span data-ttu-id="2f574-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2f574-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f574-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f574-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f574-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f574-140">CommonParameters</span></span>
<span data-ttu-id="2f574-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f574-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f574-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f574-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f574-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f574-143">INPUTS</span></span>

### <span data-ttu-id="2f574-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2f574-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="2f574-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f574-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="2f574-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2f574-146">System.String</span></span>

## <span data-ttu-id="2f574-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f574-147">OUTPUTS</span></span>

### <span data-ttu-id="2f574-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f574-148">System.Boolean</span></span>

## <span data-ttu-id="2f574-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2f574-149">NOTES</span></span>

## <span data-ttu-id="2f574-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f574-150">RELATED LINKS</span></span>

[<span data-ttu-id="2f574-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f574-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="2f574-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="2f574-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="2f574-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f574-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="2f574-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f574-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)