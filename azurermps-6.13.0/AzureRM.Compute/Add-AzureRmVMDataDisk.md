---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500251"
---
# <span data-ttu-id="0c428-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0c428-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0c428-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0c428-102">SYNOPSIS</span></span>
<span data-ttu-id="0c428-103">Adatlemez hozzáadása virtuális géphez vagy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="0c428-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c428-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0c428-104">SYNTAX</span></span>

### <span data-ttu-id="0c428-105">VmNormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0c428-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c428-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0c428-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c428-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0c428-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c428-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0c428-108">DESCRIPTION</span></span>
<span data-ttu-id="0c428-109">Az **Add-AzureRmVMDataDisk** parancsmag egy virtuális gépre vagy egy Vmss VM-re helyezi az adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="0c428-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="0c428-110">A virtuális gép létrehozásakor adatlemezt vehet fel, vagy egy meglévő virtuális géphez is hozzáadhat egy adatlemezt.</span><span class="sxs-lookup"><span data-stu-id="0c428-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="0c428-111">Példák</span><span class="sxs-lookup"><span data-stu-id="0c428-111">EXAMPLES</span></span>

### <span data-ttu-id="0c428-112">1. példa: adatlemezek hozzáadása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="0c428-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="0c428-113">Az első parancs létrehoz egy virtuálisgép-objektumot, majd a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c428-114">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0c428-115">A következő három parancs három adatlemez elérési útját rendeli hozzá a $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="0c428-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="0c428-116">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="0c428-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="0c428-117">Az utolsó három parancs minden olyan adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0c428-118">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="0c428-119">Az egyes lemezek URI-ja $DataDiskVhdUri 01, $DataDiskVhdUri 02 és $DataDiskVhdUri 03-es verzióban van tárolva.</span><span class="sxs-lookup"><span data-stu-id="0c428-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="0c428-120">2. példa: adatlemez hozzáadása meglévő virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="0c428-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="0c428-121">Az első parancs a [Get-AzureRmVM](./Get-AzureRmVM.md) parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="0c428-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="0c428-122">A parancs a virtuális gépet a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c428-123">A második parancs adatlemezt ad az $VirtualMachine-ban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0c428-124">A végleges parancs frissíti a $VirtualMachineban tárolt virtuális gép állapotát a ResourceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="0c428-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="0c428-125">3. példa: adatlemez hozzáadása egy új virtuális géphez egy általános felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="0c428-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="0c428-126">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c428-127">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0c428-128">A következő két parancs az Adatkép és az adatlemezek elérési útját rendeli az $DataImageUrihez, és $DataDiskUri változókat.</span><span class="sxs-lookup"><span data-stu-id="0c428-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="0c428-129">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="0c428-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="0c428-130">A végleges parancsok felveszi az adatlemezt a $VirtualMachineban tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0c428-131">A parancs a lemez fájlnevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="0c428-132">4. példa: adatlemezek hozzáadása egy új virtuális géphez egy speciális felhasználói képből</span><span class="sxs-lookup"><span data-stu-id="0c428-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="0c428-133">Az első parancs létrehozza a virtuális gép objektumát, és a $VirtualMachine változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0c428-134">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0c428-135">A következő parancsok az adatlemez elérési útját a $DataDiskUri változóhoz rendelik.</span><span class="sxs-lookup"><span data-stu-id="0c428-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="0c428-136">Ezzel a megközelítéssel javíthatja az alábbi parancsok olvashatóságát.</span><span class="sxs-lookup"><span data-stu-id="0c428-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="0c428-137">A végleges parancs adatlemezt hoz létre a $VirtualMachine tárolt virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="0c428-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="0c428-138">A parancs a lemez nevét és helyét, valamint a lemez egyéb tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="0c428-139">Példa 5: felügyelt adatlemez felvétele Vmss VM-be</span><span class="sxs-lookup"><span data-stu-id="0c428-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="0c428-140">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="0c428-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="0c428-141">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="0c428-142">A következő parancs hozzáadja a távtárolású meghajtót az $VmssVM helyileg tárolt Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="0c428-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="0c428-143">A végleges parancs frissíti a Vmss VM-et a hozzáadott adatlemezzel.</span><span class="sxs-lookup"><span data-stu-id="0c428-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="0c428-144">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0c428-144">PARAMETERS</span></span>

