---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943089"
---
# <span data-ttu-id="612d8-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="612d8-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="612d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="612d8-102">SYNOPSIS</span></span>
<span data-ttu-id="612d8-103">Eltávolít egy adatlemezt a VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="612d8-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="612d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="612d8-104">SYNTAX</span></span>

### <span data-ttu-id="612d8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="612d8-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="612d8-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="612d8-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="612d8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="612d8-107">DESCRIPTION</span></span>
<span data-ttu-id="612d8-108">A **Remove-AzVmssDataDisk** parancsmag eltávolít egy adatlemezt a VIRTUÁLISgép-mérethalmaz (VMSS) példányból.</span><span class="sxs-lookup"><span data-stu-id="612d8-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="612d8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="612d8-109">EXAMPLES</span></span>

### <span data-ttu-id="612d8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="612d8-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="612d8-111">Ez a parancs eltávolítja a "DataDisk1" adatlemezt a VMSS-objektumból.</span><span class="sxs-lookup"><span data-stu-id="612d8-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="612d8-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="612d8-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="612d8-113">Ez a parancs eltávolítja a LUN 0 adatlemezét a VMSS-objektumból.</span><span class="sxs-lookup"><span data-stu-id="612d8-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="612d8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="612d8-114">PARAMETERS</span></span>

### <span data-ttu-id="612d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612d8-115">-DefaultProfile</span></span>
<span data-ttu-id="612d8-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="612d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="612d8-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="612d8-117">-Lun</span></span>
<span data-ttu-id="612d8-118">A lemez logikai egységszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="612d8-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612d8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="612d8-119">-Name</span></span>
<span data-ttu-id="612d8-120">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="612d8-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="612d8-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="612d8-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="612d8-122">Adja meg a VMSS-objektumot.</span><span class="sxs-lookup"><span data-stu-id="612d8-122">Specify the VMSS object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="612d8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="612d8-123">-Confirm</span></span>
<span data-ttu-id="612d8-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="612d8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612d8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612d8-125">-WhatIf</span></span>
<span data-ttu-id="612d8-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="612d8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="612d8-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="612d8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="612d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612d8-128">CommonParameters</span></span>
<span data-ttu-id="612d8-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="612d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612d8-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="612d8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612d8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="612d8-131">INPUTS</span></span>

### <span data-ttu-id="612d8-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="612d8-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="612d8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="612d8-133">System.String</span></span>

### <span data-ttu-id="612d8-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="612d8-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="612d8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="612d8-135">OUTPUTS</span></span>

### <span data-ttu-id="612d8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="612d8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="612d8-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="612d8-137">NOTES</span></span>

## <span data-ttu-id="612d8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="612d8-138">RELATED LINKS</span></span>
