---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c888c5e7a4083fd91fdddfd6d2442cb65056d42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491713"
---
# <span data-ttu-id="4dea8-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="4dea8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4dea8-102">SYNOPSIS</span></span>
<span data-ttu-id="4dea8-103">Létrehoz egy SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="4dea8-103">Creates an SAS token.</span></span>

## <span data-ttu-id="4dea8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4dea8-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dea8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4dea8-105">DESCRIPTION</span></span>
<span data-ttu-id="4dea8-106">A **New-AzureStorageSASToken** parancsmag létrehoz egy ügyfél szintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="4dea8-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>

<span data-ttu-id="4dea8-107">A SAS-tokent használhatja több szolgáltatás engedélyeinek meghatalmazására, illetve a szolgáltatások engedélyeinek meghatalmazására, ha az objektum szintű SAS-tokent használja.</span><span class="sxs-lookup"><span data-stu-id="4dea8-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="4dea8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4dea8-108">EXAMPLES</span></span>

### <span data-ttu-id="4dea8-109">1. példa: SAS-jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="4dea8-109">Example 1: Create an SAS token</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="4dea8-110">A parancs teljes hozzáféréssel létrehoz egy fiók szintű SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="4dea8-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="4dea8-111">2. példa: SAS-token létrehozása IP-címekből álló címtartományból</span><span class="sxs-lookup"><span data-stu-id="4dea8-111">Example 2: Create an SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="4dea8-112">Ez a parancs egy SAS-jogkivonatot hoz létre a HTTPS-only-kéréseknek a megadott IP-címtartományból.</span><span class="sxs-lookup"><span data-stu-id="4dea8-112">This command creates an SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="4dea8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4dea8-113">PARAMETERS</span></span>

### <span data-ttu-id="4dea8-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4dea8-114">-Context</span></span>
<span data-ttu-id="4dea8-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dea8-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4dea8-116">A New-AzureStorageContext parancsmaggal **AzureStorageContext** -objektumokat lehet kikeresni.</span><span class="sxs-lookup"><span data-stu-id="4dea8-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="4dea8-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4dea8-117">-ExpiryTime</span></span>
<span data-ttu-id="4dea8-118">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="4dea8-118">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="4dea8-119">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4dea8-119">-IPAddressOrRange</span></span>
<span data-ttu-id="4dea8-120">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="4dea8-120">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4dea8-121">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="4dea8-121">The range is inclusive.</span></span>

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

### <span data-ttu-id="4dea8-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="4dea8-122">-Permission</span></span>
<span data-ttu-id="4dea8-123">A tárolási fiók engedélyei.</span><span class="sxs-lookup"><span data-stu-id="4dea8-123">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="4dea8-124">Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrás-típusnak.</span><span class="sxs-lookup"><span data-stu-id="4dea8-124">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="4dea8-125">Az elfogadható jogosultsági értékekről további információt a fiók-SAS létrehozása című témakörben talál.https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="4dea8-125">For more information about acceptable permission values, see Constructing an Account SAShttps://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="4dea8-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="4dea8-126">-Protocol</span></span>
<span data-ttu-id="4dea8-127">Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="4dea8-127">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="4dea8-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4dea8-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4dea8-129">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4dea8-129">HttpsOnly</span></span>
- <span data-ttu-id="4dea8-130">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="4dea8-130">HttpsOrHttp</span></span>

<span data-ttu-id="4dea8-131">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4dea8-131">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4dea8-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4dea8-132">-ResourceType</span></span>
<span data-ttu-id="4dea8-133">A SAS-tokenhez elérhető erőforrás-típusokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dea8-133">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="4dea8-134">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4dea8-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4dea8-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="4dea8-135">None</span></span>
- <span data-ttu-id="4dea8-136">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="4dea8-136">Service</span></span>
- <span data-ttu-id="4dea8-137">Konténer</span><span class="sxs-lookup"><span data-stu-id="4dea8-137">Container</span></span>
- <span data-ttu-id="4dea8-138">Objektum</span><span class="sxs-lookup"><span data-stu-id="4dea8-138">Object</span></span>

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

### <span data-ttu-id="4dea8-139">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="4dea8-139">-Service</span></span>
<span data-ttu-id="4dea8-140">A szolgáltatást adja meg.</span><span class="sxs-lookup"><span data-stu-id="4dea8-140">Specifies the service.</span></span>
<span data-ttu-id="4dea8-141">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="4dea8-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4dea8-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="4dea8-142">None</span></span>
- <span data-ttu-id="4dea8-143">BLOB</span><span class="sxs-lookup"><span data-stu-id="4dea8-143">Blob</span></span>
- <span data-ttu-id="4dea8-144">Fájl</span><span class="sxs-lookup"><span data-stu-id="4dea8-144">File</span></span>
- <span data-ttu-id="4dea8-145">Várólista</span><span class="sxs-lookup"><span data-stu-id="4dea8-145">Queue</span></span>
- <span data-ttu-id="4dea8-146">Táblázat</span><span class="sxs-lookup"><span data-stu-id="4dea8-146">Table</span></span>

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

### <span data-ttu-id="4dea8-147">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="4dea8-147">-StartTime</span></span>
<span data-ttu-id="4dea8-148">Itt adhatja meg **datetime** -objektumként az időt, amelyen a biztonsági társítás érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="4dea8-148">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="4dea8-149">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4dea8-149">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="4dea8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dea8-150">CommonParameters</span></span>
<span data-ttu-id="4dea8-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4dea8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dea8-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dea8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dea8-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dea8-153">INPUTS</span></span>

## <span data-ttu-id="4dea8-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4dea8-154">OUTPUTS</span></span>

## <span data-ttu-id="4dea8-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4dea8-155">NOTES</span></span>

## <span data-ttu-id="4dea8-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4dea8-156">RELATED LINKS</span></span>

[<span data-ttu-id="4dea8-157">Új – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-157">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="4dea8-158">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="4dea8-159">Új – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-159">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="4dea8-160">Új – AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-160">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="4dea8-161">Új – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-161">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="4dea8-162">Új – AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="4dea8-162">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


