---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 5e4a6c5ad69ae8f31564335a410a67ec58181f3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848562"
---
# <span data-ttu-id="80425-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80425-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="80425-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80425-102">SYNOPSIS</span></span>
<span data-ttu-id="80425-103">Tárolhatja a tárolt elérési házirendeket egy tárterület-megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="80425-103">Gets stored access policies for a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80425-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80425-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="80425-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80425-105">DESCRIPTION</span></span>
<span data-ttu-id="80425-106">A **Get-AzureStorageShareStoredAccessPolicy** parancsmag egy Azure-tárterület elérési házirendjeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80425-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="80425-107">Ha egy adott házirendet szeretne kapni, adja meg a nevet név szerint.</span><span class="sxs-lookup"><span data-stu-id="80425-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="80425-108">Példák</span><span class="sxs-lookup"><span data-stu-id="80425-108">EXAMPLES</span></span>

### <span data-ttu-id="80425-109">Példa 1: tárolt hozzáférés-házirend beszerzése megosztásban</span><span class="sxs-lookup"><span data-stu-id="80425-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="80425-110">Ez a parancs a ContosoShare nevű GeneralPolicy nevű tárolt hozzáférés-házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="80425-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="80425-111">2. példa: az összes tárolt Access-házirend beolvasása a megosztásban</span><span class="sxs-lookup"><span data-stu-id="80425-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="80425-112">Ez a parancs a ContosoShare-ban tárolja az összes tárolt elérési házirendet.</span><span class="sxs-lookup"><span data-stu-id="80425-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="80425-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80425-113">PARAMETERS</span></span>

### <span data-ttu-id="80425-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="80425-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="80425-115">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="80425-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="80425-116">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="80425-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="80425-117">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="80425-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="80425-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="80425-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="80425-119">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="80425-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="80425-120">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="80425-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="80425-121">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="80425-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="80425-122">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="80425-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="80425-123">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="80425-123">The default value is 10.</span></span>

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

### <span data-ttu-id="80425-124">-Környezet</span><span class="sxs-lookup"><span data-stu-id="80425-124">-Context</span></span>
<span data-ttu-id="80425-125">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80425-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="80425-126">Környezet beolvasásához használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="80425-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="80425-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80425-127">-DefaultProfile</span></span>
<span data-ttu-id="80425-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80425-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80425-129">-Házirend</span><span class="sxs-lookup"><span data-stu-id="80425-129">-Policy</span></span>
<span data-ttu-id="80425-130">Annak a tárolt hozzáférési házirendnek a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="80425-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80425-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="80425-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="80425-132">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="80425-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="80425-133">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="80425-133">-ShareName</span></span>
<span data-ttu-id="80425-134">Azt a tárterület-megosztási nevet adja meg, amelyhez a parancsmag házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="80425-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80425-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80425-135">CommonParameters</span></span>
<span data-ttu-id="80425-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80425-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80425-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80425-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80425-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80425-138">INPUTS</span></span>

### <span data-ttu-id="80425-139">System. String</span><span class="sxs-lookup"><span data-stu-id="80425-139">System.String</span></span>

### <span data-ttu-id="80425-140">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="80425-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="80425-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80425-141">OUTPUTS</span></span>

### <span data-ttu-id="80425-142">Microsoft. WindowsAzure. Storage. file. SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="80425-142">Microsoft.WindowsAzure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="80425-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80425-143">NOTES</span></span>

## <span data-ttu-id="80425-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80425-144">RELATED LINKS</span></span>

[<span data-ttu-id="80425-145">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="80425-145">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="80425-146">Új – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80425-146">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="80425-147">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80425-147">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="80425-148">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="80425-148">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
