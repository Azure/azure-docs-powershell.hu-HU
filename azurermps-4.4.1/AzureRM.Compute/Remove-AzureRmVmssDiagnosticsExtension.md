---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 4f69866d6301bc4efc0c867d35cdc7777e759ed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492534"
---
# <span data-ttu-id="a479b-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a479b-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="a479b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a479b-102">SYNOPSIS</span></span>
<span data-ttu-id="a479b-103">Diagnosztikai bővítmény eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a479b-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a479b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a479b-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a479b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a479b-105">DESCRIPTION</span></span>
<span data-ttu-id="a479b-106">A **Remove-AzureRmVmssDiagnosticsExtension** parancsmag eltávolítja a diagnosztikai bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="a479b-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a479b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a479b-107">EXAMPLES</span></span>

### <span data-ttu-id="a479b-108">1. példa: a diagnosztikai bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="a479b-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="a479b-109">Ez a parancs eltávolítja a diagnosztika bővítményt a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a479b-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="a479b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a479b-110">PARAMETERS</span></span>

### <span data-ttu-id="a479b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a479b-111">-DefaultProfile</span></span>
<span data-ttu-id="a479b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a479b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a479b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a479b-113">-Name</span></span>
<span data-ttu-id="a479b-114">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a479b-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a479b-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a479b-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a479b-116">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a479b-116">Specifies the VMSS from which to remove the extension.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a479b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a479b-117">-Confirm</span></span>
<span data-ttu-id="a479b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a479b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a479b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a479b-119">-WhatIf</span></span>
<span data-ttu-id="a479b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a479b-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a479b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a479b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a479b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a479b-122">CommonParameters</span></span>
<span data-ttu-id="a479b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a479b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a479b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a479b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a479b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a479b-125">INPUTS</span></span>

## <span data-ttu-id="a479b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a479b-126">OUTPUTS</span></span>

###  
<span data-ttu-id="a479b-127">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a479b-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="a479b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a479b-128">NOTES</span></span>

## <span data-ttu-id="a479b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a479b-129">RELATED LINKS</span></span>

[<span data-ttu-id="a479b-130">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a479b-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="a479b-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a479b-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="a479b-132">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a479b-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


