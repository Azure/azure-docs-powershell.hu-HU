---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165674"
---
# <span data-ttu-id="fbe5e-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbe5e-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="fbe5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe5e-103">Létrehoz egy Azure-tárolót.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="fbe5e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-104">SYNTAX</span></span>

### <span data-ttu-id="fbe5e-105">ContainerName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fbe5e-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fbe5e-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fbe5e-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fbe5e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe5e-108">A **New-AzStorageContainer** parancsmag létrehoz egy Azure-tárolót.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="fbe5e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbe5e-109">EXAMPLES</span></span>

### <span data-ttu-id="fbe5e-110">1. példa: Azure-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbe5e-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="fbe5e-111">Ez a parancs egy tárolótárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-111">This command creates a storage container.</span></span>

### <span data-ttu-id="fbe5e-112">2. példa: Több Azure-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbe5e-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="fbe5e-113">Ez a példa több tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="fbe5e-114">A  **.NET-karakterláncosztály Felosztás** metódusát használja, majd átadja a neveket a folyamatnak.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="fbe5e-115">3. példa: Titkosítási hatókörű Azure-tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="fbe5e-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="fbe5e-116">Ez a parancs létrehoz egy tárolótárolót, amely alapértelmezett titkosítási hatókört használ myencryptscope-ként, és előtűnti a blobfeltöltést különböző titkosítási hatókörrel erre a tárolóra.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="fbe5e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-117">PARAMETERS</span></span>

### <span data-ttu-id="fbe5e-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbe5e-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fbe5e-119">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fbe5e-120">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fbe5e-121">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, ez a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fbe5e-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fbe5e-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fbe5e-123">Megadja a maximális párhuzamos hálózati hívást.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fbe5e-124">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fbe5e-125">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fbe5e-126">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fbe5e-127">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-127">The default value is 10.</span></span>

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

### <span data-ttu-id="fbe5e-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="fbe5e-128">-Context</span></span>
<span data-ttu-id="fbe5e-129">Megadja az új tároló környezetét.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="fbe5e-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="fbe5e-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="fbe5e-131">Alapértelmezés szerint a tároló a megadott titkosítási hatókört használja az összes íráshoz.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe5e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe5e-132">-DefaultProfile</span></span>
<span data-ttu-id="fbe5e-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe5e-134">-Name</span><span class="sxs-lookup"><span data-stu-id="fbe5e-134">-Name</span></span>
<span data-ttu-id="fbe5e-135">Az új tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="fbe5e-136">-Permission</span><span class="sxs-lookup"><span data-stu-id="fbe5e-136">-Permission</span></span>
<span data-ttu-id="fbe5e-137">A tárolóhoz való nyilvános hozzáférés szintjét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="fbe5e-138">Alapértelmezés szerint a tároló és a benne lévő blobok csak a tárfiók tulajdonosa által érhetők el.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="fbe5e-139">Ha névtelen felhasználóknak szeretné olvasási engedélyeket beállítani egy tárolóhoz és blobjaikhoz, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="fbe5e-140">A névtelen felhasználók a kérés hitelesítése nélkül olvashatják a blobokat egy nyilvánosan elérhető tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="fbe5e-141">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="fbe5e-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fbe5e-142">Tároló.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-142">Container.</span></span>
<span data-ttu-id="fbe5e-143">Teljes olvasási hozzáférést biztosít egy tárolóhoz és a blobshoz.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="fbe5e-144">Az ügyfelek névtelen kérésen keresztül számba tudják venni a tárolóban lévő blobokat, de a tárfiókban lévő tárolókat nem.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="fbe5e-145">Blob.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-145">Blob.</span></span>
<span data-ttu-id="fbe5e-146">Olvasási hozzáférést biztosít a blobadatokhoz a teljes tárolóban névtelen kérésen keresztül, de nem biztosít hozzáférést a tárolóadatokhoz.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="fbe5e-147">Az ügyfelek névtelen kérésekkel nem tudnak blobokat számozni a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="fbe5e-148">Kikapcsolva.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-148">Off.</span></span>
<span data-ttu-id="fbe5e-149">Ez csak a tárfiók tulajdonosára korlátozza a hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-149">Which restricts access to only the storage account owner.</span></span>

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

### <span data-ttu-id="fbe5e-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="fbe5e-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="fbe5e-151">Tiltsa le a titkosítási hatókör felülírást az alapértelmezett tárolóból.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe5e-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fbe5e-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fbe5e-153">A szolgáltatás oldalának időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fbe5e-154">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fbe5e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe5e-155">CommonParameters</span></span>
<span data-ttu-id="fbe5e-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe5e-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe5e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe5e-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-158">INPUTS</span></span>

### <span data-ttu-id="fbe5e-159">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe5e-159">System.String</span></span>

### <span data-ttu-id="fbe5e-160">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fbe5e-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fbe5e-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbe5e-161">OUTPUTS</span></span>

### <span data-ttu-id="fbe5e-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbe5e-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="fbe5e-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbe5e-163">NOTES</span></span>

## <span data-ttu-id="fbe5e-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbe5e-164">RELATED LINKS</span></span>

[<span data-ttu-id="fbe5e-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbe5e-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="fbe5e-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fbe5e-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="fbe5e-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="fbe5e-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


