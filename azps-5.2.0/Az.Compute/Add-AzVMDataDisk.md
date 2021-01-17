---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352110"
---
# <span data-ttu-id="b523c-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b523c-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="b523c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b523c-102">SYNOPSIS</span></span>
<span data-ttu-id="b523c-103">Adatlemezt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="b523c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b523c-104">SYNTAX</span></span>

### <span data-ttu-id="b523c-105">VmNormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b523c-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b523c-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="b523c-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b523c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b523c-107">DESCRIPTION</span></span>
<span data-ttu-id="b523c-108">Az **Add-AzVMDataDisk** parancsmag hozzáad egy adatlemezt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="b523c-109">Adatlemezt hozzáadhat virtuális gép létrehozásakor, vagy hozzáadhat egy adatlemezt egy meglévő virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="b523c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b523c-110">EXAMPLES</span></span>

### <span data-ttu-id="b523c-111">1. példa: Adatlemezek hozzáadása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="b523c-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="b523c-112">Az első parancs létrehoz egy virtuális gépi objektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="b523c-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b523c-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b523c-114">A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változókhoz.</span><span class="sxs-lookup"><span data-stu-id="b523c-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="b523c-115">Ez a megközelítés csak az alábbi parancsok olvashatóságát közelíti meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b523c-116">Az utolsó három parancs egy-egy adatlemezt ad hozzá a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b523c-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b523c-117">A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b523c-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="b523c-118">Az egyes lemezeket a $DataDiskVhdUri 01, a $DataDiskVhdUri 02 és a $DataDiskVhdUri 03 tárolja.</span><span class="sxs-lookup"><span data-stu-id="b523c-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="b523c-119">2. példa: Adatlemez hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="b523c-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="b523c-120">Az első parancs a VirtualMachine07 nevű virtuális gépet kapja meg [a Get-AzVM parancsmag](./Get-AzVM.md) használatával.</span><span class="sxs-lookup"><span data-stu-id="b523c-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b523c-121">A parancs a virtuális gépet a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="b523c-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b523c-122">A második parancs hozzáad egy adatlemezt a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b523c-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b523c-123">Az utolsó parancs frissíti a ResourceGroup11-ben $VirtualMachine virtuális gép állapotát.</span><span class="sxs-lookup"><span data-stu-id="b523c-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="b523c-124">3. példa: Adatlemez hozzáadása új virtuális géphez egy általánosított felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="b523c-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="b523c-125">Az első parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="b523c-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b523c-126">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b523c-127">A következő két parancs az adatkép és az adatlemezek elérési útját rendeli a $DataImageUri és $DataDiskUri változókhoz.</span><span class="sxs-lookup"><span data-stu-id="b523c-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="b523c-128">Ez a módszer az alábbi parancsok olvashatóságának javítására használható.</span><span class="sxs-lookup"><span data-stu-id="b523c-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b523c-129">Az utolsó parancsok hozzáadnak egy adatlemezt a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b523c-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b523c-130">A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b523c-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="b523c-131">4. példa: Adatlemezek hozzáadása új virtuális géphez egy speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="b523c-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="b523c-132">Az első parancs létrehoz egy virtuális gépi objektumot, és azt a $VirtualMachine tárolja.</span><span class="sxs-lookup"><span data-stu-id="b523c-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b523c-133">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b523c-134">A következő parancsok az adatlemez elérési útját rendelik a $DataDiskUri változóhoz.</span><span class="sxs-lookup"><span data-stu-id="b523c-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="b523c-135">Ez a módszer az alábbi parancsok olvashatóságának javítására használható.</span><span class="sxs-lookup"><span data-stu-id="b523c-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="b523c-136">Az utolsó parancs egy adatlemezt ad hozzá a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b523c-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b523c-137">A parancs megadja a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b523c-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="b523c-138">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b523c-138">PARAMETERS</span></span>

