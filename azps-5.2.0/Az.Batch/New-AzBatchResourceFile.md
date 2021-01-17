---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchresourcefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchResourceFile.md
ms.openlocfilehash: 43cbf86ca473b6984ee2190b1d10df61b6d32e64
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361324"
---
# <span data-ttu-id="57ebd-101">New-AzBatchResourceFile</span><span class="sxs-lookup"><span data-stu-id="57ebd-101">New-AzBatchResourceFile</span></span>

## <span data-ttu-id="57ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="57ebd-103">Létrehozza az erőforrásfájlt `New-AzBatchTask` használatra.</span><span class="sxs-lookup"><span data-stu-id="57ebd-103">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="57ebd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57ebd-104">SYNTAX</span></span>

### <span data-ttu-id="57ebd-105">HttpUrl (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57ebd-105">HttpUrl (Default)</span></span>
```
New-AzBatchResourceFile -HttpUrl <String> -FilePath <String> [-FileMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ebd-106">StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="57ebd-106">StorageContainerUrl</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] [-BlobPrefix <String>]
 -StorageContainerUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ebd-107">AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="57ebd-107">AutoStorageContainerName</span></span>
```
New-AzBatchResourceFile [-FilePath <String>] [-FileMode <String>] -AutoStorageContainerName <String>
 [-BlobPrefix <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ebd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57ebd-108">DESCRIPTION</span></span>
<span data-ttu-id="57ebd-109">Létrehozza az erőforrásfájlt `New-AzBatchTask` használatra.</span><span class="sxs-lookup"><span data-stu-id="57ebd-109">Creates a Resource File for usage by `New-AzBatchTask`.</span></span>

## <span data-ttu-id="57ebd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="57ebd-111">1. példa: Erőforrásfájl létrehozása egyetlen fájlra mutató HTTP URL-címből</span><span class="sxs-lookup"><span data-stu-id="57ebd-111">Example 1: Create a resource file from an HTTP URL pointing at a single file</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -HttpUrl "https://testacct.blob.core.windows.net/" -FilePath "file1"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="57ebd-112">`PSResourceFile`HTTP-URL-címre hivatkozó url-címet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="57ebd-112">Creates a `PSResourceFile` referencing an HTTP url.</span></span>

### <span data-ttu-id="57ebd-113">2. példa: Erőforrásfájl létrehozása Egy Azure Storage tároló URL-címében</span><span class="sxs-lookup"><span data-stu-id="57ebd-113">Example 2: Create a resource file from an Azure Storage container URL</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -StorageContainerUrl "https://testacct.blob.core.windows.net/mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="57ebd-114">Létrehoz egy, az Azure Storage tároló `PSResourceFile` URL-címére hivatkozó címet.</span><span class="sxs-lookup"><span data-stu-id="57ebd-114">Creates a `PSResourceFile` referencing an Azure Storage container URL.</span></span> <span data-ttu-id="57ebd-115">A rendszer a tárolóban lévő összes fájlt letölti a megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="57ebd-115">All files in the container will be downloaded to the specified folder.</span></span>

### <span data-ttu-id="57ebd-116">3. példa: Erőforrásfájl létrehozása automatikus tárolónévből</span><span class="sxs-lookup"><span data-stu-id="57ebd-116">Example 3: Create a resource file from an Auto Storage container name</span></span>
```
PS C:\> $file = New-AzBatchResourceFile -AutoStorageContainerName "mycontainer" -FilePath "myfolder"
PS C:\> New-AzBatchTask -JobId "Job-000001" -Id "Task23" -CommandLine "cmd /c dir /s" -ResourceFiles $file -BatchContext $Context
```

<span data-ttu-id="57ebd-117">Létrehoz `PSResourceFile` egy, az Automatikus tároló tároló nevére hivatkozó nevet.</span><span class="sxs-lookup"><span data-stu-id="57ebd-117">Creates a `PSResourceFile` referencing an Auto Storage container name.</span></span> <span data-ttu-id="57ebd-118">A rendszer a tárolóban lévő összes fájlt letölti a megadott mappába.</span><span class="sxs-lookup"><span data-stu-id="57ebd-118">All files in the container will be downloaded to the specified folder.</span></span>

## <span data-ttu-id="57ebd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57ebd-119">PARAMETERS</span></span>

### <span data-ttu-id="57ebd-120">-AutoStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="57ebd-120">-AutoStorageContainerName</span></span>
<span data-ttu-id="57ebd-121">A tároló neve az automatikus tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="57ebd-121">The storage container name in the auto storage account.</span></span>

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

### <span data-ttu-id="57ebd-122">-BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="57ebd-122">-BlobPrefix</span></span>
<span data-ttu-id="57ebd-123">A blobelőtagot használja, amikor blobokat tölt le egy Azure Storage-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="57ebd-123">Gets the blob prefix to use when downloading blobs from an Azure Storage container.</span></span>
<span data-ttu-id="57ebd-124">Csak azok a blobok tölthetők le, amelyeknek a neve a megadott előtaggal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="57ebd-124">Only the blobs whose names begin with the specified prefix will be downloaded.</span></span>
<span data-ttu-id="57ebd-125">Ez az előtag lehet egy részleges fájlnév vagy egy alkönyvtár.</span><span class="sxs-lookup"><span data-stu-id="57ebd-125">This prefix can be a partial filename or a subdirectory.</span></span>
<span data-ttu-id="57ebd-126">Ha nincs megadva előtag, a rendszer a tárolóban lévő összes fájlt letölti.</span><span class="sxs-lookup"><span data-stu-id="57ebd-126">If a prefix is not specified, all the files in the container will be downloaded.</span></span>

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

### <span data-ttu-id="57ebd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ebd-127">-DefaultProfile</span></span>
<span data-ttu-id="57ebd-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57ebd-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ebd-129">-FileMode</span><span class="sxs-lookup"><span data-stu-id="57ebd-129">-FileMode</span></span>
<span data-ttu-id="57ebd-130">A fájlengedélyek módjának attribútumát oktális formátumban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57ebd-130">Gets the file permission mode attribute in octal format.</span></span>
<span data-ttu-id="57ebd-131">Ez a tulajdonság csak akkor érvényes, ha az erőforrásfájl egy Linux-csomópontra van letöltve.</span><span class="sxs-lookup"><span data-stu-id="57ebd-131">This property is applicable only if the resource file is downloaded to a Linux node.</span></span>
<span data-ttu-id="57ebd-132">Ha ez a tulajdonság nincs megadva egy Linux-csomóponthoz, akkor az alapértelmezett érték 0770.</span><span class="sxs-lookup"><span data-stu-id="57ebd-132">If this property is not specified for a Linux node, then the default value is 0770.</span></span>

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

### <span data-ttu-id="57ebd-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="57ebd-133">-FilePath</span></span>
<span data-ttu-id="57ebd-134">A számítási csomópontnak az a helye, amelyre le szeretné tölteni a fájlt(a) a feladat munkakönyvtárához képest.</span><span class="sxs-lookup"><span data-stu-id="57ebd-134">The location on the compute node to which to download the file(s), relative to the task's working directory.</span></span> <span data-ttu-id="57ebd-135">Ha a HttpUrl paraméter meg van adva, a FilePath paraméter megadása kötelező, és ismerteti a fájl letöltési elérési útját, a fájlnévvel együtt.</span><span class="sxs-lookup"><span data-stu-id="57ebd-135">If the HttpUrl parameter is specified, the FilePath is required and describes the path which the file will be downloaded to, including the filename.</span></span> <span data-ttu-id="57ebd-136">Ellenkező esetben, ha az AutoStorageContainerName vagy a StorageContainerUrl paraméter meg van adva, a FilePath megadása nem kötelező, és az a könyvtár, amelybe le kell töltenie a fájlokat.</span><span class="sxs-lookup"><span data-stu-id="57ebd-136">Otherwise, if the AutoStorageContainerName or StorageContainerUrl parameters are specified, FilePath is optional and is the directory to download the files to.</span></span> <span data-ttu-id="57ebd-137">Abban az esetben, ha a FilePath címtárként van használva, a bemeneti adatokhoz társított esetleges címtárszerkezetek teljes egészében megmaradnak, és a megadott FilePath-címtárhoz lesznek hozzáfűzve.</span><span class="sxs-lookup"><span data-stu-id="57ebd-137">In the case where FilePath is used as a directory, any directory structure already associated with the input data will be retained in full and appended to the specified FilePath directory.</span></span> <span data-ttu-id="57ebd-138">A megadott relatív útvonal nem tud kijönni a tevékenység munkakönyvtárból (például a ".." használatával).</span><span class="sxs-lookup"><span data-stu-id="57ebd-138">The specified relative path cannot break out of the task's working directory (for example by using '..').</span></span>

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

### <span data-ttu-id="57ebd-139">-HttpUrl</span><span class="sxs-lookup"><span data-stu-id="57ebd-139">-HttpUrl</span></span>
<span data-ttu-id="57ebd-140">A letölteni kívánt fájl URL-címe.</span><span class="sxs-lookup"><span data-stu-id="57ebd-140">The URL of the file to download.</span></span>
<span data-ttu-id="57ebd-141">Ha az URL-cím Azure Blob Storage, névtelen hozzáféréssel is olvashatónak kell lennie; ez azt jelenti, hogy a Batch szolgáltatás nem ad meg hitelesítő adatokat a blob letöltésekor.</span><span class="sxs-lookup"><span data-stu-id="57ebd-141">If the URL is Azure Blob Storage, it must be readable using anonymous access; that is, the Batch service does not present any credentials when downloading the blob.</span></span>
<span data-ttu-id="57ebd-142">Az Azure-tárban lévő blobok URL-címét kétféleképpen lehet lekövetni: használjon olyan megosztott hozzáférés-aláírást (SAS), amely olvasási engedélyeket ad a blobhoz, vagy állítsa be a blob vagy tároló ACL-jét a nyilvános hozzáférés engedélyezése érdekében.</span><span class="sxs-lookup"><span data-stu-id="57ebd-142">There are two ways to get such a URL for a blob in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the blob, or set the ACL for the blob or its container to allow public access.</span></span>

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

### <span data-ttu-id="57ebd-143">-StorageContainerUrl</span><span class="sxs-lookup"><span data-stu-id="57ebd-143">-StorageContainerUrl</span></span>
<span data-ttu-id="57ebd-144">A blobtároló URL-címe az Azure Blob Storage-ban.</span><span class="sxs-lookup"><span data-stu-id="57ebd-144">The URL of the blob container within Azure Blob Storage.</span></span>
<span data-ttu-id="57ebd-145">Ennek az URL-címnek olvashatónak és listolhatónak kell lennie névtelen hozzáféréssel; azaz a Batch szolgáltatás nem ad meg hitelesítő adatokat, amikor blobokat tölt le a tárolóból.</span><span class="sxs-lookup"><span data-stu-id="57ebd-145">This URL must be readable and listable using anonymous access; that is, the Batch service does not present any credentials when downloading blobs from the container.</span></span>
<span data-ttu-id="57ebd-146">Kétféleképpen állíthat be ilyen URL-címet egy Azure-tárban található tárolóhoz: egy olyan MEGOSZTOTT hozzáférés-aláírást (SAS), amely olvasási engedélyeket ad a tárolóhoz, vagy úgy állíthatja be a tároló ACL-jét, hogy engedélyezze a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="57ebd-146">There are two ways to get such a URL for a container in Azure storage: include a Shared Access Signature (SAS) granting read permissions on the container, or set the ACL for the container to allow public access.</span></span>

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

### <span data-ttu-id="57ebd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ebd-147">CommonParameters</span></span>
<span data-ttu-id="57ebd-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ebd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ebd-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ebd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ebd-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57ebd-150">INPUTS</span></span>

### <span data-ttu-id="57ebd-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="57ebd-151">None</span></span>

## <span data-ttu-id="57ebd-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57ebd-152">OUTPUTS</span></span>

### <span data-ttu-id="57ebd-153">Microsoft.Azure.Commands.Bat. Models.PSResourceFile</span><span class="sxs-lookup"><span data-stu-id="57ebd-153">Microsoft.Azure.Commands.Batch.Models.PSResourceFile</span></span>

## <span data-ttu-id="57ebd-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57ebd-154">NOTES</span></span>

## <span data-ttu-id="57ebd-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57ebd-155">RELATED LINKS</span></span>

[<span data-ttu-id="57ebd-156">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="57ebd-156">New-AzBatchTask</span></span>](./New-AzBatchTask.md)