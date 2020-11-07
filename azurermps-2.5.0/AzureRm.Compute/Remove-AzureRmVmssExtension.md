---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848329"
---
# <span data-ttu-id="8e516-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8e516-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="8e516-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e516-102">SYNOPSIS</span></span>
<span data-ttu-id="8e516-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e516-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e516-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e516-104">SYNTAX</span></span>

### <span data-ttu-id="8e516-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e516-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e516-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e516-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e516-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e516-107">DESCRIPTION</span></span>
<span data-ttu-id="8e516-108">A **Remove-AzureRmVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="8e516-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8e516-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e516-109">EXAMPLES</span></span>

## <span data-ttu-id="8e516-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e516-110">PARAMETERS</span></span>

### <span data-ttu-id="8e516-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e516-111">-DefaultProfile</span></span>
<span data-ttu-id="8e516-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e516-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e516-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="8e516-113">-Id</span></span>
<span data-ttu-id="8e516-114">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e516-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="8e516-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e516-115">-Name</span></span>
<span data-ttu-id="8e516-116">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e516-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="8e516-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e516-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8e516-118">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="8e516-118">Specifies the VMSS from which to remove the extension from.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e516-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e516-119">-Confirm</span></span>
<span data-ttu-id="8e516-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e516-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e516-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e516-121">-WhatIf</span></span>
<span data-ttu-id="8e516-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e516-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e516-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e516-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e516-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e516-124">CommonParameters</span></span>
<span data-ttu-id="8e516-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e516-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e516-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e516-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e516-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e516-127">INPUTS</span></span>

### <span data-ttu-id="8e516-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e516-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="8e516-129">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8e516-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="8e516-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e516-130">OUTPUTS</span></span>

### <span data-ttu-id="8e516-131">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8e516-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="8e516-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e516-132">NOTES</span></span>

## <span data-ttu-id="8e516-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e516-133">RELATED LINKS</span></span>

[<span data-ttu-id="8e516-134">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8e516-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
