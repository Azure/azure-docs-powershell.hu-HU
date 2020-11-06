---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3429c142ce31f8cd08786e180b6725130501ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493916"
---
# <span data-ttu-id="09c72-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="09c72-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="09c72-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="09c72-102">SYNOPSIS</span></span>
<span data-ttu-id="09c72-103">Tárol egy tárolt hozzáférési házirendet egy Azure tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="09c72-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09c72-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="09c72-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="09c72-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="09c72-105">DESCRIPTION</span></span>
<span data-ttu-id="09c72-106">A **New-AzureStorageContainerStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="09c72-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="09c72-107">Példák</span><span class="sxs-lookup"><span data-stu-id="09c72-107">EXAMPLES</span></span>

### <span data-ttu-id="09c72-108">Példa 1: tárolt hozzáférés-házirend létrehozása tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="09c72-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="09c72-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyContainer nevű tároló tárolóban.</span><span class="sxs-lookup"><span data-stu-id="09c72-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="09c72-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="09c72-110">PARAMETERS</span></span>

### <span data-ttu-id="09c72-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09c72-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09c72-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="09c72-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09c72-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="09c72-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09c72-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="09c72-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09c72-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09c72-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09c72-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="09c72-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="09c72-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="09c72-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="09c72-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="09c72-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="09c72-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="09c72-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="09c72-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="09c72-120">The default value is 10.</span></span>

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

### <span data-ttu-id="09c72-121">-Container</span><span class="sxs-lookup"><span data-stu-id="09c72-121">-Container</span></span>
<span data-ttu-id="09c72-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09c72-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="09c72-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="09c72-123">-Context</span></span>
<span data-ttu-id="09c72-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09c72-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="09c72-125">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="09c72-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="09c72-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="09c72-126">-ExpiryTime</span></span>
<span data-ttu-id="09c72-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="09c72-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="09c72-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="09c72-128">-Permission</span></span>
<span data-ttu-id="09c72-129">A tároló elérési házirendjében szereplő engedélyeket adja meg.</span><span class="sxs-lookup"><span data-stu-id="09c72-129">Specifies permissions in the stored access policy to access the container.</span></span>

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

### <span data-ttu-id="09c72-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="09c72-130">-Policy</span></span>
<span data-ttu-id="09c72-131">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="09c72-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="09c72-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09c72-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09c72-133">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="09c72-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09c72-134">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="09c72-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09c72-135">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="09c72-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09c72-136">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="09c72-136">-StartTime</span></span>
<span data-ttu-id="09c72-137">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="09c72-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="09c72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09c72-138">CommonParameters</span></span>
<span data-ttu-id="09c72-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="09c72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09c72-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09c72-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09c72-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="09c72-141">INPUTS</span></span>

### <span data-ttu-id="09c72-142">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="09c72-142">String</span></span>

<span data-ttu-id="09c72-143">A "Container" paraméter a pipeline "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="09c72-143">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="09c72-144">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09c72-144">IStorageContext</span></span>

<span data-ttu-id="09c72-145">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="09c72-145">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="09c72-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09c72-146">OUTPUTS</span></span>

### <span data-ttu-id="09c72-147">System. String</span><span class="sxs-lookup"><span data-stu-id="09c72-147">System.String</span></span>

## <span data-ttu-id="09c72-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="09c72-148">NOTES</span></span>

## <span data-ttu-id="09c72-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09c72-149">RELATED LINKS</span></span>

[<span data-ttu-id="09c72-150">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="09c72-150">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="09c72-151">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="09c72-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="09c72-152">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="09c72-152">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="09c72-153">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="09c72-153">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


