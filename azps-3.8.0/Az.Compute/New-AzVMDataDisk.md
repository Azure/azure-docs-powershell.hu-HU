---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 7f67b8b6ff287a98fc505cb63c3a6eda90f46ef7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011442"
---
# <span data-ttu-id="94a6d-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="94a6d-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="94a6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="94a6d-103">Helyi adatlemez-objektumot hoz létre egy virtuális géphez vagy egy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="94a6d-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="94a6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94a6d-104">SYNTAX</span></span>

### <span data-ttu-id="94a6d-105">NormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="94a6d-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94a6d-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="94a6d-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94a6d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94a6d-107">DESCRIPTION</span></span>
<span data-ttu-id="94a6d-108">A **New-AzVMDataDisk** parancsmag létrehoz egy helyi Data Disk-objektumot egy virtuális géphez vagy egy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="94a6d-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="94a6d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94a6d-109">EXAMPLES</span></span>

### <span data-ttu-id="94a6d-110">1. példa: felügyelt adatlemez felvétele Vmss VM-be</span><span class="sxs-lookup"><span data-stu-id="94a6d-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="94a6d-111">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="94a6d-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="94a6d-112">A következő parancs létrehoz egy Data Disk-objektumot a kezelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="94a6d-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="94a6d-113">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="94a6d-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="94a6d-114">A végleges parancs új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="94a6d-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="94a6d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94a6d-115">PARAMETERS</span></span>

### <span data-ttu-id="94a6d-116">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="94a6d-116">-Caching</span></span>
<span data-ttu-id="94a6d-117">A virtuális gép adatlemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="94a6d-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="94a6d-118">-CreateOption</span></span>
<span data-ttu-id="94a6d-119">A virtuálisgép-adatlemez létrehozási beállítása.</span><span class="sxs-lookup"><span data-stu-id="94a6d-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a6d-120">-DefaultProfile</span></span>
<span data-ttu-id="94a6d-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94a6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a6d-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="94a6d-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="94a6d-123">A virtuálisgép-kezelés-titkosítási készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94a6d-123">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="94a6d-124">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="94a6d-124">-DiskSizeInGB</span></span>
<span data-ttu-id="94a6d-125">A virtuális gép adatlemezének mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="94a6d-125">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="94a6d-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="94a6d-126">-Lun</span></span>
<span data-ttu-id="94a6d-127">A Virtual Machine Data Disk logikai egysége.</span><span class="sxs-lookup"><span data-stu-id="94a6d-127">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="94a6d-128">-ManagedDiskId</span></span>
<span data-ttu-id="94a6d-129">A virtuális gép által felügyelt lemez azonosítója.</span><span class="sxs-lookup"><span data-stu-id="94a6d-129">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94a6d-130">-Name</span></span>
<span data-ttu-id="94a6d-131">A virtuális gép adatlemezének neve.</span><span class="sxs-lookup"><span data-stu-id="94a6d-131">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="94a6d-132">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="94a6d-132">-SourceImageUri</span></span>
<span data-ttu-id="94a6d-133">A Virtual Machine operációsrendszer-lemez forrás képe URI-ja.</span><span class="sxs-lookup"><span data-stu-id="94a6d-133">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="94a6d-134">-StorageAccountType</span></span>
<span data-ttu-id="94a6d-135">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="94a6d-135">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-136">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="94a6d-136">-VhdUri</span></span>
<span data-ttu-id="94a6d-137">A Virtual Machine Data Disk VHD-je.</span><span class="sxs-lookup"><span data-stu-id="94a6d-137">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="94a6d-138">-WriteAccelerator</span></span>
<span data-ttu-id="94a6d-139">Itt adhatja meg, hogy a WriteAccelerator engedélyezve vagy Letiltva van-e egy felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="94a6d-139">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a6d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a6d-140">CommonParameters</span></span>
<span data-ttu-id="94a6d-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94a6d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a6d-142">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94a6d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a6d-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a6d-143">INPUTS</span></span>

### <span data-ttu-id="94a6d-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="94a6d-144">System.Int32</span></span>

### <span data-ttu-id="94a6d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="94a6d-145">System.String</span></span>

### <span data-ttu-id="94a6d-146">Microsoft. Azure. Management. kiszámítás. models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="94a6d-146">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="94a6d-147">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="94a6d-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="94a6d-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94a6d-148">OUTPUTS</span></span>

### <span data-ttu-id="94a6d-149">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="94a6d-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="94a6d-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94a6d-150">NOTES</span></span>

## <span data-ttu-id="94a6d-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94a6d-151">RELATED LINKS</span></span>
