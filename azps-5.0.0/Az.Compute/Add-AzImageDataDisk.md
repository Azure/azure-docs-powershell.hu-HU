---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299630"
---
# <span data-ttu-id="1b4de-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="1b4de-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="1b4de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1b4de-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4de-103">Adatlemez felvétele a képobjektumba.</span><span class="sxs-lookup"><span data-stu-id="1b4de-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="1b4de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1b4de-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b4de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1b4de-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4de-106">A **Add-AzImageDataDisk** parancsmag adatlemezt ad hozzá egy képobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1b4de-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="1b4de-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1b4de-107">EXAMPLES</span></span>

### <span data-ttu-id="1b4de-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1b4de-108">Example 1</span></span>
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

<span data-ttu-id="1b4de-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1b4de-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="1b4de-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="1b4de-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="1b4de-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="1b4de-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="1b4de-112">A következő három parancs a $imageConfigban tárolt lemezképhez az operációs rendszer lemezét és két adatlemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="1b4de-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="1b4de-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="1b4de-114">A végleges parancs létrehoz egy ImageName01 nevű képet az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1b4de-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="1b4de-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1b4de-115">PARAMETERS</span></span>

### <span data-ttu-id="1b4de-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="1b4de-116">-BlobUri</span></span>
<span data-ttu-id="1b4de-117">A blob-azonosító hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="1b4de-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="1b4de-118">-Caching</span></span>
<span data-ttu-id="1b4de-119">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4de-120">-DefaultProfile</span></span>
<span data-ttu-id="1b4de-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b4de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b4de-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1b4de-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1b4de-123">Az ügyfél által felügyelt lemezvezérlő-titkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="1b4de-124">Ezt csak a felügyelt lemezek esetében lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="1b4de-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="1b4de-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="1b4de-125">-DiskSizeGB</span></span>
<span data-ttu-id="1b4de-126">A lemez méretének meghatározása gigabájtban (GB).</span><span class="sxs-lookup"><span data-stu-id="1b4de-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="1b4de-127">-Kép</span><span class="sxs-lookup"><span data-stu-id="1b4de-127">-Image</span></span>
<span data-ttu-id="1b4de-128">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="1b4de-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="1b4de-129">-Lun</span></span>
<span data-ttu-id="1b4de-130">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b4de-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="1b4de-131">-ManagedDiskId</span></span>
<span data-ttu-id="1b4de-132">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="1b4de-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="1b4de-133">-SnapshotId</span></span>
<span data-ttu-id="1b4de-134">A pillanatkép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1b4de-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="1b4de-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1b4de-135">-StorageAccountType</span></span>
<span data-ttu-id="1b4de-136">Az Adatlemezkép lemez tárolási fiók típusa</span><span class="sxs-lookup"><span data-stu-id="1b4de-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="1b4de-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1b4de-137">-Confirm</span></span>
<span data-ttu-id="1b4de-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1b4de-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b4de-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4de-139">-WhatIf</span></span>
<span data-ttu-id="1b4de-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1b4de-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b4de-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b4de-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b4de-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4de-142">CommonParameters</span></span>
<span data-ttu-id="1b4de-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1b4de-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4de-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1b4de-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4de-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b4de-145">INPUTS</span></span>

### <span data-ttu-id="1b4de-146">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="1b4de-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="1b4de-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1b4de-147">System.Int32</span></span>

### <span data-ttu-id="1b4de-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1b4de-148">System.String</span></span>

### <span data-ttu-id="1b4de-149">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1b4de-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1b4de-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b4de-150">OUTPUTS</span></span>

### <span data-ttu-id="1b4de-151">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="1b4de-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="1b4de-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1b4de-152">NOTES</span></span>

## <span data-ttu-id="1b4de-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b4de-153">RELATED LINKS</span></span>
