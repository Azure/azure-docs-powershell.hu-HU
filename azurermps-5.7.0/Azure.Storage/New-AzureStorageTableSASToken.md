---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 76ed7737acb26cd713aa84b26a743f3e5e43874f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672664"
---
# <span data-ttu-id="8fc09-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="8fc09-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="8fc09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fc09-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc09-103">Létrehoz egy SAS-jogkivonatot az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="8fc09-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fc09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fc09-104">SYNTAX</span></span>

### <span data-ttu-id="8fc09-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="8fc09-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="8fc09-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="8fc09-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8fc09-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fc09-107">DESCRIPTION</span></span>
<span data-ttu-id="8fc09-108">A **New-AzureStorageTableSASToken** parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Storage Table-hoz.</span><span class="sxs-lookup"><span data-stu-id="8fc09-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="8fc09-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8fc09-109">EXAMPLES</span></span>

### <span data-ttu-id="8fc09-110">Példa 1: olyan SAS-token létrehozása, amely teljes hozzáféréssel rendelkezik a táblázathoz</span><span class="sxs-lookup"><span data-stu-id="8fc09-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="8fc09-111">Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblázat teljes engedélyeivel.</span><span class="sxs-lookup"><span data-stu-id="8fc09-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8fc09-112">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="8fc09-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="8fc09-113">2. példa: egy több partíciót tartalmazó SAS-token létrehozása</span><span class="sxs-lookup"><span data-stu-id="8fc09-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="8fc09-114">Ez a parancs a ContosoResources nevű táblára vonatkozó teljes engedélyekkel generálta és a SAS-tokent hozza létre.</span><span class="sxs-lookup"><span data-stu-id="8fc09-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="8fc09-115">A parancs a tokent a *StartPartitionKey* és a *EndPartitionKey* paraméterrel megadott tartományra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="8fc09-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="8fc09-116">3. példa: olyan SAS-token létrehozása, amely egy táblához tárolt hozzáférés-házirendet tartalmaz</span><span class="sxs-lookup"><span data-stu-id="8fc09-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="8fc09-117">A parancs létrehoz egy SAS-jogkivonatot a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="8fc09-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="8fc09-118">A parancs a ClientPolicy01 nevű tárolt elérési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="8fc09-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fc09-119">PARAMETERS</span></span>

### <span data-ttu-id="8fc09-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8fc09-120">-Context</span></span>
<span data-ttu-id="8fc09-121">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8fc09-122">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8fc09-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8fc09-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8fc09-123">-EndPartitionKey</span></span>
<span data-ttu-id="8fc09-124">A parancsmag által létrehozott tokenhez tartozó sor végének a Partition (partíció) kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fc09-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="8fc09-125">-EndRowKey</span></span>
<span data-ttu-id="8fc09-126">A parancsmag által létrehozott tokenhez tartozó sor végéhez tartozó sor billentyűt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fc09-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8fc09-127">-ExpiryTime</span></span>
<span data-ttu-id="8fc09-128">Azt adja meg, hogy mikor jár le a SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="8fc09-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="8fc09-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="8fc09-129">-FullUri</span></span>
<span data-ttu-id="8fc09-130">Azt jelzi, hogy ez a parancsmag a teljes várólista-URI azonosítót adja eredményül a SAS-jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="8fc09-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="8fc09-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="8fc09-131">-IPAddressOrRange</span></span>
<span data-ttu-id="8fc09-132">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="8fc09-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="8fc09-133">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="8fc09-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="8fc09-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fc09-134">-Name</span></span>
<span data-ttu-id="8fc09-135">Az Azure Storage Table-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="8fc09-136">Ez a parancsmag létrehoz egy SAS-jogkivonatot annak a táblának, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fc09-137">– Engedély</span><span class="sxs-lookup"><span data-stu-id="8fc09-137">-Permission</span></span>
<span data-ttu-id="8fc09-138">Megadja az Azure Storage Table engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="8fc09-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="8fc09-139">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8fc09-139">-Policy</span></span>
<span data-ttu-id="8fc09-140">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="8fc09-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="8fc09-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8fc09-141">-Protocol</span></span>
<span data-ttu-id="8fc09-142">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="8fc09-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8fc09-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="8fc09-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="8fc09-144">HttpsOnly</span></span>
* <span data-ttu-id="8fc09-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="8fc09-145">HttpsOrHttp</span></span>

<span data-ttu-id="8fc09-146">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="8fc09-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="8fc09-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="8fc09-147">-StartPartitionKey</span></span>
<span data-ttu-id="8fc09-148">A parancsmag által létrehozott jogkivonat-sor kezdetének a Partition kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fc09-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="8fc09-149">-StartRowKey</span></span>
<span data-ttu-id="8fc09-150">A parancsmag által létrehozott jogkivonat-sor kezdetének a sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8fc09-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fc09-151">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="8fc09-151">-StartTime</span></span>
<span data-ttu-id="8fc09-152">Azt adja meg, hogy a SAS-token érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="8fc09-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="8fc09-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc09-153">CommonParameters</span></span>
<span data-ttu-id="8fc09-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fc09-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc09-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fc09-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc09-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc09-156">INPUTS</span></span>

### <span data-ttu-id="8fc09-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fc09-157">IStorageContext</span></span>

<span data-ttu-id="8fc09-158">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8fc09-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="8fc09-159">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="8fc09-159">String</span></span>

<span data-ttu-id="8fc09-160">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8fc09-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8fc09-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fc09-161">OUTPUTS</span></span>

### <span data-ttu-id="8fc09-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8fc09-162">System.String</span></span>

## <span data-ttu-id="8fc09-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fc09-163">NOTES</span></span>

## <span data-ttu-id="8fc09-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fc09-164">RELATED LINKS</span></span>

[<span data-ttu-id="8fc09-165">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8fc09-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
