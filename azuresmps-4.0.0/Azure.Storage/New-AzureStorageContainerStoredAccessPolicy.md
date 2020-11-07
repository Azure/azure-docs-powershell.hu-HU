---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95d5afafbed6ab6e3ba81cbfd509fd7b531217e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671808"
---
# <span data-ttu-id="a1425-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1425-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="a1425-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1425-102">SYNOPSIS</span></span>
<span data-ttu-id="a1425-103">Tárol egy tárolt hozzáférési házirendet egy Azure tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="a1425-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="a1425-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1425-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1425-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1425-105">DESCRIPTION</span></span>
<span data-ttu-id="a1425-106">A **New-AzureStorageContainerStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="a1425-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="a1425-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a1425-107">EXAMPLES</span></span>

### <span data-ttu-id="a1425-108">Példa 1: tárolt hozzáférés-házirend létrehozása tároló tárolóban</span><span class="sxs-lookup"><span data-stu-id="a1425-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="a1425-109">A parancs létrehoz egy Policy01 nevű Access-házirendet a MyContainer nevű tároló tárolóban.</span><span class="sxs-lookup"><span data-stu-id="a1425-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="a1425-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1425-110">PARAMETERS</span></span>

### <span data-ttu-id="a1425-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1425-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a1425-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a1425-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a1425-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a1425-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a1425-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a1425-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a1425-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a1425-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a1425-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1425-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a1425-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="a1425-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a1425-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="a1425-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a1425-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="a1425-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a1425-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="a1425-120">The default value is 10.</span></span>

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

### <span data-ttu-id="a1425-121">-Container</span><span class="sxs-lookup"><span data-stu-id="a1425-121">-Container</span></span>
<span data-ttu-id="a1425-122">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1425-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="a1425-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a1425-123">-Context</span></span>
<span data-ttu-id="a1425-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1425-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a1425-125">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a1425-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a1425-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a1425-126">-ExpiryTime</span></span>
<span data-ttu-id="a1425-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="a1425-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a1425-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="a1425-128">-Permission</span></span>
<span data-ttu-id="a1425-129">A tárolóhoz való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1425-129">Specifies the level of public access to this container.</span></span>

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

### <span data-ttu-id="a1425-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a1425-130">-Policy</span></span>
<span data-ttu-id="a1425-131">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="a1425-131">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="a1425-132">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a1425-132">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a1425-133">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="a1425-133">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a1425-134">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="a1425-134">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a1425-135">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="a1425-135">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a1425-136">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a1425-136">-StartTime</span></span>
<span data-ttu-id="a1425-137">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="a1425-137">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a1425-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1425-138">CommonParameters</span></span>
<span data-ttu-id="a1425-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1425-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1425-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1425-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1425-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1425-141">INPUTS</span></span>

## <span data-ttu-id="a1425-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1425-142">OUTPUTS</span></span>

## <span data-ttu-id="a1425-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1425-143">NOTES</span></span>

## <span data-ttu-id="a1425-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1425-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1425-145">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1425-145">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a1425-146">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1425-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a1425-147">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1425-147">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="a1425-148">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a1425-148">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


