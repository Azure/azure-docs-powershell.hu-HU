---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467081"
---
# <span data-ttu-id="6e87c-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="6e87c-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="6e87c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e87c-102">SYNOPSIS</span></span>
<span data-ttu-id="6e87c-103">Egyszerű Structured Query Language (SQL) utasítást alkalmaz egy blob tartalmára, és az adatoknak csak a lekérdezett részkészletét menti egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="6e87c-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="6e87c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e87c-104">SYNTAX</span></span>

### <span data-ttu-id="6e87c-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e87c-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e87c-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6e87c-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e87c-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6e87c-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e87c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e87c-108">DESCRIPTION</span></span>
<span data-ttu-id="6e87c-109">A **Get-AzStorageBlobQueryResult** parancsmag egy egyszerű Structured Query Language (SQL) utasítást alkalmaz egy blob tartalmára, és az adatok lekérdezett alkészletét helyi fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="6e87c-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="6e87c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e87c-110">EXAMPLES</span></span>

### <span data-ttu-id="6e87c-111">1. példa: Blob lekérdezése</span><span class="sxs-lookup"><span data-stu-id="6e87c-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="6e87c-112">Ez a parancs sikeresen lekérdez egy blobot CSV-fájlként megadott bemeneti és kimeneti konfigurációval jsonként, és a kimenetet a helyi fájlba "c:\resultfile.jsbe" fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="6e87c-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="6e87c-113">2. példa: Blob-pillanatfelvétel lekérdezése</span><span class="sxs-lookup"><span data-stu-id="6e87c-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="6e87c-114">Ez a parancs először blobobjektumot kap a blob-pillanatfelvételhez, majd lekérdezi a blob-pillanatfelvételt, és az eredményt lekérdezési hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="6e87c-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="6e87c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e87c-115">PARAMETERS</span></span>

### <span data-ttu-id="6e87c-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="6e87c-116">-Blob</span></span>
<span data-ttu-id="6e87c-117">Blob neve</span><span class="sxs-lookup"><span data-stu-id="6e87c-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6e87c-118">-BlobBaseClient</span></span>
<span data-ttu-id="6e87c-119">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="6e87c-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="6e87c-120">-BlobContainerClient</span></span>
<span data-ttu-id="6e87c-121">BlobContainerClient objektum</span><span class="sxs-lookup"><span data-stu-id="6e87c-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e87c-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e87c-123">Az ügyféloldali maximális végrehajtási idő másodpercben az egyes kérések esetén.</span><span class="sxs-lookup"><span data-stu-id="6e87c-123">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e87c-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e87c-125">Az egyidejű aszinkron feladatok teljes mennyisége.</span><span class="sxs-lookup"><span data-stu-id="6e87c-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="6e87c-126">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="6e87c-126">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-127">-Container</span><span class="sxs-lookup"><span data-stu-id="6e87c-127">-Container</span></span>
<span data-ttu-id="6e87c-128">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="6e87c-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6e87c-129">-Context</span></span>
<span data-ttu-id="6e87c-130">Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="6e87c-130">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e87c-131">-DefaultProfile</span></span>
<span data-ttu-id="6e87c-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e87c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-133">-Force</span><span class="sxs-lookup"><span data-stu-id="6e87c-133">-Force</span></span>
<span data-ttu-id="6e87c-134">Kényszerítsen a meglévő fájl felülírásán.</span><span class="sxs-lookup"><span data-stu-id="6e87c-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="6e87c-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e87c-135">-InputTextConfiguration</span></span>
<span data-ttu-id="6e87c-136">A lekérdezés beviteli szövegének kezeléséhez használt konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="6e87c-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="6e87c-137">Hozza létre a konfigurációs objektumot a New-AzStorageBlobQueryConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="6e87c-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="6e87c-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="6e87c-139">A lekérdezés kimeneti szövegének kezeléséhez használt konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="6e87c-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="6e87c-140">Hozza létre a konfigurációs objektumot a New-AzStorageBlobQueryConfig segítségével.</span><span class="sxs-lookup"><span data-stu-id="6e87c-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e87c-141">-PassThru</span></span>
<span data-ttu-id="6e87c-142">Adja vissza, hogy a megadott bloblekérdezés sikeres-e.</span><span class="sxs-lookup"><span data-stu-id="6e87c-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="6e87c-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="6e87c-143">-QueryString</span></span>
<span data-ttu-id="6e87c-144">Lekérdezési karakterlánc, további részletek: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="6e87c-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="6e87c-145">-ResultFile</span></span>
<span data-ttu-id="6e87c-146">A lekérdezés eredményének mentéséhez használható helyi fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="6e87c-146">Local file path to save the query result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e87c-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e87c-148">A kiszolgáló másodpercek alatt időkorrektaidőt ad az egyes kérések számára.</span><span class="sxs-lookup"><span data-stu-id="6e87c-148">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6e87c-149">-SnapshotTime</span></span>
<span data-ttu-id="6e87c-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6e87c-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="6e87c-151">-VersionId</span></span>
<span data-ttu-id="6e87c-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="6e87c-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e87c-153">-Confirm</span></span>
<span data-ttu-id="6e87c-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6e87c-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e87c-155">-WhatIf</span></span>
<span data-ttu-id="6e87c-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6e87c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e87c-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6e87c-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e87c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e87c-158">CommonParameters</span></span>
<span data-ttu-id="6e87c-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e87c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e87c-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e87c-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e87c-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e87c-161">INPUTS</span></span>

### <span data-ttu-id="6e87c-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6e87c-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="6e87c-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="6e87c-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="6e87c-164">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e87c-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e87c-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e87c-165">OUTPUTS</span></span>

### <span data-ttu-id="6e87c-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e87c-166">System.Boolean</span></span>

## <span data-ttu-id="6e87c-167">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e87c-167">NOTES</span></span>

## <span data-ttu-id="6e87c-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e87c-168">RELATED LINKS</span></span>
