---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 5e04013ee8f9452ee28cf7975066f512e2eae1c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492570"
---
# <span data-ttu-id="505f7-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="505f7-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="505f7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="505f7-102">SYNOPSIS</span></span>
<span data-ttu-id="505f7-103">Adatlemez felvétele a VMSS.</span><span class="sxs-lookup"><span data-stu-id="505f7-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="505f7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="505f7-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="505f7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="505f7-105">DESCRIPTION</span></span>
<span data-ttu-id="505f7-106">Az **Add-AzureRmVmssDataDisk** parancsmag adatlemezt ad hozzá a Virtual Machine Scale set (VMSS) példányhoz.</span><span class="sxs-lookup"><span data-stu-id="505f7-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="505f7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="505f7-107">EXAMPLES</span></span>

### <span data-ttu-id="505f7-108">1. példa: adatlemez hozzáadása</span><span class="sxs-lookup"><span data-stu-id="505f7-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="505f7-109">Ez a parancs üres adatlemezt ad a VMSS objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="505f7-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="505f7-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="505f7-110">PARAMETERS</span></span>

### <span data-ttu-id="505f7-111">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="505f7-111">-Caching</span></span>
<span data-ttu-id="505f7-112">A lemez gyorsítótár-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="505f7-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="505f7-113">-CreateOption</span></span>
<span data-ttu-id="505f7-114">A lemez létrehozási beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="505f7-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505f7-115">-DefaultProfile</span></span>
<span data-ttu-id="505f7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="505f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505f7-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="505f7-117">-DiskSizeGB</span></span>
<span data-ttu-id="505f7-118">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="505f7-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="505f7-119">-Lun</span></span>
<span data-ttu-id="505f7-120">A lemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="505f7-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="505f7-121">-Name</span></span>
<span data-ttu-id="505f7-122">A lemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="505f7-122">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="505f7-123">-StorageAccountType</span></span>
<span data-ttu-id="505f7-124">A lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="505f7-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="505f7-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="505f7-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="505f7-126">Adja meg a VMSS objektumot.</span><span class="sxs-lookup"><span data-stu-id="505f7-126">Specify the VMSS object.</span></span>
<span data-ttu-id="505f7-127">Az objektum létrehozásához használhatja a [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="505f7-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="505f7-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="505f7-128">-Confirm</span></span>
<span data-ttu-id="505f7-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="505f7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505f7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505f7-130">-WhatIf</span></span>
<span data-ttu-id="505f7-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="505f7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="505f7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="505f7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="505f7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505f7-133">CommonParameters</span></span>
<span data-ttu-id="505f7-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="505f7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505f7-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="505f7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505f7-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="505f7-136">INPUTS</span></span>

### <span data-ttu-id="505f7-137">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="505f7-137">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="505f7-138">System. String System. Int32 System. null `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. kiszámítás. models. DiskCreateOptionTypes, Microsoft. Azure. Management. számítási, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] System. null `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. re. számítás. StorageAccountTypes. 14.0.0.0. PublicKeyToken. 31bf3856ad364e35..</span><span class="sxs-lookup"><span data-stu-id="505f7-138">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="505f7-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="505f7-139">OUTPUTS</span></span>

### <span data-ttu-id="505f7-140">Microsoft. Azure. Management. kiszámítás. models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="505f7-140">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="505f7-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="505f7-141">NOTES</span></span>

## <span data-ttu-id="505f7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="505f7-142">RELATED LINKS</span></span>

