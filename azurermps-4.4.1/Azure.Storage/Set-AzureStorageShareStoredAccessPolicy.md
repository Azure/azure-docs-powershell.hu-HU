---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 43e9ccca185a68d3c7b0e6cca118bb2cd63247bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503323"
---
# <span data-ttu-id="60e59-101">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60e59-101">Set-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="60e59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="60e59-102">SYNOPSIS</span></span>
<span data-ttu-id="60e59-103">A tárolt hozzáférési házirendet frissíti egy tárterület-megosztáson.</span><span class="sxs-lookup"><span data-stu-id="60e59-103">Updates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60e59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="60e59-104">SYNTAX</span></span>

```
Set-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="60e59-105">DESCRIPTION</span></span>
<span data-ttu-id="60e59-106">A **set-AzureStorageShareStoredAccessPolicy** parancsmag egy Azure tárhely-megosztáson frissíti a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="60e59-106">The **Set-AzureStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="60e59-107">Példák</span><span class="sxs-lookup"><span data-stu-id="60e59-107">EXAMPLES</span></span>

### <span data-ttu-id="60e59-108">Példa 1: tárolt hozzáférés-házirend frissítése a tárterület-megosztásban</span><span class="sxs-lookup"><span data-stu-id="60e59-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="60e59-109">Ez a parancs olyan tárolt hozzáférés-házirendet frissít, amely teljes hozzáféréssel rendelkezik egy megosztásban.</span><span class="sxs-lookup"><span data-stu-id="60e59-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="60e59-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="60e59-110">PARAMETERS</span></span>

### <span data-ttu-id="60e59-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60e59-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="60e59-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="60e59-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="60e59-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="60e59-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="60e59-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="60e59-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="60e59-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="60e59-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="60e59-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="60e59-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="60e59-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="60e59-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="60e59-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="60e59-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="60e59-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="60e59-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="60e59-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="60e59-120">The default value is 10.</span></span>

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

### <span data-ttu-id="60e59-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="60e59-121">-Context</span></span>
<span data-ttu-id="60e59-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60e59-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="60e59-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="60e59-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="60e59-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="60e59-124">-ExpiryTime</span></span>
<span data-ttu-id="60e59-125">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="60e59-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="60e59-126">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="60e59-126">-NoExpiryTime</span></span>
<span data-ttu-id="60e59-127">Jelzi, hogy ez a parancsmag törli a **ExpiryTime** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="60e59-127">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e59-128">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="60e59-128">-NoStartTime</span></span>
<span data-ttu-id="60e59-129">Azt jelzi, hogy ez a parancsmag törli az **időpont** tulajdonságot a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="60e59-129">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e59-130">– Engedély</span><span class="sxs-lookup"><span data-stu-id="60e59-130">-Permission</span></span>
<span data-ttu-id="60e59-131">A tárolt elérési házirend engedélyeinek megadása az alatta lévő megosztás vagy fájlok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="60e59-131">Specifies permissions in the stored access policy to access the share or files under it.</span></span>

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

### <span data-ttu-id="60e59-132">-Házirend</span><span class="sxs-lookup"><span data-stu-id="60e59-132">-Policy</span></span>
<span data-ttu-id="60e59-133">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60e59-133">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="60e59-134">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="60e59-134">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="60e59-135">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="60e59-135">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="60e59-136">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="60e59-136">-ShareName</span></span>
<span data-ttu-id="60e59-137">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="60e59-137">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="60e59-138">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="60e59-138">-StartTime</span></span>
<span data-ttu-id="60e59-139">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="60e59-139">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="60e59-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="60e59-140">-Confirm</span></span>
<span data-ttu-id="60e59-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="60e59-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e59-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e59-142">-WhatIf</span></span>
<span data-ttu-id="60e59-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="60e59-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60e59-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="60e59-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e59-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e59-145">CommonParameters</span></span>
<span data-ttu-id="60e59-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="60e59-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e59-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60e59-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e59-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="60e59-148">INPUTS</span></span>

### <span data-ttu-id="60e59-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="60e59-149">IStorageContext</span></span>

<span data-ttu-id="60e59-150">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="60e59-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="60e59-151">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="60e59-151">String</span></span>

<span data-ttu-id="60e59-152">A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="60e59-152">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="60e59-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60e59-153">OUTPUTS</span></span>

### <span data-ttu-id="60e59-154">System. String</span><span class="sxs-lookup"><span data-stu-id="60e59-154">System.String</span></span>

## <span data-ttu-id="60e59-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="60e59-155">NOTES</span></span>

## <span data-ttu-id="60e59-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60e59-156">RELATED LINKS</span></span>

[<span data-ttu-id="60e59-157">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60e59-157">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="60e59-158">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="60e59-158">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="60e59-159">Új – AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60e59-159">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="60e59-160">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="60e59-160">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)
