---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: 7bb670dd507a21769bd1b22cd65703f74d459923
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668543"
---
# <span data-ttu-id="db28e-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="db28e-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="db28e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db28e-102">SYNOPSIS</span></span>
<span data-ttu-id="db28e-103">A CORS szabályait állítja be.</span><span class="sxs-lookup"><span data-stu-id="db28e-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="db28e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db28e-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="db28e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="db28e-105">DESCRIPTION</span></span>
<span data-ttu-id="db28e-106">A **set-AzStorageCORSRule** parancsmag a Cross-Origin Resource Sharing (CORS) szabályait állítja be egy Azure-tárterület szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="db28e-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="db28e-107">Az e parancsmaghoz tartozó tárolási szolgáltatások típusa blob, táblázat, várólista és fájl.</span><span class="sxs-lookup"><span data-stu-id="db28e-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="db28e-108">Ez a parancsmag felülírja a meglévő szabályokat.</span><span class="sxs-lookup"><span data-stu-id="db28e-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="db28e-109">Az aktuális szabályok megtekintéséhez használja az Get-AzStorageCORSRule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db28e-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="db28e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="db28e-110">EXAMPLES</span></span>

### <span data-ttu-id="db28e-111">1. példa: CORS szabályok hozzárendelése a blob-szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="db28e-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="db28e-112">Az első parancs szabályok egy sorát rendeli a $CorsRules változóhoz.</span><span class="sxs-lookup"><span data-stu-id="db28e-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="db28e-113">Ebben a parancsban a standard a blokk több sorára terjed ki.</span><span class="sxs-lookup"><span data-stu-id="db28e-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="db28e-114">A második parancs a $CorsRules a blob-szolgáltatás típusba rendeli a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="db28e-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="db28e-115">2. példa: CORS-szabály tulajdonságainak módosítása a blob-szolgáltatásokhoz</span><span class="sxs-lookup"><span data-stu-id="db28e-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="db28e-116">Az első parancs a **Get-AzStorageCORSRule** parancsmaggal kapja meg a blob-típus aktuális CORS szabályait.</span><span class="sxs-lookup"><span data-stu-id="db28e-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="db28e-117">A parancs a $CorsRules Array változóban tárolja a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="db28e-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="db28e-118">A második és a harmadik parancs a $CorsRules első szabályát módosítja.</span><span class="sxs-lookup"><span data-stu-id="db28e-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="db28e-119">A végleges parancs a $CorsRules a blob-szolgáltatás típusba rendeli a szabályokat.</span><span class="sxs-lookup"><span data-stu-id="db28e-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="db28e-120">A módosított szabályok felülírják az aktuális CORS-szabályokat.</span><span class="sxs-lookup"><span data-stu-id="db28e-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="db28e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db28e-121">PARAMETERS</span></span>

### <span data-ttu-id="db28e-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="db28e-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="db28e-123">Az ügyféloldali időtúllépési intervallumot adja meg másodpercben egy szolgáltatási kérelemben.</span><span class="sxs-lookup"><span data-stu-id="db28e-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="db28e-124">Ha az előző hívás nem sikerült a megadott intervallumban, ez a parancsmag újból megkísérli a kérést.</span><span class="sxs-lookup"><span data-stu-id="db28e-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="db28e-125">Ha ez a parancsmag nem kap sikeres választ az intervallum lejárta előtt, ez a parancsmag hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="db28e-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="db28e-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="db28e-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="db28e-127">A párhuzamos hálózati hívásokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="db28e-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="db28e-128">Ezt a paramétert használva korlátozhatja a párhuzamosságot a helyi processzor és a sávszélesség-használat szabályozásához az egyidejű hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="db28e-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="db28e-129">A megadott érték abszolút szám, amelyet nem szoroz meg az alapszámlálóval.</span><span class="sxs-lookup"><span data-stu-id="db28e-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="db28e-130">Ez a paraméter segíthet csökkenteni a hálózati kapcsolat problémáit a kis sávszélességű környezetekben (például 100 kilobit/másodperc).</span><span class="sxs-lookup"><span data-stu-id="db28e-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="db28e-131">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="db28e-131">The default value is 10.</span></span>

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

### <span data-ttu-id="db28e-132">-Környezet</span><span class="sxs-lookup"><span data-stu-id="db28e-132">-Context</span></span>
<span data-ttu-id="db28e-133">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db28e-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="db28e-134">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="db28e-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="db28e-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="db28e-135">-CorsRules</span></span>
<span data-ttu-id="db28e-136">A CORS szabályok tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db28e-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="db28e-137">A meglévő szabályok a Get-AzStorageCORSRule parancsmag használatával olvashatók le.</span><span class="sxs-lookup"><span data-stu-id="db28e-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db28e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db28e-138">-DefaultProfile</span></span>
<span data-ttu-id="db28e-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db28e-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db28e-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db28e-140">-PassThru</span></span>
<span data-ttu-id="db28e-141">Jelzi, hogy ez a parancsmag olyan logikai értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="db28e-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="db28e-142">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="db28e-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="db28e-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="db28e-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="db28e-144">A kérés kiszolgálói részének időtúllépési időszakát adja meg.</span><span class="sxs-lookup"><span data-stu-id="db28e-144">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="db28e-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="db28e-145">-ServiceType</span></span>
<span data-ttu-id="db28e-146">Annak az Azure Storage Service-típusnak a megadása, amelyhez a parancsmag szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="db28e-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="db28e-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="db28e-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db28e-148">BLOB</span><span class="sxs-lookup"><span data-stu-id="db28e-148">Blob</span></span> 
- <span data-ttu-id="db28e-149">Táblázat</span><span class="sxs-lookup"><span data-stu-id="db28e-149">Table</span></span> 
- <span data-ttu-id="db28e-150">Várólista</span><span class="sxs-lookup"><span data-stu-id="db28e-150">Queue</span></span> 
- <span data-ttu-id="db28e-151">Fájl</span><span class="sxs-lookup"><span data-stu-id="db28e-151">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db28e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db28e-152">CommonParameters</span></span>
<span data-ttu-id="db28e-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db28e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db28e-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db28e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db28e-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db28e-155">INPUTS</span></span>

### <span data-ttu-id="db28e-156">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="db28e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="db28e-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db28e-157">OUTPUTS</span></span>

### <span data-ttu-id="db28e-158">Microsoft. WindowsAzure. Command. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="db28e-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="db28e-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db28e-159">NOTES</span></span>

## <span data-ttu-id="db28e-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db28e-160">RELATED LINKS</span></span>

[<span data-ttu-id="db28e-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="db28e-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="db28e-162">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="db28e-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="db28e-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="db28e-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


