---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025735"
---
# <span data-ttu-id="2942e-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2942e-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="2942e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2942e-102">SYNOPSIS</span></span>
<span data-ttu-id="2942e-103">Az adatlemez eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="2942e-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="2942e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2942e-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2942e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2942e-105">DESCRIPTION</span></span>
<span data-ttu-id="2942e-106">A **Remove-AzVMDataDisk** parancsmag egy virtuális gépről eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="2942e-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="2942e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2942e-107">EXAMPLES</span></span>

### <span data-ttu-id="2942e-108">1. példa: adatlemez eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="2942e-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="2942e-109">Az első parancs a **Get-AzVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="2942e-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="2942e-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2942e-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2942e-111">A második parancs eltávolítja a Disk3 nevű adatlemezt a $VirtualMachineban tárolt virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="2942e-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="2942e-112">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="2942e-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="2942e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2942e-113">PARAMETERS</span></span>

### <span data-ttu-id="2942e-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="2942e-114">-DataDiskNames</span></span>
<span data-ttu-id="2942e-115">A parancsmag által eltávolított egy vagy több adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2942e-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2942e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2942e-116">-DefaultProfile</span></span>
<span data-ttu-id="2942e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2942e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2942e-118">-VM</span><span class="sxs-lookup"><span data-stu-id="2942e-118">-VM</span></span>
<span data-ttu-id="2942e-119">Annak a helyi virtuális gépnek az objektumát adja meg, amelyből el szeretné távolítani az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="2942e-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="2942e-120">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2942e-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="2942e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2942e-121">-Confirm</span></span>
<span data-ttu-id="2942e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2942e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2942e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2942e-123">-WhatIf</span></span>
<span data-ttu-id="2942e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2942e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2942e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2942e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2942e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2942e-126">CommonParameters</span></span>
<span data-ttu-id="2942e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2942e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2942e-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2942e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2942e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2942e-129">INPUTS</span></span>

### <span data-ttu-id="2942e-130">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2942e-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2942e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2942e-131">OUTPUTS</span></span>

### <span data-ttu-id="2942e-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2942e-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2942e-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2942e-133">NOTES</span></span>

## <span data-ttu-id="2942e-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2942e-134">RELATED LINKS</span></span>

[<span data-ttu-id="2942e-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2942e-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="2942e-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2942e-136">Get-AzVM</span></span>](./Get-AzVM.md)


