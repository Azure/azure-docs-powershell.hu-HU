---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: ec233765f401348895275291ddad0571d1ddfc85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931354"
---
# <span data-ttu-id="1ff78-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="1ff78-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="1ff78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff78-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff78-103">Beállítja a VMSS tárolóprofil-tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1ff78-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="1ff78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ff78-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ff78-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ff78-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff78-106">A **Set-AzVmssStorageProfile** parancsmag beállítja a virtuális gép méretaránykészletének (VMSS) tárolóprofil-tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1ff78-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1ff78-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ff78-107">EXAMPLES</span></span>

### <span data-ttu-id="1ff78-108">1. példa: A VMSS tárolóprofil-tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="1ff78-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="1ff78-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolóprofil-tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="1ff78-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1ff78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff78-110">PARAMETERS</span></span>

### <span data-ttu-id="1ff78-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="1ff78-111">-DataDisk</span></span>
<span data-ttu-id="1ff78-112">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff78-113">-DefaultProfile</span></span>
<span data-ttu-id="1ff78-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ff78-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ff78-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="1ff78-115">-DiffDiskSetting</span></span>
<span data-ttu-id="1ff78-116">Az operációs rendszer lemezének eltérő lemezbeállításai.</span><span class="sxs-lookup"><span data-stu-id="1ff78-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="1ff78-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1ff78-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1ff78-118">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="1ff78-119">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="1ff78-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="1ff78-120">-Image</span><span class="sxs-lookup"><span data-stu-id="1ff78-120">-Image</span></span>
<span data-ttu-id="1ff78-121">A felhasználói kép blob-URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="1ff78-122">A VMSS egy operációs rendszerlemezt hoz létre a felhasználói lemezkép ugyanazon tárolóban.</span><span class="sxs-lookup"><span data-stu-id="1ff78-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="1ff78-123">-ImageReferenceId</span></span>
<span data-ttu-id="1ff78-124">A képhivatkozás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="1ff78-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="1ff78-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="1ff78-126">A virtuális gép lemezképének (VMImage) ajánlat típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="1ff78-127">Képajánlat beszerzéséhez használja a Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ff78-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="1ff78-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="1ff78-129">Egy VMImage-közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="1ff78-130">Közzétevő beszerzéséhez használja a Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ff78-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1ff78-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="1ff78-131">-ImageReferenceSku</span></span>
<span data-ttu-id="1ff78-132">A VMImage termékváltozatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="1ff78-133">Az SKUs-k beszerzéséhez használja a Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1ff78-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="1ff78-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="1ff78-135">A VMImage verziójának megadása.</span><span class="sxs-lookup"><span data-stu-id="1ff78-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="1ff78-136">A legújabb verzió csak akkor használható, ha az adott verzió helyett a legújabb értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1ff78-137">-ManagedDisk</span></span>
<span data-ttu-id="1ff78-138">A felügyelt lemez megadása.</span><span class="sxs-lookup"><span data-stu-id="1ff78-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="1ff78-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="1ff78-139">-OsDiskCaching</span></span>
<span data-ttu-id="1ff78-140">Az operációs rendszer lemezének gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="1ff78-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="1ff78-141">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1ff78-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ff78-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="1ff78-142">ReadOnly</span></span>
- <span data-ttu-id="1ff78-143">ReadWrite The default value is ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1ff78-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="1ff78-144">Ha módosítja a gyorsítótárazás értékét, a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="1ff78-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="1ff78-145">Ez a beállítás befolyásolja a lemez konzisztenciáját és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="1ff78-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="1ff78-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="1ff78-147">Azt adja meg, hogy ez a parancsmag hogyan hozza létre a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="1ff78-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="1ff78-148">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="1ff78-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1ff78-149">Csatolás: Ezt az értéket akkor használja a rendszer, ha egy speciális lemezen hozza létre a VMSS virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="1ff78-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="1ff78-150">FromImage: Ez az érték akkor használatos, amikor egy képet használ a VMSS virtuális gép létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="1ff78-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="1ff78-151">Platformkép használata esetén a *imageReference paramétert is használhatja.*</span><span class="sxs-lookup"><span data-stu-id="1ff78-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="1ff78-152">-OsDiskName</span></span>
<span data-ttu-id="1ff78-153">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-153">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="1ff78-154">-OsDiskOsType</span></span>
<span data-ttu-id="1ff78-155">A lemezen található operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="1ff78-156">Erre csak felhasználói kép esetén van szükség, platformkép esetén nem.</span><span class="sxs-lookup"><span data-stu-id="1ff78-156">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1ff78-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="1ff78-158">Azt adja meg, hogy a WriteAccelerator engedélyezve vagy letiltva legyen-e az operációs rendszer lemezén.</span><span class="sxs-lookup"><span data-stu-id="1ff78-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="1ff78-159">-VhdContainer</span></span>
<span data-ttu-id="1ff78-160">Megadja a VMSS operációs rendszer lemezének tárolására használt tároló URL-eket.</span><span class="sxs-lookup"><span data-stu-id="1ff78-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ff78-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1ff78-162">A VMSS-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ff78-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="1ff78-163">Az objektum beszerzéséhez használja a New-AzVmssConfig objektumot.</span><span class="sxs-lookup"><span data-stu-id="1ff78-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ff78-164">-Confirm</span></span>
<span data-ttu-id="1ff78-165">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ff78-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff78-166">-WhatIf</span></span>
<span data-ttu-id="1ff78-167">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ff78-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ff78-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ff78-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff78-169">CommonParameters</span></span>
<span data-ttu-id="1ff78-170">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff78-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff78-171">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ff78-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff78-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ff78-172">INPUTS</span></span>

### <span data-ttu-id="1ff78-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ff78-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1ff78-174">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff78-174">System.String</span></span>

### <span data-ttu-id="1ff78-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1ff78-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1ff78-176">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1ff78-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1ff78-177">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1ff78-177">System.String[]</span></span>

### <span data-ttu-id="1ff78-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="1ff78-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="1ff78-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ff78-179">OUTPUTS</span></span>

### <span data-ttu-id="1ff78-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1ff78-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1ff78-181">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ff78-181">NOTES</span></span>

## <span data-ttu-id="1ff78-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ff78-182">RELATED LINKS</span></span>

[<span data-ttu-id="1ff78-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="1ff78-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="1ff78-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="1ff78-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="1ff78-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1ff78-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="1ff78-186">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1ff78-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


