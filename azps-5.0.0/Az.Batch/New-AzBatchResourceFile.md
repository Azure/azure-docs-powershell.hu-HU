---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188134"
---
# <span data-ttu-id="5a5d3-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="5a5d3-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="5a5d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5d3-103">Létrehoz egy erőforrást a felhasználáshoz `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="5a5d3-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="5a5d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a5d3-104">SYNTAX</span></span>

### <span data-ttu-id="5a5d3-105">HttpUrl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a5d3-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a5d3-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="5a5d3-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a5d3-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5a5d3-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a5d3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a5d3-108">DESCRIPTION</span></span>
<span data-ttu-id="5a5d3-109">Létrehoz egy erőforrást a felhasználáshoz `New-AzBatchTask` .</span><span class="sxs-lookup"><span data-stu-id="5a5d3-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="5a5d3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5a5d3-110">EXAMPLES</span></span>

### <span data-ttu-id="5a5d3-111">Példa 1: erőforrásfájl létrehozása egy, a HTTP URL-címéről egyetlen fájlra mutatva</span><span class="sxs-lookup"><span data-stu-id="5a5d3-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5a5d3-112">`PSResourceFile`Http-URL-címre hivatkozó hivatkozás létrehozása</span><span class="sxs-lookup"><span data-stu-id="5a5d3-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="5a5d3-113">2. példa: erőforrásfájl létrehozása Azure Storage Container URL-címről</span><span class="sxs-lookup"><span data-stu-id="5a5d3-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5a5d3-114">`PSResourceFile`Az Azure Storage Container URL-jének hivatkozását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="5a5d3-115">A program a tárolóban lévő összes fájlt letölti a megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="5a5d3-116">3. példa: erőforrásfájl létrehozása automatikus tárterület-tároló nevében</span><span class="sxs-lookup"><span data-stu-id="5a5d3-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="5a5d3-117">Létrehozza `PSResourceFile` az automatikus tárterület-tároló neve hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="5a5d3-118">A program a tárolóban lévő összes fájlt letölti a megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="5a5d3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a5d3-119">PARAMETERS</span></span>

### <span data-ttu-id="5a5d3-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="5a5d3-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="5a5d3-121">A tároló tároló neve az automatikus tárterület-fiókban.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-121">The storage container name in the auto storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: AutoStorageContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="5a5d3-122">-BlobPrefix</span></span>
<span data-ttu-id="5a5d3-123">Az Azure-tárterületről való letöltéskor használandó blob-előtagot kapja.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="5a5d3-124">A program csak azokat a festékfoltok-t tölti le, amelyek nevei a megadott előtaggal kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="5a5d3-125">Ez az előtag lehet részleges fájlnév vagy alkönyvtár.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="5a5d3-126">Ha nem adja meg az előtagot, a program a tárolóban lévő összes fájlt letölti.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5d3-127">-DefaultProfile</span></span>
<span data-ttu-id="5a5d3-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a5d3-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="5a5d3-129">-FileMode</span></span>
<span data-ttu-id="5a5d3-130">A fájl jogosultsági mód attribútumát oktális formátumban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="5a5d3-131">Ez a tulajdonság csak akkor érvényes, ha az erőforrást egy Linux-csomópontra tölti le.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="5a5d3-132">Ha a tulajdonság nem egy Linux-csomóponthoz van megadva, az alapértelmezett érték az 0770.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5a5d3-133">-FilePath</span></span>
<span data-ttu-id="5a5d3-134">A számítási csomópont azon helye, amelyre a fájl (ok) letöltése a tevékenység munkakönyvtárához viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="5a5d3-135">Ha a HttpUrl paramétert adja meg, a FilePath szükséges, és leírja, hogy a fájl milyen elérési utat fog letölteni, például a fájlnevet.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="5a5d3-136">Ellenkező esetben, ha a AutoStorageContainerName vagy a StorageContainerUrl paraméter van megadva, a FilePath nem kötelező, és a címtár a fájlok letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="5a5d3-137">Abban az esetben, ha a FilePath címtárként használja, a bemeneti adatokhoz társított bármely címtár-szerkezet teljes egészében megmarad, és a program hozzáfűzi a megadott FilePath-könyvtárhoz.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="5a5d3-138">A megadott relatív elérési út nem szünteti meg a tevékenység munkakönyvtárát (például: "...").</span><span class="sxs-lookup"><span data-stu-id="5a5d3-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl, AutoStorageContainerName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="5a5d3-139">-HttpUrl</span></span>
<span data-ttu-id="5a5d3-140">A letöltendő fájl URL-címe.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-140">The URL of the file to download.</span></span>
<span data-ttu-id="5a5d3-141">Ha az URL-cím az Azure Blob-tároló, akkor a névtelen hozzáférés szolgáltatással olvashatónak kell lennie; vagyis a köteg szolgáltatás nem jelent meg hitelesítő adatokat a blob letöltésekor.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="5a5d3-142">Az Azure Storage szolgáltatásban kétféleképpen lehet egy blob-URL-címet beolvasni: az olvasási engedélyeket biztosító megosztott hozzáférés-aláírás (SAS), illetve a blob vagy a tárolója HOZZÁFÉRÉSének beállítása a nyilvános hozzáférés engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: HttpUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="5a5d3-143">-StorageContainerUrl</span></span>
<span data-ttu-id="5a5d3-144">A blob-tároló URL-címe az Azure Blob-tárterületen belül.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="5a5d3-145">Ennek az URL-címnek olvashatónak és olvashatónak kell lennie a névtelen hozzáférés használatával; vagyis a köteg szolgáltatás nem jelent meg hitelesítő adatokat a tárolóból való letöltéskor.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="5a5d3-146">Az Azure-tárterületen lévő tárolók esetében kétféle módon lehet URL-t beolvasni: egy megosztott hozzáférés-aláírást (SAS) kell megadni, amely olvasási engedélyeket ad a tárolónak, vagy a tároló hozzáférés-vezérlési listáját a nyilvános hozzáférés engedélyezéséhez adja meg.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageContainerUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a5d3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5d3-147">CommonParameters</span></span>
<span data-ttu-id="5a5d3-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a5d3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5d3-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a5d3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5d3-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a5d3-150">INPUTS</span></span>

### <span data-ttu-id="5a5d3-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="5a5d3-151">None</span></span>

## <span data-ttu-id="5a5d3-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a5d3-152">OUTPUTS</span></span>

### <span data-ttu-id="5a5d3-153">Microsoft.Azure.Commands.BatCH. Modellek. PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="5a5d3-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="5a5d3-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a5d3-154">NOTES</span></span>

## <span data-ttu-id="5a5d3-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a5d3-155">RELATED LINKS</span></span>

[<span data-ttu-id="5a5d3-156">Új – AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5a5d3-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)