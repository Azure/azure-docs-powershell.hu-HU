---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2eaa58523ef71d90aa7ef6566d18c050fe16a51f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496716"
---
# <span data-ttu-id="30250-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30250-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="30250-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30250-102">SYNOPSIS</span></span>
<span data-ttu-id="30250-103">Tárolt hozzáférési házirendet hoz létre egy tárterület-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="30250-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30250-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30250-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="30250-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30250-105">DESCRIPTION</span></span>
<span data-ttu-id="30250-106">A **New-AzureStorageShareStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárhelyen.</span><span class="sxs-lookup"><span data-stu-id="30250-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="30250-107">Példák</span><span class="sxs-lookup"><span data-stu-id="30250-107">EXAMPLES</span></span>

### <span data-ttu-id="30250-108">Példa 1: tárolt hozzáférés-házirend létrehozása egy megosztásban</span><span class="sxs-lookup"><span data-stu-id="30250-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="30250-109">Ez a parancs egy olyan tárolt hozzáférési házirendet hoz létre, amely teljes hozzáféréssel rendelkezik a megosztásban.</span><span class="sxs-lookup"><span data-stu-id="30250-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="30250-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30250-110">PARAMETERS</span></span>

### <span data-ttu-id="30250-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30250-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="30250-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="30250-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="30250-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="30250-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="30250-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="30250-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="30250-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="30250-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="30250-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="30250-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="30250-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="30250-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="30250-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="30250-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="30250-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="30250-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="30250-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="30250-120">The default value is 10.</span></span>

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

### <span data-ttu-id="30250-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="30250-121">-Context</span></span>
<span data-ttu-id="30250-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30250-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="30250-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="30250-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="30250-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="30250-124">-ExpiryTime</span></span>
<span data-ttu-id="30250-125">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="30250-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30250-126">– Engedély</span><span class="sxs-lookup"><span data-stu-id="30250-126">-Permission</span></span>
<span data-ttu-id="30250-127">A tárolt elérési házirend engedélyeinek megadása a tárterület-megosztás vagy-fájlok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="30250-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30250-128">-Házirend</span><span class="sxs-lookup"><span data-stu-id="30250-128">-Policy</span></span>
<span data-ttu-id="30250-129">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30250-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30250-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="30250-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="30250-131">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="30250-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="30250-132">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="30250-132">-ShareName</span></span>
<span data-ttu-id="30250-133">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="30250-133">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30250-134">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="30250-134">-StartTime</span></span>
<span data-ttu-id="30250-135">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="30250-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30250-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30250-136">CommonParameters</span></span>
<span data-ttu-id="30250-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30250-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30250-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30250-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30250-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30250-139">INPUTS</span></span>

### <span data-ttu-id="30250-140">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="30250-140">IStorageContext</span></span>

<span data-ttu-id="30250-141">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="30250-141">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="30250-142">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="30250-142">String</span></span>

<span data-ttu-id="30250-143">A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="30250-143">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="30250-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30250-144">OUTPUTS</span></span>

### <span data-ttu-id="30250-145">System. String</span><span class="sxs-lookup"><span data-stu-id="30250-145">System.String</span></span>

## <span data-ttu-id="30250-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30250-146">NOTES</span></span>

## <span data-ttu-id="30250-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30250-147">RELATED LINKS</span></span>

[<span data-ttu-id="30250-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30250-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="30250-149">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="30250-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="30250-150">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30250-150">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="30250-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30250-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
