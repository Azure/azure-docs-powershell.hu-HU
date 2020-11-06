---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491812"
---
# <span data-ttu-id="a895a-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="a895a-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="a895a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a895a-102">SYNOPSIS</span></span>
<span data-ttu-id="a895a-103">Létrehoz egy SAS-jogkivonatot az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="a895a-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="a895a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a895a-104">SYNTAX</span></span>

### <span data-ttu-id="a895a-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="a895a-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="a895a-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="a895a-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a895a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a895a-107">DESCRIPTION</span></span>
<span data-ttu-id="a895a-108">A **New-AzureStorageTableSASToken** parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Storage Table-hoz.</span><span class="sxs-lookup"><span data-stu-id="a895a-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="a895a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a895a-109">EXAMPLES</span></span>

### <span data-ttu-id="a895a-110">Példa 1: olyan SAS-token létrehozása, amely teljes hozzáféréssel rendelkezik a táblázathoz</span><span class="sxs-lookup"><span data-stu-id="a895a-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="a895a-111">Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblázat teljes engedélyeivel.</span><span class="sxs-lookup"><span data-stu-id="a895a-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="a895a-112">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="a895a-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="a895a-113">2. példa: egy több partíciót tartalmazó SAS-token létrehozása</span><span class="sxs-lookup"><span data-stu-id="a895a-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="a895a-114">Ez a parancs a ContosoResources nevű táblára vonatkozó teljes engedélyekkel generálta és a SAS-tokent hozza létre.</span><span class="sxs-lookup"><span data-stu-id="a895a-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="a895a-115">A parancs a tokent a *StartPartitionKey* és a *EndPartitionKey* paraméterrel megadott tartományra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="a895a-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="a895a-116">3. példa: olyan SAS-token létrehozása, amely egy táblához tárolt hozzáférés-házirendet tartalmaz</span><span class="sxs-lookup"><span data-stu-id="a895a-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="a895a-117">A parancs létrehoz egy SAS-jogkivonatot a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="a895a-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="a895a-118">A parancs a ClientPolicy01 nevű tárolt elérési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="a895a-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a895a-119">PARAMETERS</span></span>

### <span data-ttu-id="a895a-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a895a-120">-Context</span></span>
<span data-ttu-id="a895a-121">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a895a-122">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a895a-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a895a-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="a895a-123">-EndPartitionKey</span></span>
<span data-ttu-id="a895a-124">A parancsmag által létrehozott tokenhez tartozó sor végének a Partition (partíció) kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a895a-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="a895a-125">-EndRowKey</span></span>
<span data-ttu-id="a895a-126">A parancsmag által létrehozott tokenhez tartozó sor végéhez tartozó sor billentyűt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a895a-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a895a-127">-ExpiryTime</span></span>
<span data-ttu-id="a895a-128">Azt adja meg, hogy mikor jár le a SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="a895a-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="a895a-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="a895a-129">-FullUri</span></span>
<span data-ttu-id="a895a-130">Azt jelzi, hogy ez a parancsmag a teljes várólista-URI azonosítót adja eredményül a SAS-jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="a895a-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="a895a-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a895a-131">-IPAddressOrRange</span></span>
<span data-ttu-id="a895a-132">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="a895a-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="a895a-133">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="a895a-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="a895a-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a895a-134">-Name</span></span>
<span data-ttu-id="a895a-135">Az Azure Storage Table-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="a895a-136">Ez a parancsmag létrehoz egy SAS-jogkivonatot annak a táblának, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="a895a-137">– Engedély</span><span class="sxs-lookup"><span data-stu-id="a895a-137">-Permission</span></span>
<span data-ttu-id="a895a-138">Megadja az Azure Storage Table engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="a895a-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="a895a-139">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a895a-139">-Policy</span></span>
<span data-ttu-id="a895a-140">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="a895a-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="a895a-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a895a-141">-Protocol</span></span>
<span data-ttu-id="a895a-142">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="a895a-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="a895a-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="a895a-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a895a-144">HttpsOnly</span></span>
* <span data-ttu-id="a895a-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="a895a-145">HttpsOrHttp</span></span>

<span data-ttu-id="a895a-146">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="a895a-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="a895a-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="a895a-147">-StartPartitionKey</span></span>
<span data-ttu-id="a895a-148">A parancsmag által létrehozott jogkivonat-sor kezdetének a Partition kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a895a-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="a895a-149">-StartRowKey</span></span>
<span data-ttu-id="a895a-150">A parancsmag által létrehozott jogkivonat-sor kezdetének a sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a895a-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a895a-151">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a895a-151">-StartTime</span></span>
<span data-ttu-id="a895a-152">Azt adja meg, hogy a SAS-token érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="a895a-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="a895a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a895a-153">CommonParameters</span></span>
<span data-ttu-id="a895a-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a895a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a895a-155">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a895a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a895a-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a895a-156">INPUTS</span></span>

## <span data-ttu-id="a895a-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a895a-157">OUTPUTS</span></span>

## <span data-ttu-id="a895a-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a895a-158">NOTES</span></span>

## <span data-ttu-id="a895a-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a895a-159">RELATED LINKS</span></span>

[<span data-ttu-id="a895a-160">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a895a-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
