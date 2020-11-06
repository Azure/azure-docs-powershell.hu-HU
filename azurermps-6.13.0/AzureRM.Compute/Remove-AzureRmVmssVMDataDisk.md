---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: 5c82c2dfb852cd6c3d397b34e90d9a611ff0efaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504476"
---
# <span data-ttu-id="7a825-101">Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7a825-101">Remove-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="7a825-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a825-102">SYNOPSIS</span></span>
<span data-ttu-id="7a825-103">Az adatlemez eltávolítása a virtuálisgép-készlet virtuális gépén</span><span class="sxs-lookup"><span data-stu-id="7a825-103">Removes a data disk from a virtual machine scale set VM</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a825-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a825-104">SYNTAX</span></span>

```
Remove-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a825-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a825-105">DESCRIPTION</span></span>
<span data-ttu-id="7a825-106">A **Remove-AzureRmVmssVMDataDisk** PARANCSMAG egy VM-beli VM-készletből eltávolítja az adatlemezt</span><span class="sxs-lookup"><span data-stu-id="7a825-106">The **Remove-AzureRmVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="7a825-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a825-107">EXAMPLES</span></span>

### <span data-ttu-id="7a825-108">1. példa: adatlemez eltávolítása VM-méretarányos VM-készletről</span><span class="sxs-lookup"><span data-stu-id="7a825-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzureRmVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="7a825-109">Az első parancs az erőforráscsoport nevével, a Vmss nevével és a getsan a létező Vmss VM-et adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a825-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="7a825-110">A második parancs eltávolítja az adatlemez LUN 0 értéket a VM set VM-es verzióban, amelyet az $VmssVM a végleges parancs az eltávolított adatlemezzel együtt frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="7a825-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="7a825-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a825-111">PARAMETERS</span></span>

### <span data-ttu-id="7a825-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a825-112">-DefaultProfile</span></span>
<span data-ttu-id="7a825-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a825-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a825-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="7a825-114">-Lun</span></span>
<span data-ttu-id="7a825-115">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a825-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="7a825-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a825-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="7a825-117">A virtuális gép méretarány beállítása VM-profil.</span><span class="sxs-lookup"><span data-stu-id="7a825-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a825-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a825-118">CommonParameters</span></span>
<span data-ttu-id="7a825-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a825-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a825-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a825-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a825-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a825-121">INPUTS</span></span>

### <span data-ttu-id="7a825-122">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a825-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7a825-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a825-123">OUTPUTS</span></span>

### <span data-ttu-id="7a825-124">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="7a825-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="7a825-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a825-125">NOTES</span></span>

## <span data-ttu-id="7a825-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a825-126">RELATED LINKS</span></span>
