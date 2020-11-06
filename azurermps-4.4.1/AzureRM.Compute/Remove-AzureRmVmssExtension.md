---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: f99df428f99ec0e75eb4b1b220dde657be6f7458
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492531"
---
# <span data-ttu-id="b615b-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b615b-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="b615b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b615b-102">SYNOPSIS</span></span>
<span data-ttu-id="b615b-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b615b-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b615b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b615b-104">SYNTAX</span></span>

### <span data-ttu-id="b615b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b615b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b615b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b615b-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b615b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b615b-107">DESCRIPTION</span></span>
<span data-ttu-id="b615b-108">A **Remove-AzureRmVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="b615b-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b615b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b615b-109">EXAMPLES</span></span>

## <span data-ttu-id="b615b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b615b-110">PARAMETERS</span></span>

### <span data-ttu-id="b615b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b615b-111">-DefaultProfile</span></span>
<span data-ttu-id="b615b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b615b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b615b-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="b615b-113">-Id</span></span>
<span data-ttu-id="b615b-114">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b615b-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="b615b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b615b-115">-Name</span></span>
<span data-ttu-id="b615b-116">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="b615b-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="b615b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b615b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b615b-118">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="b615b-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="b615b-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b615b-119">-Confirm</span></span>
<span data-ttu-id="b615b-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b615b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b615b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b615b-121">-WhatIf</span></span>
<span data-ttu-id="b615b-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b615b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b615b-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b615b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b615b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b615b-124">CommonParameters</span></span>
<span data-ttu-id="b615b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b615b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b615b-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b615b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b615b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b615b-127">INPUTS</span></span>

## <span data-ttu-id="b615b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b615b-128">OUTPUTS</span></span>

### <span data-ttu-id="b615b-129">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b615b-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b615b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b615b-130">NOTES</span></span>

## <span data-ttu-id="b615b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b615b-131">RELATED LINKS</span></span>

[<span data-ttu-id="b615b-132">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b615b-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
