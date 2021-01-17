---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480765"
---
# <span data-ttu-id="d37ee-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d37ee-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="d37ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d37ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d37ee-103">Eltávolít egy adatlemezt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="d37ee-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="d37ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d37ee-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d37ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d37ee-106">Az **Remove-AzVMDataDisk** parancsmag eltávolít egy adatlemezt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="d37ee-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="d37ee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d37ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d37ee-108">1. példa: Adatlemez eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="d37ee-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="d37ee-109">Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg **a Get-AzVM parancsmag** használatával.</span><span class="sxs-lookup"><span data-stu-id="d37ee-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="d37ee-110">A parancs a virtuális gépet a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="d37ee-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d37ee-111">A második parancs eltávolítja a Lemez3 nevű adatlemezt a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d37ee-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="d37ee-112">Az utolsó parancs frissíti a ResourceGroup11-ben $VirtualMachine virtuális gép állapotát.</span><span class="sxs-lookup"><span data-stu-id="d37ee-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="d37ee-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d37ee-113">PARAMETERS</span></span>

### <span data-ttu-id="d37ee-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="d37ee-114">-DataDiskNames</span></span>
<span data-ttu-id="d37ee-115">A parancsmag által eltávolított egy vagy több adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d37ee-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d37ee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37ee-116">-DefaultProfile</span></span>
<span data-ttu-id="d37ee-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d37ee-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d37ee-118">-VM</span><span class="sxs-lookup"><span data-stu-id="d37ee-118">-VM</span></span>
<span data-ttu-id="d37ee-119">Azt a helyi virtuális gépobjektumot adja meg, amelyből el szeretné távolítani az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="d37ee-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="d37ee-120">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d37ee-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d37ee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d37ee-121">-Confirm</span></span>
<span data-ttu-id="d37ee-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d37ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37ee-123">-WhatIf</span></span>
<span data-ttu-id="d37ee-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d37ee-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d37ee-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d37ee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37ee-126">CommonParameters</span></span>
<span data-ttu-id="d37ee-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37ee-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d37ee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37ee-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d37ee-129">INPUTS</span></span>

### <span data-ttu-id="d37ee-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d37ee-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d37ee-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d37ee-131">OUTPUTS</span></span>

### <span data-ttu-id="d37ee-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d37ee-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d37ee-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d37ee-133">NOTES</span></span>

## <span data-ttu-id="d37ee-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d37ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="d37ee-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="d37ee-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="d37ee-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d37ee-136">Get-AzVM</span></span>](./Get-AzVM.md)


