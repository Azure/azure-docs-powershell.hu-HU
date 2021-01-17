---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragefilesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageFileSASToken.md
ms.openlocfilehash: fcd58edbb3d6e03becc8e6305f58555fedf36107
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324782"
---
# <span data-ttu-id="b24f3-101">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="b24f3-101">New-AzStorageFileSASToken</span></span>

## <span data-ttu-id="b24f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b24f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b24f3-103">Megosztott hozzáférés aláírási jogkivonatot hoz létre egy tárfájlhoz.</span><span class="sxs-lookup"><span data-stu-id="b24f3-103">Generates a shared access signature token for a Storage file.</span></span>

## <span data-ttu-id="b24f3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b24f3-104">SYNTAX</span></span>

### <span data-ttu-id="b24f3-105">NameSasPermission</span><span class="sxs-lookup"><span data-stu-id="b24f3-105">NameSasPermission</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b24f3-106">NameSasPolicy</span><span class="sxs-lookup"><span data-stu-id="b24f3-106">NameSasPolicy</span></span>
```
New-AzStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b24f3-107">FileSasPermission</span><span class="sxs-lookup"><span data-stu-id="b24f3-107">FileSasPermission</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b24f3-108">FileSasPolicy</span><span class="sxs-lookup"><span data-stu-id="b24f3-108">FileSasPolicy</span></span>
```
New-AzStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24f3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b24f3-109">DESCRIPTION</span></span>
<span data-ttu-id="b24f3-110">A **New-AzStorageFileSASToken** parancsmag megosztott hozzáférési aláírási jogkivonatot hoz létre egy Azure Storage-fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="b24f3-110">The **New-AzStorageFileSASToken** cmdlet generates a shared access signature token for an Azure Storage file.</span></span>

## <span data-ttu-id="b24f3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b24f3-111">EXAMPLES</span></span>

