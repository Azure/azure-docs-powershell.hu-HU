---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 35a8ca7832727bef41d588a5551ae1f3efc86180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008054"
---
# <span data-ttu-id="581d0-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="581d0-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="581d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="581d0-102">SYNOPSIS</span></span>
<span data-ttu-id="581d0-103">Eltávolít egy bővítményt a VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="581d0-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="581d0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="581d0-104">SYNTAX</span></span>

### <span data-ttu-id="581d0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="581d0-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="581d0-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="581d0-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="581d0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="581d0-107">DESCRIPTION</span></span>
<span data-ttu-id="581d0-108">A **Remove-AzVmssExtension** parancsmag eltávolít egy bővítményt a virtuálisgép-mérethalmazból (VMSS).</span><span class="sxs-lookup"><span data-stu-id="581d0-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="581d0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="581d0-109">EXAMPLES</span></span>

### <span data-ttu-id="581d0-110">1. példa: VMSS-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="581d0-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="581d0-111">Ez a parancs eltávolítja a VMSS bővítményt, és frissíti a VMSS-t a módosítás után.</span><span class="sxs-lookup"><span data-stu-id="581d0-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="581d0-112">2. példa: Példány eltávolítása a VMSS-en belül</span><span class="sxs-lookup"><span data-stu-id="581d0-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="581d0-113">Ez a parancs eltávolítja a megadott kiterjesztésazonosítót a Group0002 nevű erőforráscsoportHOZ tartozó VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="581d0-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="581d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="581d0-114">PARAMETERS</span></span>

### <span data-ttu-id="581d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581d0-115">-DefaultProfile</span></span>
<span data-ttu-id="581d0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="581d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="581d0-117">-Id</span><span class="sxs-lookup"><span data-stu-id="581d0-117">-Id</span></span>
<span data-ttu-id="581d0-118">Annak a kiterjesztésnek az azonosítóját adja meg, amelyből a parancsmag eltávolítja a VMSS-et.</span><span class="sxs-lookup"><span data-stu-id="581d0-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581d0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="581d0-119">-Name</span></span>
<span data-ttu-id="581d0-120">Megadja annak a kiterjesztésnek a nevét, amelyből a parancsmag eltávolítja a VMSS-et.</span><span class="sxs-lookup"><span data-stu-id="581d0-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="581d0-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="581d0-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="581d0-122">Megadja azt a VMSS-t, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="581d0-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="581d0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="581d0-123">-Confirm</span></span>
<span data-ttu-id="581d0-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="581d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="581d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581d0-125">-WhatIf</span></span>
<span data-ttu-id="581d0-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="581d0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="581d0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="581d0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="581d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581d0-128">CommonParameters</span></span>
<span data-ttu-id="581d0-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581d0-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="581d0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581d0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="581d0-131">INPUTS</span></span>

### <span data-ttu-id="581d0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="581d0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="581d0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="581d0-133">System.String</span></span>

## <span data-ttu-id="581d0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="581d0-134">OUTPUTS</span></span>

### <span data-ttu-id="581d0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="581d0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="581d0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="581d0-136">NOTES</span></span>

## <span data-ttu-id="581d0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="581d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="581d0-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="581d0-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
