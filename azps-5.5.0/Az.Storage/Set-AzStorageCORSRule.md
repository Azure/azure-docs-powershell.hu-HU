---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157946"
---
# <span data-ttu-id="3d2ac-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3d2ac-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="3d2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2ac-103">Beállítja egy társzolgáltatástípus CORS-szabályait.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="3d2ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d2ac-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3d2ac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="3d2ac-106">A **Set-AzStorageCORSRule** parancsmag beállítja a források közötti erőforrás-megosztási (CORS) szabályokat egy adott Típusú Azure Storage-szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="3d2ac-107">A parancsmag társzolgáltatásának típusai a blob, a tábla, a várólista és a fájl.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="3d2ac-108">Ez a parancsmag felülírja a meglévő szabályokat.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="3d2ac-109">Az aktuális szabályokért használja a Get-AzStorageCORSRule parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="3d2ac-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d2ac-110">EXAMPLES</span></span>

### <span data-ttu-id="3d2ac-111">1. példa: CORS-szabályok hozzárendelése a blobszolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="3d2ac-111">Example 1: Assign CORS rules to the blob service</span></span>
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

<span data-ttu-id="3d2ac-112">Az első parancs egy szabálytömböt rendel a $CorsRules változóhoz.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="3d2ac-113">Ez a parancs a kódblokk több során túlnyúló normál kiterjesztést használ.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="3d2ac-114">A második parancs hozzárendeli a $CorsRules Blob szolgáltatástípushoz.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="3d2ac-115">2. példa: CORS-szabály tulajdonságainak módosítása blobszolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="3d2ac-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="3d2ac-116">Az első parancs a Blob típus aktuális CORS-szabályait kapja meg a **Get-AzStorageCORSRule** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="3d2ac-117">A parancs a szabályokat a tömbváltozóban $CorsRules tárolja.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="3d2ac-118">A második és a harmadik parancs módosítja az első szabályt a $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="3d2ac-119">Az utolsó parancs hozzárendeli a $CorsRules Blob szolgáltatástípushoz.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="3d2ac-120">A módosított szabályok felülírják az aktuális KORI-szabályokat.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="3d2ac-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d2ac-121">PARAMETERS</span></span>

### <span data-ttu-id="3d2ac-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3d2ac-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3d2ac-123">Egy szolgáltatáskérés ügyféloldali időkorrekta-intervallumát adja meg másodpercben.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3d2ac-124">Ha az előző hívás meghiúsul a megadott időszakban, ez a parancsmag újraküldi a kérelmet.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3d2ac-125">Ha ez a parancsmag nem kap sikeres választ az intervallum eltelte előtt, a parancsmag hibát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2ac-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3d2ac-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3d2ac-127">Megadja a maximális párhuzamos hálózati hívásokat.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3d2ac-128">Ezzel a paraméterrel korlátozhatja az egyidejűséget a helyi processzor- és sávszélesség-használat korlátozására a párhuzamos hálózati hívások maximális számának megadásával.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3d2ac-129">A megadott érték abszolút szám, és nem lesz megszorozva az alapszámokkal.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3d2ac-130">Ez a paraméter csökkentheti a hálózati kapcsolattal kapcsolatos problémákat alacsony sávszélességű környezetekben, például 100 kilobit/másodpercben.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3d2ac-131">Az alapértelmezett érték 10.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-131">The default value is 10.</span></span>

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

### <span data-ttu-id="3d2ac-132">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3d2ac-132">-Context</span></span>
<span data-ttu-id="3d2ac-133">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3d2ac-134">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3d2ac-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="3d2ac-135">-CorsRules</span></span>
<span data-ttu-id="3d2ac-136">A CORS-szabályok tömbje.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="3d2ac-137">A meglévő szabályokat beolvashatja a Get-AzStorageCORSRule parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

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

### <span data-ttu-id="3d2ac-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2ac-138">-DefaultProfile</span></span>
<span data-ttu-id="3d2ac-139">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d2ac-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d2ac-140">-PassThru</span></span>
<span data-ttu-id="3d2ac-141">Azt jelzi, hogy ez a parancsmag egy logikai értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="3d2ac-142">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3d2ac-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3d2ac-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3d2ac-144">A kérés kiszolgálói részében található időkorrekta hosszát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d2ac-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="3d2ac-145">-ServiceType</span></span>
<span data-ttu-id="3d2ac-146">Azt az Azure Storage szolgáltatástípust adja meg, amelyhez ez a parancsmag szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="3d2ac-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3d2ac-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d2ac-148">Blob</span><span class="sxs-lookup"><span data-stu-id="3d2ac-148">Blob</span></span> 
- <span data-ttu-id="3d2ac-149">Táblázat</span><span class="sxs-lookup"><span data-stu-id="3d2ac-149">Table</span></span> 
- <span data-ttu-id="3d2ac-150">Várólistán</span><span class="sxs-lookup"><span data-stu-id="3d2ac-150">Queue</span></span> 
- <span data-ttu-id="3d2ac-151">Fájl</span><span class="sxs-lookup"><span data-stu-id="3d2ac-151">File</span></span>

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

### <span data-ttu-id="3d2ac-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2ac-152">CommonParameters</span></span>
<span data-ttu-id="3d2ac-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2ac-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2ac-154">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d2ac-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2ac-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d2ac-155">INPUTS</span></span>

### <span data-ttu-id="3d2ac-156">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3d2ac-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3d2ac-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d2ac-157">OUTPUTS</span></span>

### <span data-ttu-id="3d2ac-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="3d2ac-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="3d2ac-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d2ac-159">NOTES</span></span>

## <span data-ttu-id="3d2ac-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d2ac-160">RELATED LINKS</span></span>

[<span data-ttu-id="3d2ac-161">Get-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3d2ac-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="3d2ac-162">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="3d2ac-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3d2ac-163">Remove-AzstorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="3d2ac-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


