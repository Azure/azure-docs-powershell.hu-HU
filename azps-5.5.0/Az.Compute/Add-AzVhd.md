---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166579"
---
# <span data-ttu-id="6c037-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="6c037-101">Add-AzVhd</span></span>

## <span data-ttu-id="6c037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c037-102">SYNOPSIS</span></span>
<span data-ttu-id="6c037-103">Virtuális merevlemezt tölt fel egy helyszíni virtuális gépről egy blobba egy felhőbeli tárfiókban az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="6c037-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="6c037-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c037-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c037-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c037-105">DESCRIPTION</span></span>
<span data-ttu-id="6c037-106">Az **Add-AzVhd** parancsmag rögzített virtuális merevlemezek formájában feltölti a helyszíni virtuális merevlemezeket .vhd fájlformátumban egy blobtároló fiókba.</span><span class="sxs-lookup"><span data-stu-id="6c037-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="6c037-107">Konfigurálhatja a használni fogja a feltöltőszálak számát, vagy felülírhat egy meglévő blobot a megadott cél URI-ban.</span><span class="sxs-lookup"><span data-stu-id="6c037-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="6c037-108">Emellett támogatott a helyszíni .vhd fájlok javítással elérhető verziójának feltöltése is.</span><span class="sxs-lookup"><span data-stu-id="6c037-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="6c037-109">Ha már feltöltött egy alap virtuális merevlemezt, különböző lemezeket tölthet fel, amelyek szülőként az alapképet használják.</span><span class="sxs-lookup"><span data-stu-id="6c037-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="6c037-110">A megosztott hozzáférés-aláírás (SAS) URI-t is támogatja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="6c037-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="6c037-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c037-111">EXAMPLES</span></span>

### <span data-ttu-id="6c037-112">1. példa: VHD-fájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="6c037-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="6c037-113">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6c037-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="6c037-114">2. példa: VHD-fájl hozzáadása és a cél felülírása</span><span class="sxs-lookup"><span data-stu-id="6c037-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="6c037-115">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6c037-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="6c037-116">A parancs felülír egy meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="6c037-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="6c037-117">3. példa: VHD-fájl hozzáadása és a szálak számának megadása</span><span class="sxs-lookup"><span data-stu-id="6c037-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="6c037-118">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6c037-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="6c037-119">A parancs megadja a fájl feltöltésekor használni kívánt szálak számát.</span><span class="sxs-lookup"><span data-stu-id="6c037-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="6c037-120">4. példa: VHD fájl hozzáadása és az SAS URI megadása</span><span class="sxs-lookup"><span data-stu-id="6c037-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="6c037-121">Ez a parancs hozzáad egy .vhd fájlt egy tárfiókhoz, és megadja az SAS URI-t.</span><span class="sxs-lookup"><span data-stu-id="6c037-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="6c037-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c037-122">PARAMETERS</span></span>

### <span data-ttu-id="6c037-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c037-123">-AsJob</span></span>
<span data-ttu-id="6c037-124">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="6c037-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6c037-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="6c037-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="6c037-126">Az Azure Blob Storage alapkép blobját adja meg URI-nak.</span><span class="sxs-lookup"><span data-stu-id="6c037-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="6c037-127">A paraméter értékeként meg lehet adni egy SAS-t.</span><span class="sxs-lookup"><span data-stu-id="6c037-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c037-128">-DefaultProfile</span></span>
<span data-ttu-id="6c037-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c037-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c037-130">-Destination</span><span class="sxs-lookup"><span data-stu-id="6c037-130">-Destination</span></span>
<span data-ttu-id="6c037-131">Egy blob URI-ját adja meg a Blob Storage-ban.</span><span class="sxs-lookup"><span data-stu-id="6c037-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="6c037-132">A paraméter támogatja az SAS URI-t, bár a javítási esetek célhelye nem lehet SAS URI.</span><span class="sxs-lookup"><span data-stu-id="6c037-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="6c037-133">-LocalFilePath</span></span>
<span data-ttu-id="6c037-134">A helyi .vhd fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c037-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="6c037-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="6c037-136">A .vhd fájl feltöltésekor használt feltöltőszálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c037-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-137">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="6c037-137">-OverWrite</span></span>
<span data-ttu-id="6c037-138">Azt jelzi, hogy ez a parancsmag felülír egy meglévő blobot a megadott cél URI-ban, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="6c037-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c037-139">-ResourceGroupName</span></span>
<span data-ttu-id="6c037-140">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6c037-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c037-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c037-141">CommonParameters</span></span>
<span data-ttu-id="6c037-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c037-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c037-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c037-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c037-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c037-144">INPUTS</span></span>

### <span data-ttu-id="6c037-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6c037-145">System.String</span></span>

### <span data-ttu-id="6c037-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="6c037-146">System.Uri</span></span>

### <span data-ttu-id="6c037-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="6c037-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="6c037-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6c037-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6c037-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6c037-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6c037-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c037-150">OUTPUTS</span></span>

### <span data-ttu-id="6c037-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="6c037-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="6c037-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c037-152">NOTES</span></span>

## <span data-ttu-id="6c037-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c037-153">RELATED LINKS</span></span>

[<span data-ttu-id="6c037-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="6c037-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


