---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: 53ad88f6e3df11eb3a8f2f9c4b21af40b9ea614b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850901"
---
# <span data-ttu-id="347c2-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="347c2-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="347c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="347c2-102">SYNOPSIS</span></span>
<span data-ttu-id="347c2-103">Egy virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="347c2-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="347c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="347c2-104">SYNTAX</span></span>

### <span data-ttu-id="347c2-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="347c2-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="347c2-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="347c2-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="347c2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="347c2-107">DESCRIPTION</span></span>
<span data-ttu-id="347c2-108">A **set-AzureRmVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="347c2-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="347c2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="347c2-109">EXAMPLES</span></span>

### <span data-ttu-id="347c2-110">Példa 1: adatlemez gyorsítótárazási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="347c2-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="347c2-111">Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="347c2-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="347c2-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="347c2-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="347c2-113">A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="347c2-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="347c2-114">A parancs átadja az eredményt az Update-AzureRmVM parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="347c2-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="347c2-115">A befizetési mód módosítása a virtuális gép újraindítását okozhatja.</span><span class="sxs-lookup"><span data-stu-id="347c2-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="347c2-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="347c2-116">PARAMETERS</span></span>

### <span data-ttu-id="347c2-117">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="347c2-117">-Caching</span></span>
<span data-ttu-id="347c2-118">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="347c2-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="347c2-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="347c2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="347c2-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="347c2-120">ReadOnly</span></span>
- <span data-ttu-id="347c2-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="347c2-121">ReadWrite</span></span>

<span data-ttu-id="347c2-122">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="347c2-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="347c2-123">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="347c2-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="347c2-124">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="347c2-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347c2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347c2-125">-DefaultProfile</span></span>
<span data-ttu-id="347c2-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="347c2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="347c2-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="347c2-127">-DiskSizeInGB</span></span>
<span data-ttu-id="347c2-128">Az adatlemez méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="347c2-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347c2-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="347c2-129">-Lun</span></span>
<span data-ttu-id="347c2-130">Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="347c2-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347c2-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="347c2-131">-Name</span></span>
<span data-ttu-id="347c2-132">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="347c2-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347c2-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="347c2-133">-StorageAccountType</span></span>
<span data-ttu-id="347c2-134">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="347c2-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="347c2-135">-VM</span><span class="sxs-lookup"><span data-stu-id="347c2-135">-VM</span></span>
<span data-ttu-id="347c2-136">Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="347c2-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="347c2-137">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="347c2-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="347c2-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="347c2-138">-WriteAccelerator</span></span>
<span data-ttu-id="347c2-139">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="347c2-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="347c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347c2-140">CommonParameters</span></span>
<span data-ttu-id="347c2-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="347c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347c2-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="347c2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347c2-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="347c2-143">INPUTS</span></span>

### <span data-ttu-id="347c2-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="347c2-144">PSVirtualMachine</span></span>
<span data-ttu-id="347c2-145">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="347c2-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="347c2-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="347c2-146">OUTPUTS</span></span>

### <span data-ttu-id="347c2-147">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="347c2-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="347c2-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="347c2-148">NOTES</span></span>

## <span data-ttu-id="347c2-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="347c2-149">RELATED LINKS</span></span>

[<span data-ttu-id="347c2-150">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="347c2-150">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="347c2-151">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="347c2-151">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


