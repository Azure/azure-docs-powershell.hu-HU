---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491440"
---
# <span data-ttu-id="470b7-101">New-AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="470b7-101">New-AzureStorageFileSASToken</span></span>

## <span data-ttu-id="470b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="470b7-102">SYNOPSIS</span></span>
<span data-ttu-id="470b7-103">Megosztott hozzáférés-aláírási tokent hoz létre egy tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="470b7-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="470b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="470b7-104">SYNTAX</span></span>

### <span data-ttu-id="470b7-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="470b7-105">NameSasPermission</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="470b7-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="470b7-106">NameSasPolicy</span></span>
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="470b7-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="470b7-107">FileSasPermission</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### <span data-ttu-id="470b7-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="470b7-108">FileSasPolicy</span></span>
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## <span data-ttu-id="470b7-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="470b7-109">DESCRIPTION</span></span>
<span data-ttu-id="470b7-110">A **New-AzureStorageFileSASToken** parancsmag létrehoz egy megosztott Access-aláírási tokent egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="470b7-110">The **New-AzureStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="470b7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="470b7-111">EXAMPLES</span></span>

### <span data-ttu-id="470b7-112">Példa 1: megosztott hozzáférés-aláírási jogkivonat létrehozása teljes fájlengedélyek birtokában</span><span class="sxs-lookup"><span data-stu-id="470b7-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="470b7-113">A parancs egy megosztott Access-aláírási jogkivonatot hoz létre, amely teljes hozzáféréssel rendelkezik a FilePath nevű fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="470b7-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="470b7-114">2. példa: olyan megosztott hozzáférés-aláírási jogkivonat létrehozása, amelynek időkorlátja van</span><span class="sxs-lookup"><span data-stu-id="470b7-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="470b7-115">Az első parancs a Get-Date parancsmag használatával **datetime** típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="470b7-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="470b7-116">A parancs az aktuális időpontot a $StartTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="470b7-116">The command stores the current time in the $StartTime variable.</span></span>

<span data-ttu-id="470b7-117">A második parancs két órát vesz fel az objektumba a $StartTime, majd az eredményt a $EndTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="470b7-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="470b7-118">Ez az objektum két óra múlva jelenik meg a jövőben.</span><span class="sxs-lookup"><span data-stu-id="470b7-118">This object is a time two hours in the future.</span></span>

<span data-ttu-id="470b7-119">A harmadik parancs egy megosztott Access-aláírási tokent hoz létre, amely a megadott engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="470b7-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="470b7-120">Ez a token az aktuális időpontban érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="470b7-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="470b7-121">A token a $EndTime-ban tárolt idő után marad érvényes.</span><span class="sxs-lookup"><span data-stu-id="470b7-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="470b7-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="470b7-122">PARAMETERS</span></span>

### <span data-ttu-id="470b7-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="470b7-123">-Context</span></span>
<span data-ttu-id="470b7-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="470b7-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="470b7-125">Környezet beolvasásához használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="470b7-125">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="470b7-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="470b7-126">-ExpiryTime</span></span>
<span data-ttu-id="470b7-127">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="470b7-127">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="470b7-128">-Fájl</span><span class="sxs-lookup"><span data-stu-id="470b7-128">-File</span></span>
<span data-ttu-id="470b7-129">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="470b7-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="470b7-130">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzureStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="470b7-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="470b7-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="470b7-131">-FullUri</span></span>
<span data-ttu-id="470b7-132">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="470b7-132">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="470b7-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="470b7-133">-IPAddressOrRange</span></span>
<span data-ttu-id="470b7-134">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="470b7-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="470b7-135">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="470b7-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="470b7-136">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="470b7-136">-Path</span></span>
<span data-ttu-id="470b7-137">A fájl elérési útját adja meg a tárterület-megosztáshoz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="470b7-137">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="470b7-138">– Engedély</span><span class="sxs-lookup"><span data-stu-id="470b7-138">-Permission</span></span>
<span data-ttu-id="470b7-139">A tárterület-fájlok engedélyeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="470b7-139">Specifies the permissions for a Storage file.</span></span>

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

### <span data-ttu-id="470b7-140">-Házirend</span><span class="sxs-lookup"><span data-stu-id="470b7-140">-Policy</span></span>
<span data-ttu-id="470b7-141">A tárolt hozzáférési házirendet adja meg egy fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="470b7-141">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="470b7-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="470b7-142">-Protocol</span></span>
<span data-ttu-id="470b7-143">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="470b7-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="470b7-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="470b7-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="470b7-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="470b7-145">HttpsOnly</span></span>
* <span data-ttu-id="470b7-146">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="470b7-146">HttpsOrHttp</span></span>

<span data-ttu-id="470b7-147">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="470b7-147">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="470b7-148">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="470b7-148">-ShareName</span></span>
<span data-ttu-id="470b7-149">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="470b7-149">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="470b7-150">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="470b7-150">-StartTime</span></span>
<span data-ttu-id="470b7-151">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="470b7-151">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="470b7-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470b7-152">CommonParameters</span></span>
<span data-ttu-id="470b7-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="470b7-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470b7-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470b7-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470b7-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="470b7-155">INPUTS</span></span>

## <span data-ttu-id="470b7-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="470b7-156">OUTPUTS</span></span>

## <span data-ttu-id="470b7-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="470b7-157">NOTES</span></span>

## <span data-ttu-id="470b7-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="470b7-158">RELATED LINKS</span></span>

[<span data-ttu-id="470b7-159">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="470b7-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="470b7-160">Új – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="470b7-160">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)
