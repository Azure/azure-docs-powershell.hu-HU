---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495423"
---
# <span data-ttu-id="89191-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="89191-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="89191-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="89191-102">SYNOPSIS</span></span>
<span data-ttu-id="89191-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="89191-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89191-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="89191-104">SYNTAX</span></span>

### <span data-ttu-id="89191-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89191-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89191-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89191-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89191-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="89191-107">DESCRIPTION</span></span>
<span data-ttu-id="89191-108">A **Remove-AzureRmVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="89191-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="89191-109">Példák</span><span class="sxs-lookup"><span data-stu-id="89191-109">EXAMPLES</span></span>

## <span data-ttu-id="89191-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="89191-110">PARAMETERS</span></span>

### <span data-ttu-id="89191-111">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="89191-111">-Id</span></span>
<span data-ttu-id="89191-112">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="89191-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89191-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="89191-113">-Name</span></span>
<span data-ttu-id="89191-114">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="89191-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89191-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89191-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="89191-116">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="89191-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="89191-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="89191-117">-Confirm</span></span>
<span data-ttu-id="89191-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="89191-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89191-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89191-119">-WhatIf</span></span>
<span data-ttu-id="89191-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="89191-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89191-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89191-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89191-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89191-122">CommonParameters</span></span>
<span data-ttu-id="89191-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="89191-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89191-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89191-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89191-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="89191-125">INPUTS</span></span>

### <span data-ttu-id="89191-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="89191-126">None</span></span>
<span data-ttu-id="89191-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="89191-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89191-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89191-128">OUTPUTS</span></span>

### <span data-ttu-id="89191-129">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="89191-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="89191-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="89191-130">NOTES</span></span>

## <span data-ttu-id="89191-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89191-131">RELATED LINKS</span></span>

[<span data-ttu-id="89191-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="89191-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