### <span data-ttu-id="b523c-139">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="b523c-139">-Caching</span></span>
<span data-ttu-id="b523c-140">A lemez gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="b523c-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="b523c-141">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b523c-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b523c-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="b523c-142">ReadOnly</span></span>
- <span data-ttu-id="b523c-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b523c-143">ReadWrite</span></span>
- <span data-ttu-id="b523c-144">Nincs az alapértelmezett érték a Beolvasott érték.</span><span class="sxs-lookup"><span data-stu-id="b523c-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="b523c-145">Ha módosítja ezt az értéket, a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="b523c-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="b523c-146">Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="b523c-146">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b523c-147">-CreateOption</span></span>
<span data-ttu-id="b523c-148">Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="b523c-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="b523c-149">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b523c-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b523c-150">Csatolás 2010.</span><span class="sxs-lookup"><span data-stu-id="b523c-150">Attach.</span></span>
<span data-ttu-id="b523c-151">Akkor válassza ezt a lehetőséget, ha egy speciális lemezről hoz létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b523c-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="b523c-152">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri paramétert.*</span><span class="sxs-lookup"><span data-stu-id="b523c-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="b523c-153">A *VhdUri* szükséges ahhoz, hogy az Azure platformnak meg tudja mondani a virtuális merevlemez (VHD) helyét, hogy adatlemezként csatolja a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="b523c-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="b523c-154">Üres.</span><span class="sxs-lookup"><span data-stu-id="b523c-154">Empty.</span></span>
<span data-ttu-id="b523c-155">Ezt megadásával üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b523c-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="b523c-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="b523c-156">FromImage.</span></span>
<span data-ttu-id="b523c-157">Akkor válassza ezt a lehetőséget, ha általánosított képből vagy lemezről hoz létre virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b523c-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="b523c-158">Ha megadja ezt a beállítást, a *SourceImageUri* paramétert is meg kell adnia ahhoz, hogy az Azure-platformnak meg tudja határozni a VHD adatlemezként csatolható helyét.</span><span class="sxs-lookup"><span data-stu-id="b523c-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="b523c-159">A *VhdUri* paraméter a virtuális gép által használt adatlemez helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b523c-160">-DefaultProfile</span></span>
<span data-ttu-id="b523c-161">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b523c-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b523c-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b523c-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b523c-163">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="b523c-164">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="b523c-164">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b523c-165">-DiskSizeInGB</span></span>
<span data-ttu-id="b523c-166">Egy virtuális géphez csatolni kívánt üres lemez gigabájtban megadott mérete.</span><span class="sxs-lookup"><span data-stu-id="b523c-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-167">-Lun</span><span class="sxs-lookup"><span data-stu-id="b523c-167">-Lun</span></span>
<span data-ttu-id="b523c-168">Egy adatlemez logikai egységszámát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="b523c-169">-ManagedDiskId</span></span>
<span data-ttu-id="b523c-170">Egy felügyelt lemez azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-170">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-171">-Name</span><span class="sxs-lookup"><span data-stu-id="b523c-171">-Name</span></span>
<span data-ttu-id="b523c-172">A hozzáadni szükséges adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="b523c-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="b523c-173">-SourceImageUri</span></span>
<span data-ttu-id="b523c-174">Annak a lemeznek az URI-ját adja meg, amelyhez a parancsmag csatolja.</span><span class="sxs-lookup"><span data-stu-id="b523c-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b523c-175">-StorageAccountType</span></span>
<span data-ttu-id="b523c-176">A felügyelt lemez tárfióktípusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b523c-176">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="b523c-177">-VhdUri</span></span>
<span data-ttu-id="b523c-178">Megadja a virtuális merevlemez -fájl (VHD) egységes erőforrás-azonosítóját (URI), amely platformkép vagy felhasználói kép használata esetén hozható létre.</span><span class="sxs-lookup"><span data-stu-id="b523c-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="b523c-179">Ez a parancsmag a kép bináris nagy objektumát (blobját) másolja erre a helyre.</span><span class="sxs-lookup"><span data-stu-id="b523c-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="b523c-180">Ez az a hely, ahol elindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="b523c-180">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-181">-VM</span><span class="sxs-lookup"><span data-stu-id="b523c-181">-VM</span></span>
<span data-ttu-id="b523c-182">Azt a helyi virtuális gépobjektumot adja meg, amelyhez adatlemezt szeretne hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="b523c-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="b523c-183">A **Get-AzVM parancsmag** használatával virtuális gépi objektumot szerezhet be.</span><span class="sxs-lookup"><span data-stu-id="b523c-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="b523c-184">A **New-AzVMConfig** parancsmaggal virtuális gépi objektumot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="b523c-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="b523c-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="b523c-185">-WriteAccelerator</span></span>
<span data-ttu-id="b523c-186">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="b523c-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b523c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b523c-187">CommonParameters</span></span>
<span data-ttu-id="b523c-188">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b523c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b523c-189">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b523c-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b523c-190">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b523c-190">INPUTS</span></span>

### <span data-ttu-id="b523c-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b523c-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b523c-192">System.String</span><span class="sxs-lookup"><span data-stu-id="b523c-192">System.String</span></span>

### <span data-ttu-id="b523c-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="b523c-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="b523c-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b523c-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b523c-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b523c-195">OUTPUTS</span></span>

### <span data-ttu-id="b523c-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b523c-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b523c-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="b523c-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b523c-198">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b523c-198">NOTES</span></span>

## <span data-ttu-id="b523c-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b523c-199">RELATED LINKS</span></span>

[<span data-ttu-id="b523c-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b523c-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="b523c-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b523c-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b523c-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b523c-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