### <span data-ttu-id="0c428-145">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="0c428-145">-Caching</span></span>
<span data-ttu-id="0c428-146">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0c428-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0c428-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c428-148">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0c428-148">ReadOnly</span></span>
- <span data-ttu-id="0c428-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0c428-149">ReadWrite</span></span>
- <span data-ttu-id="0c428-150">Nincs az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="0c428-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="0c428-151">Az érték módosításakor a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="0c428-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="0c428-152">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="0c428-152">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="0c428-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0c428-153">-CreateOption</span></span>
<span data-ttu-id="0c428-154">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="0c428-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="0c428-155">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="0c428-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0c428-156">Csatolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-156">Attach.</span></span>
<span data-ttu-id="0c428-157">Ezt a lehetőséget választva virtuális gépet hozhat létre egy speciális merevlemezről.</span><span class="sxs-lookup"><span data-stu-id="0c428-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="0c428-158">Ha ezt a beállítást adja meg, ne adja meg a *SourceImageUri* paramétert.</span><span class="sxs-lookup"><span data-stu-id="0c428-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="0c428-159">A *VhdUri* mindent meg kell tennie ahhoz, hogy az Azure platform a virtuális merevlemez (VHD) helyét a virtuális gép adatlemezéhez csatolja.</span><span class="sxs-lookup"><span data-stu-id="0c428-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="0c428-160">Üres.</span><span class="sxs-lookup"><span data-stu-id="0c428-160">Empty.</span></span>
<span data-ttu-id="0c428-161">Ezzel a beállítással üres adatlemezt hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="0c428-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="0c428-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="0c428-162">FromImage.</span></span>
<span data-ttu-id="0c428-163">Ezt a lehetőséget választva virtuális gépet hozhat létre általános képből vagy lemezről.</span><span class="sxs-lookup"><span data-stu-id="0c428-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="0c428-164">Ha ezt a beállítást választja, akkor a *SourceImageUri* paramétert is meg kell adnia, hogy az Azure platform a VHD-fájlnak az adatlemezhez való csatolását adja.</span><span class="sxs-lookup"><span data-stu-id="0c428-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="0c428-165">A *VhdUri* paraméter az a hely, ahol az ADATlemez VHD-adatlemeze a virtuális gép általi használat után tárolódik.</span><span class="sxs-lookup"><span data-stu-id="0c428-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="0c428-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c428-166">-DefaultProfile</span></span>
<span data-ttu-id="0c428-167">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c428-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c428-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0c428-168">-DiskSizeInGB</span></span>
<span data-ttu-id="0c428-169">Itt adhatja meg a virtuális géphez csatolni kívánt üres lemez méretét gigabájtban.</span><span class="sxs-lookup"><span data-stu-id="0c428-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="0c428-170">-LUN</span><span class="sxs-lookup"><span data-stu-id="0c428-170">-Lun</span></span>
<span data-ttu-id="0c428-171">Az adatlemez logikai egységének számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="0c428-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0c428-172">-ManagedDiskId</span></span>
<span data-ttu-id="0c428-173">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-173">Specifies the ID of a managed disk.</span></span>

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

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-174">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0c428-174">-Name</span></span>
<span data-ttu-id="0c428-175">A hozzáadni kívánt adatlemez nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-175">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="0c428-176">-SourceImageUri</span></span>
<span data-ttu-id="0c428-177">Annak a lemeznek az erőforrás-URI-azonosítóját adja meg, amelyre a parancsmag csatolva van.</span><span class="sxs-lookup"><span data-stu-id="0c428-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="0c428-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0c428-178">-StorageAccountType</span></span>
<span data-ttu-id="0c428-179">A felügyelt lemez tárterület-típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c428-179">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="0c428-180">-VhdUri</span></span>
<span data-ttu-id="0c428-181">A virtuális merevlemez (VHD-fájl) egységes erőforrás-azonosítóját adja meg, amely a platform képe vagy a felhasználói kép használatakor hozható létre.</span><span class="sxs-lookup"><span data-stu-id="0c428-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="0c428-182">Ez a parancsmag a binárisan nagy objektumot (blob) másolja át erre a helyre.</span><span class="sxs-lookup"><span data-stu-id="0c428-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="0c428-183">Az a hely, ahonnan a virtuális gépet el kell indítani.</span><span class="sxs-lookup"><span data-stu-id="0c428-183">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="0c428-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0c428-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="0c428-185">A helyi Virtual Machine Scale set VM objektumát adja hozzá az adatlemez hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="0c428-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="0c428-186">A **Get-AzureRmVmssVM** parancsmaggal virtuális gép méretarány-set VM-objektum beszerzése használható.</span><span class="sxs-lookup"><span data-stu-id="0c428-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-187">-VM</span><span class="sxs-lookup"><span data-stu-id="0c428-187">-VM</span></span>
<span data-ttu-id="0c428-188">Annak a helyi virtuális gépnek az objektumát adja meg, amelyhez adatlemezt kíván hozzáadni.</span><span class="sxs-lookup"><span data-stu-id="0c428-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="0c428-189">A **Get-AzureRmVM** parancsmaggal egy virtuálisgép-objektum beszerzése használható.</span><span class="sxs-lookup"><span data-stu-id="0c428-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="0c428-190">A **New-AzureRmVMConfig** parancsmaggal létrehozhatja a virtuális gép objektumát.</span><span class="sxs-lookup"><span data-stu-id="0c428-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="0c428-191">-WriteAccelerator</span></span>
<span data-ttu-id="0c428-192">Itt adhatja meg, hogy a WriteAccelerator engedélyezve vagy Letiltva van-e egy felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="0c428-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c428-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c428-193">CommonParameters</span></span>
<span data-ttu-id="0c428-194">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0c428-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c428-195">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c428-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c428-196">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c428-196">INPUTS</span></span>

### <span data-ttu-id="0c428-197">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0c428-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0c428-198">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0c428-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="0c428-199">System. String</span><span class="sxs-lookup"><span data-stu-id="0c428-199">System.String</span></span>

### <span data-ttu-id="0c428-200">Microsoft. Azure. Management. kiszámítás. models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="0c428-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="0c428-201">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0c428-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0c428-202">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c428-202">OUTPUTS</span></span>

### <span data-ttu-id="0c428-203">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0c428-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0c428-204">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="0c428-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="0c428-205">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0c428-205">NOTES</span></span>

## <span data-ttu-id="0c428-206">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c428-206">RELATED LINKS</span></span>

[<span data-ttu-id="0c428-207">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0c428-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="0c428-208">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0c428-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0c428-209">Új – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0c428-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
