---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 67158561b9a0369d65d3a846b4156f914a97358a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671304"
---
# <span data-ttu-id="40aa5-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="40aa5-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="40aa5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="40aa5-103">Helyi adatlemez-objektumot hoz létre egy virtuális géphez vagy egy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="40aa5-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="40aa5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40aa5-104">SYNTAX</span></span>

### <span data-ttu-id="40aa5-105">NormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="40aa5-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40aa5-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="40aa5-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40aa5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="40aa5-107">DESCRIPTION</span></span>
<span data-ttu-id="40aa5-108">A **New-AzVMDataDisk** parancsmag létrehoz egy helyi Data Disk-objektumot egy virtuális géphez vagy egy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="40aa5-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="40aa5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="40aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="40aa5-110">1. példa: felügyelt adatlemez felvétele Vmss VM-be</span><span class="sxs-lookup"><span data-stu-id="40aa5-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="40aa5-111">Az első parancs a meglévő távtárolású lemezt kapja.</span><span class="sxs-lookup"><span data-stu-id="40aa5-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="40aa5-112">A következő parancs létrehoz egy Data Disk-objektumot a kezelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="40aa5-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="40aa5-113">A következő parancs beolvassa a létező Vmss VM nevet, amelyet az erőforráscsoport neve, a Vmss neve és a példány azonosítója adott meg.</span><span class="sxs-lookup"><span data-stu-id="40aa5-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="40aa5-114">A végleges parancs új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="40aa5-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="40aa5-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40aa5-115">PARAMETERS</span></span>

### <span data-ttu-id="40aa5-116">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="40aa5-116">-Caching</span></span>
<span data-ttu-id="40aa5-117">A virtuális gép adatlemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="40aa5-117">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="40aa5-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="40aa5-118">-CreateOption</span></span>
<span data-ttu-id="40aa5-119">A virtuálisgép-adatlemez létrehozási beállítása.</span><span class="sxs-lookup"><span data-stu-id="40aa5-119">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="40aa5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40aa5-120">-DefaultProfile</span></span>
<span data-ttu-id="40aa5-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40aa5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40aa5-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="40aa5-122">-DiskSizeInGB</span></span>
<span data-ttu-id="40aa5-123">A virtuális gép adatlemezének mérete GB-ban</span><span class="sxs-lookup"><span data-stu-id="40aa5-123">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="40aa5-124">-LUN</span><span class="sxs-lookup"><span data-stu-id="40aa5-124">-Lun</span></span>
<span data-ttu-id="40aa5-125">A Virtual Machine Data Disk logikai egysége.</span><span class="sxs-lookup"><span data-stu-id="40aa5-125">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="40aa5-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="40aa5-126">-ManagedDiskId</span></span>
<span data-ttu-id="40aa5-127">A virtuális gép által felügyelt lemez azonosítója.</span><span class="sxs-lookup"><span data-stu-id="40aa5-127">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="40aa5-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40aa5-128">-Name</span></span>
<span data-ttu-id="40aa5-129">A virtuális gép adatlemezének neve.</span><span class="sxs-lookup"><span data-stu-id="40aa5-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="40aa5-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="40aa5-130">-SourceImageUri</span></span>
<span data-ttu-id="40aa5-131">A Virtual Machine operációsrendszer-lemez forrás képe URI-ja.</span><span class="sxs-lookup"><span data-stu-id="40aa5-131">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="40aa5-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="40aa5-132">-StorageAccountType</span></span>
<span data-ttu-id="40aa5-133">A virtuálisgép-felügyelt lemez fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="40aa5-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="40aa5-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="40aa5-134">-VhdUri</span></span>
<span data-ttu-id="40aa5-135">A Virtual Machine Data Disk VHD-je.</span><span class="sxs-lookup"><span data-stu-id="40aa5-135">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="40aa5-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="40aa5-136">-WriteAccelerator</span></span>
<span data-ttu-id="40aa5-137">Itt adhatja meg, hogy a WriteAccelerator engedélyezve vagy Letiltva van-e egy felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="40aa5-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="40aa5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40aa5-138">CommonParameters</span></span>
<span data-ttu-id="40aa5-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40aa5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40aa5-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40aa5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40aa5-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40aa5-141">INPUTS</span></span>

### <span data-ttu-id="40aa5-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="40aa5-142">System.Int32</span></span>

### <span data-ttu-id="40aa5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="40aa5-143">System.String</span></span>

### <span data-ttu-id="40aa5-144">Microsoft. Azure. Management. kiszámítás. models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="40aa5-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="40aa5-145">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40aa5-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="40aa5-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40aa5-146">OUTPUTS</span></span>

### <span data-ttu-id="40aa5-147">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="40aa5-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="40aa5-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40aa5-148">NOTES</span></span>

## <span data-ttu-id="40aa5-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40aa5-149">RELATED LINKS</span></span>
