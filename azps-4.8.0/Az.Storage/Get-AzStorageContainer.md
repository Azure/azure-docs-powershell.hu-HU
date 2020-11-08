---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017525"
---
# <span data-ttu-id="0706c-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0706c-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="0706c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0706c-102">SYNOPSIS</span></span>
<span data-ttu-id="0706c-103">Felsorolja a tároló tárolókat.</span><span class="sxs-lookup"><span data-stu-id="0706c-103">Lists the storage containers.</span></span>

## <span data-ttu-id="0706c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0706c-104">SYNTAX</span></span>

### <span data-ttu-id="0706c-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0706c-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0706c-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="0706c-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0706c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0706c-107">DESCRIPTION</span></span>
<span data-ttu-id="0706c-108">A **Get-AzStorageContainer** parancsmag az Azure-beli tárolási fiókkal társított tároló tárolókat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="0706c-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="0706c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0706c-109">EXAMPLES</span></span>

### <span data-ttu-id="0706c-110">Példa 1: Azure Storage blob beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="0706c-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="0706c-111">Ebben a példában egy helyettesítő karakter használatával visszaállíthatja az összes olyan tároló listáját, amely tárolóval kezdődik.</span><span class="sxs-lookup"><span data-stu-id="0706c-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="0706c-112">2. példa: az Azure Storage Container beszerzése tároló név előtaggal</span><span class="sxs-lookup"><span data-stu-id="0706c-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="0706c-113">Ez a példa az *előtag* paramétert használja az összes olyan tároló listájának visszaadására, amely a tárolóval kezdődő nevet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0706c-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="0706c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0706c-114">PARAMETERS</span></span>

### <span data-ttu-id="0706c-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0706c-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0706c-116">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="0706c-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0706c-117">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="0706c-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0706c-118">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0706c-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0706c-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0706c-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0706c-120">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0706c-121">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="0706c-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0706c-122">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="0706c-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0706c-123">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="0706c-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0706c-124">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="0706c-124">The default value is 10.</span></span>

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

### <span data-ttu-id="0706c-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0706c-125">-Context</span></span>
<span data-ttu-id="0706c-126">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-126">Specifies the storage context.</span></span>
<span data-ttu-id="0706c-127">A létrehozáshoz használhatja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0706c-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="0706c-128">A tároló engedélyei nem jelennek meg, amikor a SAS-tokenből létrehozott tárolási környezettel rendelkezik, mert a lekérdezési tároló engedélyeihez tárterület-kulcs szükséges.</span><span class="sxs-lookup"><span data-stu-id="0706c-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="0706c-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="0706c-129">-ContinuationToken</span></span>
<span data-ttu-id="0706c-130">A blob-lista folytatólagos jogkivonatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0706c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0706c-131">-DefaultProfile</span></span>
<span data-ttu-id="0706c-132">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0706c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0706c-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0706c-133">-MaxCount</span></span>
<span data-ttu-id="0706c-134">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0706c-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0706c-135">-Name</span></span>
<span data-ttu-id="0706c-136">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-136">Specifies the container name.</span></span>
<span data-ttu-id="0706c-137">Ha a tároló neve üres, a parancsmag felsorolja az összes tárolót.</span><span class="sxs-lookup"><span data-stu-id="0706c-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="0706c-138">Ellenkező esetben az összes olyan tárolót listázza, amely megfelel a megadott névnek vagy a normál név mintának.</span><span class="sxs-lookup"><span data-stu-id="0706c-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="0706c-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="0706c-139">-Prefix</span></span>
<span data-ttu-id="0706c-140">A beszerzéshez használni kívánt tároló vagy tárolók nevében használt előtagot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0706c-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="0706c-141">Ezzel a beállítással megkeresheti az összes olyan tárolót, amely ugyanazzal a karakterlánccal kezdődik, mint amilyen például a "saját" vagy a "teszt".</span><span class="sxs-lookup"><span data-stu-id="0706c-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="0706c-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0706c-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0706c-143">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="0706c-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="0706c-144">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="0706c-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="0706c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0706c-145">CommonParameters</span></span>
<span data-ttu-id="0706c-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0706c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0706c-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0706c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0706c-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0706c-148">INPUTS</span></span>

### <span data-ttu-id="0706c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0706c-149">System.String</span></span>

### <span data-ttu-id="0706c-150">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0706c-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0706c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0706c-151">OUTPUTS</span></span>

### <span data-ttu-id="0706c-152">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0706c-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="0706c-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0706c-153">NOTES</span></span>

## <span data-ttu-id="0706c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0706c-154">RELATED LINKS</span></span>

[<span data-ttu-id="0706c-155">Új – AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0706c-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="0706c-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0706c-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="0706c-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0706c-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


