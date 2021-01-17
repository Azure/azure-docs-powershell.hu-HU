---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361939"
---
# <span data-ttu-id="fac7c-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fac7c-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="fac7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fac7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fac7c-103">Virtuális központi útvonaltábla-erőforrás törlése egy virtuális központhoz társítva.</span><span class="sxs-lookup"><span data-stu-id="fac7c-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="fac7c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fac7c-104">SYNTAX</span></span>

### <span data-ttu-id="fac7c-105">ByVirtualHubRouteTableName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fac7c-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac7c-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="fac7c-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac7c-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="fac7c-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fac7c-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="fac7c-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fac7c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fac7c-109">DESCRIPTION</span></span>
<span data-ttu-id="fac7c-110">Törli a megadott virtuális központhoz társított útvonaltáblát.</span><span class="sxs-lookup"><span data-stu-id="fac7c-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="fac7c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fac7c-111">EXAMPLES</span></span>

### <span data-ttu-id="fac7c-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="fac7c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="fac7c-113">Ez a parancs törli a virtuális hub westushubjáról a routeTable1-et.</span><span class="sxs-lookup"><span data-stu-id="fac7c-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="fac7c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fac7c-114">PARAMETERS</span></span>

### <span data-ttu-id="fac7c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fac7c-115">-AsJob</span></span>
<span data-ttu-id="fac7c-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="fac7c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fac7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fac7c-117">-DefaultProfile</span></span>
<span data-ttu-id="fac7c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fac7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fac7c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fac7c-119">-Force</span></span>
<span data-ttu-id="fac7c-120">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="fac7c-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fac7c-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="fac7c-121">-HubName</span></span>
<span data-ttu-id="fac7c-122">A szülőerőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fac7c-122">The parent resource name.</span></span>

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

### <span data-ttu-id="fac7c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fac7c-123">-InputObject</span></span>
<span data-ttu-id="fac7c-124">Az eltávolítható virtualhubroutetable erőforrás.</span><span class="sxs-lookup"><span data-stu-id="fac7c-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="fac7c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fac7c-125">-Name</span></span>
<span data-ttu-id="fac7c-126">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="fac7c-126">The resource name.</span></span>

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

### <span data-ttu-id="fac7c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fac7c-127">-PassThru</span></span>
<span data-ttu-id="fac7c-128">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtanunk.</span><span class="sxs-lookup"><span data-stu-id="fac7c-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="fac7c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fac7c-129">-ResourceGroupName</span></span>
<span data-ttu-id="fac7c-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fac7c-130">The resource group name.</span></span>

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

### <span data-ttu-id="fac7c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fac7c-131">-ResourceId</span></span>
<span data-ttu-id="fac7c-132">A virtuálishubroutetable eltávolítható erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="fac7c-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="fac7c-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="fac7c-133">-VirtualHub</span></span>
<span data-ttu-id="fac7c-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="fac7c-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="fac7c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fac7c-135">-Confirm</span></span>
<span data-ttu-id="fac7c-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="fac7c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fac7c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fac7c-137">-WhatIf</span></span>
<span data-ttu-id="fac7c-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="fac7c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fac7c-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fac7c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fac7c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fac7c-140">CommonParameters</span></span>
<span data-ttu-id="fac7c-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fac7c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fac7c-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fac7c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fac7c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fac7c-143">INPUTS</span></span>

### <span data-ttu-id="fac7c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fac7c-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="fac7c-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fac7c-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="fac7c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fac7c-146">System.String</span></span>

## <span data-ttu-id="fac7c-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fac7c-147">OUTPUTS</span></span>

### <span data-ttu-id="fac7c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fac7c-148">System.Boolean</span></span>

## <span data-ttu-id="fac7c-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fac7c-149">NOTES</span></span>

## <span data-ttu-id="fac7c-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fac7c-150">RELATED LINKS</span></span>
