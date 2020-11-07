---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: c1a1b95dcaa06d922b0357d0e9e6a1b75fa7d793
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844717"
---
# <span data-ttu-id="68538-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="68538-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="68538-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68538-102">SYNOPSIS</span></span>
<span data-ttu-id="68538-103">Adatlemez felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="68538-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="68538-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68538-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68538-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68538-105">DESCRIPTION</span></span>
<span data-ttu-id="68538-106">Az **Add-AzVmssDataDisk** parancsmag adatlemezt ad hozzá a Virtual Machine Scale set (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="68538-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="68538-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68538-107">EXAMPLES</span></span>

### <span data-ttu-id="68538-108">1. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="68538-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="68538-109">Ez a parancs üres adatlemezt ad a VMSS objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="68538-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="68538-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68538-110">PARAMETERS</span></span>

### <span data-ttu-id="68538-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="68538-111">-Caching</span></span>
<span data-ttu-id="68538-112">A lemez gyorsítótár-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68538-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="68538-113">-CreateOption</span></span>
<span data-ttu-id="68538-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="68538-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68538-115">-DefaultProfile</span></span>
<span data-ttu-id="68538-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68538-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68538-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="68538-117">-DiskSizeGB</span></span>
<span data-ttu-id="68538-118">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="68538-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="68538-119">-Lun</span></span>
<span data-ttu-id="68538-120">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68538-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68538-121">-Name</span></span>
<span data-ttu-id="68538-122">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68538-122">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="68538-123">-StorageAccountType</span></span>
<span data-ttu-id="68538-124">A lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="68538-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68538-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68538-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="68538-126">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="68538-126">Specify the VMSS object.</span></span>
<span data-ttu-id="68538-127">Az objektum létrehozásához használhatja a [New-AzVmssConfig](./New-AzVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="68538-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="68538-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="68538-128">-WriteAccelerator</span></span>
<span data-ttu-id="68538-129">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="68538-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68538-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="68538-130">-Confirm</span></span>
<span data-ttu-id="68538-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="68538-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68538-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68538-132">-WhatIf</span></span>
<span data-ttu-id="68538-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="68538-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68538-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="68538-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68538-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68538-135">CommonParameters</span></span>
<span data-ttu-id="68538-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68538-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68538-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68538-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68538-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68538-138">INPUTS</span></span>

### <span data-ttu-id="68538-139">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68538-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="68538-140">System. String System. Int32 System. null `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. kiszámítás. models. DiskCreateOptionTypes, Microsoft. Azure. Management. számítási, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] System. null `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. re. számítás. StorageAccountTypes. 14.0.0.0. PublicKeyToken. 31bf3856ad364e35..</span><span class="sxs-lookup"><span data-stu-id="68538-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="68538-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68538-141">OUTPUTS</span></span>

### <span data-ttu-id="68538-142">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="68538-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="68538-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68538-143">NOTES</span></span>

## <span data-ttu-id="68538-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68538-144">RELATED LINKS</span></span>

