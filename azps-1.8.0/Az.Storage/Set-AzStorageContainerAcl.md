---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 75a5ed142952e7b4eae6b5e5995b83079bfd4dc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668545"
---
# <span data-ttu-id="7a58b-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7a58b-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="7a58b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7a58b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a58b-103">A nyilvános hozzáférés engedélyének megadása tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="7a58b-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="7a58b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7a58b-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7a58b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7a58b-105">DESCRIPTION</span></span>
<span data-ttu-id="7a58b-106">A **set-AzStorageContainerAcl** parancsmag a nyilvános hozzáférés engedélyét az Azure-ban megadott tárterülethez állítja.</span><span class="sxs-lookup"><span data-stu-id="7a58b-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="7a58b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7a58b-107">EXAMPLES</span></span>

### <span data-ttu-id="7a58b-108">1. példa: az Azure Storage Container-ACL beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="7a58b-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="7a58b-109">Ez a parancs olyan tárolót hoz létre, amelynek nincs nyilvános hozzáférése.</span><span class="sxs-lookup"><span data-stu-id="7a58b-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="7a58b-110">2. példa: az Azure Storage Container ACL beállítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="7a58b-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="7a58b-111">Ez a parancs minden olyan tároló tárolót beolvas, amelynek a neve tárolóval kezdődik, majd az eredményt a csővezetéken adja meg a blob-hozzáféréshez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="7a58b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7a58b-112">PARAMETERS</span></span>

### <span data-ttu-id="7a58b-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a58b-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7a58b-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="7a58b-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7a58b-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="7a58b-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7a58b-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7a58b-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7a58b-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7a58b-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a58b-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7a58b-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="7a58b-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7a58b-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="7a58b-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7a58b-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="7a58b-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7a58b-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="7a58b-122">The default value is 10.</span></span>

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

### <span data-ttu-id="7a58b-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7a58b-123">-Context</span></span>
<span data-ttu-id="7a58b-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a58b-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="7a58b-125">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="7a58b-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7a58b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a58b-126">-DefaultProfile</span></span>
<span data-ttu-id="7a58b-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a58b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a58b-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7a58b-128">-Name</span></span>
<span data-ttu-id="7a58b-129">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a58b-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="7a58b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a58b-130">-PassThru</span></span>
<span data-ttu-id="7a58b-131">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7a58b-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a58b-132">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7a58b-132">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a58b-133">– Engedély</span><span class="sxs-lookup"><span data-stu-id="7a58b-133">-Permission</span></span>
<span data-ttu-id="7a58b-134">A tárolóhoz való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7a58b-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="7a58b-135">Alapértelmezés szerint a tároló és a bennük lévő festékfoltok csak a tárolási fiók tulajdonosa érhetik el.</span><span class="sxs-lookup"><span data-stu-id="7a58b-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="7a58b-136">Ha a névtelen felhasználóknak olvasási engedélyeket szeretne adni egy tárolóhoz és a festékfoltok-hez, a tároló engedélyeinek beállításával engedélyezheti a nyilvános hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="7a58b-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="7a58b-137">A névtelen felhasználók egy nyilvánosan elérhető tárolóban olvashatják a blob-objektumokat a kérés hitelesítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="7a58b-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="7a58b-138">A paraméter elfogadható értékei a következők:---tároló.</span><span class="sxs-lookup"><span data-stu-id="7a58b-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="7a58b-139">Teljes olvasási hozzáférést biztosít egy tárolóhoz és a Blobs-hoz.</span><span class="sxs-lookup"><span data-stu-id="7a58b-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="7a58b-140">Az ügyfelek névtelen kéréssel enumerálják a tárolóban lévő blob-objektumokat, a tárolási fiókban azonban nem lehet enumerálni a tárolókat.</span><span class="sxs-lookup"><span data-stu-id="7a58b-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="7a58b-141">---BLOB.</span><span class="sxs-lookup"><span data-stu-id="7a58b-141">--Blob.</span></span>
<span data-ttu-id="7a58b-142">Névtelen kéréssel olvasási hozzáférést biztosít a blob-adattárolóhoz, de nem biztosít hozzáférést a tárolók adatainak eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="7a58b-143">Az ügyfelek névtelen kéréssel nem tudják enumerálni a blobokat a tárolóban.</span><span class="sxs-lookup"><span data-stu-id="7a58b-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="7a58b-144">--Off.</span><span class="sxs-lookup"><span data-stu-id="7a58b-144">--Off.</span></span>
<span data-ttu-id="7a58b-145">Korlátozza a hozzáférést csak a tárolási fiók tulajdonosához.</span><span class="sxs-lookup"><span data-stu-id="7a58b-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a58b-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7a58b-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7a58b-147">A szolgáltatás időkorlátját adja meg másodpercben a kéréshez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7a58b-148">Ha a megadott intervallum eltelt, mielőtt a szolgáltatás feldolgozza a kérelmet, a tárolási szolgáltatás hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="7a58b-149">Kiszolgálóoldali időtúllépés az egyes kérésekhez.</span><span class="sxs-lookup"><span data-stu-id="7a58b-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="7a58b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a58b-150">CommonParameters</span></span>
<span data-ttu-id="7a58b-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7a58b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a58b-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a58b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a58b-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a58b-153">INPUTS</span></span>

### <span data-ttu-id="7a58b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="7a58b-154">System.String</span></span>

### <span data-ttu-id="7a58b-155">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7a58b-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7a58b-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a58b-156">OUTPUTS</span></span>

### <span data-ttu-id="7a58b-157">Microsoft. WindowsAzure. Command. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7a58b-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="7a58b-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7a58b-158">NOTES</span></span>

## <span data-ttu-id="7a58b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a58b-159">RELATED LINKS</span></span>

[<span data-ttu-id="7a58b-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7a58b-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="7a58b-161">Új – AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7a58b-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="7a58b-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7a58b-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)


