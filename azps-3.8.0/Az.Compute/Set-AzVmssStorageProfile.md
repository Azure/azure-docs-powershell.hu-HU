---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014608"
---
# <span data-ttu-id="435f6-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="435f6-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="435f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="435f6-102">SYNOPSIS</span></span>
<span data-ttu-id="435f6-103">Beállítja a VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="435f6-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="435f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="435f6-104">SYNTAX</span></span>

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

## <span data-ttu-id="435f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="435f6-105">DESCRIPTION</span></span>
<span data-ttu-id="435f6-106">A **set-AzVmssStorageProfile** parancsmag a virtuálisgép-készlet (VMSS) tárolási profiljának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="435f6-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="435f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="435f6-107">EXAMPLES</span></span>

### <span data-ttu-id="435f6-108">Példa 1: a VMSS tárolási profil tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="435f6-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="435f6-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="435f6-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="435f6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="435f6-110">PARAMETERS</span></span>

### <span data-ttu-id="435f6-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="435f6-111">-DataDisk</span></span>
<span data-ttu-id="435f6-112">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="435f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435f6-113">-DefaultProfile</span></span>
<span data-ttu-id="435f6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="435f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="435f6-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="435f6-115">-DiffDiskSetting</span></span>
<span data-ttu-id="435f6-116">Az operációs rendszer merevlemezének különbséglemez adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="435f6-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="435f6-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="435f6-118">Az ügyfél által felügyelt lemezvezérlő-titkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="435f6-119">Ezt csak a felügyelt lemezek esetében lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="435f6-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="435f6-120">-Kép</span><span class="sxs-lookup"><span data-stu-id="435f6-120">-Image</span></span>
<span data-ttu-id="435f6-121">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="435f6-122">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="435f6-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="435f6-123">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="435f6-123">-ImageReferenceId</span></span>
<span data-ttu-id="435f6-124">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="435f6-125">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="435f6-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="435f6-126">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="435f6-127">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="435f6-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="435f6-128">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="435f6-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="435f6-129">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="435f6-130">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="435f6-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="435f6-131">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="435f6-131">-ImageReferenceSku</span></span>
<span data-ttu-id="435f6-132">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="435f6-133">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="435f6-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="435f6-134">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="435f6-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="435f6-135">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="435f6-136">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="435f6-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="435f6-137">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="435f6-137">-ManagedDisk</span></span>
<span data-ttu-id="435f6-138">A felügyelt merevlemezt adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="435f6-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="435f6-139">-OsDiskCaching</span></span>
<span data-ttu-id="435f6-140">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="435f6-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="435f6-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="435f6-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="435f6-142">ReadOnly</span></span>
- <span data-ttu-id="435f6-143">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="435f6-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="435f6-144">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="435f6-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="435f6-145">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="435f6-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="435f6-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="435f6-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="435f6-147">Itt adhatja meg, hogy a parancsmag hogyan hozza létre a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="435f6-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="435f6-148">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="435f6-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="435f6-149">Csatolás: ez az érték akkor használatos, ha speciális lemezt használ a VMSS virtuális gép létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="435f6-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="435f6-150">FromImage: ezt az értéket akkor használja a program, ha a VMSS virtuális gépet hozza létre a kép használatakor.</span><span class="sxs-lookup"><span data-stu-id="435f6-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="435f6-151">Ha platformot használ, akkor a *imageReference* paramétert is használhatja.</span><span class="sxs-lookup"><span data-stu-id="435f6-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="435f6-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="435f6-152">-OsDiskName</span></span>
<span data-ttu-id="435f6-153">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="435f6-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="435f6-154">-OsDiskOsType</span></span>
<span data-ttu-id="435f6-155">A lemezen az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="435f6-156">Ez csak a felhasználói képforgatókönyvek esetében szükséges, és nem platformos képhez.</span><span class="sxs-lookup"><span data-stu-id="435f6-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="435f6-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="435f6-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="435f6-158">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="435f6-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="435f6-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="435f6-159">-VhdContainer</span></span>
<span data-ttu-id="435f6-160">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="435f6-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="435f6-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="435f6-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="435f6-162">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="435f6-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="435f6-163">Az objektum beolvasásához használja a New-AzVmssConfig objektumot.</span><span class="sxs-lookup"><span data-stu-id="435f6-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="435f6-164">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="435f6-164">-Confirm</span></span>
<span data-ttu-id="435f6-165">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="435f6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435f6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435f6-166">-WhatIf</span></span>
<span data-ttu-id="435f6-167">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="435f6-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="435f6-168">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="435f6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435f6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435f6-169">CommonParameters</span></span>
<span data-ttu-id="435f6-170">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="435f6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435f6-171">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="435f6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435f6-172">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="435f6-172">INPUTS</span></span>

### <span data-ttu-id="435f6-173">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="435f6-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="435f6-174">System. String</span><span class="sxs-lookup"><span data-stu-id="435f6-174">System.String</span></span>

### <span data-ttu-id="435f6-175">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="435f6-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="435f6-176">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="435f6-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="435f6-177">System. string []</span><span class="sxs-lookup"><span data-stu-id="435f6-177">System.String[]</span></span>

### <span data-ttu-id="435f6-178">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="435f6-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="435f6-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="435f6-179">OUTPUTS</span></span>

### <span data-ttu-id="435f6-180">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="435f6-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="435f6-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="435f6-181">NOTES</span></span>

## <span data-ttu-id="435f6-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="435f6-182">RELATED LINKS</span></span>

[<span data-ttu-id="435f6-183">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="435f6-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="435f6-184">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="435f6-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="435f6-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="435f6-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="435f6-186">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="435f6-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


