---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928337"
---
# <span data-ttu-id="8482a-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8482a-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="8482a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8482a-102">SYNOPSIS</span></span>
<span data-ttu-id="8482a-103">Adatlemez eltávolítása virtuális gép méretarányú virtuális gépkészletből</span><span class="sxs-lookup"><span data-stu-id="8482a-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="8482a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8482a-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8482a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8482a-105">DESCRIPTION</span></span>
<span data-ttu-id="8482a-106">Az **Remove-AzVmssVMDataDisk** parancsmag eltávolítja az adatlemezt egy VM-méretkészlet VM-ről</span><span class="sxs-lookup"><span data-stu-id="8482a-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="8482a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8482a-107">EXAMPLES</span></span>

### <span data-ttu-id="8482a-108">1. példa: Adatlemez eltávolítása a VM-méretkészlet virtuális gépről</span><span class="sxs-lookup"><span data-stu-id="8482a-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="8482a-109">Az első parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.</span><span class="sxs-lookup"><span data-stu-id="8482a-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="8482a-110">A második parancs eltávolítja a 0-s adatlemezt a VM-méretkészletből $VmssVM Az utolsó parancs a Vmss VM-et eltávolított adatlemezzel frissíti.</span><span class="sxs-lookup"><span data-stu-id="8482a-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="8482a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8482a-111">PARAMETERS</span></span>

### <span data-ttu-id="8482a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8482a-112">-DefaultProfile</span></span>
<span data-ttu-id="8482a-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8482a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8482a-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="8482a-114">-Lun</span></span>
<span data-ttu-id="8482a-115">A lemez logikai egységszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8482a-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="8482a-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8482a-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="8482a-117">A virtuális gép méretaránya meg van állítva a VIRTUÁLIS gép profilja.</span><span class="sxs-lookup"><span data-stu-id="8482a-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="8482a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8482a-118">CommonParameters</span></span>
<span data-ttu-id="8482a-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8482a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8482a-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8482a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8482a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8482a-121">INPUTS</span></span>

### <span data-ttu-id="8482a-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8482a-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8482a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8482a-123">OUTPUTS</span></span>

### <span data-ttu-id="8482a-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8482a-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8482a-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8482a-125">NOTES</span></span>

## <span data-ttu-id="8482a-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8482a-126">RELATED LINKS</span></span>
