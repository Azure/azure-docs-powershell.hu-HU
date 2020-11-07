---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: 28d38fd88bada5b1c73557ea0d85bacf8ab2b6c0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844725"
---
# <span data-ttu-id="8266a-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="8266a-101">Add-AzVhd</span></span>

## <span data-ttu-id="8266a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8266a-102">SYNOPSIS</span></span>
<span data-ttu-id="8266a-103">Virtuális merevlemezt tölt fel egy helyszíni virtuális gépről egy blobra egy felhőalapú tároló fiókban az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="8266a-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="8266a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8266a-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8266a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8266a-105">DESCRIPTION</span></span>
<span data-ttu-id="8266a-106">A **Add-AzVhd** parancsmag a helyszíni virtuális merevlemezek,. vhd fájlformátumban rögzített virtuális merevlemezként való feltöltését adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="8266a-107">Beállíthatja, hogy hány feltöltött hozzászólásláncot fog használni a program, vagy felülírja a meglévő blobot a megadott cél URI-azonosítóban.</span><span class="sxs-lookup"><span data-stu-id="8266a-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="8266a-108">Szintén támogatott: a helyszíni. vhd fájlok foltos verziójának feltöltésére szolgáló lehetőség.</span><span class="sxs-lookup"><span data-stu-id="8266a-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="8266a-109">Ha már feltöltött egy virtuális virtuális merevlemezt, feltöltheti a különbséglemez-lemezeket, amelyek az alapképet használják szülőként.</span><span class="sxs-lookup"><span data-stu-id="8266a-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="8266a-110">A megosztott hozzáférés-aláírások (SAS) is támogatottak.</span><span class="sxs-lookup"><span data-stu-id="8266a-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="8266a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8266a-111">EXAMPLES</span></span>

### <span data-ttu-id="8266a-112">1. példa: VHD-fájl hozzáadása</span><span class="sxs-lookup"><span data-stu-id="8266a-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="8266a-113">Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="8266a-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="8266a-114">2. példa: a VHD-fájl hozzáadása és a cél felülírása</span><span class="sxs-lookup"><span data-stu-id="8266a-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="8266a-115">Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="8266a-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="8266a-116">A parancs felülír egy meglévő fájlt.</span><span class="sxs-lookup"><span data-stu-id="8266a-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="8266a-117">3. példa: adjon hozzá egy VHD-fájlt, és adja meg a szálak számát</span><span class="sxs-lookup"><span data-stu-id="8266a-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="8266a-118">Ez a parancs a. vhd fájlt felveszi a tárterület-fiókba.</span><span class="sxs-lookup"><span data-stu-id="8266a-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="8266a-119">A parancs a fájl feltöltéséhez használható szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="8266a-120">4. példa: a VHD-fájl hozzáadása és a SAS-URI megadása</span><span class="sxs-lookup"><span data-stu-id="8266a-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="8266a-121">Ez a parancs a. vhd fájlt felveszi egy tárterület-fiókba, és a SAS-URI azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="8266a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8266a-122">PARAMETERS</span></span>

### <span data-ttu-id="8266a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8266a-123">-AsJob</span></span>
<span data-ttu-id="8266a-124">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="8266a-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8266a-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="8266a-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="8266a-126">Annak az URI-azonosítónak az URI-ja, amely az Azure Blob-tárolóban található.</span><span class="sxs-lookup"><span data-stu-id="8266a-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="8266a-127">A SAS a paraméter értékeként adható meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-127">An SAS can be specified as the value for this parameter.</span></span>

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

### <span data-ttu-id="8266a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8266a-128">-DefaultProfile</span></span>
<span data-ttu-id="8266a-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8266a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8266a-130">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="8266a-130">-Destination</span></span>
<span data-ttu-id="8266a-131">A blob-tárolóban lévő blob URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="8266a-132">A paraméter támogatja a SAS-URI-t, de a kijavítási forgatókönyvek a cél nem lehet SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="8266a-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

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

### <span data-ttu-id="8266a-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="8266a-133">-LocalFilePath</span></span>
<span data-ttu-id="8266a-134">A helyi. vhd fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-134">Specifies the path of the local .vhd file.</span></span>

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

### <span data-ttu-id="8266a-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="8266a-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="8266a-136">A. vhd fájl feltöltésekor használandó feltöltött szálak számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

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

### <span data-ttu-id="8266a-137">-Átír</span><span class="sxs-lookup"><span data-stu-id="8266a-137">-OverWrite</span></span>
<span data-ttu-id="8266a-138">Azt jelzi, hogy ez a parancsmag felülírja a megadott cél URI-ban egy meglévő blobot, ha van ilyen.</span><span class="sxs-lookup"><span data-stu-id="8266a-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

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

### <span data-ttu-id="8266a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8266a-139">-ResourceGroupName</span></span>
<span data-ttu-id="8266a-140">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8266a-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8266a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8266a-141">CommonParameters</span></span>
<span data-ttu-id="8266a-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8266a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8266a-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8266a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8266a-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8266a-144">INPUTS</span></span>

### <span data-ttu-id="8266a-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="8266a-145">None</span></span>
<span data-ttu-id="8266a-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="8266a-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8266a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8266a-147">OUTPUTS</span></span>

### <span data-ttu-id="8266a-148">Microsoft. Azure. commands. kiszámítás. models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="8266a-148">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="8266a-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8266a-149">NOTES</span></span>

## <span data-ttu-id="8266a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8266a-150">RELATED LINKS</span></span>

[<span data-ttu-id="8266a-151">Mentés-AzVhd</span><span class="sxs-lookup"><span data-stu-id="8266a-151">Save-AzVhd</span></span>](./Save-AzVhd.md)


