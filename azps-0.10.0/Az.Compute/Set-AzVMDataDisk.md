---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844221"
---
# <span data-ttu-id="83936-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="83936-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="83936-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83936-102">SYNOPSIS</span></span>
<span data-ttu-id="83936-103">Egy virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="83936-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="83936-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83936-104">SYNTAX</span></span>

### <span data-ttu-id="83936-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="83936-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83936-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="83936-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83936-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="83936-107">DESCRIPTION</span></span>
<span data-ttu-id="83936-108">A **set-AzVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="83936-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="83936-109">Példák</span><span class="sxs-lookup"><span data-stu-id="83936-109">EXAMPLES</span></span>

### <span data-ttu-id="83936-110">Példa 1: adatlemez gyorsítótárazási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="83936-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="83936-111">Az első parancs a **Get-AzVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="83936-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="83936-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="83936-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="83936-113">A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="83936-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="83936-114">A parancs átadja az eredményt az Update-AzVM parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="83936-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="83936-115">A befizetési mód módosítása a virtuális gép újraindítását okozhatja.</span><span class="sxs-lookup"><span data-stu-id="83936-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="83936-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83936-116">PARAMETERS</span></span>

### <span data-ttu-id="83936-117">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="83936-117">-Caching</span></span>
<span data-ttu-id="83936-118">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="83936-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="83936-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="83936-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83936-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="83936-120">ReadOnly</span></span>
- <span data-ttu-id="83936-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83936-121">ReadWrite</span></span>

<span data-ttu-id="83936-122">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="83936-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="83936-123">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="83936-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="83936-124">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="83936-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="83936-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83936-125">-DefaultProfile</span></span>
<span data-ttu-id="83936-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83936-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83936-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="83936-127">-DiskSizeInGB</span></span>
<span data-ttu-id="83936-128">Az adatlemez méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="83936-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="83936-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="83936-129">-Lun</span></span>
<span data-ttu-id="83936-130">Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="83936-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="83936-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83936-131">-Name</span></span>
<span data-ttu-id="83936-132">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="83936-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="83936-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="83936-133">-StorageAccountType</span></span>
<span data-ttu-id="83936-134">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="83936-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="83936-135">-VM</span><span class="sxs-lookup"><span data-stu-id="83936-135">-VM</span></span>
<span data-ttu-id="83936-136">Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="83936-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="83936-137">A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="83936-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="83936-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="83936-138">-WriteAccelerator</span></span>
<span data-ttu-id="83936-139">Itt adhatja meg, hogy az adatlemezen engedélyezni vagy letiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="83936-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="83936-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83936-140">CommonParameters</span></span>
<span data-ttu-id="83936-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83936-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83936-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83936-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83936-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83936-143">INPUTS</span></span>

### <span data-ttu-id="83936-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="83936-144">PSVirtualMachine</span></span>
<span data-ttu-id="83936-145">A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="83936-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="83936-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83936-146">OUTPUTS</span></span>

### <span data-ttu-id="83936-147">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="83936-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="83936-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83936-148">NOTES</span></span>

## <span data-ttu-id="83936-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83936-149">RELATED LINKS</span></span>

[<span data-ttu-id="83936-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="83936-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="83936-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="83936-151">Update-AzVM</span></span>](./Update-AzVM.md)


