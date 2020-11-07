---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848941"
---
# <span data-ttu-id="34d42-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="34d42-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="34d42-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34d42-102">SYNOPSIS</span></span>
<span data-ttu-id="34d42-103">Adatlemez felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="34d42-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d42-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34d42-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d42-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="34d42-105">DESCRIPTION</span></span>
<span data-ttu-id="34d42-106">Az **Add-AzureRmVmssDataDisk** parancsmag adatlemezt ad hozzá a Virtual Machine Scale set (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="34d42-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="34d42-107">Példák</span><span class="sxs-lookup"><span data-stu-id="34d42-107">EXAMPLES</span></span>

### <span data-ttu-id="34d42-108">1. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="34d42-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="34d42-109">Ez a parancs üres adatlemezt ad a VMSS objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="34d42-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="34d42-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34d42-110">PARAMETERS</span></span>

### <span data-ttu-id="34d42-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="34d42-111">-Caching</span></span>
<span data-ttu-id="34d42-112">A lemez gyorsítótár-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="34d42-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="34d42-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="34d42-113">-CreateOption</span></span>
<span data-ttu-id="34d42-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="34d42-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="34d42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d42-115">-DefaultProfile</span></span>
<span data-ttu-id="34d42-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34d42-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34d42-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="34d42-117">-DiskSizeGB</span></span>
<span data-ttu-id="34d42-118">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="34d42-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="34d42-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="34d42-119">-Lun</span></span>
<span data-ttu-id="34d42-120">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="34d42-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="34d42-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34d42-121">-Name</span></span>
<span data-ttu-id="34d42-122">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="34d42-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="34d42-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="34d42-123">-StorageAccountType</span></span>
<span data-ttu-id="34d42-124">A lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="34d42-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="34d42-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34d42-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="34d42-126">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="34d42-126">Specify the VMSS object.</span></span>
<span data-ttu-id="34d42-127">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="34d42-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="34d42-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="34d42-128">-WriteAccelerator</span></span>
<span data-ttu-id="34d42-129">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="34d42-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="34d42-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="34d42-130">-Confirm</span></span>
<span data-ttu-id="34d42-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="34d42-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d42-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d42-132">-WhatIf</span></span>
<span data-ttu-id="34d42-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="34d42-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d42-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="34d42-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d42-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d42-135">CommonParameters</span></span>
<span data-ttu-id="34d42-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34d42-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d42-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d42-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d42-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34d42-138">INPUTS</span></span>

### <span data-ttu-id="34d42-139">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34d42-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="34d42-140">System. String System. Int32 System. null `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. kiszámítás. models. DiskCreateOptionTypes, Microsoft. Azure. Management. számítási, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] System. null `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. re. számítás. StorageAccountTypes. 14.0.0.0. PublicKeyToken. 31bf3856ad364e35..</span><span class="sxs-lookup"><span data-stu-id="34d42-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="34d42-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34d42-141">OUTPUTS</span></span>

### <span data-ttu-id="34d42-142">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34d42-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="34d42-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34d42-143">NOTES</span></span>

## <span data-ttu-id="34d42-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34d42-144">RELATED LINKS</span></span>

