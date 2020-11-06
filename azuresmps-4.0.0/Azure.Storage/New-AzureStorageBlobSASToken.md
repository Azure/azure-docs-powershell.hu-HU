---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8d84b310a16a73456bcd519332fa76ad1a6566
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491712"
---
# <span data-ttu-id="728fc-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="728fc-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="728fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="728fc-102">SYNOPSIS</span></span>
<span data-ttu-id="728fc-103">Létrehoz egy SAS-jogkivonatot az Azure Storage blob szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="728fc-103">Generates an SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="728fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="728fc-104">SYNTAX</span></span>

### <span data-ttu-id="728fc-105">BlobNameWithPermission (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="728fc-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="728fc-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="728fc-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="728fc-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="728fc-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="728fc-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="728fc-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="728fc-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="728fc-109">DESCRIPTION</span></span>
<span data-ttu-id="728fc-110">A **New-AzureStorageBlobSASToken** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SAS) tokent egy Azure Storage blob számára.</span><span class="sxs-lookup"><span data-stu-id="728fc-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="728fc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="728fc-111">EXAMPLES</span></span>

### <span data-ttu-id="728fc-112">1. példa: blob SAS-jogkivonat létrehozása teljes blob-engedély birtokában</span><span class="sxs-lookup"><span data-stu-id="728fc-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="728fc-113">Ez a példa blob SAS-jogkivonatot hoz létre teljes blob-engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="728fc-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="728fc-114">2. példa: blob SAS-token létrehozása a Life Time szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="728fc-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="728fc-115">Ez a példa blob SAS-tokent hoz létre a Life Time szolgáltatóval.</span><span class="sxs-lookup"><span data-stu-id="728fc-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="728fc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="728fc-116">PARAMETERS</span></span>

### <span data-ttu-id="728fc-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="728fc-117">-Blob</span></span>
<span data-ttu-id="728fc-118">A Storage blob nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="728fc-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="728fc-119">-CloudBlob</span></span>
<span data-ttu-id="728fc-120">A **CloudBlob** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="728fc-121">Ha **CloudBlob** objektumot szeretne beolvasni, használja a [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="728fc-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="728fc-122">-Container</span><span class="sxs-lookup"><span data-stu-id="728fc-122">-Container</span></span>
<span data-ttu-id="728fc-123">A tároló tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="728fc-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="728fc-124">-Context</span></span>
<span data-ttu-id="728fc-125">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="728fc-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="728fc-126">-ExpiryTime</span></span>
<span data-ttu-id="728fc-127">Azt adja meg, hogy mikor jár le a megosztott Access-aláírás.</span><span class="sxs-lookup"><span data-stu-id="728fc-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="728fc-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="728fc-128">-FullUri</span></span>
<span data-ttu-id="728fc-129">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="728fc-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="728fc-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="728fc-130">-IPAddressOrRange</span></span>
<span data-ttu-id="728fc-131">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="728fc-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="728fc-132">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="728fc-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="728fc-133">– Engedély</span><span class="sxs-lookup"><span data-stu-id="728fc-133">-Permission</span></span>
<span data-ttu-id="728fc-134">A tárterület-blob engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="728fc-134">Specifies the permissions for a storage blob.</span></span>

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

### <span data-ttu-id="728fc-135">-Házirend</span><span class="sxs-lookup"><span data-stu-id="728fc-135">-Policy</span></span>
<span data-ttu-id="728fc-136">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-136">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="728fc-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="728fc-137">-Protocol</span></span>
<span data-ttu-id="728fc-138">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="728fc-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="728fc-139">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="728fc-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="728fc-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="728fc-140">HttpsOnly</span></span>
* <span data-ttu-id="728fc-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="728fc-141">HttpsOrHttp</span></span>

<span data-ttu-id="728fc-142">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="728fc-142">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="728fc-143">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="728fc-143">-StartTime</span></span>
<span data-ttu-id="728fc-144">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="728fc-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="728fc-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728fc-145">CommonParameters</span></span>
<span data-ttu-id="728fc-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="728fc-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728fc-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728fc-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728fc-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="728fc-148">INPUTS</span></span>

## <span data-ttu-id="728fc-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="728fc-149">OUTPUTS</span></span>

## <span data-ttu-id="728fc-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="728fc-150">NOTES</span></span>

## <span data-ttu-id="728fc-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="728fc-151">RELATED LINKS</span></span>

[<span data-ttu-id="728fc-152">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="728fc-152">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="728fc-153">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="728fc-153">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
