---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498996"
---
# <span data-ttu-id="6c8aa-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="6c8aa-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="6c8aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6c8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8aa-103">Beállítja a VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c8aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6c8aa-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c8aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6c8aa-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8aa-106">A **set-AzureRmVmssStorageProfile** parancsmag a virtuálisgép-készlet (VMSS) tárolási profiljának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="6c8aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6c8aa-107">EXAMPLES</span></span>

### <span data-ttu-id="6c8aa-108">Példa 1: a VMSS tárolási profil tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="6c8aa-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="6c8aa-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="6c8aa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6c8aa-110">PARAMETERS</span></span>

### <span data-ttu-id="6c8aa-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="6c8aa-111">-DataDisk</span></span>
<span data-ttu-id="6c8aa-112">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-113">-Kép</span><span class="sxs-lookup"><span data-stu-id="6c8aa-113">-Image</span></span>
<span data-ttu-id="6c8aa-114">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="6c8aa-115">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-116">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="6c8aa-116">-ImageReferenceId</span></span>
<span data-ttu-id="6c8aa-117">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-117">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-118">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="6c8aa-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="6c8aa-119">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="6c8aa-120">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="6c8aa-121">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="6c8aa-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="6c8aa-122">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="6c8aa-123">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="6c8aa-124">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="6c8aa-124">-ImageReferenceSku</span></span>
<span data-ttu-id="6c8aa-125">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="6c8aa-126">A SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-127">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="6c8aa-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="6c8aa-128">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="6c8aa-129">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-130">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="6c8aa-130">-ManagedDisk</span></span>
<span data-ttu-id="6c8aa-131">A felügyelt merevlemezt adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-131">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="6c8aa-132">-OsDiskCaching</span></span>
<span data-ttu-id="6c8aa-133">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="6c8aa-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6c8aa-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c8aa-135">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6c8aa-135">ReadOnly</span></span>
- <span data-ttu-id="6c8aa-136">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6c8aa-136">ReadWrite</span></span>

<span data-ttu-id="6c8aa-137">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="6c8aa-138">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="6c8aa-139">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-139">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="6c8aa-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="6c8aa-141">Itt adhatja meg, hogy a parancsmag hogyan hozza létre a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="6c8aa-142">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="6c8aa-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c8aa-143">Csatolás: ez az érték akkor használatos, ha speciális lemezt használ a VMSS virtuális gép létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="6c8aa-144">FromImage: ezt az értéket akkor használja a program, ha a VMSS virtuális gépet hozza létre a kép használatakor.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="6c8aa-145">Ha platformot használ, akkor a *imageReference* paramétert is használhatja.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="6c8aa-146">-OsDiskName</span></span>
<span data-ttu-id="6c8aa-147">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="6c8aa-148">-OsDiskOsType</span></span>
<span data-ttu-id="6c8aa-149">A lemezen az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="6c8aa-150">Ez csak a felhasználói képforgatókönyvek esetében szükséges, és nem platformos képhez.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-150">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="6c8aa-151">-VhdContainer</span></span>
<span data-ttu-id="6c8aa-152">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6c8aa-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6c8aa-154">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="6c8aa-155">Az objektum beolvasásához használja a New-AzureRmVmssConfig objektumot.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-156">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6c8aa-156">-Confirm</span></span>
<span data-ttu-id="6c8aa-157">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8aa-158">-WhatIf</span></span>
<span data-ttu-id="6c8aa-159">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c8aa-160">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c8aa-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8aa-161">CommonParameters</span></span>
<span data-ttu-id="6c8aa-162">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6c8aa-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8aa-163">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8aa-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8aa-164">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c8aa-164">INPUTS</span></span>

###  
<span data-ttu-id="6c8aa-165">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6c8aa-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6c8aa-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c8aa-166">OUTPUTS</span></span>

## <span data-ttu-id="6c8aa-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6c8aa-167">NOTES</span></span>

## <span data-ttu-id="6c8aa-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c8aa-168">RELATED LINKS</span></span>

[<span data-ttu-id="6c8aa-169">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="6c8aa-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="6c8aa-170">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="6c8aa-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="6c8aa-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="6c8aa-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="6c8aa-172">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6c8aa-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


