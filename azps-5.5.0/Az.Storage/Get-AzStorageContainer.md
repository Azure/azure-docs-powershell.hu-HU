---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145442"
---
# <span data-ttu-id="a901c-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a901c-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="a901c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a901c-102">SYNOPSIS</span></span>
<span data-ttu-id="a901c-103">Felsorolja a tárolókat.</span><span class="sxs-lookup"><span data-stu-id="a901c-103">Lists the storage containers.</span></span>

## <span data-ttu-id="a901c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a901c-104">SYNTAX</span></span>

### <span data-ttu-id="a901c-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a901c-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a901c-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="a901c-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="a901c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a901c-107">DESCRIPTION</span></span>
<span data-ttu-id="a901c-108">A **Get-AzStorageContainer** parancsmag felsorolja az Azure-beli tárfiókhoz társított tárolókat.</span><span class="sxs-lookup"><span data-stu-id="a901c-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a901c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a901c-109">EXAMPLES</span></span>

### <span data-ttu-id="a901c-110">1. példa: Azure Storage blob lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="a901c-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="a901c-111">Ebben a példában egy helyettesítő karakter visszaadja a tárolóval kezdődik nevű összes tároló listáját.</span><span class="sxs-lookup"><span data-stu-id="a901c-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="a901c-112">2. példa: Azure Storage tároló lekérte tárolónév előtagja alapján</span><span class="sxs-lookup"><span data-stu-id="a901c-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="a901c-113">Ez a példa az *Előtag* paraméter segítségével visszaadja a tárolóval kezdődik nevű összes tároló listáját.</span><span class="sxs-lookup"><span data-stu-id="a901c-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="a901c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a901c-114">PARAMETERS</span></span>

### <span data-ttu-id="a901c-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a901c-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a901c-116">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a901c-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a901c-117">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="a901c-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a901c-118">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a901c-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a901c-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a901c-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a901c-120">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="a901c-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a901c-121">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a901c-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a901c-122">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="a901c-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a901c-123">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="a901c-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a901c-124">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a901c-124">The default value is 10.</span></span>

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

### <span data-ttu-id="a901c-125">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a901c-125">-Context</span></span>
<span data-ttu-id="a901c-126">A tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a901c-126">Specifies the storage context.</span></span>
<span data-ttu-id="a901c-127">A létrehozásához használhatja a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a901c-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="a901c-128">A tárolóengedélyeket a rendszer nem olvassa be, ha EGY SAS-jogkivonatból létrehozott tárterület-környezetet használ, mert a lekérdezéstároló-engedélyekhez tárfiókkulcs-engedély szükséges.</span><span class="sxs-lookup"><span data-stu-id="a901c-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="a901c-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="a901c-129">-ContinuationToken</span></span>
<span data-ttu-id="a901c-130">A bloblista folytatására vonatkozó jogkivonatot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a901c-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="a901c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a901c-131">-DefaultProfile</span></span>
<span data-ttu-id="a901c-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a901c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a901c-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a901c-133">-MaxCount</span></span>
<span data-ttu-id="a901c-134">A parancsmag által visszaadott objektumok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a901c-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="a901c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a901c-135">-Name</span></span>
<span data-ttu-id="a901c-136">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a901c-136">Specifies the container name.</span></span>
<span data-ttu-id="a901c-137">Ha a tároló neve üres, a parancsmag felsorolja az összes tárolót.</span><span class="sxs-lookup"><span data-stu-id="a901c-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="a901c-138">Ellenkező esetben felsorolja az összes olyan tárolót, amely megfelel a megadott névnek vagy a normál névmintának.</span><span class="sxs-lookup"><span data-stu-id="a901c-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="a901c-139">-Előtag</span><span class="sxs-lookup"><span data-stu-id="a901c-139">-Prefix</span></span>
<span data-ttu-id="a901c-140">Megadja a lekért tároló vagy tárolók nevében használt előtagot.</span><span class="sxs-lookup"><span data-stu-id="a901c-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="a901c-141">Ezzel a segítségével megkeresheti az összes olyan tárolót, amely ugyanazokkal a karakterláncokkal kezdődik, például "én" vagy "teszt".</span><span class="sxs-lookup"><span data-stu-id="a901c-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="a901c-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a901c-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a901c-143">A szolgáltatás oldalának időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="a901c-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a901c-144">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="a901c-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a901c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a901c-145">CommonParameters</span></span>
<span data-ttu-id="a901c-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a901c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a901c-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a901c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a901c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a901c-148">INPUTS</span></span>

### <span data-ttu-id="a901c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a901c-149">System.String</span></span>

### <span data-ttu-id="a901c-150">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a901c-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a901c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a901c-151">OUTPUTS</span></span>

### <span data-ttu-id="a901c-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a901c-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="a901c-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a901c-153">NOTES</span></span>

## <span data-ttu-id="a901c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a901c-154">RELATED LINKS</span></span>

[<span data-ttu-id="a901c-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a901c-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="a901c-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="a901c-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="a901c-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="a901c-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


