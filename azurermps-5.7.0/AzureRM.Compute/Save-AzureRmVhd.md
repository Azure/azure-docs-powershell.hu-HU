---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: b428ec98090c0fdd2d6b12bf7dfa06e833b58d42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672870"
---
# <span data-ttu-id="ab24c-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="ab24c-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="ab24c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab24c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab24c-103">A letöltött. vhd képek helyi mentése</span><span class="sxs-lookup"><span data-stu-id="ab24c-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab24c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab24c-104">SYNTAX</span></span>

### <span data-ttu-id="ab24c-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab24c-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [<CommonParameters>]
```

### <span data-ttu-id="ab24c-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ab24c-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [<CommonParameters>]
```

## <span data-ttu-id="ab24c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab24c-107">DESCRIPTION</span></span>
<span data-ttu-id="ab24c-108">A **Save-AzureRmVhd** parancsmag. vhd képeket ment egy blobról, ahol fájlt tárolnak.</span><span class="sxs-lookup"><span data-stu-id="ab24c-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="ab24c-109">Megadhatja, hogy hány letöltött hozzászólásláncot használ a folyamat, és hogy lecseréli-e a már meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="ab24c-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="ab24c-110">Ez a parancsmag a tartalom letöltését is letölti.</span><span class="sxs-lookup"><span data-stu-id="ab24c-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="ab24c-111">A virtuális merevlemez (VHD) formátum konvertálása nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="ab24c-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="ab24c-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ab24c-112">EXAMPLES</span></span>

### <span data-ttu-id="ab24c-113">Példa 1: kép letöltése</span><span class="sxs-lookup"><span data-stu-id="ab24c-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="ab24c-114">Ez a parancs letölti a. vhd fájlt, és a helyi elérési út C:\vhd\Win7Image.vhd. tárolja.</span><span class="sxs-lookup"><span data-stu-id="ab24c-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="ab24c-115">2. példa: kép letöltése és a helyi fájl felülírása</span><span class="sxs-lookup"><span data-stu-id="ab24c-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="ab24c-116">Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.</span><span class="sxs-lookup"><span data-stu-id="ab24c-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ab24c-117">A parancs a *felülírás* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ab24c-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="ab24c-118">Ha a C:\vhd\Win7Image.vhd már létezik, ez a parancs a helyére lép.</span><span class="sxs-lookup"><span data-stu-id="ab24c-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="ab24c-119">3. példa: képek letöltése megadott számú szál használatával</span><span class="sxs-lookup"><span data-stu-id="ab24c-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="ab24c-120">Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.</span><span class="sxs-lookup"><span data-stu-id="ab24c-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ab24c-121">A parancs a 32 értékét adja meg a *NumberOfThreads* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="ab24c-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="ab24c-122">Ezért a parancsmag 32-szálakat használ ehhez a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="ab24c-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="ab24c-123">Példa 4: kép letöltése és a tárolási kulcs megadása</span><span class="sxs-lookup"><span data-stu-id="ab24c-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="ab24c-124">Ez a parancs letölti a. vhd fájlt, és megadja a tárterület kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab24c-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="ab24c-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab24c-125">PARAMETERS</span></span>

### <span data-ttu-id="ab24c-126">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ab24c-126">-LocalFilePath</span></span>
<span data-ttu-id="ab24c-127">A mentett kép helyi fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab24c-127">Specifies the local file path of the saved image.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-128">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="ab24c-128">-NumberOfThreads</span></span>
<span data-ttu-id="ab24c-129">A parancsmag által a letöltés során használt letöltési szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab24c-129">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-130">-Átír</span><span class="sxs-lookup"><span data-stu-id="ab24c-130">-OverWrite</span></span>
<span data-ttu-id="ab24c-131">Jelzi, hogy ez a parancsmag a *LocalFilePath* -fájl által megadott fájlt cseréli le, ha létezik.</span><span class="sxs-lookup"><span data-stu-id="ab24c-131">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab24c-132">-ResourceGroupName</span></span>
<span data-ttu-id="ab24c-133">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab24c-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ab24c-134">-SourceUri</span></span>
<span data-ttu-id="ab24c-135">A blob azonosítójának egységes erőforrás-azonosítóját adja meg `Azure` .</span><span class="sxs-lookup"><span data-stu-id="ab24c-135">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ab24c-136">-StorageKey</span></span>
<span data-ttu-id="ab24c-137">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab24c-137">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="ab24c-138">Ha nem ad meg billentyűt, ez a parancsmag megkísérli meghatározni az Azure-ról az *SourceUri* -ról származó fiók tárolási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ab24c-138">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab24c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab24c-139">CommonParameters</span></span>
<span data-ttu-id="ab24c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab24c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab24c-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab24c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab24c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab24c-142">INPUTS</span></span>

### <span data-ttu-id="ab24c-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="ab24c-143">None</span></span>
<span data-ttu-id="ab24c-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ab24c-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ab24c-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab24c-145">OUTPUTS</span></span>

## <span data-ttu-id="ab24c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab24c-146">NOTES</span></span>

## <span data-ttu-id="ab24c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab24c-147">RELATED LINKS</span></span>

[<span data-ttu-id="ab24c-148">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="ab24c-148">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


