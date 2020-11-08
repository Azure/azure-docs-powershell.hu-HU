---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013657"
---
# <span data-ttu-id="cfafe-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cfafe-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="cfafe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfafe-102">SYNOPSIS</span></span>
<span data-ttu-id="cfafe-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfafe-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="cfafe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfafe-104">SYNTAX</span></span>

### <span data-ttu-id="cfafe-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfafe-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfafe-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfafe-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfafe-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfafe-107">DESCRIPTION</span></span>
<span data-ttu-id="cfafe-108">A **Remove-AzVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="cfafe-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="cfafe-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cfafe-109">EXAMPLES</span></span>

### <span data-ttu-id="cfafe-110">1. példa: VMSS-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="cfafe-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="cfafe-111">Ez a parancs eltávolítja a VMSS meghosszabbítását, és a módosítás után frissíti a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfafe-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="cfafe-112">2. példa: példány eltávolítása egy VMSS belül</span><span class="sxs-lookup"><span data-stu-id="cfafe-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="cfafe-113">Ez a parancs eltávolítja a Group002 nevű erőforráscsoport VMSS tartozó bővítmény-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="cfafe-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="cfafe-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfafe-114">PARAMETERS</span></span>

### <span data-ttu-id="cfafe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfafe-115">-DefaultProfile</span></span>
<span data-ttu-id="cfafe-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfafe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfafe-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cfafe-117">-Id</span></span>
<span data-ttu-id="cfafe-118">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfafe-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="cfafe-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfafe-119">-Name</span></span>
<span data-ttu-id="cfafe-120">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="cfafe-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="cfafe-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cfafe-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cfafe-122">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="cfafe-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="cfafe-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfafe-123">-Confirm</span></span>
<span data-ttu-id="cfafe-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfafe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfafe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfafe-125">-WhatIf</span></span>
<span data-ttu-id="cfafe-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfafe-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfafe-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfafe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfafe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfafe-128">CommonParameters</span></span>
<span data-ttu-id="cfafe-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfafe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfafe-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cfafe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfafe-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfafe-131">INPUTS</span></span>

### <span data-ttu-id="cfafe-132">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cfafe-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cfafe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cfafe-133">System.String</span></span>

## <span data-ttu-id="cfafe-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfafe-134">OUTPUTS</span></span>

### <span data-ttu-id="cfafe-135">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cfafe-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cfafe-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfafe-136">NOTES</span></span>

## <span data-ttu-id="cfafe-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfafe-137">RELATED LINKS</span></span>

[<span data-ttu-id="cfafe-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="cfafe-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
