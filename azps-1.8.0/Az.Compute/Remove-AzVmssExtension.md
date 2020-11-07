---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: aeb07f9d9e2faaaf9fc09867fcfee045a5bc8351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671269"
---
# <span data-ttu-id="61bef-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="61bef-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="61bef-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61bef-102">SYNOPSIS</span></span>
<span data-ttu-id="61bef-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="61bef-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="61bef-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61bef-104">SYNTAX</span></span>

### <span data-ttu-id="61bef-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bef-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bef-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61bef-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bef-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="61bef-107">DESCRIPTION</span></span>
<span data-ttu-id="61bef-108">A **Remove-AzVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="61bef-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="61bef-109">Példák</span><span class="sxs-lookup"><span data-stu-id="61bef-109">EXAMPLES</span></span>

### <span data-ttu-id="61bef-110">1. példa: VMSS-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61bef-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="61bef-111">Ez a parancs eltávolítja a VMSS meghosszabbítását, és a módosítás után frissíti a VMSS.</span><span class="sxs-lookup"><span data-stu-id="61bef-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="61bef-112">2. példa: példány eltávolítása egy VMSS belül</span><span class="sxs-lookup"><span data-stu-id="61bef-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="61bef-113">Ez a parancs eltávolítja a Group002 nevű erőforráscsoport VMSS tartozó bővítmény-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="61bef-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="61bef-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61bef-114">PARAMETERS</span></span>

### <span data-ttu-id="61bef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bef-115">-DefaultProfile</span></span>
<span data-ttu-id="61bef-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61bef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61bef-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="61bef-117">-Id</span></span>
<span data-ttu-id="61bef-118">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="61bef-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="61bef-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="61bef-119">-Name</span></span>
<span data-ttu-id="61bef-120">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="61bef-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="61bef-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61bef-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="61bef-122">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="61bef-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="61bef-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61bef-123">-Confirm</span></span>
<span data-ttu-id="61bef-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61bef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bef-125">-WhatIf</span></span>
<span data-ttu-id="61bef-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61bef-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61bef-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61bef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bef-128">CommonParameters</span></span>
<span data-ttu-id="61bef-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61bef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bef-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bef-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bef-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61bef-131">INPUTS</span></span>

### <span data-ttu-id="61bef-132">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61bef-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="61bef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="61bef-133">System.String</span></span>

## <span data-ttu-id="61bef-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61bef-134">OUTPUTS</span></span>

### <span data-ttu-id="61bef-135">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="61bef-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="61bef-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61bef-136">NOTES</span></span>

## <span data-ttu-id="61bef-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61bef-137">RELATED LINKS</span></span>

[<span data-ttu-id="61bef-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="61bef-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
