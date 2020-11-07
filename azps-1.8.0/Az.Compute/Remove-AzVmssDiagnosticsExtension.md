---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 724135c1f9ed920414cdeb3c2e53724bd2e512ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836705"
---
# <span data-ttu-id="5bf10-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5bf10-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="5bf10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5bf10-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf10-103">Diagnosztikai bővítmény eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf10-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="5bf10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5bf10-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5bf10-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf10-106">A **Remove-AzVmssDiagnosticsExtension** parancsmag eltávolítja a diagnosztikai bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="5bf10-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5bf10-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5bf10-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf10-108">1. példa: a diagnosztikai bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="5bf10-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="5bf10-109">Ez a parancs eltávolítja a diagnosztika bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf10-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="5bf10-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5bf10-110">PARAMETERS</span></span>

### <span data-ttu-id="5bf10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf10-111">-DefaultProfile</span></span>
<span data-ttu-id="5bf10-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5bf10-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf10-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5bf10-113">-Name</span></span>
<span data-ttu-id="5bf10-114">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="5bf10-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="5bf10-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5bf10-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5bf10-116">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="5bf10-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="5bf10-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5bf10-117">-Confirm</span></span>
<span data-ttu-id="5bf10-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5bf10-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf10-119">-WhatIf</span></span>
<span data-ttu-id="5bf10-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5bf10-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf10-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5bf10-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf10-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf10-122">CommonParameters</span></span>
<span data-ttu-id="5bf10-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5bf10-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf10-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf10-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf10-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf10-125">INPUTS</span></span>

### <span data-ttu-id="5bf10-126">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5bf10-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5bf10-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf10-127">System.String</span></span>

## <span data-ttu-id="5bf10-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5bf10-128">OUTPUTS</span></span>

### <span data-ttu-id="5bf10-129">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5bf10-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5bf10-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5bf10-130">NOTES</span></span>

## <span data-ttu-id="5bf10-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5bf10-131">RELATED LINKS</span></span>

[<span data-ttu-id="5bf10-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5bf10-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="5bf10-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5bf10-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="5bf10-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="5bf10-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


