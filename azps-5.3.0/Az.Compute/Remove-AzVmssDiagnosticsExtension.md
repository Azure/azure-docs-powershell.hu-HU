---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480744"
---
# <span data-ttu-id="cf2ab-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cf2ab-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="cf2ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2ab-103">Eltávolít egy diagnosztikai bővítményt a VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="cf2ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cf2ab-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf2ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cf2ab-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2ab-106">A **Remove-AzVmssDiagnosticsExtension** parancsmag eltávolít egy diagnosztikai bővítményt a virtuálisgép-mérethalmazból (VMSS).</span><span class="sxs-lookup"><span data-stu-id="cf2ab-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cf2ab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cf2ab-107">EXAMPLES</span></span>

### <span data-ttu-id="cf2ab-108">1. példa: Diagnosztikai bővítmény eltávolítása a VMSS-ről</span><span class="sxs-lookup"><span data-stu-id="cf2ab-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="cf2ab-109">Ez a parancs eltávolítja a diagnosztikai bővítményt a VMSS-ről.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="cf2ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf2ab-110">PARAMETERS</span></span>

### <span data-ttu-id="cf2ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2ab-111">-DefaultProfile</span></span>
<span data-ttu-id="cf2ab-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf2ab-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cf2ab-113">-Name</span></span>
<span data-ttu-id="cf2ab-114">Megadja annak a kiterjesztésnek a nevét, amelyből a parancsmag eltávolítja a VMSS-et.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2ab-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf2ab-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cf2ab-116">Megadja a VMSS-t, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="cf2ab-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf2ab-117">-Confirm</span></span>
<span data-ttu-id="cf2ab-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2ab-119">-WhatIf</span></span>
<span data-ttu-id="cf2ab-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf2ab-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2ab-122">CommonParameters</span></span>
<span data-ttu-id="cf2ab-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2ab-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf2ab-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2ab-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf2ab-125">INPUTS</span></span>

### <span data-ttu-id="cf2ab-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf2ab-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cf2ab-127">System.String</span><span class="sxs-lookup"><span data-stu-id="cf2ab-127">System.String</span></span>

## <span data-ttu-id="cf2ab-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf2ab-128">OUTPUTS</span></span>

### <span data-ttu-id="cf2ab-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cf2ab-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cf2ab-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cf2ab-130">NOTES</span></span>

## <span data-ttu-id="cf2ab-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf2ab-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf2ab-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cf2ab-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="cf2ab-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="cf2ab-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="cf2ab-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cf2ab-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


