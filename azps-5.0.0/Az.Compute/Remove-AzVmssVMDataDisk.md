---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185610"
---
# <span data-ttu-id="cd5a0-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cd5a0-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="cd5a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd5a0-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5a0-103">Az adatlemez eltávolítása a virtuálisgép-készlet virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="cd5a0-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="cd5a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd5a0-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd5a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd5a0-105">DESCRIPTION</span></span>
<span data-ttu-id="cd5a0-106">A **Remove-AzVmssVMDataDisk** PARANCSMAG egy VM-beli VM-készletből eltávolítja az adatlemezt</span><span class="sxs-lookup"><span data-stu-id="cd5a0-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="cd5a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd5a0-107">EXAMPLES</span></span>

### <span data-ttu-id="cd5a0-108">1. példa: adatlemez eltávolítása VM-méretarányos VM-készletről</span><span class="sxs-lookup"><span data-stu-id="cd5a0-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="cd5a0-109">Az első parancs az erőforráscsoport nevével, a Vmss nevével és a getsan a létező Vmss VM-et adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="cd5a0-110">A második parancs eltávolítja az adatlemez LUN 0 értéket a VM set VM-es verzióban, amelyet az $VmssVM a végleges parancs az eltávolított adatlemezzel együtt frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="cd5a0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd5a0-111">PARAMETERS</span></span>

### <span data-ttu-id="cd5a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5a0-112">-DefaultProfile</span></span>
<span data-ttu-id="cd5a0-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd5a0-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="cd5a0-114">-Lun</span></span>
<span data-ttu-id="cd5a0-115">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd5a0-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cd5a0-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="cd5a0-117">A virtuális gép méretarány beállítása VM-profil.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5a0-118">CommonParameters</span></span>
<span data-ttu-id="cd5a0-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd5a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5a0-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd5a0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5a0-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd5a0-121">INPUTS</span></span>

### <span data-ttu-id="cd5a0-122">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cd5a0-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cd5a0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd5a0-123">OUTPUTS</span></span>

### <span data-ttu-id="cd5a0-124">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cd5a0-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cd5a0-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd5a0-125">NOTES</span></span>

## <span data-ttu-id="cd5a0-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd5a0-126">RELATED LINKS</span></span>
