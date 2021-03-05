---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 23aa7e6df5aae820980551db445339ade34ac779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002262"
---
# <span data-ttu-id="aaae5-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="aaae5-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="aaae5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaae5-102">SYNOPSIS</span></span>
<span data-ttu-id="aaae5-103">A nyilvános hozzáférési engedélyt egy tárolóra állítja.</span><span class="sxs-lookup"><span data-stu-id="aaae5-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="aaae5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aaae5-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="aaae5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aaae5-105">DESCRIPTION</span></span>
<span data-ttu-id="aaae5-106">A **Set-AzStorageContainerAcl** parancsmag a nyilvános hozzáférési engedélyt az Azure-ban megadott tárolóhoz állítja be.</span><span class="sxs-lookup"><span data-stu-id="aaae5-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="aaae5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aaae5-107">EXAMPLES</span></span>

### <span data-ttu-id="aaae5-108">1. példa: Azure storage container ACL beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="aaae5-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="aaae5-109">Ez a parancs létrehoz egy olyan tárolót, amely nem rendelkezik nyilvános hozzáféréssel.</span><span class="sxs-lookup"><span data-stu-id="aaae5-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="aaae5-110">2. példa: Azure storage container ACL beállítása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="aaae5-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="aaae5-111">Ez a parancs az összes olyan tárolótárolót beveszi, amelynek a neve tárolóval kezdődik, majd átadja az eredményt a folyamatnak, és az engedélyt blob-elérésre adja.</span><span class="sxs-lookup"><span data-stu-id="aaae5-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="aaae5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaae5-112">PARAMETERS</span></span>

### <span data-ttu-id="aaae5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aaae5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="aaae5-114">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="aaae5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="aaae5-115">Ha az előző hívás nem sikerül a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="aaae5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="aaae5-116">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="aaae5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="aaae5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="aaae5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="aaae5-118">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="aaae5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="aaae5-119">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használatra a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="aaae5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="aaae5-120">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="aaae5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="aaae5-121">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="aaae5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="aaae5-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="aaae5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="aaae5-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="aaae5-123">-Context</span></span>
<span data-ttu-id="aaae5-124">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="aaae5-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="aaae5-125">A parancsmagot a New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="aaae5-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aaae5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaae5-126">-DefaultProfile</span></span>
<span data-ttu-id="aaae5-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aaae5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaae5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="aaae5-128">-Name</span></span>
<span data-ttu-id="aaae5-129">Egy tárolónevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="aaae5-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="aaae5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaae5-130">-PassThru</span></span>
<span data-ttu-id="aaae5-131">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="aaae5-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aaae5-132">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="aaae5-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aaae5-133">-Engedély</span><span class="sxs-lookup"><span data-stu-id="aaae5-133">-Permission</span></span>
<span data-ttu-id="aaae5-134">A tárolóhoz való nyilvános hozzáférés szintjét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="aaae5-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="aaae5-135">Alapértelmezés szerint a tároló és a benne lévő blobok csak a tárfiók tulajdonosa által érhetők el.</span><span class="sxs-lookup"><span data-stu-id="aaae5-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="aaae5-136">Ha névtelen felhasználóknak szeretné olvasási engedélyeket beállítani egy tárolóhoz és blobjaikhoz, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="aaae5-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="aaae5-137">A névtelen felhasználók a kérés hitelesítése nélkül olvashatják a blobokat egy nyilvánosan elérhető tárolóban.</span><span class="sxs-lookup"><span data-stu-id="aaae5-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="aaae5-138">A paraméter elfogadható értékei a következőek: --Container.</span><span class="sxs-lookup"><span data-stu-id="aaae5-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="aaae5-139">Teljes olvasási hozzáférést biztosít a tárolókhoz és a blobjaikhoz.</span><span class="sxs-lookup"><span data-stu-id="aaae5-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="aaae5-140">Az ügyfelek névtelen kérésen keresztül számba tudják venni a tárolóban lévő blobokat, de a tárfiókban lévő tárolókat nem.</span><span class="sxs-lookup"><span data-stu-id="aaae5-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="aaae5-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="aaae5-141">--Blob.</span></span>
<span data-ttu-id="aaae5-142">Névtelen kérésen keresztül olvasási hozzáférést biztosít egy tárolóban lévő blobadatokhoz, de nem biztosít hozzáférést a tárolóadatokhoz.</span><span class="sxs-lookup"><span data-stu-id="aaae5-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="aaae5-143">Az ügyfelek névtelen kérésekkel nem tudnak blobokat számozni a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="aaae5-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="aaae5-144">--Kikapcsolva.</span><span class="sxs-lookup"><span data-stu-id="aaae5-144">--Off.</span></span>
<span data-ttu-id="aaae5-145">Csak a tárfiók tulajdonosára korlátozza a hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="aaae5-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaae5-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aaae5-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="aaae5-147">A szolgáltatás időkorrekta-intervallumát adja meg másodpercben egy kéréshez.</span><span class="sxs-lookup"><span data-stu-id="aaae5-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="aaae5-148">Ha a megadott időköz eltelik, mielőtt a szolgáltatás feldolgozza a kérelmet, a társzolgáltatás hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="aaae5-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="aaae5-149">Kiszolgálói időkorrekta az egyes kérések esetén.</span><span class="sxs-lookup"><span data-stu-id="aaae5-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="aaae5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaae5-150">CommonParameters</span></span>
<span data-ttu-id="aaae5-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaae5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaae5-152">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaae5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaae5-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaae5-153">INPUTS</span></span>

### <span data-ttu-id="aaae5-154">System.String</span><span class="sxs-lookup"><span data-stu-id="aaae5-154">System.String</span></span>

### <span data-ttu-id="aaae5-155">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aaae5-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aaae5-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aaae5-156">OUTPUTS</span></span>

### <span data-ttu-id="aaae5-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaae5-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="aaae5-158">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aaae5-158">NOTES</span></span>

## <span data-ttu-id="aaae5-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aaae5-159">RELATED LINKS</span></span>

[<span data-ttu-id="aaae5-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaae5-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="aaae5-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaae5-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="aaae5-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="aaae5-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


