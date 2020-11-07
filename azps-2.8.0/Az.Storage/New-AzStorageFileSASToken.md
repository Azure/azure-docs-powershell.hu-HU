---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: 9a0a25664a5512dcdecea268cff1e2cdc177d3dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838368"
---
# <span data-ttu-id="354ce-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="354ce-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="354ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="354ce-102">SYNOPSIS</span></span>
<span data-ttu-id="354ce-103">Megosztott hozzáférés-aláírási tokent hoz létre egy tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="354ce-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="354ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="354ce-104">SYNTAX</span></span>

### <span data-ttu-id="354ce-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="354ce-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="354ce-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="354ce-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="354ce-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="354ce-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="354ce-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="354ce-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354ce-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="354ce-109">DESCRIPTION</span></span>
<span data-ttu-id="354ce-110">A **New-AzStorageFileSASToken** parancsmag létrehoz egy megosztott Access-aláírási tokent egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="354ce-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="354ce-111">Példák</span><span class="sxs-lookup"><span data-stu-id="354ce-111">EXAMPLES</span></span>

### <span data-ttu-id="354ce-112">Példa 1: megosztott hozzáférés-aláírási jogkivonat létrehozása teljes fájlengedélyek birtokában</span><span class="sxs-lookup"><span data-stu-id="354ce-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="354ce-113">A parancs egy megosztott Access-aláírási jogkivonatot hoz létre, amely teljes hozzáféréssel rendelkezik a FilePath nevű fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="354ce-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="354ce-114">2. példa: olyan megosztott hozzáférés-aláírási jogkivonat létrehozása, amelynek időkorlátja van</span><span class="sxs-lookup"><span data-stu-id="354ce-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="354ce-115">Az első parancs a Get-Date parancsmag használatával **datetime** típusú objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="354ce-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="354ce-116">A parancs az aktuális időpontot a $StartTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="354ce-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="354ce-117">A második parancs két órát vesz fel az objektumba a $StartTime, majd az eredményt a $EndTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="354ce-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="354ce-118">Ez az objektum két óra múlva jelenik meg a jövőben.</span><span class="sxs-lookup"><span data-stu-id="354ce-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="354ce-119">A harmadik parancs egy megosztott Access-aláírási tokent hoz létre, amely a megadott engedélyekkel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="354ce-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="354ce-120">Ez a token az aktuális időpontban érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="354ce-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="354ce-121">A token a $EndTime-ban tárolt idő után marad érvényes.</span><span class="sxs-lookup"><span data-stu-id="354ce-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="354ce-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="354ce-122">PARAMETERS</span></span>

### <span data-ttu-id="354ce-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="354ce-123">-Context</span></span>
<span data-ttu-id="354ce-124">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="354ce-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="354ce-125">Környezet beolvasásához használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="354ce-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354ce-126">-DefaultProfile</span></span>
<span data-ttu-id="354ce-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="354ce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354ce-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="354ce-128">-ExpiryTime</span></span>
<span data-ttu-id="354ce-129">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="354ce-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="354ce-130">-Fájl</span><span class="sxs-lookup"><span data-stu-id="354ce-130">-File</span></span>
<span data-ttu-id="354ce-131">Egy **CloudFile** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="354ce-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="354ce-132">Létrehozhat egy felhőalapú fájlt, vagy megadhat egyet az Get-AzStorageFile parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="354ce-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="354ce-133">-FullUri</span></span>
<span data-ttu-id="354ce-134">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="354ce-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="354ce-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="354ce-135">-IPAddressOrRange</span></span>
<span data-ttu-id="354ce-136">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="354ce-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="354ce-137">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="354ce-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="354ce-138">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="354ce-138">-Path</span></span>
<span data-ttu-id="354ce-139">A fájl elérési útját adja meg a tárterület-megosztáshoz viszonyítva.</span><span class="sxs-lookup"><span data-stu-id="354ce-139">Specifies the path of the file relative to a Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-140">– Engedély</span><span class="sxs-lookup"><span data-stu-id="354ce-140">-Permission</span></span>
<span data-ttu-id="354ce-141">A tárterület-fájlok engedélyeit adja meg.</span><span class="sxs-lookup"><span data-stu-id="354ce-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="354ce-142">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="354ce-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-143">-Házirend</span><span class="sxs-lookup"><span data-stu-id="354ce-143">-Policy</span></span>
<span data-ttu-id="354ce-144">A tárolt hozzáférési házirendet adja meg egy fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="354ce-144">Specifies the stored access policy for a file.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="354ce-145">-Protocol</span></span>
<span data-ttu-id="354ce-146">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="354ce-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="354ce-147">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="354ce-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="354ce-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="354ce-148">HttpsOnly</span></span>
* <span data-ttu-id="354ce-149">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="354ce-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-150">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="354ce-150">-ShareName</span></span>
<span data-ttu-id="354ce-151">A tárolási megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="354ce-151">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="354ce-152">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="354ce-152">-StartTime</span></span>
<span data-ttu-id="354ce-153">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="354ce-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="354ce-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354ce-154">CommonParameters</span></span>
<span data-ttu-id="354ce-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="354ce-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354ce-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="354ce-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354ce-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="354ce-157">INPUTS</span></span>

### <span data-ttu-id="354ce-158">System. String</span><span class="sxs-lookup"><span data-stu-id="354ce-158">System.String</span></span>

### <span data-ttu-id="354ce-159">Microsoft. Azure. Storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="354ce-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="354ce-160">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="354ce-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="354ce-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="354ce-161">OUTPUTS</span></span>

### <span data-ttu-id="354ce-162">System. String</span><span class="sxs-lookup"><span data-stu-id="354ce-162">System.String</span></span>

## <span data-ttu-id="354ce-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="354ce-163">NOTES</span></span>

## <span data-ttu-id="354ce-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="354ce-164">RELATED LINKS</span></span>

[<span data-ttu-id="354ce-165">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="354ce-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="354ce-166">Új – AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="354ce-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
