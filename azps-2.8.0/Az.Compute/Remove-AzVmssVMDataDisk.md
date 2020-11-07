---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: cd41b7f09bbcf972d28aa38e9c1f4eb622e59b2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667271"
---
# <span data-ttu-id="0170b-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0170b-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="0170b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0170b-102">SYNOPSIS</span></span>
<span data-ttu-id="0170b-103">Az adatlemez eltávolítása a virtuálisgép-készlet virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="0170b-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="0170b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0170b-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0170b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0170b-105">DESCRIPTION</span></span>
<span data-ttu-id="0170b-106">A **Remove-AzVmssVMDataDisk** PARANCSMAG egy VM-beli VM-készletből eltávolítja az adatlemezt</span><span class="sxs-lookup"><span data-stu-id="0170b-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="0170b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0170b-107">EXAMPLES</span></span>

### <span data-ttu-id="0170b-108">1. példa: adatlemez eltávolítása VM-méretarányos VM-készletről</span><span class="sxs-lookup"><span data-stu-id="0170b-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="0170b-109">Az első parancs az erőforráscsoport nevével, a Vmss nevével és a getsan a létező Vmss VM-et adja meg.</span><span class="sxs-lookup"><span data-stu-id="0170b-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="0170b-110">A második parancs eltávolítja az adatlemez LUN 0 értéket a VM set VM-es verzióban, amelyet az $VmssVM a végleges parancs az eltávolított adatlemezzel együtt frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="0170b-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="0170b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0170b-111">PARAMETERS</span></span>

### <span data-ttu-id="0170b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0170b-112">-DefaultProfile</span></span>
<span data-ttu-id="0170b-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0170b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0170b-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="0170b-114">-Lun</span></span>
<span data-ttu-id="0170b-115">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0170b-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="0170b-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0170b-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="0170b-117">A virtuális gép méretarány beállítása VM-profil.</span><span class="sxs-lookup"><span data-stu-id="0170b-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="0170b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0170b-118">CommonParameters</span></span>
<span data-ttu-id="0170b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0170b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0170b-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0170b-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0170b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0170b-121">INPUTS</span></span>

### <span data-ttu-id="0170b-122">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0170b-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="0170b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0170b-123">OUTPUTS</span></span>

### <span data-ttu-id="0170b-124">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0170b-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="0170b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0170b-125">NOTES</span></span>

## <span data-ttu-id="0170b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0170b-126">RELATED LINKS</span></span>
