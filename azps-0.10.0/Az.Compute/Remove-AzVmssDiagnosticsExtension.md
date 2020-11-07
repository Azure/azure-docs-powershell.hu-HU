---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: c1280b6e59b4dc1c4ddd70b924863eacce0c6e81
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844338"
---
# <span data-ttu-id="1ad6e-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ad6e-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="1ad6e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ad6e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad6e-103">Diagnosztikai bővítmény eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="1ad6e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ad6e-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad6e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ad6e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad6e-106">A **Remove-AzVmssDiagnosticsExtension** parancsmag eltávolítja a diagnosztikai bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1ad6e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1ad6e-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad6e-108">1. példa: a diagnosztikai bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="1ad6e-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="1ad6e-109">Ez a parancs eltávolítja a diagnosztika bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="1ad6e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ad6e-110">PARAMETERS</span></span>

### <span data-ttu-id="1ad6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad6e-111">-DefaultProfile</span></span>
<span data-ttu-id="1ad6e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ad6e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ad6e-113">-Name</span></span>
<span data-ttu-id="1ad6e-114">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="1ad6e-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ad6e-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1ad6e-116">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="1ad6e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ad6e-117">-Confirm</span></span>
<span data-ttu-id="1ad6e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad6e-119">-WhatIf</span></span>
<span data-ttu-id="1ad6e-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1ad6e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad6e-122">CommonParameters</span></span>
<span data-ttu-id="1ad6e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ad6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad6e-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ad6e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad6e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad6e-125">INPUTS</span></span>

### <span data-ttu-id="1ad6e-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ad6e-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="1ad6e-127">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ad6e-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="1ad6e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ad6e-128">OUTPUTS</span></span>

###  
<span data-ttu-id="1ad6e-129">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ad6e-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1ad6e-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ad6e-130">NOTES</span></span>

## <span data-ttu-id="1ad6e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ad6e-131">RELATED LINKS</span></span>

[<span data-ttu-id="1ad6e-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ad6e-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="1ad6e-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ad6e-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="1ad6e-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1ad6e-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


