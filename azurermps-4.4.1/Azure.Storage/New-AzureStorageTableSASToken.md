---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 739cd5b12cfc33abb57e4e04d2834b195966b126
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680784"
---
# <span data-ttu-id="28e47-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="28e47-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="28e47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28e47-102">SYNOPSIS</span></span>
<span data-ttu-id="28e47-103">Létrehoz egy SAS-jogkivonatot az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="28e47-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28e47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28e47-104">SYNTAX</span></span>

### <span data-ttu-id="28e47-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="28e47-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="28e47-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="28e47-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="28e47-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28e47-107">DESCRIPTION</span></span>
<span data-ttu-id="28e47-108">A **New-AzureStorageTableSASToken** parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Storage Table-hoz.</span><span class="sxs-lookup"><span data-stu-id="28e47-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="28e47-109">Példák</span><span class="sxs-lookup"><span data-stu-id="28e47-109">EXAMPLES</span></span>

### <span data-ttu-id="28e47-110">Példa 1: olyan SAS-token létrehozása, amely teljes hozzáféréssel rendelkezik a táblázathoz</span><span class="sxs-lookup"><span data-stu-id="28e47-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="28e47-111">Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblázat teljes engedélyeivel.</span><span class="sxs-lookup"><span data-stu-id="28e47-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="28e47-112">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="28e47-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="28e47-113">2. példa: egy több partíciót tartalmazó SAS-token létrehozása</span><span class="sxs-lookup"><span data-stu-id="28e47-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="28e47-114">Ez a parancs a ContosoResources nevű táblára vonatkozó teljes engedélyekkel generálta és a SAS-tokent hozza létre.</span><span class="sxs-lookup"><span data-stu-id="28e47-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="28e47-115">A parancs a tokent a *StartPartitionKey* és a *EndPartitionKey* paraméterrel megadott tartományra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="28e47-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="28e47-116">3. példa: olyan SAS-token létrehozása, amely egy táblához tárolt hozzáférés-házirendet tartalmaz</span><span class="sxs-lookup"><span data-stu-id="28e47-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="28e47-117">A parancs létrehoz egy SAS-jogkivonatot a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="28e47-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="28e47-118">A parancs a ClientPolicy01 nevű tárolt elérési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="28e47-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28e47-119">PARAMETERS</span></span>

### <span data-ttu-id="28e47-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="28e47-120">-Context</span></span>
<span data-ttu-id="28e47-121">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="28e47-122">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="28e47-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="28e47-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="28e47-123">-EndPartitionKey</span></span>
<span data-ttu-id="28e47-124">A parancsmag által létrehozott tokenhez tartozó sor végének a Partition (partíció) kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="28e47-125">-EndRowKey</span></span>
<span data-ttu-id="28e47-126">A parancsmag által létrehozott tokenhez tartozó sor végéhez tartozó sor billentyűt adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="28e47-127">-ExpiryTime</span></span>
<span data-ttu-id="28e47-128">Azt adja meg, hogy mikor jár le a SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="28e47-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="28e47-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="28e47-129">-FullUri</span></span>
<span data-ttu-id="28e47-130">Azt jelzi, hogy ez a parancsmag a teljes várólista-URI azonosítót adja eredményül a SAS-jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="28e47-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="28e47-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="28e47-131">-IPAddressOrRange</span></span>
<span data-ttu-id="28e47-132">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="28e47-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="28e47-133">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="28e47-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="28e47-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28e47-134">-Name</span></span>
<span data-ttu-id="28e47-135">Az Azure Storage Table-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="28e47-136">Ez a parancsmag létrehoz egy SAS-jogkivonatot annak a táblának, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-137">– Engedély</span><span class="sxs-lookup"><span data-stu-id="28e47-137">-Permission</span></span>
<span data-ttu-id="28e47-138">Megadja az Azure Storage Table engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="28e47-138">Specifies permissions for an Azure Storage table.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-139">-Házirend</span><span class="sxs-lookup"><span data-stu-id="28e47-139">-Policy</span></span>
<span data-ttu-id="28e47-140">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="28e47-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="28e47-141">-Protocol</span></span>
<span data-ttu-id="28e47-142">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="28e47-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="28e47-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="28e47-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="28e47-144">HttpsOnly</span></span>
* <span data-ttu-id="28e47-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="28e47-145">HttpsOrHttp</span></span>

<span data-ttu-id="28e47-146">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="28e47-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="28e47-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="28e47-147">-StartPartitionKey</span></span>
<span data-ttu-id="28e47-148">A parancsmag által létrehozott jogkivonat-sor kezdetének a Partition kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="28e47-149">-StartRowKey</span></span>
<span data-ttu-id="28e47-150">A parancsmag által létrehozott jogkivonat-sor kezdetének a sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28e47-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e47-151">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="28e47-151">-StartTime</span></span>
<span data-ttu-id="28e47-152">Azt adja meg, hogy a SAS-token érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="28e47-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="28e47-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e47-153">CommonParameters</span></span>
<span data-ttu-id="28e47-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28e47-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e47-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28e47-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e47-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e47-156">INPUTS</span></span>

### <span data-ttu-id="28e47-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="28e47-157">IStorageContext</span></span>

<span data-ttu-id="28e47-158">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="28e47-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="28e47-159">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="28e47-159">String</span></span>

<span data-ttu-id="28e47-160">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="28e47-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="28e47-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28e47-161">OUTPUTS</span></span>

### <span data-ttu-id="28e47-162">System. String</span><span class="sxs-lookup"><span data-stu-id="28e47-162">System.String</span></span>

## <span data-ttu-id="28e47-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28e47-163">NOTES</span></span>

## <span data-ttu-id="28e47-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28e47-164">RELATED LINKS</span></span>

[<span data-ttu-id="28e47-165">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="28e47-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
