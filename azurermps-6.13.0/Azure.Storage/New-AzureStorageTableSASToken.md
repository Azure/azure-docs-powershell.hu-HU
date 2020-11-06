---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 99dc4097c1b54459e121e87b9a52e3ab38a325f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502299"
---
# <span data-ttu-id="88e1c-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="88e1c-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="88e1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="88e1c-103">Létrehoz egy SAS-jogkivonatot az Azure Storage-táblájához.</span><span class="sxs-lookup"><span data-stu-id="88e1c-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88e1c-104">SYNTAX</span></span>

### <span data-ttu-id="88e1c-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="88e1c-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e1c-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="88e1c-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e1c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="88e1c-108">A **New-AzureStorageTableSASToken** parancsmag létrehoz egy megosztott Access-aláírási (SAS) tokent az Azure Storage Table-hoz.</span><span class="sxs-lookup"><span data-stu-id="88e1c-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="88e1c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88e1c-109">EXAMPLES</span></span>

### <span data-ttu-id="88e1c-110">Példa 1: olyan SAS-token létrehozása, amely teljes hozzáféréssel rendelkezik a táblázathoz</span><span class="sxs-lookup"><span data-stu-id="88e1c-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="88e1c-111">Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblázat teljes engedélyeivel.</span><span class="sxs-lookup"><span data-stu-id="88e1c-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="88e1c-112">Ez a token az olvasási, a hozzáadási, a frissítési és a törlési engedély.</span><span class="sxs-lookup"><span data-stu-id="88e1c-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="88e1c-113">2. példa: egy több partíciót tartalmazó SAS-token létrehozása</span><span class="sxs-lookup"><span data-stu-id="88e1c-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="88e1c-114">Ez a parancs a ContosoResources nevű táblára vonatkozó teljes engedélyekkel generálta és a SAS-tokent hozza létre.</span><span class="sxs-lookup"><span data-stu-id="88e1c-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="88e1c-115">A parancs a tokent a *StartPartitionKey* és a *EndPartitionKey* paraméterrel megadott tartományra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="88e1c-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="88e1c-116">3. példa: olyan SAS-token létrehozása, amely egy táblához tárolt hozzáférés-házirendet tartalmaz</span><span class="sxs-lookup"><span data-stu-id="88e1c-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="88e1c-117">A parancs létrehoz egy SAS-jogkivonatot a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="88e1c-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="88e1c-118">A parancs a ClientPolicy01 nevű tárolt elérési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="88e1c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88e1c-119">PARAMETERS</span></span>

### <span data-ttu-id="88e1c-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="88e1c-120">-Context</span></span>
<span data-ttu-id="88e1c-121">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="88e1c-122">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="88e1c-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="88e1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e1c-123">-DefaultProfile</span></span>
<span data-ttu-id="88e1c-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88e1c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e1c-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="88e1c-125">-EndPartitionKey</span></span>
<span data-ttu-id="88e1c-126">A parancsmag által létrehozott tokenhez tartozó sor végének a Partition (partíció) kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="88e1c-127">-EndRowKey</span></span>
<span data-ttu-id="88e1c-128">A parancsmag által létrehozott tokenhez tartozó sor végéhez tartozó sor billentyűt adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88e1c-129">-ExpiryTime</span></span>
<span data-ttu-id="88e1c-130">Azt adja meg, hogy mikor jár le a SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="88e1c-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="88e1c-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="88e1c-131">-FullUri</span></span>
<span data-ttu-id="88e1c-132">Azt jelzi, hogy ez a parancsmag a teljes várólista-URI azonosítót adja eredményül a SAS-jogkivonattal.</span><span class="sxs-lookup"><span data-stu-id="88e1c-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="88e1c-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="88e1c-133">-IPAddressOrRange</span></span>
<span data-ttu-id="88e1c-134">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="88e1c-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="88e1c-135">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="88e1c-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="88e1c-136">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88e1c-136">-Name</span></span>
<span data-ttu-id="88e1c-137">Az Azure Storage Table-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="88e1c-138">Ez a parancsmag létrehoz egy SAS-jogkivonatot annak a táblának, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-139">– Engedély</span><span class="sxs-lookup"><span data-stu-id="88e1c-139">-Permission</span></span>
<span data-ttu-id="88e1c-140">Megadja az Azure Storage Table engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="88e1c-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="88e1c-141">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="88e1c-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-142">-Házirend</span><span class="sxs-lookup"><span data-stu-id="88e1c-142">-Policy</span></span>
<span data-ttu-id="88e1c-143">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="88e1c-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="88e1c-144">-Protocol</span></span>
<span data-ttu-id="88e1c-145">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="88e1c-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="88e1c-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="88e1c-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="88e1c-147">HttpsOnly</span></span>
* <span data-ttu-id="88e1c-148">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="88e1c-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="88e1c-149">-StartPartitionKey</span></span>
<span data-ttu-id="88e1c-150">A parancsmag által létrehozott jogkivonat-sor kezdetének a Partition kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="88e1c-151">-StartRowKey</span></span>
<span data-ttu-id="88e1c-152">A parancsmag által létrehozott jogkivonat-sor kezdetének a sorát adja meg.</span><span class="sxs-lookup"><span data-stu-id="88e1c-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e1c-153">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="88e1c-153">-StartTime</span></span>
<span data-ttu-id="88e1c-154">Azt adja meg, hogy a SAS-token érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="88e1c-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="88e1c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e1c-155">CommonParameters</span></span>
<span data-ttu-id="88e1c-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88e1c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e1c-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e1c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e1c-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e1c-158">INPUTS</span></span>

### <span data-ttu-id="88e1c-159">System. String</span><span class="sxs-lookup"><span data-stu-id="88e1c-159">System.String</span></span>

### <span data-ttu-id="88e1c-160">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e1c-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88e1c-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88e1c-161">OUTPUTS</span></span>

### <span data-ttu-id="88e1c-162">System. String</span><span class="sxs-lookup"><span data-stu-id="88e1c-162">System.String</span></span>

## <span data-ttu-id="88e1c-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88e1c-163">NOTES</span></span>

## <span data-ttu-id="88e1c-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88e1c-164">RELATED LINKS</span></span>

[<span data-ttu-id="88e1c-165">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="88e1c-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
