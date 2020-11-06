---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499027"
---
# <span data-ttu-id="2db67-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2db67-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="2db67-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2db67-102">SYNOPSIS</span></span>
<span data-ttu-id="2db67-103">Egy virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="2db67-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2db67-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2db67-104">SYNTAX</span></span>

### <span data-ttu-id="2db67-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="2db67-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2db67-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="2db67-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2db67-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2db67-107">DESCRIPTION</span></span>
<span data-ttu-id="2db67-108">A **set-AzureRmVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="2db67-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="2db67-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2db67-109">EXAMPLES</span></span>

### <span data-ttu-id="2db67-110">Példa 1: adatlemez gyorsítótárazási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="2db67-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="2db67-111">Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="2db67-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="2db67-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2db67-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="2db67-113">A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="2db67-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="2db67-114">A parancs átadja az eredményt az Update-AzureRmVM parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="2db67-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="2db67-115">A gyorsítótárazási mód módosítása a virtuális gép újraindítását okozhatja.</span><span class="sxs-lookup"><span data-stu-id="2db67-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="2db67-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2db67-116">PARAMETERS</span></span>

### <span data-ttu-id="2db67-117">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="2db67-117">-Caching</span></span>
<span data-ttu-id="2db67-118">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2db67-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="2db67-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2db67-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2db67-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2db67-120">ReadOnly</span></span>
- <span data-ttu-id="2db67-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2db67-121">ReadWrite</span></span>

<span data-ttu-id="2db67-122">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2db67-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="2db67-123">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="2db67-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="2db67-124">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="2db67-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="2db67-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2db67-125">-DiskSizeInGB</span></span>
<span data-ttu-id="2db67-126">Az adatlemez méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="2db67-126">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="2db67-127">-LUN</span><span class="sxs-lookup"><span data-stu-id="2db67-127">-Lun</span></span>
<span data-ttu-id="2db67-128">Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2db67-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2db67-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2db67-129">-Name</span></span>
<span data-ttu-id="2db67-130">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="2db67-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2db67-131">-VM</span><span class="sxs-lookup"><span data-stu-id="2db67-131">-VM</span></span>
<span data-ttu-id="2db67-132">Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="2db67-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="2db67-133">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2db67-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="2db67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2db67-134">CommonParameters</span></span>
<span data-ttu-id="2db67-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2db67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2db67-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2db67-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2db67-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db67-137">INPUTS</span></span>

### <span data-ttu-id="2db67-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="2db67-138">None</span></span>
<span data-ttu-id="2db67-139">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2db67-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2db67-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2db67-140">OUTPUTS</span></span>

## <span data-ttu-id="2db67-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2db67-141">NOTES</span></span>

## <span data-ttu-id="2db67-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2db67-142">RELATED LINKS</span></span>

[<span data-ttu-id="2db67-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2db67-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2db67-144">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2db67-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


