---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844349"
---
# <span data-ttu-id="54e8f-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="54e8f-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="54e8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="54e8f-103">Adatlemez eltávolítása a VMSS.</span><span class="sxs-lookup"><span data-stu-id="54e8f-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="54e8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54e8f-104">SYNTAX</span></span>

### <span data-ttu-id="54e8f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e8f-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54e8f-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="54e8f-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e8f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="54e8f-107">DESCRIPTION</span></span>
<span data-ttu-id="54e8f-108">A **Remove-AzVmssDataDisk** parancsmag a Virtual Machine Scale set (VMSS) példányból távolítja el az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="54e8f-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="54e8f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="54e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="54e8f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54e8f-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="54e8f-111">Ez a parancs eltávolítja az "DataDisk1" nevű adatlemezt a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="54e8f-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="54e8f-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="54e8f-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="54e8f-113">Ez a parancs eltávolítja a LUN 0 adatlemezét a VMSS objektumból.</span><span class="sxs-lookup"><span data-stu-id="54e8f-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="54e8f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54e8f-114">PARAMETERS</span></span>

### <span data-ttu-id="54e8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e8f-115">-DefaultProfile</span></span>
<span data-ttu-id="54e8f-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54e8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e8f-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="54e8f-117">-Lun</span></span>
<span data-ttu-id="54e8f-118">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="54e8f-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="54e8f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="54e8f-119">-Name</span></span>
<span data-ttu-id="54e8f-120">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="54e8f-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="54e8f-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54e8f-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="54e8f-122">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="54e8f-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="54e8f-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54e8f-123">-Confirm</span></span>
<span data-ttu-id="54e8f-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54e8f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e8f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e8f-125">-WhatIf</span></span>
<span data-ttu-id="54e8f-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54e8f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e8f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54e8f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e8f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e8f-128">CommonParameters</span></span>
<span data-ttu-id="54e8f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54e8f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e8f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e8f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e8f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e8f-131">INPUTS</span></span>

### <span data-ttu-id="54e8f-132">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54e8f-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="54e8f-133">System. String System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54e8f-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="54e8f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54e8f-134">OUTPUTS</span></span>

### <span data-ttu-id="54e8f-135">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54e8f-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="54e8f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54e8f-136">NOTES</span></span>

## <span data-ttu-id="54e8f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54e8f-137">RELATED LINKS</span></span>

