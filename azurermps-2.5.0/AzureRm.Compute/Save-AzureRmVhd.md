---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/save-azurermvhd
schema: 2.0.0
ms.openlocfilehash: 86a4cdb4fc0d6709d6cb9311d243f12dcb65e5de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850905"
---
# <span data-ttu-id="ff163-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="ff163-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="ff163-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff163-102">SYNOPSIS</span></span>
<span data-ttu-id="ff163-103">A letöltött. vhd képek helyi mentése</span><span class="sxs-lookup"><span data-stu-id="ff163-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff163-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff163-104">SYNTAX</span></span>

### <span data-ttu-id="ff163-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff163-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff163-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff163-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff163-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff163-107">DESCRIPTION</span></span>
<span data-ttu-id="ff163-108">A **Save-AzureRmVhd** parancsmag. vhd képeket ment egy blobról, ahol fájlt tárolnak.</span><span class="sxs-lookup"><span data-stu-id="ff163-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="ff163-109">Megadhatja, hogy hány letöltött hozzászólásláncot használ a folyamat, és hogy lecseréli-e a már meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="ff163-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="ff163-110">Ez a parancsmag a tartalom letöltését is letölti.</span><span class="sxs-lookup"><span data-stu-id="ff163-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="ff163-111">A virtuális merevlemez (VHD) formátum konvertálása nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="ff163-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="ff163-112">Példák</span><span class="sxs-lookup"><span data-stu-id="ff163-112">EXAMPLES</span></span>

### <span data-ttu-id="ff163-113">Példa 1: kép letöltése</span><span class="sxs-lookup"><span data-stu-id="ff163-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="ff163-114">Ez a parancs letölti a. vhd fájlt, és a helyi elérési út C:\vhd\Win7Image.vhd. tárolja.</span><span class="sxs-lookup"><span data-stu-id="ff163-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="ff163-115">2. példa: kép letöltése és a helyi fájl felülírása</span><span class="sxs-lookup"><span data-stu-id="ff163-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="ff163-116">Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.</span><span class="sxs-lookup"><span data-stu-id="ff163-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ff163-117">A parancs a *felülírás* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="ff163-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="ff163-118">Ha a C:\vhd\Win7Image.vhd már létezik, ez a parancs a helyére lép.</span><span class="sxs-lookup"><span data-stu-id="ff163-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="ff163-119">3. példa: képek letöltése megadott számú szál használatával</span><span class="sxs-lookup"><span data-stu-id="ff163-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="ff163-120">Ez a parancs letölti a. vhd fájlt, és a helyi elérési útra menti.</span><span class="sxs-lookup"><span data-stu-id="ff163-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="ff163-121">A parancs a 32 értékét adja meg a *NumberOfThreads* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="ff163-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="ff163-122">Ezért a parancsmag 32-szálakat használ ehhez a tevékenységhez.</span><span class="sxs-lookup"><span data-stu-id="ff163-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="ff163-123">Példa 4: kép letöltése és a tárolási kulcs megadása</span><span class="sxs-lookup"><span data-stu-id="ff163-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="ff163-124">Ez a parancs letölti a. vhd fájlt, és megadja a tárterület kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ff163-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="ff163-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff163-125">PARAMETERS</span></span>

### <span data-ttu-id="ff163-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff163-126">-AsJob</span></span>
<span data-ttu-id="ff163-127">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="ff163-127">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff163-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff163-128">-DefaultProfile</span></span>
<span data-ttu-id="ff163-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff163-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff163-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ff163-130">-LocalFilePath</span></span>
<span data-ttu-id="ff163-131">A mentett kép helyi fájlelérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff163-131">Specifies the local file path of the saved image.</span></span>

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

### <span data-ttu-id="ff163-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="ff163-132">-NumberOfThreads</span></span>
<span data-ttu-id="ff163-133">A parancsmag által a letöltés során használt letöltési szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff163-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="ff163-134">-Átír</span><span class="sxs-lookup"><span data-stu-id="ff163-134">-OverWrite</span></span>
<span data-ttu-id="ff163-135">Jelzi, hogy ez a parancsmag a *LocalFilePath* -fájl által megadott fájlt cseréli le, ha létezik.</span><span class="sxs-lookup"><span data-stu-id="ff163-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

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

### <span data-ttu-id="ff163-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff163-136">-ResourceGroupName</span></span>
<span data-ttu-id="ff163-137">A tárolási fiók erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff163-137">Specifies the name of the resource group of the storage account.</span></span>

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

### <span data-ttu-id="ff163-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ff163-138">-SourceUri</span></span>
<span data-ttu-id="ff163-139">A blob azonosítójának egységes erőforrás-azonosítóját adja meg `Azure` .</span><span class="sxs-lookup"><span data-stu-id="ff163-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

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

### <span data-ttu-id="ff163-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ff163-140">-StorageKey</span></span>
<span data-ttu-id="ff163-141">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff163-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="ff163-142">Ha nem ad meg billentyűt, ez a parancsmag megkísérli meghatározni az Azure-ról az *SourceUri* -ról származó fiók tárolási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="ff163-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

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

### <span data-ttu-id="ff163-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff163-143">CommonParameters</span></span>
<span data-ttu-id="ff163-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff163-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff163-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff163-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff163-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff163-146">INPUTS</span></span>

### <span data-ttu-id="ff163-147">Nincs</span><span class="sxs-lookup"><span data-stu-id="ff163-147">None</span></span>
<span data-ttu-id="ff163-148">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ff163-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff163-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff163-149">OUTPUTS</span></span>

### <span data-ttu-id="ff163-150">Microsoft. Azure. commands. kiszámítás. models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="ff163-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="ff163-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff163-151">NOTES</span></span>

## <span data-ttu-id="ff163-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff163-152">RELATED LINKS</span></span>

[<span data-ttu-id="ff163-153">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="ff163-153">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


