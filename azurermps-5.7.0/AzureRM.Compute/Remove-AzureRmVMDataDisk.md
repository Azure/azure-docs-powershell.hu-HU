---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672544"
---
# <span data-ttu-id="fafb8-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fafb8-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="fafb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fafb8-102">SYNOPSIS</span></span>
<span data-ttu-id="fafb8-103">Az adatlemez eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fafb8-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fafb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fafb8-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fafb8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fafb8-105">DESCRIPTION</span></span>
<span data-ttu-id="fafb8-106">A **Remove-AzureRmVMDataDisk** parancsmag egy virtuális gépről eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="fafb8-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="fafb8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fafb8-107">EXAMPLES</span></span>

### <span data-ttu-id="fafb8-108">1. példa: adatlemez eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="fafb8-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="fafb8-109">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="fafb8-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="fafb8-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fafb8-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="fafb8-111">A második parancs eltávolítja a Disk3 nevű adatlemezt a $VirtualMachineban tárolt virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fafb8-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="fafb8-112">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="fafb8-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="fafb8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fafb8-113">PARAMETERS</span></span>

### <span data-ttu-id="fafb8-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="fafb8-114">-DataDiskNames</span></span>
<span data-ttu-id="fafb8-115">A parancsmag által eltávolított egy vagy több adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fafb8-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafb8-116">-VM</span><span class="sxs-lookup"><span data-stu-id="fafb8-116">-VM</span></span>
<span data-ttu-id="fafb8-117">Annak a helyi virtuális gépnek az objektumát adja meg, amelyből el szeretné távolítani az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="fafb8-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="fafb8-118">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fafb8-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fafb8-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fafb8-119">-Confirm</span></span>
<span data-ttu-id="fafb8-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fafb8-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafb8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fafb8-121">-WhatIf</span></span>
<span data-ttu-id="fafb8-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fafb8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fafb8-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fafb8-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fafb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fafb8-124">CommonParameters</span></span>
<span data-ttu-id="fafb8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fafb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fafb8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fafb8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fafb8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fafb8-127">INPUTS</span></span>

### <span data-ttu-id="fafb8-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="fafb8-128">None</span></span>
<span data-ttu-id="fafb8-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fafb8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fafb8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fafb8-130">OUTPUTS</span></span>

## <span data-ttu-id="fafb8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fafb8-131">NOTES</span></span>

## <span data-ttu-id="fafb8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fafb8-132">RELATED LINKS</span></span>

[<span data-ttu-id="fafb8-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fafb8-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="fafb8-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="fafb8-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


