---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495471"
---
# <span data-ttu-id="34c4a-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34c4a-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="34c4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="34c4a-103">Diagnosztikai bővítmény eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34c4a-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34c4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34c4a-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34c4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="34c4a-106">A **Remove-AzureRmVmssDiagnosticsExtension** parancsmag eltávolítja a diagnosztikai bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="34c4a-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="34c4a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34c4a-107">EXAMPLES</span></span>

### <span data-ttu-id="34c4a-108">1. példa: a diagnosztikai bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="34c4a-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="34c4a-109">Ez a parancs eltávolítja a diagnosztika bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34c4a-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="34c4a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34c4a-110">PARAMETERS</span></span>

### <span data-ttu-id="34c4a-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34c4a-111">-Name</span></span>
<span data-ttu-id="34c4a-112">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34c4a-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34c4a-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34c4a-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="34c4a-114">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="34c4a-114">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34c4a-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34c4a-115">-Confirm</span></span>
<span data-ttu-id="34c4a-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34c4a-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c4a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34c4a-117">-WhatIf</span></span>
<span data-ttu-id="34c4a-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34c4a-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="34c4a-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34c4a-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34c4a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c4a-120">CommonParameters</span></span>
<span data-ttu-id="34c4a-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34c4a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c4a-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34c4a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c4a-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c4a-123">INPUTS</span></span>

### <span data-ttu-id="34c4a-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="34c4a-124">None</span></span>
<span data-ttu-id="34c4a-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="34c4a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34c4a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34c4a-126">OUTPUTS</span></span>

###  
<span data-ttu-id="34c4a-127">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="34c4a-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="34c4a-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34c4a-128">NOTES</span></span>

## <span data-ttu-id="34c4a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34c4a-129">RELATED LINKS</span></span>

[<span data-ttu-id="34c4a-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34c4a-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="34c4a-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="34c4a-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="34c4a-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="34c4a-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


