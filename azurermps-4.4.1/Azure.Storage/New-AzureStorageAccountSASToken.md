---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageAccountSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 8b280a13e7eb7a2e6ea3f52b4a121f313504b2ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492643"
---
# <span data-ttu-id="2d6b5-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="2d6b5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6b5-103">Ügyfél szintű SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d6b5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d6b5-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d6b5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d6b5-105">DESCRIPTION</span></span>
<span data-ttu-id="2d6b5-106">A **New-AzureStorageSASToken** parancsmag létrehoz egy ügyfél szintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="2d6b5-107">A SAS-tokent használhatja több szolgáltatás engedélyeinek meghatalmazására, illetve a szolgáltatások engedélyeinek meghatalmazására, ha az objektum szintű SAS-tokent használja.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="2d6b5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2d6b5-108">EXAMPLES</span></span>

### <span data-ttu-id="2d6b5-109">Példa 1: egy fiók szintű SAS-token létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="2d6b5-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="2d6b5-110">A parancs teljes hozzáféréssel létrehoz egy fiók szintű SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="2d6b5-111">2. példa: fiók szintű SAS-token létrehozása IP-címekhez</span><span class="sxs-lookup"><span data-stu-id="2d6b5-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="2d6b5-112">Ez a parancs egy fiók szintű SAS-jogkivonatot hoz létre a HTTPS-only kérelmekhez a megadott IP-címtartományból.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="2d6b5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d6b5-113">PARAMETERS</span></span>

### <span data-ttu-id="2d6b5-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="2d6b5-114">-Context</span></span>
<span data-ttu-id="2d6b5-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2d6b5-116">A New-AzureStorageContext parancsmaggal **AzureStorageContext** -objektumokat lehet kikeresni.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="2d6b5-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2d6b5-117">-ExpiryTime</span></span>
<span data-ttu-id="2d6b5-118">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="2d6b5-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2d6b5-119">-IPAddressOrRange</span></span>
<span data-ttu-id="2d6b5-120">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2d6b5-121">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="2d6b5-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="2d6b5-122">-Permission</span></span>
<span data-ttu-id="2d6b5-123">A tárolási fiók engedélyei.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="2d6b5-124">Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrás-típusnak.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="2d6b5-125">Az elfogadható jogosultsági értékekről további információt a fiók-SAS létrehozása című témakörben talál.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="2d6b5-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="2d6b5-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="2d6b5-126">-Protocol</span></span>
<span data-ttu-id="2d6b5-127">Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="2d6b5-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2d6b5-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d6b5-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2d6b5-129">HttpsOnly</span></span>
- <span data-ttu-id="2d6b5-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="2d6b5-130">HttpsOrHttp</span></span>

<span data-ttu-id="2d6b5-131">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-131">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6b5-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2d6b5-132">-ResourceType</span></span>
<span data-ttu-id="2d6b5-133">A SAS-tokenhez elérhető erőforrás-típusokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="2d6b5-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2d6b5-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d6b5-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d6b5-135">None</span></span>
- <span data-ttu-id="2d6b5-136">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2d6b5-136">Service</span></span>
- <span data-ttu-id="2d6b5-137">Konténer</span><span class="sxs-lookup"><span data-stu-id="2d6b5-137">Container</span></span>
- <span data-ttu-id="2d6b5-138">Objektum</span><span class="sxs-lookup"><span data-stu-id="2d6b5-138">Object</span></span>

```yaml
Type: SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6b5-139">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="2d6b5-139">-Service</span></span>
<span data-ttu-id="2d6b5-140">A szolgáltatást adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-140">Specifies the service.</span></span>
<span data-ttu-id="2d6b5-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2d6b5-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2d6b5-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d6b5-142">None</span></span>
- <span data-ttu-id="2d6b5-143">BLOB</span><span class="sxs-lookup"><span data-stu-id="2d6b5-143">Blob</span></span>
- <span data-ttu-id="2d6b5-144">Fájl</span><span class="sxs-lookup"><span data-stu-id="2d6b5-144">File</span></span>
- <span data-ttu-id="2d6b5-145">Várólista</span><span class="sxs-lookup"><span data-stu-id="2d6b5-145">Queue</span></span>
- <span data-ttu-id="2d6b5-146">Táblázat</span><span class="sxs-lookup"><span data-stu-id="2d6b5-146">Table</span></span>

```yaml
Type: SharedAccessAccountServices
Parameter Sets: (All)
Aliases: 
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6b5-147">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="2d6b5-147">-StartTime</span></span>
<span data-ttu-id="2d6b5-148">Itt adhatja meg **datetime** -objektumként az időt, amelyen a biztonsági társítás érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="2d6b5-149">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2d6b5-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="2d6b5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6b5-150">CommonParameters</span></span>
<span data-ttu-id="2d6b5-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d6b5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6b5-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6b5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6b5-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6b5-153">INPUTS</span></span>

### <span data-ttu-id="2d6b5-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2d6b5-154">IStorageContext</span></span>

<span data-ttu-id="2d6b5-155">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2d6b5-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2d6b5-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6b5-156">OUTPUTS</span></span>

### <span data-ttu-id="2d6b5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2d6b5-157">System.String</span></span>

## <span data-ttu-id="2d6b5-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d6b5-158">NOTES</span></span>

## <span data-ttu-id="2d6b5-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d6b5-159">RELATED LINKS</span></span>

[<span data-ttu-id="2d6b5-160">Új – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-160">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="2d6b5-161">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-161">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="2d6b5-162">Új – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-162">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="2d6b5-163">Új – AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-163">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="2d6b5-164">Új – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-164">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="2d6b5-165">Új – AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="2d6b5-165">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


