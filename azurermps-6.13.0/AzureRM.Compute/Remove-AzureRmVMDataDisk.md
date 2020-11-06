---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: e0f8b1d4e47cfe488fcba02228bd35c09f4d3ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491990"
---
# <span data-ttu-id="190f4-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="190f4-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="190f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="190f4-102">SYNOPSIS</span></span>
<span data-ttu-id="190f4-103">Az adatlemez eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="190f4-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="190f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="190f4-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="190f4-105">DESCRIPTION</span></span>
<span data-ttu-id="190f4-106">A **Remove-AzureRmVMDataDisk** parancsmag egy virtuális gépről eltávolítja az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="190f4-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="190f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="190f4-107">EXAMPLES</span></span>

### <span data-ttu-id="190f4-108">1. példa: adatlemez eltávolítása virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="190f4-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="190f4-109">Az első parancs a **Get-AzureRmVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="190f4-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="190f4-110">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="190f4-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="190f4-111">A második parancs eltávolítja a Disk3 nevű adatlemezt a $VirtualMachineban tárolt virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="190f4-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="190f4-112">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="190f4-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="190f4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="190f4-113">PARAMETERS</span></span>

### <span data-ttu-id="190f4-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="190f4-114">-DataDiskNames</span></span>
<span data-ttu-id="190f4-115">A parancsmag által eltávolított egy vagy több adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="190f4-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="190f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190f4-116">-DefaultProfile</span></span>
<span data-ttu-id="190f4-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="190f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="190f4-118">-VM</span><span class="sxs-lookup"><span data-stu-id="190f4-118">-VM</span></span>
<span data-ttu-id="190f4-119">Annak a helyi virtuális gépnek az objektumát adja meg, amelyből el szeretné távolítani az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="190f4-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="190f4-120">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="190f4-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="190f4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="190f4-121">-Confirm</span></span>
<span data-ttu-id="190f4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="190f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190f4-123">-WhatIf</span></span>
<span data-ttu-id="190f4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="190f4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="190f4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="190f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190f4-126">CommonParameters</span></span>
<span data-ttu-id="190f4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="190f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190f4-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="190f4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190f4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="190f4-129">INPUTS</span></span>

### <span data-ttu-id="190f4-130">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="190f4-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="190f4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="190f4-131">OUTPUTS</span></span>

### <span data-ttu-id="190f4-132">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="190f4-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="190f4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="190f4-133">NOTES</span></span>

## <span data-ttu-id="190f4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="190f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="190f4-135">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="190f4-135">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="190f4-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="190f4-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


