---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937306"
---
# <span data-ttu-id="6b022-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6b022-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="6b022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b022-102">SYNOPSIS</span></span>
<span data-ttu-id="6b022-103">Blob másolása szinkron módon.</span><span class="sxs-lookup"><span data-stu-id="6b022-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="6b022-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6b022-104">SYNTAX</span></span>

### <span data-ttu-id="6b022-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b022-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b022-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="6b022-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b022-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="6b022-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b022-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6b022-108">DESCRIPTION</span></span>
<span data-ttu-id="6b022-109">A **Copy-AzStorageBlob** parancsmag szinkronizálva másol egy blobot, jelenleg csak a blokk blob támogatását támogatja.</span><span class="sxs-lookup"><span data-stu-id="6b022-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="6b022-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6b022-110">EXAMPLES</span></span>

### <span data-ttu-id="6b022-111">1. példa: Elnevezett blob másolása egy másikba</span><span class="sxs-lookup"><span data-stu-id="6b022-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6b022-112">Ez a parancs egy blobot másol a forrástárolóból egy új blobnévvel a céltárolóba.</span><span class="sxs-lookup"><span data-stu-id="6b022-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="6b022-113">2. példa: Blob másolása blobobjektumból</span><span class="sxs-lookup"><span data-stu-id="6b022-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6b022-114">Ez a parancs egy blobot másol a forrás blobobjektumból a céltárolóba egy új blobnévvel.</span><span class="sxs-lookup"><span data-stu-id="6b022-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="6b022-115">3. példa: Blob másolása blob Uri-ból</span><span class="sxs-lookup"><span data-stu-id="6b022-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6b022-116">Az első parancs létrehoz egy blob Uri-t a forrás blobból, "rt" jogosultsági jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="6b022-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="6b022-117">A második parancs a forrás blob Uri-ból a cél blobba másol.</span><span class="sxs-lookup"><span data-stu-id="6b022-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="6b022-118">4. példa: Blokk blobtitkosítási hatókör frissítése</span><span class="sxs-lookup"><span data-stu-id="6b022-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="6b022-119">Ez a parancs egy blokk blobtitkosítási hatókört frissít új titkosítási hatókörrel.</span><span class="sxs-lookup"><span data-stu-id="6b022-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="6b022-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b022-120">PARAMETERS</span></span>

### <span data-ttu-id="6b022-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6b022-121">-AbsoluteUri</span></span>
<span data-ttu-id="6b022-122">Source blob uri</span><span class="sxs-lookup"><span data-stu-id="6b022-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b022-123">-AsJob</span></span>
<span data-ttu-id="6b022-124">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6b022-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b022-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6b022-125">-BlobBaseClient</span></span>
<span data-ttu-id="6b022-126">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="6b022-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-127">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6b022-127">-Context</span></span>
<span data-ttu-id="6b022-128">Source Azure Storage Context Object</span><span class="sxs-lookup"><span data-stu-id="6b022-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b022-129">-DefaultProfile</span></span>
<span data-ttu-id="6b022-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6b022-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b022-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="6b022-131">-DestBlob</span></span>
<span data-ttu-id="6b022-132">Cél blobneve</span><span class="sxs-lookup"><span data-stu-id="6b022-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="6b022-133">-DestContainer</span></span>
<span data-ttu-id="6b022-134">Céltároló neve</span><span class="sxs-lookup"><span data-stu-id="6b022-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="6b022-135">-DestContext</span></span>
<span data-ttu-id="6b022-136">Destination Storage context object</span><span class="sxs-lookup"><span data-stu-id="6b022-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6b022-137">-EncryptionScope</span></span>
<span data-ttu-id="6b022-138">Titkosítási hatókör a dest blobra való kérelmek igénylésekor.</span><span class="sxs-lookup"><span data-stu-id="6b022-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="6b022-139">-Force</span><span class="sxs-lookup"><span data-stu-id="6b022-139">-Force</span></span>
<span data-ttu-id="6b022-140">A meglévő blob vagy fájl felülírása kényszerítve</span><span class="sxs-lookup"><span data-stu-id="6b022-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="6b022-141">-RehidradvePriority</span><span class="sxs-lookup"><span data-stu-id="6b022-141">-RehydratePriority</span></span>
<span data-ttu-id="6b022-142">Blob RehidrasztálásPrioritás blokkolása</span><span class="sxs-lookup"><span data-stu-id="6b022-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="6b022-143">Az archivált blob rehidrálásának prioritása.</span><span class="sxs-lookup"><span data-stu-id="6b022-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="6b022-144">Érvényes értékek: High/Standard.</span><span class="sxs-lookup"><span data-stu-id="6b022-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6b022-145">-SrcBlob</span></span>
<span data-ttu-id="6b022-146">Blob neve</span><span class="sxs-lookup"><span data-stu-id="6b022-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6b022-147">-SrcContainer</span></span>
<span data-ttu-id="6b022-148">Forrástároló neve</span><span class="sxs-lookup"><span data-stu-id="6b022-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6b022-149">-StandardBlobTier</span></span>
<span data-ttu-id="6b022-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span><span class="sxs-lookup"><span data-stu-id="6b022-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6b022-151">Részleteket itt láthat: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6b022-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b022-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b022-152">-Confirm</span></span>
<span data-ttu-id="6b022-153">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6b022-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b022-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b022-154">-WhatIf</span></span>
<span data-ttu-id="6b022-155">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6b022-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b022-156">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b022-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b022-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b022-157">CommonParameters</span></span>
<span data-ttu-id="6b022-158">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b022-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b022-159">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b022-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b022-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b022-160">INPUTS</span></span>

### <span data-ttu-id="6b022-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6b022-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="6b022-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6b022-162">System.String</span></span>

### <span data-ttu-id="6b022-163">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6b022-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6b022-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b022-164">OUTPUTS</span></span>

### <span data-ttu-id="6b022-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6b022-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6b022-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6b022-166">NOTES</span></span>

## <span data-ttu-id="6b022-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b022-167">RELATED LINKS</span></span>
