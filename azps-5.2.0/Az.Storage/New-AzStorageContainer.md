---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: b056504786d641d137d5188ed529eecb0ede690f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324795"
---
# <span data-ttu-id="c23a0-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c23a0-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="c23a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c23a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c23a0-103">Létrehoz egy Azure-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c23a0-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="c23a0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c23a0-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c23a0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c23a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c23a0-106">A **New-AzStorageContainer** parancsmag létrehoz egy Azure-tárolót.</span><span class="sxs-lookup"><span data-stu-id="c23a0-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="c23a0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c23a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c23a0-108">1. példa: Azure-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="c23a0-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="c23a0-109">Ez a parancs egy tárolótárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c23a0-109">This command creates a storage container.</span></span>

### <span data-ttu-id="c23a0-110">2. példa: Több Azure-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="c23a0-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="c23a0-111">Ez a példa több tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c23a0-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="c23a0-112">A  **.NET-karakterláncosztály Felosztás** metódusát használja, majd átadja a neveket a folyamatnak.</span><span class="sxs-lookup"><span data-stu-id="c23a0-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="c23a0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c23a0-113">PARAMETERS</span></span>

### <span data-ttu-id="c23a0-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c23a0-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c23a0-115">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c23a0-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c23a0-116">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="c23a0-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c23a0-117">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c23a0-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c23a0-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c23a0-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c23a0-119">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="c23a0-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c23a0-120">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="c23a0-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c23a0-121">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="c23a0-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c23a0-122">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="c23a0-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c23a0-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="c23a0-123">The default value is 10.</span></span>

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

### <span data-ttu-id="c23a0-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c23a0-124">-Context</span></span>
<span data-ttu-id="c23a0-125">Megadja az új tároló környezetét.</span><span class="sxs-lookup"><span data-stu-id="c23a0-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="c23a0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23a0-126">-DefaultProfile</span></span>
<span data-ttu-id="c23a0-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c23a0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c23a0-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c23a0-128">-Name</span></span>
<span data-ttu-id="c23a0-129">Az új tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c23a0-129">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="c23a0-130">-Engedély</span><span class="sxs-lookup"><span data-stu-id="c23a0-130">-Permission</span></span>
<span data-ttu-id="c23a0-131">A tárolóhoz való nyilvános hozzáférés szintjét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c23a0-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="c23a0-132">Alapértelmezés szerint a tároló és a benne lévő blobok csak a tárfiók tulajdonosa által érhetők el.</span><span class="sxs-lookup"><span data-stu-id="c23a0-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="c23a0-133">Ha névtelen felhasználóknak szeretné olvasási engedélyeket beállítani egy tárolóhoz és blobjaikhoz, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="c23a0-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="c23a0-134">A névtelen felhasználók a kérés hitelesítése nélkül olvashatják a blobokat egy nyilvánosan elérhető tárolóban.</span><span class="sxs-lookup"><span data-stu-id="c23a0-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="c23a0-135">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c23a0-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c23a0-136">Tároló.</span><span class="sxs-lookup"><span data-stu-id="c23a0-136">Container.</span></span>
<span data-ttu-id="c23a0-137">Teljes olvasási hozzáférést biztosít a tárolókhoz és a blobjaikhoz.</span><span class="sxs-lookup"><span data-stu-id="c23a0-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="c23a0-138">Az ügyfelek névtelen kérésen keresztül számba tudják venni a tárolóban lévő blobokat, de a tárfiókban lévő tárolókat nem.</span><span class="sxs-lookup"><span data-stu-id="c23a0-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="c23a0-139">Blob.</span><span class="sxs-lookup"><span data-stu-id="c23a0-139">Blob.</span></span>
<span data-ttu-id="c23a0-140">Olvasási hozzáférést biztosít a blobadatokhoz a teljes tárolóban névtelen kérésen keresztül, de nem biztosít hozzáférést a tárolóadatokhoz.</span><span class="sxs-lookup"><span data-stu-id="c23a0-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="c23a0-141">Az ügyfelek névtelen kérésekkel nem tudnak blobokat számozni a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="c23a0-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="c23a0-142">Kikapcsolva.</span><span class="sxs-lookup"><span data-stu-id="c23a0-142">Off.</span></span>
<span data-ttu-id="c23a0-143">Ez csak a tárfiók tulajdonosára korlátozza a hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="c23a0-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23a0-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c23a0-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c23a0-145">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="c23a0-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c23a0-146">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="c23a0-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c23a0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23a0-147">CommonParameters</span></span>
<span data-ttu-id="c23a0-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23a0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23a0-149">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c23a0-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23a0-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c23a0-150">INPUTS</span></span>

### <span data-ttu-id="c23a0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c23a0-151">System.String</span></span>

### <span data-ttu-id="c23a0-152">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c23a0-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c23a0-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c23a0-153">OUTPUTS</span></span>

### <span data-ttu-id="c23a0-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c23a0-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="c23a0-155">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c23a0-155">NOTES</span></span>

## <span data-ttu-id="c23a0-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c23a0-156">RELATED LINKS</span></span>

[<span data-ttu-id="c23a0-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c23a0-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="c23a0-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c23a0-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="c23a0-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="c23a0-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


