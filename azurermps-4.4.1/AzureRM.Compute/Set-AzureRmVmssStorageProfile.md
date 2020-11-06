---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 60d525cc50b62350853755ae46698cbecb358654
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492491"
---
# <span data-ttu-id="d32a3-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="d32a3-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="d32a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d32a3-102">SYNOPSIS</span></span>
<span data-ttu-id="d32a3-103">Beállítja a VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d32a3-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d32a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d32a3-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d32a3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d32a3-105">DESCRIPTION</span></span>
<span data-ttu-id="d32a3-106">A **set-AzureRmVmssStorageProfile** parancsmag a virtuálisgép-készlet (VMSS) tárolási profiljának tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="d32a3-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d32a3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d32a3-107">EXAMPLES</span></span>

### <span data-ttu-id="d32a3-108">Példa 1: a VMSS tárolási profil tulajdonságainak beállítása</span><span class="sxs-lookup"><span data-stu-id="d32a3-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="d32a3-109">Ez a parancs beállítja a ContosoVMSS nevű VMSS tárolási profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d32a3-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="d32a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d32a3-110">PARAMETERS</span></span>

### <span data-ttu-id="d32a3-111">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="d32a3-111">-DataDisk</span></span>
<span data-ttu-id="d32a3-112">Az adatlemez-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="d32a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d32a3-113">-DefaultProfile</span></span>
<span data-ttu-id="d32a3-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d32a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d32a3-115">-Kép</span><span class="sxs-lookup"><span data-stu-id="d32a3-115">-Image</span></span>
<span data-ttu-id="d32a3-116">A felhasználói kép blob-URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="d32a3-117">A VMSS létrehozza az operációs rendszer lemezét a felhasználói kép ugyanazon tárolójában.</span><span class="sxs-lookup"><span data-stu-id="d32a3-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="d32a3-118">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="d32a3-118">-ImageReferenceId</span></span>
<span data-ttu-id="d32a3-119">A kép hivatkozási AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="d32a3-120">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="d32a3-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="d32a3-121">A Virtual Machine Image (VMImage) ajánlat típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="d32a3-122">Képajánlat beolvasásához használja az Get-AzureRmVMImageOffer parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d32a3-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="d32a3-123">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="d32a3-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="d32a3-124">A VMImage közzétevő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="d32a3-125">Publisher beolvasásához használja az Get-AzureRmVMImagePublisher parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d32a3-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="d32a3-126">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="d32a3-126">-ImageReferenceSku</span></span>
<span data-ttu-id="d32a3-127">A VMImage SKU-ot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="d32a3-128">A SKU beolvasásához használja az Get-AzureRmVMImageSku parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d32a3-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="d32a3-129">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="d32a3-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="d32a3-130">A VMImage verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="d32a3-131">A legújabb verzió használatához adjon meg egy új értéket az adott verzió helyett.</span><span class="sxs-lookup"><span data-stu-id="d32a3-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="d32a3-132">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="d32a3-132">-ManagedDisk</span></span>
<span data-ttu-id="d32a3-133">A felügyelt merevlemezt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-133">Specifies the managed disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d32a3-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="d32a3-134">-OsDiskCaching</span></span>
<span data-ttu-id="d32a3-135">Az operációs rendszer lemezének gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="d32a3-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d32a3-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d32a3-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="d32a3-137">ReadOnly</span></span>
- <span data-ttu-id="d32a3-138">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d32a3-138">ReadWrite</span></span>

<span data-ttu-id="d32a3-139">Az alapértelmezett érték a ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="d32a3-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="d32a3-140">Ha módosítja a gyorsítótár értékét, akkor a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="d32a3-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="d32a3-141">Ez a beállítás befolyásolja a lemez egységességét és teljesítményét.</span><span class="sxs-lookup"><span data-stu-id="d32a3-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="d32a3-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="d32a3-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="d32a3-143">Itt adhatja meg, hogy a parancsmag hogyan hozza létre a VMSS virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="d32a3-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="d32a3-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d32a3-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d32a3-145">Csatolás: ez az érték akkor használatos, ha speciális lemezt használ a VMSS virtuális gép létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="d32a3-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="d32a3-146">FromImage: ezt az értéket akkor használja a program, ha a VMSS virtuális gépet hozza létre a kép használatakor.</span><span class="sxs-lookup"><span data-stu-id="d32a3-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="d32a3-147">Ha platformot használ, akkor a *imageReference* paramétert is használhatja.</span><span class="sxs-lookup"><span data-stu-id="d32a3-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d32a3-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="d32a3-148">-OsDiskName</span></span>
<span data-ttu-id="d32a3-149">Az operációs rendszer lemezének nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="d32a3-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="d32a3-150">-OsDiskOsType</span></span>
<span data-ttu-id="d32a3-151">A lemezen az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="d32a3-152">Ez csak a felhasználói képforgatókönyvek esetében szükséges, és nem platformos képhez.</span><span class="sxs-lookup"><span data-stu-id="d32a3-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="d32a3-153">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="d32a3-153">-VhdContainer</span></span>
<span data-ttu-id="d32a3-154">Annak a tárolónak a tároló URL-címét adja meg, amely a VMSS operációs rendszer lemezének tárolására szolgál.</span><span class="sxs-lookup"><span data-stu-id="d32a3-154">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="d32a3-155">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d32a3-155">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d32a3-156">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d32a3-156">Specifies the VMSS object.</span></span>
<span data-ttu-id="d32a3-157">Az objektum beolvasásához használja a New-AzureRmVmssConfig objektumot.</span><span class="sxs-lookup"><span data-stu-id="d32a3-157">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

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

### <span data-ttu-id="d32a3-158">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d32a3-158">-Confirm</span></span>
<span data-ttu-id="d32a3-159">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d32a3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d32a3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d32a3-160">-WhatIf</span></span>
<span data-ttu-id="d32a3-161">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d32a3-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d32a3-162">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d32a3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d32a3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d32a3-163">CommonParameters</span></span>
<span data-ttu-id="d32a3-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d32a3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d32a3-165">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d32a3-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d32a3-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32a3-166">INPUTS</span></span>

###  
<span data-ttu-id="d32a3-167">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d32a3-167">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d32a3-168">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d32a3-168">OUTPUTS</span></span>

## <span data-ttu-id="d32a3-169">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d32a3-169">NOTES</span></span>

## <span data-ttu-id="d32a3-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d32a3-170">RELATED LINKS</span></span>

[<span data-ttu-id="d32a3-171">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d32a3-171">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="d32a3-172">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d32a3-172">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="d32a3-173">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d32a3-173">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="d32a3-174">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d32a3-174">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


