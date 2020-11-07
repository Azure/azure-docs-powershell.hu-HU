---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 16c15838b07ab2589f5590128f5d948ae3cd6be0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667218"
---
# <span data-ttu-id="60445-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="60445-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="60445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60445-102">SYNOPSIS</span></span>
<span data-ttu-id="60445-103">Egy virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="60445-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="60445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60445-104">SYNTAX</span></span>

### <span data-ttu-id="60445-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="60445-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60445-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="60445-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60445-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="60445-107">DESCRIPTION</span></span>
<span data-ttu-id="60445-108">A **set-AzVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="60445-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="60445-109">Példák</span><span class="sxs-lookup"><span data-stu-id="60445-109">EXAMPLES</span></span>

### <span data-ttu-id="60445-110">Példa 1: adatlemez gyorsítótárazási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="60445-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="60445-111">Az első parancs a **Get-AzVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="60445-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="60445-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="60445-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="60445-113">A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="60445-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="60445-114">A parancs átadja az eredményt az Update-AzVM parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="60445-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="60445-115">A befizetési mód módosítása a virtuális gép újraindítását okozhatja.</span><span class="sxs-lookup"><span data-stu-id="60445-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="60445-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60445-116">PARAMETERS</span></span>

### <span data-ttu-id="60445-117">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="60445-117">-Caching</span></span>
<span data-ttu-id="60445-118">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="60445-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="60445-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="60445-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60445-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="60445-120">ReadOnly</span></span>
- <span data-ttu-id="60445-121">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="60445-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="60445-122">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="60445-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="60445-123">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="60445-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60445-124">-DefaultProfile</span></span>
<span data-ttu-id="60445-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60445-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60445-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="60445-126">-DiskSizeInGB</span></span>
<span data-ttu-id="60445-127">Az adatlemez méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="60445-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="60445-128">-Lun</span></span>
<span data-ttu-id="60445-129">Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="60445-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="60445-130">-Name</span></span>
<span data-ttu-id="60445-131">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="60445-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="60445-132">-StorageAccountType</span></span>
<span data-ttu-id="60445-133">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="60445-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-134">-VM</span><span class="sxs-lookup"><span data-stu-id="60445-134">-VM</span></span>
<span data-ttu-id="60445-135">Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="60445-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="60445-136">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="60445-136">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60445-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="60445-137">-WriteAccelerator</span></span>
<span data-ttu-id="60445-138">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="60445-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60445-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60445-139">CommonParameters</span></span>
<span data-ttu-id="60445-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60445-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60445-141">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="60445-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60445-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60445-142">INPUTS</span></span>

### <span data-ttu-id="60445-143">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60445-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="60445-144">System. String</span><span class="sxs-lookup"><span data-stu-id="60445-144">System.String</span></span>

### <span data-ttu-id="60445-145">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="60445-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="60445-146">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="60445-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="60445-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60445-147">OUTPUTS</span></span>

### <span data-ttu-id="60445-148">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="60445-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="60445-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60445-149">NOTES</span></span>

## <span data-ttu-id="60445-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60445-150">RELATED LINKS</span></span>

[<span data-ttu-id="60445-151">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="60445-151">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="60445-152">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="60445-152">Update-AzVM</span></span>](./Update-AzVM.md)


