---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: a3abd3a6e0b3c3dcc04de6ca4bc69c6ed80bcab9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849798"
---
# <span data-ttu-id="580c3-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="580c3-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="580c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="580c3-102">SYNOPSIS</span></span>
<span data-ttu-id="580c3-103">Tárolt hozzáférési házirendet hoz létre egy tárterület-megosztásban.</span><span class="sxs-lookup"><span data-stu-id="580c3-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="580c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="580c3-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="580c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="580c3-105">DESCRIPTION</span></span>
<span data-ttu-id="580c3-106">A **New-AzureStorageShareStoredAccessPolicy** parancsmag létrehoz egy tárolt hozzáférési házirendet egy Azure-tárhelyen.</span><span class="sxs-lookup"><span data-stu-id="580c3-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="580c3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="580c3-107">EXAMPLES</span></span>

### <span data-ttu-id="580c3-108">Példa 1: tárolt hozzáférés-házirend létrehozása egy megosztásban</span><span class="sxs-lookup"><span data-stu-id="580c3-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="580c3-109">Ez a parancs egy olyan tárolt hozzáférési házirendet hoz létre, amely teljes hozzáféréssel rendelkezik a megosztásban.</span><span class="sxs-lookup"><span data-stu-id="580c3-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="580c3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="580c3-110">PARAMETERS</span></span>

### <span data-ttu-id="580c3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="580c3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="580c3-112">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="580c3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="580c3-113">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="580c3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="580c3-114">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="580c3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="580c3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="580c3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="580c3-116">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="580c3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="580c3-117">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="580c3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="580c3-118">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="580c3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="580c3-119">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="580c3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="580c3-120">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="580c3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="580c3-121">-Környezet</span><span class="sxs-lookup"><span data-stu-id="580c3-121">-Context</span></span>
<span data-ttu-id="580c3-122">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="580c3-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="580c3-123">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="580c3-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="580c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="580c3-124">-DefaultProfile</span></span>
<span data-ttu-id="580c3-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="580c3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="580c3-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="580c3-126">-ExpiryTime</span></span>
<span data-ttu-id="580c3-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="580c3-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580c3-128">– Engedély</span><span class="sxs-lookup"><span data-stu-id="580c3-128">-Permission</span></span>
<span data-ttu-id="580c3-129">A tárolt elérési házirend engedélyeinek megadása a tárterület-megosztás vagy-fájlok eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="580c3-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="580c3-130">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="580c3-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580c3-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="580c3-131">-Policy</span></span>
<span data-ttu-id="580c3-132">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="580c3-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580c3-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="580c3-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="580c3-134">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="580c3-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="580c3-135">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="580c3-135">-ShareName</span></span>
<span data-ttu-id="580c3-136">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="580c3-136">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="580c3-137">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="580c3-137">-StartTime</span></span>
<span data-ttu-id="580c3-138">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="580c3-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="580c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="580c3-139">CommonParameters</span></span>
<span data-ttu-id="580c3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="580c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="580c3-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="580c3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="580c3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="580c3-142">INPUTS</span></span>

### <span data-ttu-id="580c3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="580c3-143">System.String</span></span>

### <span data-ttu-id="580c3-144">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="580c3-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="580c3-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="580c3-145">OUTPUTS</span></span>

### <span data-ttu-id="580c3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="580c3-146">System.String</span></span>

## <span data-ttu-id="580c3-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="580c3-147">NOTES</span></span>

## <span data-ttu-id="580c3-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="580c3-148">RELATED LINKS</span></span>

[<span data-ttu-id="580c3-149">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="580c3-149">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="580c3-150">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="580c3-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="580c3-151">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="580c3-151">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="580c3-152">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="580c3-152">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
