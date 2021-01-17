---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480906"
---
# <span data-ttu-id="d908f-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="d908f-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="d908f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d908f-102">SYNOPSIS</span></span>
<span data-ttu-id="d908f-103">Adatlemez hozzáadása képobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d908f-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="d908f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d908f-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d908f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d908f-105">DESCRIPTION</span></span>
<span data-ttu-id="d908f-106">Az **Add-AzImageDataDisk** parancsmag adatlemezt ad egy képobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="d908f-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="d908f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d908f-107">EXAMPLES</span></span>

### <span data-ttu-id="d908f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d908f-108">Example 1</span></span>
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

<span data-ttu-id="d908f-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="d908f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="d908f-110">A következő három parancs az operációs rendszer lemezének elérési útját és két adatlemezt rendel a $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="d908f-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d908f-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát közelíti meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="d908f-112">A következő három parancs egy operációs rendszerlemezt és két adatlemezt ad hozzá a $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d908f-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d908f-113">Az egyes lemezeket a $osDiskVhdUri, a $dataDiskVhdUri 1 és a $dataDiskVhdUri 2 tárolja.</span><span class="sxs-lookup"><span data-stu-id="d908f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="d908f-114">Az utolsó parancs létrehoz egy ImageName01 nevű képet az ResourceGroup01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d908f-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="d908f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d908f-115">PARAMETERS</span></span>

### <span data-ttu-id="d908f-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d908f-116">-BlobUri</span></span>
<span data-ttu-id="d908f-117">A blob URI-ként való hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="d908f-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="d908f-118">-Caching</span></span>
<span data-ttu-id="d908f-119">A lemez gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="d908f-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="d908f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d908f-120">-DefaultProfile</span></span>
<span data-ttu-id="d908f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d908f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d908f-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d908f-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d908f-123">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d908f-124">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="d908f-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d908f-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d908f-125">-DiskSizeGB</span></span>
<span data-ttu-id="d908f-126">A lemez gigabájtban (GB) megadott mérete.</span><span class="sxs-lookup"><span data-stu-id="d908f-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="d908f-127">-Image</span><span class="sxs-lookup"><span data-stu-id="d908f-127">-Image</span></span>
<span data-ttu-id="d908f-128">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="d908f-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="d908f-129">-Lun</span></span>
<span data-ttu-id="d908f-130">A logikai egység számát (LUN) adja meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-130">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d908f-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d908f-131">-ManagedDiskId</span></span>
<span data-ttu-id="d908f-132">Egy felügyelt lemez azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d908f-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d908f-133">-SnapshotId</span></span>
<span data-ttu-id="d908f-134">Egy pillanatfelvétel azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d908f-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d908f-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d908f-135">-StorageAccountType</span></span>
<span data-ttu-id="d908f-136">The Storage Account type of the data image disk</span><span class="sxs-lookup"><span data-stu-id="d908f-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="d908f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d908f-137">-Confirm</span></span>
<span data-ttu-id="d908f-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d908f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d908f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d908f-139">-WhatIf</span></span>
<span data-ttu-id="d908f-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d908f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d908f-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d908f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d908f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d908f-142">CommonParameters</span></span>
<span data-ttu-id="d908f-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d908f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d908f-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d908f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d908f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d908f-145">INPUTS</span></span>

### <span data-ttu-id="d908f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d908f-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="d908f-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d908f-147">System.Int32</span></span>

### <span data-ttu-id="d908f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d908f-148">System.String</span></span>

### <span data-ttu-id="d908f-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d908f-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d908f-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d908f-150">OUTPUTS</span></span>

### <span data-ttu-id="d908f-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d908f-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d908f-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d908f-152">NOTES</span></span>

## <span data-ttu-id="d908f-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d908f-153">RELATED LINKS</span></span>
