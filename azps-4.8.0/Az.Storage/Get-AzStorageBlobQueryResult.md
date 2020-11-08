---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: fbb1c8e4e2a5421ea7714a0d7a82b1f1cc2567f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017530"
---
# <span data-ttu-id="c3c98-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="c3c98-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="c3c98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c3c98-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c98-103">Egy egyszerű strukturált lekérdezési nyelv (SQL) utasítását alkalmazza egy blob-tartalomra, és csak az adatok lekérdezett részhalmazát menti egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="c3c98-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="c3c98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c3c98-104">SYNTAX</span></span>

### <span data-ttu-id="c3c98-105">NamePipeline (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3c98-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3c98-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="c3c98-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3c98-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="c3c98-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c3c98-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c3c98-108">DESCRIPTION</span></span>
<span data-ttu-id="c3c98-109">A **Get-AzStorageBlobQueryResult** parancsmag egy egyszerű strukturált lekérdezési nyelv (SQL) utasítását alkalmazza egy blob tartalmára, és menti az adatok lekérdezett részhalmazát egy helyi fájlba.</span><span class="sxs-lookup"><span data-stu-id="c3c98-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="c3c98-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c3c98-110">EXAMPLES</span></span>

### <span data-ttu-id="c3c98-111">Példa 1: blob lekérdezése</span><span class="sxs-lookup"><span data-stu-id="c3c98-111">Example 1: Query a blob</span></span>
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

<span data-ttu-id="c3c98-112">Ez a parancs a blob-succsssfully CSV-fájlként, a kimeneti konfigurációt pedig JSON-ként, a kimenetet pedig helyi fájlként menti "c:\resultfile.jsbe" értékre.</span><span class="sxs-lookup"><span data-stu-id="c3c98-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="c3c98-113">2. példa: blob-pillanatfelvétel lekérdezése</span><span class="sxs-lookup"><span data-stu-id="c3c98-113">Example 2: Query a blob snapshot</span></span>
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

<span data-ttu-id="c3c98-114">Ez a parancs először a blob-pillanatfelvételhez kap egy blob-objektumot, majd lekérdezi a blob-pillanatfelvételt, és megjeleníti az eredmény lekérdezési hibáját.</span><span class="sxs-lookup"><span data-stu-id="c3c98-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="c3c98-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c3c98-115">PARAMETERS</span></span>

### <span data-ttu-id="c3c98-116">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c3c98-116">-Blob</span></span>
<span data-ttu-id="c3c98-117">BLOB neve</span><span class="sxs-lookup"><span data-stu-id="c3c98-117">Blob name</span></span>

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

### <span data-ttu-id="c3c98-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c3c98-118">-BlobBaseClient</span></span>
<span data-ttu-id="c3c98-119">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="c3c98-119">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="c3c98-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="c3c98-120">-BlobContainerClient</span></span>
<span data-ttu-id="c3c98-121">BlobContainerClient objektum</span><span class="sxs-lookup"><span data-stu-id="c3c98-121">BlobContainerClient Object</span></span>

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

### <span data-ttu-id="c3c98-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c3c98-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c3c98-123">Az ügyféloldali kérelmek maximális végrehajtási ideje másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c3c98-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="c3c98-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c3c98-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c3c98-125">Az egyidejű aszinkron feladatok teljes összege.</span><span class="sxs-lookup"><span data-stu-id="c3c98-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="c3c98-126">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c3c98-126">The default value is 10.</span></span>

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

### <span data-ttu-id="c3c98-127">-Container</span><span class="sxs-lookup"><span data-stu-id="c3c98-127">-Container</span></span>
<span data-ttu-id="c3c98-128">Tároló neve</span><span class="sxs-lookup"><span data-stu-id="c3c98-128">Container name</span></span>

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

### <span data-ttu-id="c3c98-129">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c3c98-129">-Context</span></span>
<span data-ttu-id="c3c98-130">Azure Storage Context objektum</span><span class="sxs-lookup"><span data-stu-id="c3c98-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c3c98-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c98-131">-DefaultProfile</span></span>
<span data-ttu-id="c3c98-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3c98-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3c98-133">-Force</span><span class="sxs-lookup"><span data-stu-id="c3c98-133">-Force</span></span>
<span data-ttu-id="c3c98-134">Kényszeríti a meglévő fájl felülírását.</span><span class="sxs-lookup"><span data-stu-id="c3c98-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="c3c98-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c98-135">-InputTextConfiguration</span></span>
<span data-ttu-id="c3c98-136">A lekérdezés szövegbeviteli szövegének kezelését szolgáló konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="c3c98-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="c3c98-137">Konfigurációs objektum létrehozása a új AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="c3c98-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="c3c98-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3c98-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="c3c98-139">A lekérdezés kimeneti szövegének kezelését szolgáló konfiguráció.</span><span class="sxs-lookup"><span data-stu-id="c3c98-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="c3c98-140">Konfigurációs objektum létrehozása a új AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="c3c98-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

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

### <span data-ttu-id="c3c98-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3c98-141">-PassThru</span></span>
<span data-ttu-id="c3c98-142">A megadott blob sikeres lekérdezésének visszaadása.</span><span class="sxs-lookup"><span data-stu-id="c3c98-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="c3c98-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="c3c98-143">-QueryString</span></span>
<span data-ttu-id="c3c98-144">Lekérdezési karakterlánc, további információ: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="c3c98-144">Query string, see more details in: https://docs.microsoft.com/en-us/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="c3c98-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="c3c98-145">-ResultFile</span></span>
<span data-ttu-id="c3c98-146">Helyi fájlelérési út a lekérdezés eredményének mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="c3c98-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="c3c98-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c3c98-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c3c98-148">A kiszolgáló az egyes kérésekhez másodpercben megadott időpontot.</span><span class="sxs-lookup"><span data-stu-id="c3c98-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="c3c98-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c3c98-149">-SnapshotTime</span></span>
<span data-ttu-id="c3c98-150">BLOB SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c3c98-150">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="c3c98-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="c3c98-151">-VersionId</span></span>
<span data-ttu-id="c3c98-152">BLOB VersionId</span><span class="sxs-lookup"><span data-stu-id="c3c98-152">Blob VersionId</span></span>

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

### <span data-ttu-id="c3c98-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c3c98-153">-Confirm</span></span>
<span data-ttu-id="c3c98-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c3c98-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3c98-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3c98-155">-WhatIf</span></span>
<span data-ttu-id="c3c98-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c3c98-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3c98-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c3c98-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3c98-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c98-158">CommonParameters</span></span>
<span data-ttu-id="c3c98-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c3c98-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c98-160">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3c98-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c98-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c98-161">INPUTS</span></span>

### <span data-ttu-id="c3c98-162">Azure. Storage. Blobs. specializ. BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="c3c98-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="c3c98-163">Azure. Storage. Blobs. BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="c3c98-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="c3c98-164">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3c98-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c3c98-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3c98-165">OUTPUTS</span></span>

### <span data-ttu-id="c3c98-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3c98-166">System.Boolean</span></span>

## <span data-ttu-id="c3c98-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c3c98-167">NOTES</span></span>

## <span data-ttu-id="c3c98-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3c98-168">RELATED LINKS</span></span>
