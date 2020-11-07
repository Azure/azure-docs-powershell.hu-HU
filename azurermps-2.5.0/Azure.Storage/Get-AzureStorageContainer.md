---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
ms.openlocfilehash: 62d2e0cfa96c2085b13416ba8a305acf565b23ee
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849849"
---
# <span data-ttu-id="0a083-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a083-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="0a083-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a083-102">SYNOPSIS</span></span>
<span data-ttu-id="0a083-103">Felsorolja a tároló tárolókat.</span><span class="sxs-lookup"><span data-stu-id="0a083-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a083-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a083-104">SYNTAX</span></span>

### <span data-ttu-id="0a083-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a083-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0a083-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="0a083-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0a083-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a083-107">DESCRIPTION</span></span>
<span data-ttu-id="0a083-108">A **Get-AzureStorageContainer** parancsmag az Azure-beli tárolási fiókkal társított tároló tárolókat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="0a083-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="0a083-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0a083-109">EXAMPLES</span></span>

### <span data-ttu-id="0a083-110">Példa 1: Azure Storage blob beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="0a083-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="0a083-111">Ebben a példában egy helyettesítő karakter használatával visszaállíthatja az összes olyan tároló listáját, amely tárolóval kezdődik.</span><span class="sxs-lookup"><span data-stu-id="0a083-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="0a083-112">2. példa: az Azure Storage Container beszerzése tároló név előtaggal</span><span class="sxs-lookup"><span data-stu-id="0a083-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="0a083-113">Ez a példa az *előtag* paramétert használja az összes olyan tároló listájának visszaadására, amely a tárolóval kezdődő nevet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0a083-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="0a083-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a083-114">PARAMETERS</span></span>

### <span data-ttu-id="0a083-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a083-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0a083-116">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="0a083-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0a083-117">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="0a083-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0a083-118">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0a083-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0a083-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0a083-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0a083-120">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0a083-121">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0a083-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0a083-122">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="0a083-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0a083-123">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="0a083-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0a083-124">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0a083-124">The default value is 10.</span></span>

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

### <span data-ttu-id="0a083-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0a083-125">-Context</span></span>
<span data-ttu-id="0a083-126">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-126">Specifies the storage context.</span></span>
<span data-ttu-id="0a083-127">A létrehozáshoz használhatja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0a083-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="0a083-128">A parancsmag nem fog működni a SAS-tokenből létrehozott tárolási környezet használatakor, mert a parancsmag a tároló engedélyeinek lekérdezését kéri, ami a tárolási fiók kulcsának engedélyét igényli.</span><span class="sxs-lookup"><span data-stu-id="0a083-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="0a083-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="0a083-129">-ContinuationToken</span></span>
<span data-ttu-id="0a083-130">A blob-lista folytatólagos jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a083-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a083-131">-DefaultProfile</span></span>
<span data-ttu-id="0a083-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a083-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a083-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0a083-133">-MaxCount</span></span>
<span data-ttu-id="0a083-134">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0a083-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a083-135">-Name</span></span>
<span data-ttu-id="0a083-136">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-136">Specifies the container name.</span></span>
<span data-ttu-id="0a083-137">Ha a tároló neve üres, a parancsmag felsorolja az összes tárolót.</span><span class="sxs-lookup"><span data-stu-id="0a083-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="0a083-138">Ellenkező esetben az összes olyan tárolót listázza, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="0a083-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a083-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="0a083-139">-Prefix</span></span>
<span data-ttu-id="0a083-140">A beszerzéshez használni kívánt tároló vagy tárolók nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a083-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="0a083-141">Ezzel a beállítással megkeresheti az összes olyan tárolót, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a "saját" vagy a "teszt".</span><span class="sxs-lookup"><span data-stu-id="0a083-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a083-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0a083-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0a083-143">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="0a083-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0a083-144">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0a083-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0a083-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a083-145">CommonParameters</span></span>
<span data-ttu-id="0a083-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a083-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a083-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a083-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a083-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a083-148">INPUTS</span></span>

### <span data-ttu-id="0a083-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0a083-149">System.String</span></span>

### <span data-ttu-id="0a083-150">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a083-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a083-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a083-151">OUTPUTS</span></span>

### <span data-ttu-id="0a083-152">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a083-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="0a083-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a083-153">NOTES</span></span>

## <span data-ttu-id="0a083-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a083-154">RELATED LINKS</span></span>

[<span data-ttu-id="0a083-155">Új – AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a083-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="0a083-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a083-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="0a083-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0a083-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


