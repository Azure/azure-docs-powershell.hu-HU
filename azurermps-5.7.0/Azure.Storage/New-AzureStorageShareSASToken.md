---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareSASToken.md
ms.openlocfilehash: 44080736635a5b4e8964340aeeee448798ffaefc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496719"
---
# <span data-ttu-id="73317-101">New-AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="73317-101">New-AzureStorageShareSASToken</span></span>

## <span data-ttu-id="73317-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73317-102">SYNOPSIS</span></span>
<span data-ttu-id="73317-103">Megosztott hozzáférés-aláírási jogkivonat létrehozása az Azure tárhely-megosztásához.</span><span class="sxs-lookup"><span data-stu-id="73317-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73317-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73317-104">SYNTAX</span></span>

### <span data-ttu-id="73317-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="73317-105">SasPolicy</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="73317-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="73317-106">SasPermission</span></span>
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="73317-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="73317-107">DESCRIPTION</span></span>
<span data-ttu-id="73317-108">A **New-AzureStorageShareSASToken** parancsmag létrehoz egy Access-aláírási jogkivonatot egy Azure-tárterület-megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="73317-108">The **New-AzureStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="73317-109">Példák</span><span class="sxs-lookup"><span data-stu-id="73317-109">EXAMPLES</span></span>

### <span data-ttu-id="73317-110">Példa 1: megosztott hozzáférés-aláírási jogkivonat létrehozása megosztáshoz</span><span class="sxs-lookup"><span data-stu-id="73317-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="73317-111">Ez a parancs létrehoz egy megosztott Access-aláírási tokent a ContosoShare nevű megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="73317-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="73317-112">2. példa: több megosztott hozzáférés-aláírási jogkivonat létrehozása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="73317-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="73317-113">Ez a parancs beilleszti az előtag-teszthez tartozó összes tárolási megosztást.</span><span class="sxs-lookup"><span data-stu-id="73317-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="73317-114">A parancs a csővezeték-kezelő segítségével átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="73317-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="73317-115">Az aktuális parancsmag létrehoz egy megosztott hozzáférési jogkivonatot minden olyan tárterülethez, amely a megadott engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="73317-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="73317-116">3. példa: egy megosztott hozzáférés-vezérlőt használó, megosztott hozzáférésű aláírási jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="73317-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="73317-117">Ez a parancs létrehoz egy megosztott Access-aláírási jogkivonatot a ContosoShare nevű tároló-megosztáshoz, amely a ContosoPolicy03 nevű házirenddel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="73317-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="73317-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73317-118">PARAMETERS</span></span>

### <span data-ttu-id="73317-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="73317-119">-Context</span></span>
<span data-ttu-id="73317-120">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73317-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="73317-121">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="73317-121">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="73317-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="73317-122">-ExpiryTime</span></span>
<span data-ttu-id="73317-123">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="73317-123">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="73317-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="73317-124">-FullUri</span></span>
<span data-ttu-id="73317-125">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="73317-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="73317-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="73317-126">-IPAddressOrRange</span></span>
<span data-ttu-id="73317-127">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="73317-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="73317-128">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="73317-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="73317-129">– Engedély</span><span class="sxs-lookup"><span data-stu-id="73317-129">-Permission</span></span>
<span data-ttu-id="73317-130">A jogkivonatban található engedélyeket a megosztás alatti megosztás és fájlok eléréséhez adja meg.</span><span class="sxs-lookup"><span data-stu-id="73317-130">Specifies the permissions in the token to access the share and files under the share.</span></span>

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

### <span data-ttu-id="73317-131">-Házirend</span><span class="sxs-lookup"><span data-stu-id="73317-131">-Policy</span></span>
<span data-ttu-id="73317-132">Megadhatja a megosztáshoz tartozó tárolt hozzáférés-házirendet.</span><span class="sxs-lookup"><span data-stu-id="73317-132">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="73317-133">-Protocol</span><span class="sxs-lookup"><span data-stu-id="73317-133">-Protocol</span></span>
<span data-ttu-id="73317-134">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="73317-134">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="73317-135">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="73317-135">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="73317-136">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="73317-136">HttpsOnly</span></span>
* <span data-ttu-id="73317-137">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="73317-137">HttpsOrHttp</span></span>

<span data-ttu-id="73317-138">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="73317-138">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="73317-139">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="73317-139">-ShareName</span></span>
<span data-ttu-id="73317-140">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="73317-140">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73317-141">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="73317-141">-StartTime</span></span>
<span data-ttu-id="73317-142">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="73317-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="73317-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73317-143">CommonParameters</span></span>
<span data-ttu-id="73317-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73317-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73317-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73317-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73317-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73317-146">INPUTS</span></span>

### <span data-ttu-id="73317-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="73317-147">IStorageContext</span></span>

<span data-ttu-id="73317-148">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="73317-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="73317-149">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="73317-149">String</span></span>

<span data-ttu-id="73317-150">A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="73317-150">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="73317-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73317-151">OUTPUTS</span></span>

### <span data-ttu-id="73317-152">System. String</span><span class="sxs-lookup"><span data-stu-id="73317-152">System.String</span></span>

## <span data-ttu-id="73317-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73317-153">NOTES</span></span>
* <span data-ttu-id="73317-154">Kulcsszavak: gyakori, Azure, Services, Data, Storage, blob, queue, Table</span><span class="sxs-lookup"><span data-stu-id="73317-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="73317-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73317-155">RELATED LINKS</span></span>

[<span data-ttu-id="73317-156">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="73317-156">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="73317-157">Új – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="73317-157">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)
