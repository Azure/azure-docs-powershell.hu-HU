---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: 14b0ad981eb44a855f57e6d86df5fd1c03de42e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204790"
---
# <span data-ttu-id="7f3d6-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="7f3d6-101">Save-AzVhd</span></span>

## <span data-ttu-id="7f3d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f3d6-103">A letöltött .vhd képeket helyileg menti.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="7f3d6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f3d6-104">SYNTAX</span></span>

### <span data-ttu-id="7f3d6-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f3d6-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f3d6-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f3d6-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>]
 [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f3d6-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f3d6-107">DESCRIPTION</span></span>
<span data-ttu-id="7f3d6-108">A **Save-AzVhd** parancsmag .vhd képeket ment egy blobból, ahol azok egy fájlba vannak mentve.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="7f3d6-109">Megadhatja, hogy a folyamat hány letöltőszálat használ, és hogy lecserélje-e a már létező fájlokat.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>
<span data-ttu-id="7f3d6-110">Ez a parancsmag a tartalom teljes tartalmát letölti.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="7f3d6-111">Nem alkalmaz virtuális merevlemez-formátumkonverziót.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="7f3d6-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f3d6-112">EXAMPLES</span></span>

### <span data-ttu-id="7f3d6-113">1. példa: Kép letöltése</span><span class="sxs-lookup"><span data-stu-id="7f3d6-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="7f3d6-114">Ez a parancs letölt egy .vhd fájlt, és a C:\vhd\Win7Image.vhd elérési úton tárolja.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="7f3d6-115">2. példa: Kép letöltése és a helyi fájl felülírása</span><span class="sxs-lookup"><span data-stu-id="7f3d6-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="7f3d6-116">Ez a parancs letölt egy .vhd fájlt, és a helyi elérési úton tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7f3d6-117">A parancs tartalmazza *a Felülírás* paramétert.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="7f3d6-118">Ezért ha a C:\vhd\Win7Image.vhd már létezik, ez a parancs helyettesíti azt.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="7f3d6-119">3. példa: Kép letöltése megadott számú szál használatával</span><span class="sxs-lookup"><span data-stu-id="7f3d6-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="7f3d6-120">Ez a parancs letölt egy .vhd fájlt, és a helyi elérési úton tárolja azt.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="7f3d6-121">A parancs 32 értéket ad meg a *NumberOfThreads paraméterhez.*</span><span class="sxs-lookup"><span data-stu-id="7f3d6-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="7f3d6-122">Ezért a parancsmag 32 szálat használ ehhez a művelethez.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="7f3d6-123">4. példa: Kép letöltése és a tárkulcs megadása</span><span class="sxs-lookup"><span data-stu-id="7f3d6-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="7f3d6-124">Ez a parancs letölt egy .vhd fájlt, és megadja a tárkulcsot.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="7f3d6-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f3d6-125">PARAMETERS</span></span>

### <span data-ttu-id="7f3d6-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f3d6-126">-AsJob</span></span>
<span data-ttu-id="7f3d6-127">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f3d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f3d6-128">-DefaultProfile</span></span>
<span data-ttu-id="7f3d6-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f3d6-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="7f3d6-130">-LocalFilePath</span></span>
<span data-ttu-id="7f3d6-131">A mentett kép helyi elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="7f3d6-132">-NumberOfThreads</span></span>
<span data-ttu-id="7f3d6-133">A parancsmag által a letöltés során használt letöltési szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-134">-Felülírás</span><span class="sxs-lookup"><span data-stu-id="7f3d6-134">-OverWrite</span></span>
<span data-ttu-id="7f3d6-135">Azt jelzi, hogy ez a parancsmag lecseréli a *LocalFilePath-fájl* által megadott fájlt, ha létezik.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f3d6-136">-ResourceGroupName</span></span>
<span data-ttu-id="7f3d6-137">A tárfiók erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7f3d6-138">-SourceUri</span></span>
<span data-ttu-id="7f3d6-139">A blob egységes erőforrás-azonosítóját (URI) adja `Azure` meg.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="7f3d6-140">-StorageKey</span></span>
<span data-ttu-id="7f3d6-141">A blobtároló-fiók tárkulcsát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="7f3d6-142">Ha nem ad meg kulcsot, ez a parancsmag megkísérli meghatározni a fiók tárkulcsát az *Azure-ból származó SourceUri-ban.*</span><span class="sxs-lookup"><span data-stu-id="7f3d6-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f3d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f3d6-143">CommonParameters</span></span>
<span data-ttu-id="7f3d6-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f3d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f3d6-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f3d6-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f3d6-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f3d6-146">INPUTS</span></span>

### <span data-ttu-id="7f3d6-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7f3d6-147">System.String</span></span>

### <span data-ttu-id="7f3d6-148">System.Uri</span><span class="sxs-lookup"><span data-stu-id="7f3d6-148">System.Uri</span></span>

## <span data-ttu-id="7f3d6-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f3d6-149">OUTPUTS</span></span>

### <span data-ttu-id="7f3d6-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="7f3d6-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="7f3d6-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f3d6-151">NOTES</span></span>

## <span data-ttu-id="7f3d6-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f3d6-152">RELATED LINKS</span></span>

[<span data-ttu-id="7f3d6-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="7f3d6-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


