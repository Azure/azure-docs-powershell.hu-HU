---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194464"
---
# <span data-ttu-id="af96a-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="af96a-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="af96a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af96a-102">SYNOPSIS</span></span>
<span data-ttu-id="af96a-103">Adatlemez eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="af96a-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="af96a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af96a-104">SYNTAX</span></span>

### <span data-ttu-id="af96a-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af96a-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af96a-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="af96a-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af96a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af96a-107">DESCRIPTION</span></span>
<span data-ttu-id="af96a-108">A **Remove-AzVmssDataDisk** parancsmag a Virtual Machine Scale set (VMSS) példányból távolítja el az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="af96a-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="af96a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af96a-109">EXAMPLES</span></span>

### <span data-ttu-id="af96a-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af96a-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="af96a-111">Ez a parancs eltávolítja az "DataDisk1" nevű adatlemezt a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="af96a-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="af96a-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="af96a-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="af96a-113">Ez a parancs eltávolítja a LUN 0 adatlemezét a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="af96a-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="af96a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af96a-114">PARAMETERS</span></span>

### <span data-ttu-id="af96a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af96a-115">-DefaultProfile</span></span>
<span data-ttu-id="af96a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af96a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af96a-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="af96a-117">-Lun</span></span>
<span data-ttu-id="af96a-118">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af96a-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af96a-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af96a-119">-Name</span></span>
<span data-ttu-id="af96a-120">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af96a-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="af96a-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af96a-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="af96a-122">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="af96a-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="af96a-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af96a-123">-Confirm</span></span>
<span data-ttu-id="af96a-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af96a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af96a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af96a-125">-WhatIf</span></span>
<span data-ttu-id="af96a-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af96a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af96a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af96a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af96a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af96a-128">CommonParameters</span></span>
<span data-ttu-id="af96a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af96a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af96a-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af96a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af96a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af96a-131">INPUTS</span></span>

### <span data-ttu-id="af96a-132">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af96a-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="af96a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="af96a-133">System.String</span></span>

### <span data-ttu-id="af96a-134">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af96a-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="af96a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af96a-135">OUTPUTS</span></span>

### <span data-ttu-id="af96a-136">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af96a-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="af96a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af96a-137">NOTES</span></span>

## <span data-ttu-id="af96a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af96a-138">RELATED LINKS</span></span>
