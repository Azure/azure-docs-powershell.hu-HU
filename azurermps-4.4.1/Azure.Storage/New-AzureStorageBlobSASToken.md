---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 17efee05b4d10ce87d327d8b7de26063bfc0cac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672080"
---
# <span data-ttu-id="15b49-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="15b49-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="15b49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15b49-102">SYNOPSIS</span></span>
<span data-ttu-id="15b49-103">Egy, az Azure Storage blob-hoz generált SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="15b49-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15b49-104">SYNTAX</span></span>

### <span data-ttu-id="15b49-105">BlobNameWithPermission (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15b49-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15b49-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="15b49-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15b49-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="15b49-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15b49-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="15b49-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="15b49-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="15b49-109">DESCRIPTION</span></span>
<span data-ttu-id="15b49-110">A **New-AzureStorageBlobSASToken** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SAS) tokent egy Azure Storage blob számára.</span><span class="sxs-lookup"><span data-stu-id="15b49-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="15b49-111">Példák</span><span class="sxs-lookup"><span data-stu-id="15b49-111">EXAMPLES</span></span>

### <span data-ttu-id="15b49-112">1. példa: blob SAS-jogkivonat létrehozása teljes blob-engedély birtokában</span><span class="sxs-lookup"><span data-stu-id="15b49-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="15b49-113">Ez a példa blob SAS-jogkivonatot hoz létre teljes blob-engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="15b49-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="15b49-114">2. példa: blob SAS-token létrehozása a Life Time szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="15b49-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="15b49-115">Ez a példa blob SAS-tokent hoz létre a Life Time szolgáltatóval.</span><span class="sxs-lookup"><span data-stu-id="15b49-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="15b49-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15b49-116">PARAMETERS</span></span>

### <span data-ttu-id="15b49-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="15b49-117">-Blob</span></span>
<span data-ttu-id="15b49-118">A Storage blob nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="15b49-119">-CloudBlob</span></span>
<span data-ttu-id="15b49-120">A **CloudBlob** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="15b49-121">Ha **CloudBlob** objektumot szeretne beolvasni, használja a [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="15b49-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-122">-Container</span><span class="sxs-lookup"><span data-stu-id="15b49-122">-Container</span></span>
<span data-ttu-id="15b49-123">A tároló tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="15b49-124">-Context</span></span>
<span data-ttu-id="15b49-125">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-125">Specifies the storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="15b49-126">-ExpiryTime</span></span>
<span data-ttu-id="15b49-127">Azt adja meg, hogy mikor jár le a megosztott Access-aláírás.</span><span class="sxs-lookup"><span data-stu-id="15b49-127">Specifies when the shared access signature expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="15b49-128">-FullUri</span></span>
<span data-ttu-id="15b49-129">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="15b49-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="15b49-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="15b49-130">-IPAddressOrRange</span></span>
<span data-ttu-id="15b49-131">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="15b49-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="15b49-132">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="15b49-132">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-133">– Engedély</span><span class="sxs-lookup"><span data-stu-id="15b49-133">-Permission</span></span>
<span data-ttu-id="15b49-134">A tárterület-blob engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="15b49-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="15b49-135">-Policy</span></span>
<span data-ttu-id="15b49-136">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="15b49-137">-Protocol</span></span>
<span data-ttu-id="15b49-138">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="15b49-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="15b49-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="15b49-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="15b49-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="15b49-140">HttpsOnly</span></span>
* <span data-ttu-id="15b49-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="15b49-141">HttpsOrHttp</span></span>

<span data-ttu-id="15b49-142">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="15b49-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-143">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="15b49-143">-StartTime</span></span>
<span data-ttu-id="15b49-144">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="15b49-144">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15b49-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b49-145">CommonParameters</span></span>
<span data-ttu-id="15b49-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15b49-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b49-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b49-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b49-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b49-148">INPUTS</span></span>

### <span data-ttu-id="15b49-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15b49-149">IStorageContext</span></span>

<span data-ttu-id="15b49-150">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="15b49-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="15b49-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15b49-151">OUTPUTS</span></span>

### <span data-ttu-id="15b49-152">System. String</span><span class="sxs-lookup"><span data-stu-id="15b49-152">System.String</span></span>

## <span data-ttu-id="15b49-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15b49-153">NOTES</span></span>

## <span data-ttu-id="15b49-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15b49-154">RELATED LINKS</span></span>

[<span data-ttu-id="15b49-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="15b49-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="15b49-156">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="15b49-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
