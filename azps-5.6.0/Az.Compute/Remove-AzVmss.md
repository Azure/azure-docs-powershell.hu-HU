---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: 2ed7be0cf790a596a2a2fc9b23c0e6aa50f67623
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943097"
---
# <span data-ttu-id="252b9-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="252b9-101">Remove-AzVmss</span></span>

## <span data-ttu-id="252b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="252b9-102">SYNOPSIS</span></span>
<span data-ttu-id="252b9-103">Eltávolítja a VMSS-t vagy egy virtuális gépet, amely a VMSS-en belül található.</span><span class="sxs-lookup"><span data-stu-id="252b9-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="252b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="252b9-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252b9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="252b9-105">DESCRIPTION</span></span>
<span data-ttu-id="252b9-106">A **Remove-AzVmss** parancsmag eltávolítja a virtuálisgép-mérethalmazt (VMSS) az Azure-ból.</span><span class="sxs-lookup"><span data-stu-id="252b9-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="252b9-107">Ez a parancsmag a VMSS-en belül egy adott virtuális gép eltávolítására is használható.</span><span class="sxs-lookup"><span data-stu-id="252b9-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="252b9-108">A *InstanceId paraméter* használatával eltávolíthat egy adott virtuális gépet a VMSS-en belül.</span><span class="sxs-lookup"><span data-stu-id="252b9-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="252b9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="252b9-109">EXAMPLES</span></span>

### <span data-ttu-id="252b9-110">1. példa: VMSS eltávolítása</span><span class="sxs-lookup"><span data-stu-id="252b9-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="252b9-111">Ez a parancs eltávolítja a VMScaleSet001 nevű VMSS-t, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="252b9-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="252b9-112">2. példa: Virtuális gép eltávolítása a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="252b9-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="252b9-113">Ez a parancs eltávolítja a 3. példányazonosítójú virtuális gépet a VMScaleSet002 nevű VMSS-ről, amely a Group002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="252b9-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="252b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="252b9-114">PARAMETERS</span></span>

### <span data-ttu-id="252b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="252b9-115">-AsJob</span></span>
<span data-ttu-id="252b9-116">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="252b9-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252b9-117">-DefaultProfile</span></span>
<span data-ttu-id="252b9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="252b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="252b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="252b9-119">-Force</span></span>
<span data-ttu-id="252b9-120">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="252b9-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="252b9-121">-InstanceId</span></span>
<span data-ttu-id="252b9-122">Karakterlánc-tömbként megadja az elindítandó példányok azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="252b9-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="252b9-123">Például: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="252b9-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="252b9-125">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a VMSS tartozik.</span><span class="sxs-lookup"><span data-stu-id="252b9-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="252b9-126">-VMScaleSetName</span></span>
<span data-ttu-id="252b9-127">A parancsmag által eltávolított VMSS nevének fakása.</span><span class="sxs-lookup"><span data-stu-id="252b9-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="252b9-128">Ha megadja a *InstanceId paramétert,* a parancsmag eltávolítja a megadott virtuális gépet az ezzel a paraméterrel elnevezett VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="252b9-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="252b9-129">-Confirm</span></span>
<span data-ttu-id="252b9-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="252b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252b9-131">-WhatIf</span></span>
<span data-ttu-id="252b9-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="252b9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="252b9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="252b9-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252b9-134">CommonParameters</span></span>
<span data-ttu-id="252b9-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252b9-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="252b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252b9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="252b9-137">INPUTS</span></span>

### <span data-ttu-id="252b9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="252b9-138">System.String</span></span>

### <span data-ttu-id="252b9-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="252b9-139">System.String[]</span></span>

## <span data-ttu-id="252b9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="252b9-140">OUTPUTS</span></span>

### <span data-ttu-id="252b9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="252b9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="252b9-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="252b9-142">NOTES</span></span>

## <span data-ttu-id="252b9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="252b9-143">RELATED LINKS</span></span>

[<span data-ttu-id="252b9-144">Get-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="252b9-145">Új-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="252b9-146">Restart-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="252b9-147">Set-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="252b9-148">Start-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="252b9-149">Stop-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="252b9-150">Update-AzVms</span><span class="sxs-lookup"><span data-stu-id="252b9-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


