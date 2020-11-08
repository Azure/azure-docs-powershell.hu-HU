---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025750"
---
# <span data-ttu-id="198d7-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="198d7-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="198d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="198d7-102">SYNOPSIS</span></span>
<span data-ttu-id="198d7-103">Adatlemez felvétele virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="198d7-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="198d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="198d7-104">SYNTAX</span></span>

### <span data-ttu-id="198d7-105">VmNormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="198d7-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="198d7-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="198d7-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="198d7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="198d7-107">DESCRIPTION</span></span>
<span data-ttu-id="198d7-108">Az **Add-AzVMDataDisk** parancsmag adatlemezt ad hozzá egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="198d7-109">A virtuális gép létrehozásakor adatlemezt vehet fel, vagy egy meglévő virtuális géphez is hozzáadhat egy adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="198d7-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="198d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="198d7-110">EXAMPLES</span></span>

### <span data-ttu-id="198d7-111">1. példa: adatlemezek hozzáadása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="198d7-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="198d7-112">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="198d7-113">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="198d7-114">A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="198d7-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="198d7-115">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="198d7-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="198d7-116">Az utolsó három parancs minden olyan adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="198d7-117">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="198d7-118">Az egyes lemezek URI-ja $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03-es verzióban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="198d7-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="198d7-119">2. példa: adatlemez hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="198d7-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="198d7-120">Az első parancs a [Get-AzVM](./Get-AzVM.md) parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="198d7-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="198d7-121">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="198d7-122">A második parancs adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="198d7-123">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="198d7-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="198d7-124">3. példa: adatlemez hozzáadása egy új virtuális géphez egy általános felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="198d7-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="198d7-125">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="198d7-126">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="198d7-127">A következő két parancs az Adatkép és az adatlemezek elérési útját rendeli az $DataImageUrihez, és $DataDiskUri változókat.</span><span class="sxs-lookup"><span data-stu-id="198d7-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="198d7-128">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="198d7-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="198d7-129">A végleges parancsok felveszi az adatlemezt a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="198d7-130">A parancs a lemez fájlnevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="198d7-131">4. példa: adatlemezek hozzáadása egy új virtuális géphez egy speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="198d7-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="198d7-132">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="198d7-133">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="198d7-134">A következő parancsok az adatlemez elérési útját a $DataDiskUri változóhoz rendelik.</span><span class="sxs-lookup"><span data-stu-id="198d7-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="198d7-135">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="198d7-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="198d7-136">A végleges parancs adatlemezt hoz létre a $VirtualMachine tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="198d7-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="198d7-137">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="198d7-138">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="198d7-138">PARAMETERS</span></span>

