---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024809"
---
# <span data-ttu-id="e8fe6-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="e8fe6-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="e8fe6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fe6-103">Az operációs rendszer lemezének tulajdonságait állítja be egy kép objektumon.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="e8fe6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8fe6-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8fe6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8fe6-105">DESCRIPTION</span></span>
<span data-ttu-id="e8fe6-106">A **set-AzImageOsDisk** parancsmag az operációs rendszer lemezének tulajdonságait állítja be egy kép objektumon.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="e8fe6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e8fe6-107">EXAMPLES</span></span>

### <span data-ttu-id="e8fe6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8fe6-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="e8fe6-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="e8fe6-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="e8fe6-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="e8fe6-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e8fe6-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="e8fe6-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e8fe6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8fe6-115">PARAMETERS</span></span>

### <span data-ttu-id="e8fe6-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="e8fe6-116">-BlobUri</span></span>
<span data-ttu-id="e8fe6-117">A blob URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="e8fe6-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="e8fe6-118">-Caching</span></span>
<span data-ttu-id="e8fe6-119">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fe6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fe6-120">-DefaultProfile</span></span>
<span data-ttu-id="e8fe6-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8fe6-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e8fe6-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e8fe6-123">Az ügyfél által felügyelt lemezvezérlő-titkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="e8fe6-124">Ezt csak a felügyelt lemezek esetében lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="e8fe6-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e8fe6-125">-DiskSizeGB</span></span>
<span data-ttu-id="e8fe6-126">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-126">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fe6-127">-Kép</span><span class="sxs-lookup"><span data-stu-id="e8fe6-127">-Image</span></span>
<span data-ttu-id="e8fe6-128">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fe6-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e8fe6-129">-ManagedDiskId</span></span>
<span data-ttu-id="e8fe6-130">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="e8fe6-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="e8fe6-131">-OsState</span></span>
<span data-ttu-id="e8fe6-132">Az operációs rendszer állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fe6-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="e8fe6-133">-OsType</span></span>
<span data-ttu-id="e8fe6-134">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fe6-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="e8fe6-135">-SnapshotId</span></span>
<span data-ttu-id="e8fe6-136">A pillanatkép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="e8fe6-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e8fe6-137">-StorageAccountType</span></span>
<span data-ttu-id="e8fe6-138">Az operációs rendszer képlemezének tárolási fiók típusa</span><span class="sxs-lookup"><span data-stu-id="e8fe6-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="e8fe6-139">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e8fe6-139">-Confirm</span></span>
<span data-ttu-id="e8fe6-140">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8fe6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8fe6-141">-WhatIf</span></span>
<span data-ttu-id="e8fe6-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8fe6-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8fe6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fe6-144">CommonParameters</span></span>
<span data-ttu-id="e8fe6-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8fe6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fe6-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e8fe6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fe6-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fe6-147">INPUTS</span></span>

### <span data-ttu-id="e8fe6-148">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e8fe6-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="e8fe6-149">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e8fe6-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e8fe6-150">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemStateTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e8fe6-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e8fe6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e8fe6-151">System.String</span></span>

### <span data-ttu-id="e8fe6-152">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e8fe6-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e8fe6-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e8fe6-153">System.Int32</span></span>

## <span data-ttu-id="e8fe6-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8fe6-154">OUTPUTS</span></span>

### <span data-ttu-id="e8fe6-155">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e8fe6-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e8fe6-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8fe6-156">NOTES</span></span>

## <span data-ttu-id="e8fe6-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8fe6-157">RELATED LINKS</span></span>
