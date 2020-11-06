---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492536"
---
# <span data-ttu-id="839bc-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="839bc-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="839bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="839bc-102">SYNOPSIS</span></span>
<span data-ttu-id="839bc-103">Adatlemez eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="839bc-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="839bc-104">SYNTAX</span></span>

### <span data-ttu-id="839bc-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="839bc-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="839bc-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="839bc-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="839bc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="839bc-107">DESCRIPTION</span></span>
<span data-ttu-id="839bc-108">A **Remove-AzureRmVmssDataDisk** parancsmag a Virtual Machine Scale set (VMSS) példányból távolítja el az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="839bc-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="839bc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="839bc-109">EXAMPLES</span></span>

### <span data-ttu-id="839bc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="839bc-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="839bc-111">Ez a parancs eltávolítja az "DataDisk1" nevű adatlemezt a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="839bc-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="839bc-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="839bc-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="839bc-113">Ez a parancs eltávolítja a LUN 0 adatlemezét a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="839bc-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="839bc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="839bc-114">PARAMETERS</span></span>

### <span data-ttu-id="839bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839bc-115">-DefaultProfile</span></span>
<span data-ttu-id="839bc-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="839bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839bc-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="839bc-117">-Lun</span></span>
<span data-ttu-id="839bc-118">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="839bc-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="839bc-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="839bc-119">-Name</span></span>
<span data-ttu-id="839bc-120">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="839bc-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="839bc-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="839bc-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="839bc-122">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="839bc-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="839bc-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="839bc-123">-Confirm</span></span>
<span data-ttu-id="839bc-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="839bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="839bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839bc-125">-WhatIf</span></span>
<span data-ttu-id="839bc-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="839bc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="839bc-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="839bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="839bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839bc-128">CommonParameters</span></span>
<span data-ttu-id="839bc-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="839bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839bc-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839bc-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="839bc-131">INPUTS</span></span>

### <span data-ttu-id="839bc-132">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="839bc-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="839bc-133">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="839bc-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="839bc-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="839bc-134">OUTPUTS</span></span>

### <span data-ttu-id="839bc-135">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="839bc-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="839bc-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="839bc-136">NOTES</span></span>

## <span data-ttu-id="839bc-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="839bc-137">RELATED LINKS</span></span>

