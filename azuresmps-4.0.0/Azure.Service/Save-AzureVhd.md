---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015461"
---
# <span data-ttu-id="18bf4-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="18bf4-101">Save-AzureVhd</span></span>

## <span data-ttu-id="18bf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="18bf4-103">Engedélyezi a. vhd képek letöltését.</span><span class="sxs-lookup"><span data-stu-id="18bf4-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="18bf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18bf4-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="18bf4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="18bf4-105">DESCRIPTION</span></span>
<span data-ttu-id="18bf4-106">A **Save-AzureVhd** parancsmag lehetővé teszi a. vhd képek letöltését egy olyan blobról, amelyben fájlokat tárolnak.</span><span class="sxs-lookup"><span data-stu-id="18bf4-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="18bf4-107">A letöltési folyamat konfigurálására szolgáló paraméterekkel megadhatja, hogy hány letöltött hozzászóláslánc van használatban, vagy felülírja a fájlt, amely már létezik a megadott elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="18bf4-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="18bf4-108">A **Save-AzureVhd** nem végez semmilyen VHD-formátumú konverziót, és a blob le van letöltve.</span><span class="sxs-lookup"><span data-stu-id="18bf4-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="18bf4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="18bf4-110">1. példa: a VHD-fájl letöltése</span><span class="sxs-lookup"><span data-stu-id="18bf4-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="18bf4-111">Ez a parancs letölti a. vhd fájlt.</span><span class="sxs-lookup"><span data-stu-id="18bf4-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="18bf4-112">2. példa: a VHD-fájl letöltése és a helyi fájl felülírása</span><span class="sxs-lookup"><span data-stu-id="18bf4-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="18bf4-113">Ez a parancs letölti a. vhd fájlt, és felülír minden fájlt a célhely elérési útján.</span><span class="sxs-lookup"><span data-stu-id="18bf4-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="18bf4-114">3. példa: a VHD-fájl letöltése és a szálak számának megadása</span><span class="sxs-lookup"><span data-stu-id="18bf4-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="18bf4-115">Ez a parancs letölti a. vhd fájlt, és a szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18bf4-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="18bf4-116">4. példa: a VHD-fájl letöltése és a tárolási kulcs megadása</span><span class="sxs-lookup"><span data-stu-id="18bf4-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="18bf4-117">Ez a parancs letölti a. vhd fájlt, és megadja a tárterület kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18bf4-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="18bf4-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18bf4-118">PARAMETERS</span></span>

### <span data-ttu-id="18bf4-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="18bf4-119">-InformationAction</span></span>
<span data-ttu-id="18bf4-120">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="18bf4-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="18bf4-121">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="18bf4-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="18bf4-122">Folytassa</span><span class="sxs-lookup"><span data-stu-id="18bf4-122">Continue</span></span>
- <span data-ttu-id="18bf4-123">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="18bf4-123">Ignore</span></span>
- <span data-ttu-id="18bf4-124">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="18bf4-124">Inquire</span></span>
- <span data-ttu-id="18bf4-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="18bf4-125">SilentlyContinue</span></span>
- <span data-ttu-id="18bf4-126">állj</span><span class="sxs-lookup"><span data-stu-id="18bf4-126">Stop</span></span>
- <span data-ttu-id="18bf4-127">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="18bf4-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="18bf4-128">-InformationVariable</span></span>
<span data-ttu-id="18bf4-129">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="18bf4-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="18bf4-130">-LocalFilePath</span></span>
<span data-ttu-id="18bf4-131">A helyi fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="18bf4-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="18bf4-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="18bf4-132">-NumberOfThreads</span></span>
<span data-ttu-id="18bf4-133">A parancsmag által a letöltés során használt letöltési szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18bf4-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="18bf4-134">-Átír</span><span class="sxs-lookup"><span data-stu-id="18bf4-134">-OverWrite</span></span>
<span data-ttu-id="18bf4-135">Itt adhatja meg, hogy az adott parancsmag törölje a *LocalFilePath* -fájl által megadott fájlt, ha létezik.</span><span class="sxs-lookup"><span data-stu-id="18bf4-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="18bf4-136">-Profile</span></span>
<span data-ttu-id="18bf4-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="18bf4-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18bf4-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="18bf4-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-139">-Forrás</span><span class="sxs-lookup"><span data-stu-id="18bf4-139">-Source</span></span>
<span data-ttu-id="18bf4-140">A blobhoz tartozó egységes erőforrás-azonosító (URI) megadása `Azure` .</span><span class="sxs-lookup"><span data-stu-id="18bf4-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="18bf4-141">-StorageKey</span></span>
<span data-ttu-id="18bf4-142">A blob-tároló fiók tárolási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="18bf4-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="18bf4-143">Ha nem adja meg, a **Save-AzureVhd** megkísérli meghatározni az Azure-ról az *SourceUri* -fiókban lévő fiók tárolási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="18bf4-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18bf4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18bf4-144">CommonParameters</span></span>
<span data-ttu-id="18bf4-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18bf4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18bf4-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18bf4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18bf4-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18bf4-147">INPUTS</span></span>

## <span data-ttu-id="18bf4-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18bf4-148">OUTPUTS</span></span>

## <span data-ttu-id="18bf4-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18bf4-149">NOTES</span></span>

## <span data-ttu-id="18bf4-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18bf4-150">RELATED LINKS</span></span>

[<span data-ttu-id="18bf4-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="18bf4-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


