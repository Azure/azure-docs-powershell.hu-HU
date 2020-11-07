---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 87967dbaaa57bb8050191ee1b20ebb5a760bc045
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849441"
---
# <span data-ttu-id="a6a8b-101">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6a8b-101">New-AzureStorageContainer</span></span>

## <span data-ttu-id="a6a8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a8b-103">Azure-tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-103">Creates an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6a8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6a8b-104">SYNTAX</span></span>

```
New-AzureStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a6a8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a8b-106">A **New-AzureStorageContainer** parancsmag Azure tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-106">The **New-AzureStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="a6a8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a6a8b-107">EXAMPLES</span></span>

### <span data-ttu-id="a6a8b-108">Példa 1: Azure Storage tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="a6a8b-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzureStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="a6a8b-109">A parancs létrehoz egy tároló tárolót.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-109">This command creates a storage container.</span></span>

### <span data-ttu-id="a6a8b-110">2. példa: több Azure-tároló tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="a6a8b-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzureStorageContainer -Permission Container
```

<span data-ttu-id="a6a8b-111">Ebben a példában több tároló tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="a6a8b-112">A .NET **String** osztály **felosztott** metódusát használja, és a neveket átadja a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a6a8b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6a8b-113">PARAMETERS</span></span>

### <span data-ttu-id="a6a8b-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6a8b-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a6a8b-115">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a6a8b-116">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a6a8b-117">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a6a8b-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a6a8b-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a6a8b-119">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a6a8b-120">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a6a8b-121">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a6a8b-122">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a6a8b-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a6a8b-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a6a8b-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a6a8b-124">-Context</span></span>
<span data-ttu-id="a6a8b-125">Az új tároló környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="a6a8b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a8b-126">-DefaultProfile</span></span>
<span data-ttu-id="a6a8b-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a8b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6a8b-128">-Name</span></span>
<span data-ttu-id="a6a8b-129">Az új tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a8b-130">– Engedély</span><span class="sxs-lookup"><span data-stu-id="a6a8b-130">-Permission</span></span>
<span data-ttu-id="a6a8b-131">A tárolóhoz való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="a6a8b-132">Alapértelmezés szerint a tároló és a bennük lévő festékfoltok csak a tárolási fiók tulajdonosa érhetik el.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="a6a8b-133">Ha a névtelen felhasználóknak olvasási engedélyeket szeretne adni egy tárolóhoz és a festékfoltok-hez, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="a6a8b-134">A névtelen felhasználók egy nyilvánosan elérhető tárolóban olvashatják a blob-objektumokat a kérés hitelesítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="a6a8b-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a6a8b-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6a8b-136">Konténer.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-136">Container.</span></span>
<span data-ttu-id="a6a8b-137">Teljes olvasási hozzáférést biztosít egy tárolóhoz és a Blobs-hoz.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="a6a8b-138">Az ügyfelek névtelen kéréssel enumerálják a tárolóban lévő blob-objektumokat, a tárolási fiókban azonban nem lehet enumerálni a tárolókat.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="a6a8b-139">BLOB.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-139">Blob.</span></span>
<span data-ttu-id="a6a8b-140">Névtelen kéréssel olvasási hozzáférést biztosít a blob-adatforrásokhoz, de nem biztosít hozzáférést a tárolók adatainak eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="a6a8b-141">Az ügyfelek névtelen kéréssel nem tudják enumerálni a blobokat a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="a6a8b-142">Ki.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-142">Off.</span></span>
<span data-ttu-id="a6a8b-143">Amely korlátozza a hozzáférést csak a tárterület-tulajdonoshoz.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a8b-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a6a8b-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a6a8b-145">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a6a8b-146">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a6a8b-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a6a8b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a8b-147">CommonParameters</span></span>
<span data-ttu-id="a6a8b-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6a8b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a8b-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a8b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a8b-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6a8b-150">INPUTS</span></span>

### <span data-ttu-id="a6a8b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a6a8b-151">System.String</span></span>

### <span data-ttu-id="a6a8b-152">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a6a8b-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a6a8b-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6a8b-153">OUTPUTS</span></span>

### <span data-ttu-id="a6a8b-154">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6a8b-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="a6a8b-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6a8b-155">NOTES</span></span>

## <span data-ttu-id="a6a8b-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6a8b-156">RELATED LINKS</span></span>

[<span data-ttu-id="a6a8b-157">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6a8b-157">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="a6a8b-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a6a8b-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="a6a8b-159">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a6a8b-159">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


