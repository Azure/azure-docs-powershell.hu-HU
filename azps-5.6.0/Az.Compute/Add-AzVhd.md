---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 6e86ed8cde1297af54ffaf8f8c8fbc912da30e69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933153"
---
# <span data-ttu-id="a2b4e-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="a2b4e-101">Add-AzVhd</span></span>

## <span data-ttu-id="a2b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b4e-103">Virtuális merevlemezt tölt fel egy helyszíni virtuális gépről egy blobba egy felhőbeli tárfiókban az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="a2b4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2b4e-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2b4e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b4e-106">Az **Add-AzVhd** parancsmag .vhd fájlformátumban feltölti a helyszíni virtuális merevlemezeket egy blobtároló fiókba rögzített virtuális merevlemezként.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="a2b4e-107">Beállíthatja, hogy hány feltöltőszálat fog használni, vagy felülírhat egy meglévő blobot a megadott cél URI-ban.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="a2b4e-108">Emellett támogatott a helyszíni .vhd fájlok javítással elérhető verziójának feltöltése is.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="a2b4e-109">Ha már feltöltött egy alap virtuális merevlemezt, különböző lemezeket tölthet fel, amelyek szülőként az alapképet használják.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="a2b4e-110">A megosztott hozzáférés-aláírás (SAS) URI-t is támogatja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="a2b4e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2b4e-111">EXAMPLES</span></span>

### <span data-ttu-id="a2b4e-112">1. példa: VHD-fájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="a2b4e-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="a2b4e-113">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="a2b4e-114">2. példa: VHD-fájl hozzáadása és a cél felülírása</span><span class="sxs-lookup"><span data-stu-id="a2b4e-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="a2b4e-115">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="a2b4e-116">A parancs felülír egy meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="a2b4e-117">3. példa: VHD-fájl hozzáadása és a szálak számának megadása</span><span class="sxs-lookup"><span data-stu-id="a2b4e-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="a2b4e-118">Ez a parancs .vhd fájlt ad hozzá egy tárfiókhoz.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="a2b4e-119">A parancs megadja a fájl feltöltésekor használni kívánt szálak számát.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="a2b4e-120">4. példa: VHD fájl hozzáadása és az SAS URI megadása</span><span class="sxs-lookup"><span data-stu-id="a2b4e-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="a2b4e-121">Ez a parancs hozzáad egy .vhd fájlt egy tárfiókhoz, és megadja az SAS URI-t.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="a2b4e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2b4e-122">PARAMETERS</span></span>

### <span data-ttu-id="a2b4e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2b4e-123">-AsJob</span></span>
<span data-ttu-id="a2b4e-124">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a2b4e-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="a2b4e-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="a2b4e-126">Az Azure Blob Storage alapkép blobját adja meg URI-nak.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="a2b4e-127">A paraméter értékeként meg lehet adni egy SAS-t.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="a2b4e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b4e-128">-DefaultProfile</span></span>
<span data-ttu-id="a2b4e-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2b4e-130">-Destination</span><span class="sxs-lookup"><span data-stu-id="a2b4e-130">-Destination</span></span>
<span data-ttu-id="a2b4e-131">Egy blob URI-ját adja meg a Blob Storage-ban.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="a2b4e-132">A paraméter támogatja az SAS URI-t, bár a javítási esetek célhelye nem lehet SAS URI.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="a2b4e-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="a2b4e-133">-LocalFilePath</span></span>
<span data-ttu-id="a2b4e-134">A helyi .vhd fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="a2b4e-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="a2b4e-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="a2b4e-136">A .vhd fájl feltöltésekor használt feltöltőszálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="a2b4e-137">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="a2b4e-137">-OverWrite</span></span>
<span data-ttu-id="a2b4e-138">Azt jelzi, hogy ez a parancsmag felülír egy meglévő blobot a megadott cél URI-ban, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="a2b4e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b4e-139">-ResourceGroupName</span></span>
<span data-ttu-id="a2b4e-140">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a2b4e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b4e-141">CommonParameters</span></span>
<span data-ttu-id="a2b4e-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b4e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b4e-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2b4e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b4e-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2b4e-144">INPUTS</span></span>

### <span data-ttu-id="a2b4e-145">System.String</span><span class="sxs-lookup"><span data-stu-id="a2b4e-145">System.String</span></span>

### <span data-ttu-id="a2b4e-146">System.Uri</span><span class="sxs-lookup"><span data-stu-id="a2b4e-146">System.Uri</span></span>

### <span data-ttu-id="a2b4e-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="a2b4e-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="a2b4e-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a2b4e-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a2b4e-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2b4e-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2b4e-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2b4e-150">OUTPUTS</span></span>

### <span data-ttu-id="a2b4e-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="a2b4e-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="a2b4e-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2b4e-152">NOTES</span></span>

## <span data-ttu-id="a2b4e-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2b4e-153">RELATED LINKS</span></span>

[<span data-ttu-id="a2b4e-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="a2b4e-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