### <span data-ttu-id="198d7-139">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="198d7-139">-Caching</span></span>
<span data-ttu-id="198d7-140">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="198d7-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="198d7-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="198d7-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="198d7-142">ReadOnly</span></span>
- <span data-ttu-id="198d7-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="198d7-143">ReadWrite</span></span>
- <span data-ttu-id="198d7-144">Nincs az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="198d7-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="198d7-145">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="198d7-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="198d7-146">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="198d7-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="198d7-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="198d7-147">-CreateOption</span></span>
<span data-ttu-id="198d7-148">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="198d7-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="198d7-149">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="198d7-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="198d7-150">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-150">Attach.</span></span>
<span data-ttu-id="198d7-151">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="198d7-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="198d7-152">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="198d7-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="198d7-153">A *VhdUri* mindent meg kell tennie ahhoz, hogy az Azure platform a virtuális merevlemez (VHD) helyét a virtuális gép adatlemezéhez csatolja.</span><span class="sxs-lookup"><span data-stu-id="198d7-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="198d7-154">Üres.</span><span class="sxs-lookup"><span data-stu-id="198d7-154">Empty.</span></span>
<span data-ttu-id="198d7-155">Ezzel a beállítással üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="198d7-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="198d7-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="198d7-156">FromImage.</span></span>
<span data-ttu-id="198d7-157">Ezt a lehetőséget választva virtuális gépet hozhat létre általános képből vagy lemezről.</span><span class="sxs-lookup"><span data-stu-id="198d7-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="198d7-158">Ha ezt a beállítást választja, akkor a *SourceImageUri* paramétert is meg kell adnia, hogy az Azure platform a VHD-fájlnak az adatlemezhez való csatolását adja.</span><span class="sxs-lookup"><span data-stu-id="198d7-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="198d7-159">A *VhdUri* paraméter az a hely, ahol az ADATlemez VHD-adatlemeze a virtuális gép általi használat után tárolódik.</span><span class="sxs-lookup"><span data-stu-id="198d7-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="198d7-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="198d7-160">-DefaultProfile</span></span>
<span data-ttu-id="198d7-161">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="198d7-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="198d7-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="198d7-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="198d7-163">Az ügyfél által felügyelt lemezvezérlő-titkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="198d7-164">Ezt csak a felügyelt lemezek esetében lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="198d7-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="198d7-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="198d7-165">-DiskSizeInGB</span></span>
<span data-ttu-id="198d7-166">Itt adhatja meg a virtuális géphez csatolni kívánt üres lemez méretét gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="198d7-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="198d7-167">-LUN</span><span class="sxs-lookup"><span data-stu-id="198d7-167">-Lun</span></span>
<span data-ttu-id="198d7-168">Az adatlemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="198d7-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="198d7-169">-ManagedDiskId</span></span>
<span data-ttu-id="198d7-170">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="198d7-171">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="198d7-171">-Name</span></span>
<span data-ttu-id="198d7-172">A hozzáadni kívánt adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="198d7-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="198d7-173">-SourceImageUri</span></span>
<span data-ttu-id="198d7-174">Annak a lemeznek az erőforrás-URI-azonosítóját adja meg, amelyre a parancsmag csatolva van.</span><span class="sxs-lookup"><span data-stu-id="198d7-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="198d7-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="198d7-175">-StorageAccountType</span></span>
<span data-ttu-id="198d7-176">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="198d7-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="198d7-177">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="198d7-177">-VhdUri</span></span>
<span data-ttu-id="198d7-178">A virtuális merevlemez (VHD-fájl) egységes erőforrás-azonosítóját adja meg, amely a platform képe vagy a felhasználói kép használatakor hozható létre.</span><span class="sxs-lookup"><span data-stu-id="198d7-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="198d7-179">Ez a parancsmag a binárisan nagy objektumot (blob) másolja át erre a helyre.</span><span class="sxs-lookup"><span data-stu-id="198d7-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="198d7-180">Az a hely, ahonnan a virtuális gépet el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="198d7-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="198d7-181">-VM</span><span class="sxs-lookup"><span data-stu-id="198d7-181">-VM</span></span>
<span data-ttu-id="198d7-182">Annak a helyi virtuális gépnek az objektumát adja meg, amelyhez adatlemezt kíván hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="198d7-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="198d7-183">A **Get-AzVM** parancsmaggal egy virtuálisgép-objektum beszerzése használható.</span><span class="sxs-lookup"><span data-stu-id="198d7-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="198d7-184">A **New-AzVMConfig** parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="198d7-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="198d7-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="198d7-185">-WriteAccelerator</span></span>
<span data-ttu-id="198d7-186">Itt adhatja meg, hogy a WriteAccelerator engedélyezve vagy Letiltva van-e egy felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="198d7-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="198d7-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198d7-187">CommonParameters</span></span>
<span data-ttu-id="198d7-188">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="198d7-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198d7-189">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="198d7-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198d7-190">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="198d7-190">INPUTS</span></span>

### <span data-ttu-id="198d7-191">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="198d7-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="198d7-192">System. String</span><span class="sxs-lookup"><span data-stu-id="198d7-192">System.String</span></span>

### <span data-ttu-id="198d7-193">Microsoft. Azure. Management. kiszámítás. models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="198d7-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="198d7-194">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="198d7-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="198d7-195">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="198d7-195">OUTPUTS</span></span>

### <span data-ttu-id="198d7-196">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="198d7-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="198d7-197">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="198d7-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="198d7-198">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="198d7-198">NOTES</span></span>

## <span data-ttu-id="198d7-199">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="198d7-199">RELATED LINKS</span></span>

[<span data-ttu-id="198d7-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="198d7-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="198d7-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="198d7-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="198d7-202">Új – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="198d7-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
