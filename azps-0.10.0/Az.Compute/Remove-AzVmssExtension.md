---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: 8044be4e6d9c353dd50420fe73066a8f47d53855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844326"
---
# <span data-ttu-id="3fa03-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3fa03-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="3fa03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3fa03-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa03-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="3fa03-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="3fa03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3fa03-104">SYNTAX</span></span>

### <span data-ttu-id="3fa03-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa03-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa03-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fa03-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3fa03-107">DESCRIPTION</span></span>
<span data-ttu-id="3fa03-108">A **Remove-AzVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="3fa03-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3fa03-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3fa03-109">EXAMPLES</span></span>

### <span data-ttu-id="3fa03-110">1. példa: a bővítmény eltávolítása a VMSS</span><span class="sxs-lookup"><span data-stu-id="3fa03-110">Example 1: Remove extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

## <span data-ttu-id="3fa03-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3fa03-111">PARAMETERS</span></span>

### <span data-ttu-id="3fa03-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa03-112">-DefaultProfile</span></span>
<span data-ttu-id="3fa03-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3fa03-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fa03-114">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="3fa03-114">-Id</span></span>
<span data-ttu-id="3fa03-115">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="3fa03-115">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="3fa03-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3fa03-116">-Name</span></span>
<span data-ttu-id="3fa03-117">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="3fa03-117">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="3fa03-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3fa03-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3fa03-119">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="3fa03-119">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="3fa03-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3fa03-120">-Confirm</span></span>
<span data-ttu-id="3fa03-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3fa03-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa03-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa03-122">-WhatIf</span></span>
<span data-ttu-id="3fa03-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3fa03-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fa03-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3fa03-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa03-125">CommonParameters</span></span>
<span data-ttu-id="3fa03-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3fa03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa03-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa03-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa03-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fa03-128">INPUTS</span></span>

### <span data-ttu-id="3fa03-129">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3fa03-129">VirtualMachineScaleSet</span></span>
<span data-ttu-id="3fa03-130">A ' VirtualMachineScaleSet ' paraméter az "VirtualMachineScaleSet" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3fa03-130">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="3fa03-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3fa03-131">OUTPUTS</span></span>

### <span data-ttu-id="3fa03-132">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3fa03-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3fa03-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3fa03-133">NOTES</span></span>

## <span data-ttu-id="3fa03-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3fa03-134">RELATED LINKS</span></span>

[<span data-ttu-id="3fa03-135">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3fa03-135">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
