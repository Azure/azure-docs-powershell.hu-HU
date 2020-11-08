---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015718"
---
# <span data-ttu-id="3c232-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="3c232-101">Add-AzureVhd</span></span>

## <span data-ttu-id="3c232-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c232-102">SYNOPSIS</span></span>
<span data-ttu-id="3c232-103">Egy helyszíni számítógépről egy VHD-fájlt tölt fel egy felhőalapú tárterület-fiókba az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="3c232-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="3c232-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c232-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3c232-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c232-105">DESCRIPTION</span></span>
<span data-ttu-id="3c232-106">Az **Add-AzureVhd** parancsmag a helyszíni virtuális merevlemez-(VHD-) képeken rögzített. vhd képként</span><span class="sxs-lookup"><span data-stu-id="3c232-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="3c232-107">A feltöltési folyamat konfigurálására szolgáló paramétereket tartalmaz, például megadhatja a feltöltött szálak számát, vagy felülírhatja azokat a blobokat, amelyek már megtalálható a megadott cél URI-ban.</span><span class="sxs-lookup"><span data-stu-id="3c232-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="3c232-108">A helyszíni VHD-képek esetében a javítás is támogatott, így a már feltöltött alapképek feltöltése nélkül is feltölthetők a diff-lemezképek.</span><span class="sxs-lookup"><span data-stu-id="3c232-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="3c232-109">A megosztott hozzáférés-aláírás (SAS) URI-ja is támogatott.</span><span class="sxs-lookup"><span data-stu-id="3c232-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="3c232-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c232-110">EXAMPLES</span></span>

### <span data-ttu-id="3c232-111">1. példa: VHD-fájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="3c232-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="3c232-112">Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="3c232-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="3c232-113">2. példa: a VHD-fájl hozzáadása és a cél felülírása</span><span class="sxs-lookup"><span data-stu-id="3c232-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="3c232-114">Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="3c232-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="3c232-115">3. példa: adjon hozzá egy VHD-fájlt, és adja meg a szálak számát</span><span class="sxs-lookup"><span data-stu-id="3c232-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="3c232-116">Ez a parancs a. vhd fájlt felveszi a tárolási fiókba, és megadja a fájlok feltöltéséhez használható szálak számát.</span><span class="sxs-lookup"><span data-stu-id="3c232-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="3c232-117">4. példa: a VHD-fájl hozzáadása és a SAS-URI megadása</span><span class="sxs-lookup"><span data-stu-id="3c232-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="3c232-118">Ez a parancs a. vhd fájlt felveszi egy tárterület-fiókba, és a SAS-URI azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c232-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="3c232-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c232-119">PARAMETERS</span></span>

### <span data-ttu-id="3c232-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="3c232-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="3c232-121">Egy URI-azonosítót ad meg az Azure Blob-tárolóban lévő lemezképfájlok számára.</span><span class="sxs-lookup"><span data-stu-id="3c232-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="3c232-122">A SAS az URI-bevitelben is támogatott.</span><span class="sxs-lookup"><span data-stu-id="3c232-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c232-123">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="3c232-123">-Destination</span></span>
<span data-ttu-id="3c232-124">A Microsoft Azure Blob-tárolóban lévő blob-AZONOSÍTÓkat adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c232-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="3c232-125">Az URI-bevitel támogatja a SAS-t.</span><span class="sxs-lookup"><span data-stu-id="3c232-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="3c232-126">A javítás során azonban a cél nem lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="3c232-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c232-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3c232-127">-InformationAction</span></span>
<span data-ttu-id="3c232-128">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="3c232-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3c232-129">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="3c232-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c232-130">Folytassa</span><span class="sxs-lookup"><span data-stu-id="3c232-130">Continue</span></span>
- <span data-ttu-id="3c232-131">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="3c232-131">Ignore</span></span>
- <span data-ttu-id="3c232-132">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="3c232-132">Inquire</span></span>
- <span data-ttu-id="3c232-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3c232-133">SilentlyContinue</span></span>
- <span data-ttu-id="3c232-134">állj</span><span class="sxs-lookup"><span data-stu-id="3c232-134">Stop</span></span>
- <span data-ttu-id="3c232-135">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="3c232-135">Suspend</span></span>

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

### <span data-ttu-id="3c232-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3c232-136">-InformationVariable</span></span>
<span data-ttu-id="3c232-137">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="3c232-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3c232-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="3c232-138">-LocalFilePath</span></span>
<span data-ttu-id="3c232-139">Faj: a helyi. vhd fájl fájlelérési útja.</span><span class="sxs-lookup"><span data-stu-id="3c232-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c232-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="3c232-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="3c232-141">A feltöltéshez használni kívánt szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c232-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c232-142">-Átír</span><span class="sxs-lookup"><span data-stu-id="3c232-142">-OverWrite</span></span>
<span data-ttu-id="3c232-143">Azt adja meg, hogy a parancsmag a megadott cél URI-ban törli a meglévő blobot (ha létezik).</span><span class="sxs-lookup"><span data-stu-id="3c232-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="3c232-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c232-144">-Profile</span></span>
<span data-ttu-id="3c232-145">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3c232-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c232-146">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3c232-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c232-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c232-147">CommonParameters</span></span>
<span data-ttu-id="3c232-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c232-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c232-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c232-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c232-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c232-150">INPUTS</span></span>

## <span data-ttu-id="3c232-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c232-151">OUTPUTS</span></span>

## <span data-ttu-id="3c232-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c232-152">NOTES</span></span>

## <span data-ttu-id="3c232-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c232-153">RELATED LINKS</span></span>

[<span data-ttu-id="3c232-154">Mentés-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="3c232-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


