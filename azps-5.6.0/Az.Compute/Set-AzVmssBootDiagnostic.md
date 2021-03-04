---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 58a45d6f9e3a24ca11c298935fc0d9676617737e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935825"
---
# <span data-ttu-id="d863f-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d863f-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="d863f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d863f-102">SYNOPSIS</span></span>
<span data-ttu-id="d863f-103">Beállítja a virtuális gép méretarányú halmazának indítási diagnosztikai profilját.</span><span class="sxs-lookup"><span data-stu-id="d863f-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d863f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d863f-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d863f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d863f-105">DESCRIPTION</span></span>
<span data-ttu-id="d863f-106">Beállítja a virtuális gép méretarányú halmazának indítási diagnosztikai profilját.</span><span class="sxs-lookup"><span data-stu-id="d863f-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="d863f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d863f-107">EXAMPLES</span></span>

### <span data-ttu-id="d863f-108">1. példa: A VMSS rendszerindításkor használt diagnosztikai profiltulajdonságának beállítása</span><span class="sxs-lookup"><span data-stu-id="d863f-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="d863f-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS rendszerindítási diagnosztikai profiltulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="d863f-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d863f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d863f-110">PARAMETERS</span></span>

### <span data-ttu-id="d863f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d863f-111">-DefaultProfile</span></span>
<span data-ttu-id="d863f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d863f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d863f-113">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="d863f-113">-Enabled</span></span>
<span data-ttu-id="d863f-114">Be kell-e állítani a rendszerindítási diagnosztika funkciót a virtuális gép méretarány-készletében.</span><span class="sxs-lookup"><span data-stu-id="d863f-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d863f-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="d863f-115">-StorageUri</span></span>
<span data-ttu-id="d863f-116">A konzol kimenetének és képernyőképének elhelyezéséhez használt tárfiók URI-ja.</span><span class="sxs-lookup"><span data-stu-id="d863f-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d863f-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d863f-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d863f-118">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d863f-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="d863f-119">Az objektum létrehozásához használhatja New-AzVmssConfig parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d863f-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d863f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d863f-120">-Confirm</span></span>
<span data-ttu-id="d863f-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d863f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d863f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d863f-122">-WhatIf</span></span>
<span data-ttu-id="d863f-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d863f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d863f-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d863f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d863f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d863f-125">CommonParameters</span></span>
<span data-ttu-id="d863f-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d863f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d863f-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d863f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d863f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d863f-128">INPUTS</span></span>

### <span data-ttu-id="d863f-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d863f-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d863f-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d863f-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d863f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d863f-131">System.String</span></span>

## <span data-ttu-id="d863f-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d863f-132">OUTPUTS</span></span>

### <span data-ttu-id="d863f-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d863f-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d863f-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d863f-134">NOTES</span></span>

## <span data-ttu-id="d863f-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d863f-135">RELATED LINKS</span></span>
