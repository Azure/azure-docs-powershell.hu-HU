---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672033"
---
# <span data-ttu-id="69a6b-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="69a6b-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="69a6b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="69a6b-103">Adatlemez eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="69a6b-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69a6b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69a6b-104">SYNTAX</span></span>

### <span data-ttu-id="69a6b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69a6b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69a6b-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="69a6b-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69a6b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="69a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="69a6b-108">A **Remove-AzureRmVmssDataDisk** parancsmag a Virtual Machine Scale set (VMSS) példányból távolítja el az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="69a6b-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="69a6b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="69a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="69a6b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="69a6b-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="69a6b-111">Ez a parancs eltávolítja az "DataDisk1" nevű adatlemezt a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="69a6b-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="69a6b-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="69a6b-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="69a6b-113">Ez a parancs eltávolítja a LUN 0 adatlemezét a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="69a6b-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="69a6b-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69a6b-114">PARAMETERS</span></span>

### <span data-ttu-id="69a6b-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="69a6b-115">-Lun</span></span>
<span data-ttu-id="69a6b-116">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a6b-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69a6b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="69a6b-117">-Name</span></span>
<span data-ttu-id="69a6b-118">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="69a6b-118">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="69a6b-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69a6b-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="69a6b-120">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="69a6b-120">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="69a6b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="69a6b-121">-Confirm</span></span>
<span data-ttu-id="69a6b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="69a6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69a6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69a6b-123">-WhatIf</span></span>
<span data-ttu-id="69a6b-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="69a6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69a6b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="69a6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69a6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69a6b-126">CommonParameters</span></span>
<span data-ttu-id="69a6b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69a6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69a6b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69a6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69a6b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69a6b-129">INPUTS</span></span>

### <span data-ttu-id="69a6b-130">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69a6b-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="69a6b-131">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="69a6b-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="69a6b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69a6b-132">OUTPUTS</span></span>

### <span data-ttu-id="69a6b-133">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="69a6b-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="69a6b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69a6b-134">NOTES</span></span>

## <span data-ttu-id="69a6b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69a6b-135">RELATED LINKS</span></span>

