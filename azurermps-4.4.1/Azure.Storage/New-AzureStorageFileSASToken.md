---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageFileSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 052eae9a995aafe9d5d966ae5a17aae31a0fc0fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680787"
---
# <span data-ttu-id="e617c-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="e617c-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="e617c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e617c-102">SYNOPSIS</span></span>
<span data-ttu-id="e617c-103">Megosztott hozzáférés-aláírási tokent hoz létre egy tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="e617c-103">Generates a shared access signature token for a Storage file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e617c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e617c-104">SYNTAX</span></span>

### <span data-ttu-id="e617c-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="e617c-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e617c-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="e617c-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="e617c-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="e617c-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="e617c-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="e617c-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="e617c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e617c-109">DESCRIPTION</span></span>
<span data-ttu-id="e617c-110">A **New-AzureStorageFileSASToken** parancsmag létrehoz egy megosztott Access-aláírási tokent egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="e617c-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="e617c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e617c-111">EXAMPLES</span></span>

### <span data-ttu-id="e617c-112">Példa 1: megosztott hozzáférés-aláírási jogkivonat létrehozása teljes fájlengedélyek birtokában</span><span class="sxs-lookup"><span data-stu-id="e617c-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="e617c-113">A parancs egy megosztott Access-aláírási jogkivonatot hoz létre, amely teljes hozzáféréssel rendelkezik a FilePath nevű fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="e617c-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="e617c-114">2. példa: olyan megosztott hozzáférés-aláírási jogkivonat létrehozása, amelynek időkorlátja van</span><span class="sxs-lookup"><span data-stu-id="e617c-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="e617c-115">Az első parancs a Get-Date parancsmag használatával **datetime** típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e617c-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="e617c-116">A parancs az aktuális időpontot a $StartTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e617c-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="e617c-117">A második parancs két órát vesz fel az objektumba a $StartTime, majd az eredményt a $EndTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e617c-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="e617c-118">Ez az objektum két óra múlva jelenik meg a jövőben.</span><span class="sxs-lookup"><span data-stu-id="e617c-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="e617c-119">A harmadik parancs egy megosztott Access-aláírási tokent hoz létre, amely a megadott engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="e617c-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="e617c-120">Ez a token az aktuális időpontban érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="e617c-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="e617c-121">A token a $EndTime-ban tárolt idő után marad érvényes.</span><span class="sxs-lookup"><span data-stu-id="e617c-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="e617c-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e617c-122">PARAMETERS</span></span>

### <span data-ttu-id="e617c-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e617c-123">-Context</span></span>
<span data-ttu-id="e617c-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e617c-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e617c-125">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e617c-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e617c-126">-ExpiryTime</span></span>
<span data-ttu-id="e617c-127">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="e617c-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="e617c-128">-Fájl</span><span class="sxs-lookup"><span data-stu-id="e617c-128">-File</span></span>
<span data-ttu-id="e617c-129">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e617c-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e617c-130">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="e617c-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="e617c-131">-FullUri</span></span>
<span data-ttu-id="e617c-132">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="e617c-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="e617c-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e617c-133">-IPAddressOrRange</span></span>
<span data-ttu-id="e617c-134">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="e617c-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="e617c-135">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="e617c-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="e617c-136">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e617c-136">-Path</span></span>
<span data-ttu-id="e617c-137">A fájl elérési útját adja meg a tárterület-megosztáshoz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="e617c-137">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-138">– Engedély</span><span class="sxs-lookup"><span data-stu-id="e617c-138">-Permission</span></span>
<span data-ttu-id="e617c-139">A tárterület-fájlok engedélyeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="e617c-139">Specifies the permissions for a Storage file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-140">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e617c-140">-Policy</span></span>
<span data-ttu-id="e617c-141">A tárolt hozzáférési házirendet adja meg egy fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="e617c-141">Specifies the stored access policy for a file.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e617c-142">-Protocol</span></span>
<span data-ttu-id="e617c-143">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="e617c-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="e617c-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e617c-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="e617c-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e617c-145">HttpsOnly</span></span>
* <span data-ttu-id="e617c-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="e617c-146">HttpsOrHttp</span></span>

<span data-ttu-id="e617c-147">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="e617c-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="e617c-148">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="e617c-148">-ShareName</span></span>
<span data-ttu-id="e617c-149">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e617c-149">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e617c-150">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="e617c-150">-StartTime</span></span>
<span data-ttu-id="e617c-151">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="e617c-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="e617c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e617c-152">CommonParameters</span></span>
<span data-ttu-id="e617c-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e617c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e617c-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e617c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e617c-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e617c-155">INPUTS</span></span>

### <span data-ttu-id="e617c-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e617c-156">IStorageContext</span></span>

<span data-ttu-id="e617c-157">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e617c-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e617c-158">CloudFile</span><span class="sxs-lookup"><span data-stu-id="e617c-158">CloudFile</span></span>

<span data-ttu-id="e617c-159">A "fájl" paraméter elfogadja a "CloudFile" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e617c-159">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="e617c-160">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e617c-160">String</span></span>

<span data-ttu-id="e617c-161">Az elérési út paraméter a "string" típusú értéket adja meg a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="e617c-161">Parameter 'Path' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e617c-162">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e617c-162">String</span></span>

<span data-ttu-id="e617c-163">A "megosztásnév" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e617c-163">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e617c-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e617c-164">OUTPUTS</span></span>

### <span data-ttu-id="e617c-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e617c-165">System.String</span></span>

## <span data-ttu-id="e617c-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e617c-166">NOTES</span></span>

## <span data-ttu-id="e617c-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e617c-167">RELATED LINKS</span></span>

[<span data-ttu-id="e617c-168">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e617c-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e617c-169">Új – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="e617c-169">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
