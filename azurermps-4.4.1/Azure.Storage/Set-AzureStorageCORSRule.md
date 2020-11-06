---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503355"
---
# <span data-ttu-id="e2241-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e2241-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="e2241-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2241-102">SYNOPSIS</span></span>
<span data-ttu-id="e2241-103">A CORS szabályait állítja be.</span><span class="sxs-lookup"><span data-stu-id="e2241-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2241-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2241-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e2241-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2241-105">DESCRIPTION</span></span>
<span data-ttu-id="e2241-106">A **set-AzureStorageCORSRule** parancsmag a Cross-Origin Resource Sharing (CORS) szabályait állítja be egy Azure-tárterület szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="e2241-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="e2241-107">Az e parancsmaghoz tartozó tárolási szolgáltatások típusa blob, táblázat, várólista és fájl.</span><span class="sxs-lookup"><span data-stu-id="e2241-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="e2241-108">Ez a parancsmag felülírja a meglévő szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e2241-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="e2241-109">Az aktuális szabályok megtekintéséhez használja az Get-AzureStorageCORSRule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e2241-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="e2241-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e2241-110">EXAMPLES</span></span>

### <span data-ttu-id="e2241-111">1. példa: CORS szabályok hozzárendelése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="e2241-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e2241-112">Az első parancs szabályok egy sorát rendeli a $CorsRules változóhoz.</span><span class="sxs-lookup"><span data-stu-id="e2241-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="e2241-113">Ebben a parancsban a standard a blokk több sorára terjed ki.</span><span class="sxs-lookup"><span data-stu-id="e2241-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="e2241-114">A második parancs a $CorsRules a blob-szolgáltatás típusba rendeli a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e2241-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="e2241-115">2. példa: CORS-szabály tulajdonságainak módosítása a blob-szolgáltatásokhoz</span><span class="sxs-lookup"><span data-stu-id="e2241-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="e2241-116">Az első parancs a **Get-AzureStorageCORSRule** parancsmaggal kapja meg a blob-típus aktuális CORS szabályait.</span><span class="sxs-lookup"><span data-stu-id="e2241-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="e2241-117">A parancs a $CorsRules Array változóban tárolja a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e2241-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="e2241-118">A második és a harmadik parancs a $CorsRules első szabályát módosítja.</span><span class="sxs-lookup"><span data-stu-id="e2241-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="e2241-119">A végleges parancs a $CorsRules a blob-szolgáltatás típusba rendeli a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e2241-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="e2241-120">A módosított szabályok felülírják az aktuális CORS-szabályokat.</span><span class="sxs-lookup"><span data-stu-id="e2241-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="e2241-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2241-121">PARAMETERS</span></span>

### <span data-ttu-id="e2241-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2241-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e2241-123">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="e2241-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e2241-124">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="e2241-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e2241-125">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="e2241-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e2241-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e2241-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e2241-127">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2241-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e2241-128">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="e2241-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e2241-129">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="e2241-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e2241-130">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="e2241-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e2241-131">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="e2241-131">The default value is 10.</span></span>

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

### <span data-ttu-id="e2241-132">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e2241-132">-Context</span></span>
<span data-ttu-id="e2241-133">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2241-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e2241-134">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e2241-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e2241-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="e2241-135">-CorsRules</span></span>
<span data-ttu-id="e2241-136">A CORS szabályok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2241-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="e2241-137">A meglévő szabályok a Get-AzureStorageCORSRule parancsmag használatával olvashatók le.</span><span class="sxs-lookup"><span data-stu-id="e2241-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2241-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2241-138">-PassThru</span></span>
<span data-ttu-id="e2241-139">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="e2241-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="e2241-140">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="e2241-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e2241-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e2241-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e2241-142">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e2241-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e2241-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="e2241-143">-ServiceType</span></span>
<span data-ttu-id="e2241-144">Annak az Azure Storage Service-típusnak a megadása, amelyhez a parancsmag szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="e2241-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="e2241-145">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e2241-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e2241-146">BLOB</span><span class="sxs-lookup"><span data-stu-id="e2241-146">Blob</span></span> 
- <span data-ttu-id="e2241-147">Táblázat</span><span class="sxs-lookup"><span data-stu-id="e2241-147">Table</span></span> 
- <span data-ttu-id="e2241-148">Várólista</span><span class="sxs-lookup"><span data-stu-id="e2241-148">Queue</span></span> 
- <span data-ttu-id="e2241-149">Fájl</span><span class="sxs-lookup"><span data-stu-id="e2241-149">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2241-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2241-150">CommonParameters</span></span>
<span data-ttu-id="e2241-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2241-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2241-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2241-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2241-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2241-153">INPUTS</span></span>

### <span data-ttu-id="e2241-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2241-154">IStorageContext</span></span>

<span data-ttu-id="e2241-155">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e2241-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e2241-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2241-156">OUTPUTS</span></span>

### <span data-ttu-id="e2241-157">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="e2241-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="e2241-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2241-158">NOTES</span></span>

## <span data-ttu-id="e2241-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2241-159">RELATED LINKS</span></span>

[<span data-ttu-id="e2241-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e2241-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="e2241-161">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e2241-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e2241-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="e2241-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


