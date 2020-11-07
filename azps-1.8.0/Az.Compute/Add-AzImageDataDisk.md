---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 53c9909fb6934e94fc9d0076b73e413856968c8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671383"
---
# <span data-ttu-id="88dee-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="88dee-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="88dee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88dee-102">SYNOPSIS</span></span>
<span data-ttu-id="88dee-103">Adatlemez felvétele a képobjektumba.</span><span class="sxs-lookup"><span data-stu-id="88dee-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="88dee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88dee-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88dee-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="88dee-105">DESCRIPTION</span></span>
<span data-ttu-id="88dee-106">A **Add-AzImageDataDisk** parancsmag adatlemezt ad hozzá egy képobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="88dee-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="88dee-107">Példák</span><span class="sxs-lookup"><span data-stu-id="88dee-107">EXAMPLES</span></span>

### <span data-ttu-id="88dee-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="88dee-108">Example 1</span></span>
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

<span data-ttu-id="88dee-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="88dee-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="88dee-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="88dee-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="88dee-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="88dee-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="88dee-112">A következő három parancs a $imageConfigban tárolt lemezképhez az operációs rendszer lemezét és két adatlemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="88dee-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="88dee-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="88dee-114">A végleges parancs létrehoz egy ImageName01 nevű képet az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="88dee-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="88dee-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88dee-115">PARAMETERS</span></span>

### <span data-ttu-id="88dee-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="88dee-116">-BlobUri</span></span>
<span data-ttu-id="88dee-117">A blob-azonosító hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="88dee-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="88dee-118">-Caching</span></span>
<span data-ttu-id="88dee-119">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="88dee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dee-120">-DefaultProfile</span></span>
<span data-ttu-id="88dee-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88dee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88dee-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="88dee-122">-DiskSizeGB</span></span>
<span data-ttu-id="88dee-123">A lemez méretének meghatározása gigabájtban (GB).</span><span class="sxs-lookup"><span data-stu-id="88dee-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="88dee-124">-Kép</span><span class="sxs-lookup"><span data-stu-id="88dee-124">-Image</span></span>
<span data-ttu-id="88dee-125">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="88dee-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="88dee-126">-Lun</span></span>
<span data-ttu-id="88dee-127">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="88dee-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="88dee-128">-ManagedDiskId</span></span>
<span data-ttu-id="88dee-129">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="88dee-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="88dee-130">-SnapshotId</span></span>
<span data-ttu-id="88dee-131">A pillanatkép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="88dee-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="88dee-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="88dee-132">-StorageAccountType</span></span>
<span data-ttu-id="88dee-133">Az Adatlemezkép lemez tárolási fiók típusa</span><span class="sxs-lookup"><span data-stu-id="88dee-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="88dee-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88dee-134">-Confirm</span></span>
<span data-ttu-id="88dee-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88dee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88dee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88dee-136">-WhatIf</span></span>
<span data-ttu-id="88dee-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88dee-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88dee-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88dee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88dee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dee-139">CommonParameters</span></span>
<span data-ttu-id="88dee-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88dee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dee-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dee-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dee-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88dee-142">INPUTS</span></span>

### <span data-ttu-id="88dee-143">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="88dee-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="88dee-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="88dee-144">System.Int32</span></span>

### <span data-ttu-id="88dee-145">System. String</span><span class="sxs-lookup"><span data-stu-id="88dee-145">System.String</span></span>

### <span data-ttu-id="88dee-146">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. CachingTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="88dee-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="88dee-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88dee-147">OUTPUTS</span></span>

### <span data-ttu-id="88dee-148">Microsoft. Azure. commands. számítási. Automation. models. PSImage</span><span class="sxs-lookup"><span data-stu-id="88dee-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="88dee-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88dee-149">NOTES</span></span>

## <span data-ttu-id="88dee-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88dee-150">RELATED LINKS</span></span>
