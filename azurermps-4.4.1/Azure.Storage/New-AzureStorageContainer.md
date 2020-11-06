---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7e7672368a2f9e102e1e073c1f10be609e658cfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492640"
---
# <span data-ttu-id="47d4b-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47d4b-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="47d4b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="47d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="47d4b-103">Azure-tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47d4b-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47d4b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="47d4b-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="47d4b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="47d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="47d4b-106">A **New-AzureStorageContainer** parancsmag Azure tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47d4b-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="47d4b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="47d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="47d4b-108">Példa 1: Azure Storage tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="47d4b-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="47d4b-109">A parancs létrehoz egy tároló tárolót.</span><span class="sxs-lookup"><span data-stu-id="47d4b-109">This command creates a storage container.</span></span>

### <span data-ttu-id="47d4b-110">2. példa: több Azure-tároló tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="47d4b-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="47d4b-111">Ebben a példában több tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="47d4b-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="47d4b-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="47d4b-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="47d4b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="47d4b-113">PARAMETERS</span></span>

### <span data-ttu-id="47d4b-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="47d4b-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="47d4b-115">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="47d4b-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="47d4b-116">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="47d4b-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="47d4b-117">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="47d4b-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d4b-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="47d4b-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="47d4b-119">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d4b-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="47d4b-120">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="47d4b-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="47d4b-121">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="47d4b-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="47d4b-122">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="47d4b-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="47d4b-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="47d4b-123">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d4b-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="47d4b-124">-Context</span></span>
<span data-ttu-id="47d4b-125">Az új tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d4b-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="47d4b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="47d4b-126">-Name</span></span>
<span data-ttu-id="47d4b-127">Az új tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d4b-127">Specifies a name for the new container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47d4b-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="47d4b-128">-Permission</span></span>
<span data-ttu-id="47d4b-129">A tárolóhoz való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="47d4b-129">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="47d4b-130">Alapértelmezés szerint a tároló és a bennük lévő festékfoltok csak a tárolási fiók tulajdonosa érhetik el.</span><span class="sxs-lookup"><span data-stu-id="47d4b-130">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="47d4b-131">Ha a névtelen felhasználóknak olvasási engedélyeket szeretne adni egy tárolóhoz és a festékfoltok-hez, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="47d4b-131">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="47d4b-132">A névtelen felhasználók egy nyilvánosan elérhető tárolóban olvashatják a blob-objektumokat a kérés hitelesítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="47d4b-132">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="47d4b-133">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="47d4b-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47d4b-134">Konténer.</span><span class="sxs-lookup"><span data-stu-id="47d4b-134">Container.</span></span>
<span data-ttu-id="47d4b-135">Teljes olvasási hozzáférést biztosít egy tárolóhoz és a Blobs-hoz.</span><span class="sxs-lookup"><span data-stu-id="47d4b-135">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="47d4b-136">Az ügyfelek névtelen kéréssel enumerálják a tárolóban lévő blob-objektumokat, a tárolási fiókban azonban nem lehet enumerálni a tárolókat.</span><span class="sxs-lookup"><span data-stu-id="47d4b-136">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="47d4b-137">BLOB.</span><span class="sxs-lookup"><span data-stu-id="47d4b-137">Blob.</span></span>
<span data-ttu-id="47d4b-138">Névtelen kéréssel olvasási hozzáférést biztosít a blob-adatforrásokhoz, de nem biztosít hozzáférést a tárolók adatainak eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="47d4b-138">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="47d4b-139">Az ügyfelek névtelen kéréssel nem tudják enumerálni a blobokat a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="47d4b-139">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="47d4b-140">Ki.</span><span class="sxs-lookup"><span data-stu-id="47d4b-140">Off.</span></span>
<span data-ttu-id="47d4b-141">Amely korlátozza a hozzáférést csak a tárterület-tulajdonoshoz.</span><span class="sxs-lookup"><span data-stu-id="47d4b-141">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d4b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="47d4b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="47d4b-143">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="47d4b-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="47d4b-144">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="47d4b-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d4b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d4b-145">CommonParameters</span></span>
<span data-ttu-id="47d4b-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="47d4b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d4b-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47d4b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d4b-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d4b-148">INPUTS</span></span>

### <span data-ttu-id="47d4b-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="47d4b-149">IStorageContext</span></span>

<span data-ttu-id="47d4b-150">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="47d4b-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="47d4b-151">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="47d4b-151">String</span></span>

<span data-ttu-id="47d4b-152">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="47d4b-152">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="47d4b-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="47d4b-153">OUTPUTS</span></span>

### <span data-ttu-id="47d4b-154">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47d4b-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="47d4b-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="47d4b-155">NOTES</span></span>

## <span data-ttu-id="47d4b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="47d4b-156">RELATED LINKS</span></span>

[<span data-ttu-id="47d4b-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47d4b-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="47d4b-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="47d4b-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="47d4b-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="47d4b-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


