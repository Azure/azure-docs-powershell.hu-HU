---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 06b2a0d72d2195cfd73beb44bbfc8f61e5b87fa9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667277"
---
# <span data-ttu-id="70233-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="70233-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="70233-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70233-102">SYNOPSIS</span></span>
<span data-ttu-id="70233-103">Diagnosztikai bővítmény eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="70233-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="70233-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70233-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70233-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="70233-105">DESCRIPTION</span></span>
<span data-ttu-id="70233-106">A **Remove-AzVmssDiagnosticsExtension** parancsmag eltávolítja a diagnosztikai bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="70233-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="70233-107">Példák</span><span class="sxs-lookup"><span data-stu-id="70233-107">EXAMPLES</span></span>

### <span data-ttu-id="70233-108">1. példa: a diagnosztikai bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="70233-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="70233-109">Ez a parancs eltávolítja a diagnosztika bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="70233-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="70233-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70233-110">PARAMETERS</span></span>

### <span data-ttu-id="70233-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70233-111">-DefaultProfile</span></span>
<span data-ttu-id="70233-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70233-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70233-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70233-113">-Name</span></span>
<span data-ttu-id="70233-114">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="70233-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="70233-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70233-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="70233-116">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="70233-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="70233-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70233-117">-Confirm</span></span>
<span data-ttu-id="70233-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70233-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70233-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70233-119">-WhatIf</span></span>
<span data-ttu-id="70233-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70233-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70233-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70233-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70233-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70233-122">CommonParameters</span></span>
<span data-ttu-id="70233-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70233-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70233-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="70233-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70233-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70233-125">INPUTS</span></span>

### <span data-ttu-id="70233-126">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70233-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="70233-127">System. String</span><span class="sxs-lookup"><span data-stu-id="70233-127">System.String</span></span>

## <span data-ttu-id="70233-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70233-128">OUTPUTS</span></span>

### <span data-ttu-id="70233-129">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70233-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="70233-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70233-130">NOTES</span></span>

## <span data-ttu-id="70233-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70233-131">RELATED LINKS</span></span>

[<span data-ttu-id="70233-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="70233-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="70233-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="70233-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="70233-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="70233-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


