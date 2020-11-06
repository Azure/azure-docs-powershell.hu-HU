---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494563"
---
# <span data-ttu-id="761f4-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="761f4-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="761f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="761f4-102">SYNOPSIS</span></span>
<span data-ttu-id="761f4-103">Adatlemez felvétele virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="761f4-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="761f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="761f4-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="761f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="761f4-105">DESCRIPTION</span></span>
<span data-ttu-id="761f4-106">Az **Add-AzureRmVMDataDisk** parancsmag adatlemezt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="761f4-107">A virtuális gép létrehozásakor adatlemezt vehet fel, vagy egy meglévő virtuális géphez is hozzáadhat egy adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="761f4-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="761f4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="761f4-108">EXAMPLES</span></span>

### <span data-ttu-id="761f4-109">1. példa: adatlemezek hozzáadása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="761f4-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="761f4-110">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="761f4-111">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="761f4-112">A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="761f4-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="761f4-113">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="761f4-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="761f4-114">Az utolsó három parancs minden olyan adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="761f4-115">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="761f4-116">Az egyes lemezek URI-ja $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03-es verzióban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="761f4-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="761f4-117">2. példa: adatlemez hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="761f4-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="761f4-118">Az első parancs a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="761f4-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="761f4-119">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="761f4-120">A második parancs adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="761f4-121">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="761f4-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="761f4-122">3. példa: adatlemez hozzáadása egy új virtuális géphez egy általános felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="761f4-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="761f4-123">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="761f4-124">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="761f4-125">A következő két parancs az Adatkép és az adatlemezek elérési útját rendeli az $DataImageUrihez, és $DataDiskUri változókat.</span><span class="sxs-lookup"><span data-stu-id="761f4-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="761f4-126">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="761f4-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="761f4-127">A végleges parancsok felveszi az adatlemezt a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="761f4-128">A parancs a lemez fájlnevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="761f4-129">4. példa: adatlemezek hozzáadása egy új virtuális géphez egy speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="761f4-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="761f4-130">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="761f4-131">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="761f4-132">A következő parancsok az adatlemez elérési útját a $DataDiskUri változóhoz rendelik.</span><span class="sxs-lookup"><span data-stu-id="761f4-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="761f4-133">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="761f4-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="761f4-134">A végleges parancs adatlemezt hoz létre a $VirtualMachine tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="761f4-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="761f4-135">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="761f4-136">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="761f4-136">PARAMETERS</span></span>

### <span data-ttu-id="761f4-137">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="761f4-137">-Caching</span></span>
<span data-ttu-id="761f4-138">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="761f4-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="761f4-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="761f4-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="761f4-140">ReadOnly</span></span>
- <span data-ttu-id="761f4-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="761f4-141">ReadWrite</span></span>
- <span data-ttu-id="761f4-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="761f4-142">None</span></span>

<span data-ttu-id="761f4-143">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="761f4-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="761f4-144">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="761f4-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="761f4-145">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="761f4-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="761f4-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="761f4-146">-CreateOption</span></span>
<span data-ttu-id="761f4-147">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="761f4-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="761f4-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="761f4-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="761f4-149">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-149">Attach.</span></span>
<span data-ttu-id="761f4-150">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="761f4-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="761f4-151">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="761f4-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="761f4-152">A *VhdUri* mindent meg kell tennie ahhoz, hogy az Azure platform a virtuális merevlemez (VHD) helyét a virtuális gép adatlemezéhez csatolja.</span><span class="sxs-lookup"><span data-stu-id="761f4-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="761f4-153">Üres.</span><span class="sxs-lookup"><span data-stu-id="761f4-153">Empty.</span></span>
<span data-ttu-id="761f4-154">Ezzel a beállítással üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="761f4-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="761f4-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="761f4-155">FromImage.</span></span>
<span data-ttu-id="761f4-156">Ezt a lehetőséget választva virtuális gépet hozhat létre általános képből vagy lemezről.</span><span class="sxs-lookup"><span data-stu-id="761f4-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="761f4-157">Ha ezt a beállítást választja, akkor a *SourceImageUri* paramétert is meg kell adnia, hogy az Azure platform a VHD-fájlnak az adatlemezhez való csatolását adja.</span><span class="sxs-lookup"><span data-stu-id="761f4-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="761f4-158">A *VhdUri* paraméter az a hely, ahol az ADATlemez VHD-adatlemeze a virtuális gép általi használat után tárolódik.</span><span class="sxs-lookup"><span data-stu-id="761f4-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="761f4-159">-DiskSizeInGB</span></span>
<span data-ttu-id="761f4-160">Itt adhatja meg a virtuális géphez csatolni kívánt üres lemez méretét gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="761f4-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-161">-LUN</span><span class="sxs-lookup"><span data-stu-id="761f4-161">-Lun</span></span>
<span data-ttu-id="761f4-162">Az adatlemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-163">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="761f4-163">-ManagedDiskId</span></span>
<span data-ttu-id="761f4-164">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-165">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="761f4-165">-Name</span></span>
<span data-ttu-id="761f4-166">A hozzáadni kívánt adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-166">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="761f4-167">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="761f4-167">-SourceImageUri</span></span>
<span data-ttu-id="761f4-168">Annak a lemeznek az erőforrás-URI-azonosítóját adja meg, amelyre a parancsmag csatolva van.</span><span class="sxs-lookup"><span data-stu-id="761f4-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="761f4-169">-StorageAccountType</span></span>
<span data-ttu-id="761f4-170">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="761f4-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="761f4-171">-VhdUri</span></span>
<span data-ttu-id="761f4-172">A virtuális merevlemez (VHD-fájl) egységes erőforrás-azonosítóját adja meg, amely a platform képe vagy a felhasználói kép használatakor hozható létre.</span><span class="sxs-lookup"><span data-stu-id="761f4-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="761f4-173">Ez a parancsmag a binárisan nagy objektumot (blob) másolja át erre a helyre.</span><span class="sxs-lookup"><span data-stu-id="761f4-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="761f4-174">Az a hely, ahonnan a virtuális gépet el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="761f4-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761f4-175">-VM</span><span class="sxs-lookup"><span data-stu-id="761f4-175">-VM</span></span>
<span data-ttu-id="761f4-176">Annak a helyi virtuális gépnek az objektumát adja meg, amelyhez adatlemezt kíván hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="761f4-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="761f4-177">A **Get-AzureRmVM** parancsmaggal egy virtuálisgép-objektum beszerzése használható.</span><span class="sxs-lookup"><span data-stu-id="761f4-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="761f4-178">A **New-AzureRmVMConfig** parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="761f4-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="761f4-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761f4-179">CommonParameters</span></span>
<span data-ttu-id="761f4-180">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="761f4-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761f4-181">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="761f4-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761f4-182">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="761f4-182">INPUTS</span></span>

### <span data-ttu-id="761f4-183">Nincs</span><span class="sxs-lookup"><span data-stu-id="761f4-183">None</span></span>
<span data-ttu-id="761f4-184">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="761f4-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="761f4-185">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="761f4-185">OUTPUTS</span></span>

## <span data-ttu-id="761f4-186">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="761f4-186">NOTES</span></span>

## <span data-ttu-id="761f4-187">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="761f4-187">RELATED LINKS</span></span>

[<span data-ttu-id="761f4-188">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="761f4-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="761f4-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="761f4-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="761f4-190">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="761f4-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
