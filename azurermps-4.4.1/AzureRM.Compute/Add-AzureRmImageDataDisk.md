---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: 6c96114e7f3c430ca81679733d7bb3b007cab27f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505211"
---
# <span data-ttu-id="aa8f1-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="aa8f1-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="aa8f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aa8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8f1-103">Adatlemez felvétele a képobjektumba.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa8f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aa8f1-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa8f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aa8f1-105">DESCRIPTION</span></span>
<span data-ttu-id="aa8f1-106">A **Add-AzureRmImageDataDisk** parancsmag adatlemezt ad hozzá egy képobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="aa8f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aa8f1-107">EXAMPLES</span></span>

### <span data-ttu-id="aa8f1-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aa8f1-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="aa8f1-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="aa8f1-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="aa8f1-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="aa8f1-112">A következő három parancs a $imageConfigban tárolt lemezképhez az operációs rendszer lemezét és két adatlemezét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="aa8f1-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="aa8f1-114">A végleges parancs létrehoz egy ImageName01 nevű képet az erőforráscsoport ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="aa8f1-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aa8f1-115">PARAMETERS</span></span>

### <span data-ttu-id="aa8f1-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="aa8f1-116">-BlobUri</span></span>
<span data-ttu-id="aa8f1-117">A blob-azonosító hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="aa8f1-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="aa8f1-118">-Caching</span></span>
<span data-ttu-id="aa8f1-119">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="aa8f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8f1-120">-DefaultProfile</span></span>
<span data-ttu-id="aa8f1-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa8f1-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="aa8f1-122">-DiskSizeGB</span></span>
<span data-ttu-id="aa8f1-123">A lemez méretének meghatározása gigabájtban (GB).</span><span class="sxs-lookup"><span data-stu-id="aa8f1-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="aa8f1-124">-Kép</span><span class="sxs-lookup"><span data-stu-id="aa8f1-124">-Image</span></span>
<span data-ttu-id="aa8f1-125">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="aa8f1-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="aa8f1-126">-Lun</span></span>
<span data-ttu-id="aa8f1-127">A logikai egység (LUN) számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="aa8f1-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="aa8f1-128">-ManagedDiskId</span></span>
<span data-ttu-id="aa8f1-129">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="aa8f1-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="aa8f1-130">-SnapshotId</span></span>
<span data-ttu-id="aa8f1-131">A pillanatkép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="aa8f1-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aa8f1-132">-StorageAccountType</span></span>
<span data-ttu-id="aa8f1-133">Az Adatlemezkép lemez tárolási fiók típusa</span><span class="sxs-lookup"><span data-stu-id="aa8f1-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="aa8f1-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aa8f1-134">-Confirm</span></span>
<span data-ttu-id="aa8f1-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa8f1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa8f1-136">-WhatIf</span></span>
<span data-ttu-id="aa8f1-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa8f1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aa8f1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa8f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8f1-139">CommonParameters</span></span>
<span data-ttu-id="aa8f1-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aa8f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8f1-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa8f1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8f1-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa8f1-142">INPUTS</span></span>

### <span data-ttu-id="aa8f1-143">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="aa8f1-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="aa8f1-144">System. Int32 System. String System. null `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="aa8f1-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="aa8f1-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aa8f1-145">OUTPUTS</span></span>

### <span data-ttu-id="aa8f1-146">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="aa8f1-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="aa8f1-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aa8f1-147">NOTES</span></span>

## <span data-ttu-id="aa8f1-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aa8f1-148">RELATED LINKS</span></span>