### <span data-ttu-id="b24f3-112">1. példa: Teljes fájlengedélyekkel rendelkező megosztott hozzáférés-aláírási jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="b24f3-112">Example 1: Generate a shared access signature token that has full file permissions</span></span>
```
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

<span data-ttu-id="b24f3-113">Ez a parancs létrehoz egy megosztott hozzáférés-aláírási jogkivonatot, amely teljes engedélyekkel rendelkezik a FilePath nevű fájlhoz.</span><span class="sxs-lookup"><span data-stu-id="b24f3-113">This command generates a shared access signature token that has full permissions for the file that is named FilePath.</span></span>

### <span data-ttu-id="b24f3-114">2. példa: Időkorláttal elérhető megosztott hozzáférés-aláírási jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="b24f3-114">Example 2: Generate a shared access signature token that has a time limit</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="b24f3-115">Az első parancs egy **DateTime-objektumot** hoz létre a Get-Date parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="b24f3-115">The first command creates a **DateTime** object by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="b24f3-116">A parancs az aktuális időt tárolja a $StartTime változóban.</span><span class="sxs-lookup"><span data-stu-id="b24f3-116">The command stores the current time in the $StartTime variable.</span></span>
<span data-ttu-id="b24f3-117">A második parancs hozzáad két órát a $StartTime objektumhoz, majd az eredményt a $EndTime változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b24f3-117">The second command adds two hours to the object in $StartTime, and then stores the result in the $EndTime variable.</span></span>
<span data-ttu-id="b24f3-118">Ez az objektum a jövőben két órával későbbi időpont.</span><span class="sxs-lookup"><span data-stu-id="b24f3-118">This object is a time two hours in the future.</span></span>
<span data-ttu-id="b24f3-119">A harmadik parancs létrehoz egy megosztott hozzáférés-aláírási jogkivonatot, amely rendelkezik a megadott engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="b24f3-119">The third command generates a shared access signature token that has the specified permissions.</span></span>
<span data-ttu-id="b24f3-120">Ez a jogkivonat érvényessé válik a jelenlegi időpontban.</span><span class="sxs-lookup"><span data-stu-id="b24f3-120">This token becomes valid at the current time.</span></span>
<span data-ttu-id="b24f3-121">A jogkivonat mindaddig érvényes marad, amíg a $EndTime.</span><span class="sxs-lookup"><span data-stu-id="b24f3-121">The token remains valid until time stored in $EndTime.</span></span>

## <span data-ttu-id="b24f3-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b24f3-122">PARAMETERS</span></span>

### <span data-ttu-id="b24f3-123">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b24f3-123">-Context</span></span>
<span data-ttu-id="b24f3-124">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b24f3-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="b24f3-125">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b24f3-125">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b24f3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24f3-126">-DefaultProfile</span></span>
<span data-ttu-id="b24f3-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b24f3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b24f3-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b24f3-128">-ExpiryTime</span></span>
<span data-ttu-id="b24f3-129">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="b24f3-129">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="b24f3-130">-File</span><span class="sxs-lookup"><span data-stu-id="b24f3-130">-File</span></span>
<span data-ttu-id="b24f3-131">Egy **CloudFile-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="b24f3-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="b24f3-132">Létrehozhat felhőfájlt, vagy beszerezhet egyet a Get-AzStorageFile parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="b24f3-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b24f3-133">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b24f3-133">-FullUri</span></span>
<span data-ttu-id="b24f3-134">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b24f3-134">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b24f3-135">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b24f3-135">-IPAddressOrRange</span></span>
<span data-ttu-id="b24f3-136">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b24f3-136">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b24f3-137">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="b24f3-137">The range is inclusive.</span></span>

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

### <span data-ttu-id="b24f3-138">-Path</span><span class="sxs-lookup"><span data-stu-id="b24f3-138">-Path</span></span>
<span data-ttu-id="b24f3-139">A fájl elérési útját adja meg a tárterület-megosztáshoz képest.</span><span class="sxs-lookup"><span data-stu-id="b24f3-139">Specifies the path of the file relative to a Storage share.</span></span>

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

### <span data-ttu-id="b24f3-140">-Engedély</span><span class="sxs-lookup"><span data-stu-id="b24f3-140">-Permission</span></span>
<span data-ttu-id="b24f3-141">A Tárfájl engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="b24f3-141">Specifies the permissions for a Storage file.</span></span>
<span data-ttu-id="b24f3-142">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="b24f3-142">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b24f3-143">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b24f3-143">-Policy</span></span>
<span data-ttu-id="b24f3-144">Egy fájl tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="b24f3-144">Specifies the stored access policy for a file.</span></span>

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

### <span data-ttu-id="b24f3-145">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b24f3-145">-Protocol</span></span>
<span data-ttu-id="b24f3-146">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b24f3-146">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b24f3-147">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b24f3-147">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b24f3-148">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b24f3-148">HttpsOnly</span></span>
* <span data-ttu-id="b24f3-149">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b24f3-149">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b24f3-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b24f3-150">-ShareName</span></span>
<span data-ttu-id="b24f3-151">A tárterület-megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b24f3-151">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="b24f3-152">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b24f3-152">-StartTime</span></span>
<span data-ttu-id="b24f3-153">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="b24f3-153">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b24f3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24f3-154">CommonParameters</span></span>
<span data-ttu-id="b24f3-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24f3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24f3-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24f3-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24f3-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b24f3-157">INPUTS</span></span>

### <span data-ttu-id="b24f3-158">System.String</span><span class="sxs-lookup"><span data-stu-id="b24f3-158">System.String</span></span>

### <span data-ttu-id="b24f3-159">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="b24f3-159">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="b24f3-160">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b24f3-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b24f3-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b24f3-161">OUTPUTS</span></span>

### <span data-ttu-id="b24f3-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b24f3-162">System.String</span></span>

## <span data-ttu-id="b24f3-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b24f3-163">NOTES</span></span>

## <span data-ttu-id="b24f3-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b24f3-164">RELATED LINKS</span></span>

[<span data-ttu-id="b24f3-165">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="b24f3-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b24f3-166">New-AzstorageSharesASToken</span><span class="sxs-lookup"><span data-stu-id="b24f3-166">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)
