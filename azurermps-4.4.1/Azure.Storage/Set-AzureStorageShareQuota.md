---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d1db19d4b49815f5c4e9c6a413008e55707c291b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503328"
---
# <span data-ttu-id="06ff4-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="06ff4-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="06ff4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="06ff4-103">A megosztás tárterület-kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06ff4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06ff4-104">SYNTAX</span></span>

### <span data-ttu-id="06ff4-105">Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="06ff4-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="06ff4-106">Megosztása</span><span class="sxs-lookup"><span data-stu-id="06ff4-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="06ff4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="06ff4-107">DESCRIPTION</span></span>
<span data-ttu-id="06ff4-108">A **set-AzureStorageShareQuota** parancsmag a megadott megosztás tárolási kapacitását adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="06ff4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="06ff4-109">EXAMPLES</span></span>

### <span data-ttu-id="06ff4-110">1. példa: egy megosztás tárterület-kapacitásának beállítása</span><span class="sxs-lookup"><span data-stu-id="06ff4-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="06ff4-111">Ez a parancs beállítja a ContosoShare01 nevű megosztás 1024 GB-ra való tárolási kapacitását.</span><span class="sxs-lookup"><span data-stu-id="06ff4-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="06ff4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="06ff4-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06ff4-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="06ff4-114">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="06ff4-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="06ff4-115">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="06ff4-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="06ff4-116">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="06ff4-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="06ff4-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="06ff4-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="06ff4-118">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="06ff4-119">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="06ff4-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="06ff4-120">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="06ff4-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="06ff4-121">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="06ff4-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="06ff4-122">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="06ff4-122">The default value is 10.</span></span>

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

### <span data-ttu-id="06ff4-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="06ff4-123">-Context</span></span>
<span data-ttu-id="06ff4-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="06ff4-125">A tárolási környezet eléréséhez használja a [New-AzureStorageContext](./New-AzureStorageContext.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="06ff4-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ff4-126">-Kvóta</span><span class="sxs-lookup"><span data-stu-id="06ff4-126">-Quota</span></span>
<span data-ttu-id="06ff4-127">A kvóta értékét gigabájtban (GB) adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ff4-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="06ff4-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="06ff4-129">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="06ff4-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="06ff4-130">-Share (megosztás)</span><span class="sxs-lookup"><span data-stu-id="06ff4-130">-Share</span></span>
<span data-ttu-id="06ff4-131">Itt adhatja meg azt a **CloudFileShare** -objektumot, amely azt a megosztást jelképezi, amelyhez a parancsmagok kvótát állítanak be.</span><span class="sxs-lookup"><span data-stu-id="06ff4-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="06ff4-132">**CloudFileShare** objektum beolvasásához használja az Get-AzureStorageShare parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="06ff4-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ff4-133">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="06ff4-133">-ShareName</span></span>
<span data-ttu-id="06ff4-134">Annak a fájlnak a nevét adja meg, amelyhez kvótát szeretne beállítani.</span><span class="sxs-lookup"><span data-stu-id="06ff4-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06ff4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ff4-135">CommonParameters</span></span>
<span data-ttu-id="06ff4-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06ff4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ff4-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ff4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ff4-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06ff4-138">INPUTS</span></span>

### <span data-ttu-id="06ff4-139">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="06ff4-139">IStorageContext</span></span>

<span data-ttu-id="06ff4-140">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="06ff4-140">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="06ff4-141">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="06ff4-141">CloudFileShare</span></span>

<span data-ttu-id="06ff4-142">A "share" paraméter értéke "CloudFileShare" típusú értéket ad a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="06ff4-142">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

### <span data-ttu-id="06ff4-143">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="06ff4-143">String</span></span>

<span data-ttu-id="06ff4-144">A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="06ff4-144">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="06ff4-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06ff4-145">OUTPUTS</span></span>

### <span data-ttu-id="06ff4-146">Microsoft. WindowsAzure. Storage. file. FileShareProperties</span><span class="sxs-lookup"><span data-stu-id="06ff4-146">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="06ff4-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06ff4-147">NOTES</span></span>

## <span data-ttu-id="06ff4-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06ff4-148">RELATED LINKS</span></span>

[<span data-ttu-id="06ff4-149">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="06ff4-149">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="06ff4-150">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="06ff4-150">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="06ff4-151">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="06ff4-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
