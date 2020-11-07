---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 883c976df7223a03421550f2a27c2baf51be4dcb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667187"
---
# <span data-ttu-id="38da8-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="38da8-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="38da8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38da8-102">SYNOPSIS</span></span>
<span data-ttu-id="38da8-103">Beállítja a VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="38da8-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="38da8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38da8-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38da8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38da8-105">DESCRIPTION</span></span>
<span data-ttu-id="38da8-106">A **set-AzVmssStorageProfile** parancsmag a virtuálisgép-készlet (VMSS) tárolási profiljának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="38da8-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="38da8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38da8-107">EXAMPLES</span></span>

### <span data-ttu-id="38da8-108">Példa 1: a VMSS tárolási profil tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="38da8-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="38da8-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="38da8-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="38da8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38da8-110">PARAMETERS</span></span>

### <span data-ttu-id="38da8-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="38da8-111">-DataDisk</span></span>
<span data-ttu-id="38da8-112">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="38da8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38da8-113">-DefaultProfile</span></span>
<span data-ttu-id="38da8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38da8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38da8-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="38da8-115">-DiffDiskSetting</span></span>
<span data-ttu-id="38da8-116">Az operációs rendszer merevlemezének különbséglemez adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="38da8-117">-Kép</span><span class="sxs-lookup"><span data-stu-id="38da8-117">-Image</span></span>
<span data-ttu-id="38da8-118">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="38da8-119">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="38da8-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="38da8-120">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="38da8-120">-ImageReferenceId</span></span>
<span data-ttu-id="38da8-121">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="38da8-122">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="38da8-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="38da8-123">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="38da8-124">Képajánlat beolvasásához használja az Get-AzVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="38da8-124">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="38da8-125">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="38da8-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="38da8-126">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="38da8-127">Publisher beolvasásához használja az Get-AzVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="38da8-127">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="38da8-128">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="38da8-128">-ImageReferenceSku</span></span>
<span data-ttu-id="38da8-129">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="38da8-130">A SKU beolvasásához használja az Get-AzVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="38da8-130">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="38da8-131">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="38da8-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="38da8-132">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="38da8-133">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="38da8-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="38da8-134">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="38da8-134">-ManagedDisk</span></span>
<span data-ttu-id="38da8-135">A felügyelt merevlemezt adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="38da8-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="38da8-136">-OsDiskCaching</span></span>
<span data-ttu-id="38da8-137">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="38da8-138">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="38da8-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38da8-139">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="38da8-139">ReadOnly</span></span>
- <span data-ttu-id="38da8-140">ReadWrite: az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="38da8-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="38da8-141">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="38da8-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="38da8-142">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="38da8-142">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="38da8-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="38da8-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="38da8-144">Itt adhatja meg, hogy a parancsmag hogyan hozza létre a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="38da8-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="38da8-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="38da8-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="38da8-146">Csatolás: ez az érték akkor használatos, ha speciális lemezt használ a VMSS virtuális gép létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="38da8-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="38da8-147">FromImage: ezt az értéket akkor használja a program, ha a VMSS virtuális gépet hozza létre a kép használatakor.</span><span class="sxs-lookup"><span data-stu-id="38da8-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="38da8-148">Ha platformot használ, akkor a *imageReference* paramétert is használhatja.</span><span class="sxs-lookup"><span data-stu-id="38da8-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="38da8-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="38da8-149">-OsDiskName</span></span>
<span data-ttu-id="38da8-150">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-150">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="38da8-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="38da8-151">-OsDiskOsType</span></span>
<span data-ttu-id="38da8-152">A lemezen az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="38da8-153">Ez csak a felhasználói képforgatókönyvek esetében szükséges, és nem platformos képhez.</span><span class="sxs-lookup"><span data-stu-id="38da8-153">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="38da8-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="38da8-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="38da8-155">Megadja, hogy az operációs rendszer merevlemezén engedélyezni vagy tiltani kell-e a WriteAccelerator.</span><span class="sxs-lookup"><span data-stu-id="38da8-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="38da8-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="38da8-156">-VhdContainer</span></span>
<span data-ttu-id="38da8-157">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="38da8-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="38da8-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="38da8-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="38da8-159">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="38da8-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="38da8-160">Az objektum beolvasásához használja a New-AzVmssConfig objektumot.</span><span class="sxs-lookup"><span data-stu-id="38da8-160">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="38da8-161">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="38da8-161">-Confirm</span></span>
<span data-ttu-id="38da8-162">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="38da8-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38da8-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38da8-163">-WhatIf</span></span>
<span data-ttu-id="38da8-164">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="38da8-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38da8-165">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38da8-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38da8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38da8-166">CommonParameters</span></span>
<span data-ttu-id="38da8-167">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38da8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38da8-168">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="38da8-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38da8-169">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38da8-169">INPUTS</span></span>

### <span data-ttu-id="38da8-170">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="38da8-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="38da8-171">System. String</span><span class="sxs-lookup"><span data-stu-id="38da8-171">System.String</span></span>

### <span data-ttu-id="38da8-172">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="38da8-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="38da8-173">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="38da8-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="38da8-174">System. string []</span><span class="sxs-lookup"><span data-stu-id="38da8-174">System.String[]</span></span>

### <span data-ttu-id="38da8-175">Microsoft. Azure. Management. számítás. models. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="38da8-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="38da8-176">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38da8-176">OUTPUTS</span></span>

### <span data-ttu-id="38da8-177">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="38da8-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="38da8-178">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38da8-178">NOTES</span></span>

## <span data-ttu-id="38da8-179">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38da8-179">RELATED LINKS</span></span>

[<span data-ttu-id="38da8-180">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="38da8-180">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="38da8-181">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="38da8-181">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="38da8-182">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="38da8-182">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="38da8-183">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="38da8-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


