---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148818"
---
# <span data-ttu-id="8a8de-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8a8de-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="8a8de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a8de-102">SYNOPSIS</span></span>
<span data-ttu-id="8a8de-103">Helyi adatlemez-objektumot hoz létre virtuális géphez vagy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="8a8de-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="8a8de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8a8de-104">SYNTAX</span></span>

### <span data-ttu-id="8a8de-105">NormalDiskParameterSetName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a8de-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a8de-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8a8de-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a8de-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8a8de-107">DESCRIPTION</span></span>
<span data-ttu-id="8a8de-108">A **New-AzVMDataDisk** parancsmag helyi lemezobjektumot hoz létre egy virtuális géphez vagy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="8a8de-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="8a8de-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8a8de-109">EXAMPLES</span></span>

### <span data-ttu-id="8a8de-110">1. példa: Felügyelt adatlemez hozzáadása Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="8a8de-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="8a8de-111">Az első parancs egy meglévő felügyelt lemezhez jut.</span><span class="sxs-lookup"><span data-stu-id="8a8de-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="8a8de-112">A következő parancs létrehoz egy adatlemez-objektumot a felügyelt lemezzel.</span><span class="sxs-lookup"><span data-stu-id="8a8de-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="8a8de-113">A következő parancs egy meglévő Vmss VM-et kap, amelyet az erőforráscsoport neve, a vmss neve és a példányazonosító ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a8de-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="8a8de-114">Az utolsó parancs egy új adatlemez hozzáadásával frissíti a Vmss VM-et.</span><span class="sxs-lookup"><span data-stu-id="8a8de-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="8a8de-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="8a8de-115">Example 2</span></span>

<span data-ttu-id="8a8de-116">Helyi adatlemez-objektumot hoz létre virtuális géphez vagy Vmss VM-hez.</span><span class="sxs-lookup"><span data-stu-id="8a8de-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="8a8de-117">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="8a8de-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="8a8de-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a8de-118">PARAMETERS</span></span>

### <span data-ttu-id="8a8de-119">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="8a8de-119">-Caching</span></span>
<span data-ttu-id="8a8de-120">A virtuális gép adatlemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="8a8de-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="8a8de-121">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="8a8de-121">-CreateOption</span></span>
<span data-ttu-id="8a8de-122">A virtuális gép adatlemezének létrehozási lehetősége.</span><span class="sxs-lookup"><span data-stu-id="8a8de-122">The virtual machine data disk's create option.</span></span>

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

### <span data-ttu-id="8a8de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a8de-123">-DefaultProfile</span></span>
<span data-ttu-id="8a8de-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a8de-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a8de-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8a8de-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8a8de-126">A virtuális gép által felügyelt lemeztitkosítási készlet azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a8de-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="8a8de-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8a8de-127">-DiskSizeInGB</span></span>
<span data-ttu-id="8a8de-128">A virtuális gép adatlemezének mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="8a8de-128">The virtual machine data disk's size in GB.</span></span>

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

### <span data-ttu-id="8a8de-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="8a8de-129">-Lun</span></span>
<span data-ttu-id="8a8de-130">A virtuális gép adatlemezének Lunja.</span><span class="sxs-lookup"><span data-stu-id="8a8de-130">The virtual machine data disk's Lun.</span></span>

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

### <span data-ttu-id="8a8de-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="8a8de-131">-ManagedDiskId</span></span>
<span data-ttu-id="8a8de-132">A virtuális gép által felügyelt lemez azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8a8de-132">The virtual machine managed disk's Id.</span></span>

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

### <span data-ttu-id="8a8de-133">-Name</span><span class="sxs-lookup"><span data-stu-id="8a8de-133">-Name</span></span>
<span data-ttu-id="8a8de-134">A virtuális gép adatlemezének neve.</span><span class="sxs-lookup"><span data-stu-id="8a8de-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="8a8de-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="8a8de-135">-SourceImageUri</span></span>
<span data-ttu-id="8a8de-136">A virtuális operációs rendszer lemezének forrásképe Uri.</span><span class="sxs-lookup"><span data-stu-id="8a8de-136">The virtual machine OS disk's source image Uri.</span></span>

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

### <span data-ttu-id="8a8de-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8a8de-137">-StorageAccountType</span></span>
<span data-ttu-id="8a8de-138">A virtuális gép által felügyelt lemez fióktípusa.</span><span class="sxs-lookup"><span data-stu-id="8a8de-138">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="8a8de-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="8a8de-139">-VhdUri</span></span>
<span data-ttu-id="8a8de-140">A virtuális gép adatlemezének Vhd Uri-ja.</span><span class="sxs-lookup"><span data-stu-id="8a8de-140">The virtual machine data disk's Vhd Uri.</span></span>

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

### <span data-ttu-id="8a8de-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8a8de-141">-WriteAccelerator</span></span>
<span data-ttu-id="8a8de-142">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e felügyelt adatlemezen.</span><span class="sxs-lookup"><span data-stu-id="8a8de-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="8a8de-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a8de-143">CommonParameters</span></span>
<span data-ttu-id="8a8de-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a8de-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a8de-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a8de-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a8de-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8a8de-146">INPUTS</span></span>

### <span data-ttu-id="8a8de-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8a8de-147">System.Int32</span></span>

### <span data-ttu-id="8a8de-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8a8de-148">System.String</span></span>

### <span data-ttu-id="8a8de-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="8a8de-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="8a8de-150">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8a8de-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8a8de-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a8de-151">OUTPUTS</span></span>

### <span data-ttu-id="8a8de-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="8a8de-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="8a8de-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8a8de-153">NOTES</span></span>

## <span data-ttu-id="8a8de-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a8de-154">RELATED LINKS</span></span>
