---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370423"
---
# <span data-ttu-id="d0a30-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="d0a30-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="d0a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a30-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a30-103">Beállítja az operációs rendszer lemeztulajdonságokat egy képobjektumon.</span><span class="sxs-lookup"><span data-stu-id="d0a30-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d0a30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0a30-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a30-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0a30-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a30-106">A **Set-AzImageOsDisk** parancsmag beállítja az operációs rendszer lemeztulajdonságokat egy képobjektumon.</span><span class="sxs-lookup"><span data-stu-id="d0a30-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="d0a30-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0a30-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a30-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d0a30-108">Example 1</span></span>
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

<span data-ttu-id="d0a30-109">Az első parancs létrehoz egy képobjektumot, majd a $imageConfig tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0a30-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="d0a30-110">A következő három parancs az operációs rendszer lemezének és két adatlemezének elérési útját rendeli a $osDiskVhdUri, $dataDiskVhdUri 1 és $dataDiskVhdUri 2 változóhoz.</span><span class="sxs-lookup"><span data-stu-id="d0a30-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="d0a30-111">Ez a megközelítés csak az alábbi parancsok olvashatóságát közelíti meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="d0a30-112">A következő három parancs egy operációs rendszerlemezt és két adatlemezt ad hozzá a $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="d0a30-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="d0a30-113">Az egyes lemezeket a $osDiskVhdUri, a $dataDiskVhdUri 1 és a $dataDiskVhdUri 2 tárolja.</span><span class="sxs-lookup"><span data-stu-id="d0a30-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="d0a30-114">Az utolsó parancs létrehoz egy "ImageName01" nevű képet az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="d0a30-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d0a30-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0a30-115">PARAMETERS</span></span>

### <span data-ttu-id="d0a30-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="d0a30-116">-BlobUri</span></span>
<span data-ttu-id="d0a30-117">A blob Uri-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="d0a30-118">-Gyorsítótárazás</span><span class="sxs-lookup"><span data-stu-id="d0a30-118">-Caching</span></span>
<span data-ttu-id="d0a30-119">A lemez gyorsítótárazása.</span><span class="sxs-lookup"><span data-stu-id="d0a30-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="d0a30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a30-120">-DefaultProfile</span></span>
<span data-ttu-id="d0a30-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d0a30-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0a30-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="d0a30-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="d0a30-123">Az ügyfél által felügyelt lemeztitkosítási készlet erőforrás-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="d0a30-124">Ez csak felügyelt lemezhez lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="d0a30-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="d0a30-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="d0a30-125">-DiskSizeGB</span></span>
<span data-ttu-id="d0a30-126">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="d0a30-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="d0a30-127">-Image</span><span class="sxs-lookup"><span data-stu-id="d0a30-127">-Image</span></span>
<span data-ttu-id="d0a30-128">Helyi képobjektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="d0a30-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="d0a30-129">-ManagedDiskId</span></span>
<span data-ttu-id="d0a30-130">Egy felügyelt lemez azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="d0a30-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="d0a30-131">-OsState</span></span>
<span data-ttu-id="d0a30-132">Az operációs rendszer állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="d0a30-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="d0a30-133">-OsType</span></span>
<span data-ttu-id="d0a30-134">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="d0a30-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="d0a30-135">-SnapshotId</span></span>
<span data-ttu-id="d0a30-136">Egy pillanatfelvétel azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a30-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="d0a30-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d0a30-137">-StorageAccountType</span></span>
<span data-ttu-id="d0a30-138">Az operációs rendszer lemezképének tárfióktípusa</span><span class="sxs-lookup"><span data-stu-id="d0a30-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="d0a30-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0a30-139">-Confirm</span></span>
<span data-ttu-id="d0a30-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0a30-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a30-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a30-141">-WhatIf</span></span>
<span data-ttu-id="d0a30-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0a30-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0a30-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0a30-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a30-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a30-144">CommonParameters</span></span>
<span data-ttu-id="d0a30-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a30-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a30-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0a30-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a30-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0a30-147">INPUTS</span></span>

### <span data-ttu-id="d0a30-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d0a30-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="d0a30-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0a30-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d0a30-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0a30-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d0a30-151">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a30-151">System.String</span></span>

### <span data-ttu-id="d0a30-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d0a30-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d0a30-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d0a30-153">System.Int32</span></span>

## <span data-ttu-id="d0a30-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a30-154">OUTPUTS</span></span>

### <span data-ttu-id="d0a30-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="d0a30-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="d0a30-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0a30-156">NOTES</span></span>

## <span data-ttu-id="d0a30-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0a30-157">RELATED LINKS</span></span>
