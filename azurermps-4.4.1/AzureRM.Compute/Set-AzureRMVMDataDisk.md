---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672063"
---
# <span data-ttu-id="ba2f9-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ba2f9-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="ba2f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2f9-103">Egy virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba2f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba2f9-104">SYNTAX</span></span>

### <span data-ttu-id="ba2f9-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="ba2f9-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba2f9-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="ba2f9-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba2f9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba2f9-107">DESCRIPTION</span></span>
<span data-ttu-id="ba2f9-108">A **set-AzureRmVMDataDisk** parancsmag a virtuális gép adatlemezének tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="ba2f9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba2f9-109">EXAMPLES</span></span>

### <span data-ttu-id="ba2f9-110">Példa 1: adatlemez gyorsítótárazási módjának módosítása</span><span class="sxs-lookup"><span data-stu-id="ba2f9-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="ba2f9-111">Az első parancs a **Get-AzureRmVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="ba2f9-112">A parancs a $VM változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="ba2f9-113">A második parancs módosítja a DataDisk01 nevű adatlemez gyorsítótárazási módját az $VM virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="ba2f9-114">A parancs átadja az eredményt az Update-AzureRmVM parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="ba2f9-115">A befizetési mód módosítása a virtuális gép újraindítását okozhatja.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="ba2f9-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba2f9-116">PARAMETERS</span></span>

### <span data-ttu-id="ba2f9-117">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="ba2f9-117">-Caching</span></span>
<span data-ttu-id="ba2f9-118">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="ba2f9-119">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="ba2f9-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba2f9-120">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ba2f9-120">ReadOnly</span></span>
- <span data-ttu-id="ba2f9-121">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ba2f9-121">ReadWrite</span></span>

<span data-ttu-id="ba2f9-122">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="ba2f9-123">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="ba2f9-124">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ba2f9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2f9-125">-DefaultProfile</span></span>
<span data-ttu-id="ba2f9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba2f9-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ba2f9-127">-DiskSizeInGB</span></span>
<span data-ttu-id="ba2f9-128">Az adatlemez méretének meghatározása gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="ba2f9-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="ba2f9-129">-Lun</span></span>
<span data-ttu-id="ba2f9-130">Annak a logikai egységnek a logikai egység számát adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba2f9-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ba2f9-131">-Name</span></span>
<span data-ttu-id="ba2f9-132">Megadja annak az adatlemeznek a nevét, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ba2f9-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ba2f9-133">-StorageAccountType</span></span>
<span data-ttu-id="ba2f9-134">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="ba2f9-135">-VM</span><span class="sxs-lookup"><span data-stu-id="ba2f9-135">-VM</span></span>
<span data-ttu-id="ba2f9-136">Azt a virtuális gépet adja meg, amelynek a parancsmagja módosította az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="ba2f9-137">A virtuálisgép-objektum beolvasásához használja az Get-AzureRmVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ba2f9-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="ba2f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2f9-138">CommonParameters</span></span>
<span data-ttu-id="ba2f9-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba2f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2f9-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba2f9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2f9-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba2f9-141">INPUTS</span></span>

## <span data-ttu-id="ba2f9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba2f9-142">OUTPUTS</span></span>

## <span data-ttu-id="ba2f9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba2f9-143">NOTES</span></span>

## <span data-ttu-id="ba2f9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba2f9-144">RELATED LINKS</span></span>

[<span data-ttu-id="ba2f9-145">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba2f9-145">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ba2f9-146">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba2f9-146">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


