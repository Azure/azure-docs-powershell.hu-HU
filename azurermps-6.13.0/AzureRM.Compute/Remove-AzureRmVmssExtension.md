---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 7ede92fa653fe04072b75ce03dd6928421e01c6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491988"
---
# <span data-ttu-id="a1701-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a1701-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="a1701-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1701-102">SYNOPSIS</span></span>
<span data-ttu-id="a1701-103">Eltávolít egy kiterjesztést a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1701-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1701-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1701-104">SYNTAX</span></span>

### <span data-ttu-id="a1701-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1701-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1701-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1701-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1701-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1701-107">DESCRIPTION</span></span>
<span data-ttu-id="a1701-108">A **Remove-AzureRmVmssExtension** parancsmag eltávolítja a bővítményt a Virtual Machine Scale set (VMSS) alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="a1701-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a1701-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a1701-109">EXAMPLES</span></span>

### <span data-ttu-id="a1701-110">1. példa: VMSS-bővítmény eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a1701-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzureRmVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="a1701-111">Ez a parancs eltávolítja a VMSS meghosszabbítását, és a módosítás után frissíti a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1701-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="a1701-112">2. példa: példány eltávolítása egy VMSS belül</span><span class="sxs-lookup"><span data-stu-id="a1701-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzureRmVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzureRmVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="a1701-113">Ez a parancs eltávolítja a Group002 nevű erőforráscsoport VMSS tartozó bővítmény-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="a1701-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a1701-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1701-114">PARAMETERS</span></span>

### <span data-ttu-id="a1701-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1701-115">-DefaultProfile</span></span>
<span data-ttu-id="a1701-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1701-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1701-117">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a1701-117">-Id</span></span>
<span data-ttu-id="a1701-118">Annak a bővítménynek az AZONOSÍTÓját adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1701-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a1701-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a1701-119">-Name</span></span>
<span data-ttu-id="a1701-120">Annak a bővítménynek a nevét adja meg, amelyre a parancsmag eltávolítja a VMSS.</span><span class="sxs-lookup"><span data-stu-id="a1701-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="a1701-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1701-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a1701-122">Annak a VMSS a meghatározása, amelyből el szeretné távolítani a bővítményt.</span><span class="sxs-lookup"><span data-stu-id="a1701-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="a1701-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1701-123">-Confirm</span></span>
<span data-ttu-id="a1701-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1701-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1701-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1701-125">-WhatIf</span></span>
<span data-ttu-id="a1701-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1701-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1701-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1701-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1701-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1701-128">CommonParameters</span></span>
<span data-ttu-id="a1701-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1701-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1701-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1701-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1701-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1701-131">INPUTS</span></span>

### <span data-ttu-id="a1701-132">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1701-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a1701-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a1701-133">System.String</span></span>

## <span data-ttu-id="a1701-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1701-134">OUTPUTS</span></span>

### <span data-ttu-id="a1701-135">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a1701-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a1701-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1701-136">NOTES</span></span>

## <span data-ttu-id="a1701-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1701-137">RELATED LINKS</span></span>

[<span data-ttu-id="a1701-138">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a1701-138">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
