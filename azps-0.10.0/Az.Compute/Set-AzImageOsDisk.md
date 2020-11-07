---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 5bc92ea5aa49cb97be457fd937c7b9deb492bb0e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844285"
---
# <span data-ttu-id="d6616-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="d6616-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="d6616-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6616-102">SYNOPSIS</span></span>
<span data-ttu-id="d6616-103">Az operációs rendszer lemezének tulajdonságait állítja be egy kép objektumon.</span><span class="sxs-lookup"><span data-stu-id="d6616-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d6616-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6616-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6616-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6616-105">DESCRIPTION</span></span>
<span data-ttu-id="d6616-106">A **set-AzImageOsDisk** parancsmag az operációs rendszer lemezének tulajdonságait állítja be egy kép objektumon.</span><span class="sxs-lookup"><span data-stu-id="d6616-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d6616-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d6616-107">EXAMPLES</span></span>

### <span data-ttu-id="d6616-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6616-108">Example 1</span></span>
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

<span data-ttu-id="d6616-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d6616-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="d6616-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli hozzá a $osDiskVhdUrihoz, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változót.</span><span class="sxs-lookup"><span data-stu-id="d6616-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d6616-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát szolgálhatja.</span><span class="sxs-lookup"><span data-stu-id="d6616-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="d6616-112">A következő három parancs mindegyike egy operációs rendszert és két adatlemezt ad az $imageConfig-ban tárolt képhez.</span><span class="sxs-lookup"><span data-stu-id="d6616-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d6616-113">Az egyes lemezek URI-ja $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="d6616-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="d6616-114">A végleges parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="d6616-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d6616-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6616-115">PARAMETERS</span></span>

### <span data-ttu-id="d6616-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d6616-116">-BlobUri</span></span>
<span data-ttu-id="d6616-117">A blob URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="d6616-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="d6616-118">-Caching</span></span>
<span data-ttu-id="d6616-119">A lemez gyorsítótárazási módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6616-120">-DefaultProfile</span></span>
<span data-ttu-id="d6616-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6616-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d6616-122">-DiskSizeGB</span></span>
<span data-ttu-id="d6616-123">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="d6616-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-124">-Kép</span><span class="sxs-lookup"><span data-stu-id="d6616-124">-Image</span></span>
<span data-ttu-id="d6616-125">Helyi kép objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d6616-126">-ManagedDiskId</span></span>
<span data-ttu-id="d6616-127">A felügyelt lemezek AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d6616-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="d6616-128">-OsState</span></span>
<span data-ttu-id="d6616-129">Az operációs rendszer állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-129">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="d6616-130">-OsType</span></span>
<span data-ttu-id="d6616-131">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6616-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d6616-132">-SnapshotId</span></span>
<span data-ttu-id="d6616-133">A pillanatkép AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d6616-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d6616-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d6616-134">-StorageAccountType</span></span>
<span data-ttu-id="d6616-135">Az operációs rendszer képlemezének tárolási fiók típusa</span><span class="sxs-lookup"><span data-stu-id="d6616-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="d6616-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6616-136">-Confirm</span></span>
<span data-ttu-id="d6616-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6616-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6616-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6616-138">-WhatIf</span></span>
<span data-ttu-id="d6616-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6616-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6616-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6616-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6616-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6616-141">CommonParameters</span></span>
<span data-ttu-id="d6616-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6616-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6616-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6616-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6616-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6616-144">INPUTS</span></span>

### <span data-ttu-id="d6616-145">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="d6616-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="d6616-146">System. null- `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. számítás. models. OperatingSystemStateTypes, Microsoft. Azure. Management. számítás, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]] System. String System. null `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d6616-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d6616-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6616-147">OUTPUTS</span></span>

### <span data-ttu-id="d6616-148">Microsoft. Azure. Management. kiszámítás. modellek. kép</span><span class="sxs-lookup"><span data-stu-id="d6616-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="d6616-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6616-149">NOTES</span></span>

## <span data-ttu-id="d6616-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6616-150">RELATED LINKS</span></span>

