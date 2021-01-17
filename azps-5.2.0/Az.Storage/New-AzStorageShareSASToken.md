---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: 8dbb6f79a61d388aec033030de471092fa16ba77
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324656"
---
# <span data-ttu-id="c3e43-101">New-AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="c3e43-101">New-AzStorageShareSASToken</span></span>

## <span data-ttu-id="c3e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e43-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e43-103">Megosztott hozzáférés-aláírás jogkivonat létrehozása Azure Storage-megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c3e43-103">Generate Shared Access Signature token for Azure Storage share.</span></span>

## <span data-ttu-id="c3e43-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3e43-104">SYNTAX</span></span>

### <span data-ttu-id="c3e43-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e43-105">SasPolicy</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e43-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="c3e43-106">SasPermission</span></span>
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e43-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3e43-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e43-108">A **New-AzStorageShareSASToken** parancsmag megosztott hozzáférési aláírási jogkivonatot hoz létre egy Azure Storage-megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c3e43-108">The **New-AzStorageShareSASToken** cmdlet generates a shared access signature token for an Azure Storage share.</span></span>

## <span data-ttu-id="c3e43-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3e43-109">EXAMPLES</span></span>

### <span data-ttu-id="c3e43-110">1. példa: Megosztott hozzáférés aláírási jogkivonat létrehozása megosztáshoz</span><span class="sxs-lookup"><span data-stu-id="c3e43-110">Example 1: Generate a shared access signature token for a share</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

<span data-ttu-id="c3e43-111">Ez a parancs létrehoz egy megosztott hozzáférési aláírási jogkivonatot a ContosoShare nevű megosztáshoz.</span><span class="sxs-lookup"><span data-stu-id="c3e43-111">This command creates a shared access signature token for the share named ContosoShare.</span></span>

### <span data-ttu-id="c3e43-112">2. példa: Több megosztott hozzáférés-aláírási jogkivonat létrehozása a folyamat használatával</span><span class="sxs-lookup"><span data-stu-id="c3e43-112">Example 2: Generate multiple shared access signature token by using the pipeline</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

<span data-ttu-id="c3e43-113">Ez a parancs az előtagtesztnek megfelelő összes tárterületmegosztást leküldi.</span><span class="sxs-lookup"><span data-stu-id="c3e43-113">This command gets all the Storage shares that match the prefix test.</span></span>
<span data-ttu-id="c3e43-114">A parancs a folyamat műveleti operátorával átadja őket az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c3e43-114">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c3e43-115">Az aktuális parancsmag létrehoz egy megosztott hozzáférési jogkivonatot minden olyan tárterület-megosztáshoz, amely rendelkezik a megadott engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="c3e43-115">The current cmdlet creates a shared access token for each Storage share that has the specified permissions.</span></span>

### <span data-ttu-id="c3e43-116">3. példa: Megosztott hozzáférési házirendet használó megosztott hozzáférés-aláírási jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="c3e43-116">Example 3: Generate a shared access signature token that uses a shared access policy</span></span>
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

<span data-ttu-id="c3e43-117">Ez a parancs létrehoz egy megosztott hozzáférési aláírási jogkivonatot a ContosoShare nevű tárterület-megosztáshoz, amely a ContosoPolicy03 házirendet rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="c3e43-117">This command creates a shared access signature token for the Storage share named ContosoShare that has the policy named ContosoPolicy03.</span></span>

## <span data-ttu-id="c3e43-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e43-118">PARAMETERS</span></span>

### <span data-ttu-id="c3e43-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c3e43-119">-Context</span></span>
<span data-ttu-id="c3e43-120">Az Azure Storage környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3e43-120">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c3e43-121">Környezet lekérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c3e43-121">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c3e43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e43-122">-DefaultProfile</span></span>
<span data-ttu-id="c3e43-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3e43-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e43-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c3e43-124">-ExpiryTime</span></span>
<span data-ttu-id="c3e43-125">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="c3e43-125">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="c3e43-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c3e43-126">-FullUri</span></span>
<span data-ttu-id="c3e43-127">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c3e43-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c3e43-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c3e43-128">-IPAddressOrRange</span></span>
<span data-ttu-id="c3e43-129">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c3e43-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c3e43-130">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="c3e43-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="c3e43-131">-Engedély</span><span class="sxs-lookup"><span data-stu-id="c3e43-131">-Permission</span></span>
<span data-ttu-id="c3e43-132">Megadja a jogkivonatban a megosztás és a megosztás alatti fájlok eléréséhez szükséges engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="c3e43-132">Specifies the permissions in the token to access the share and files under the share.</span></span>
<span data-ttu-id="c3e43-133">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="c3e43-133">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="c3e43-134">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c3e43-134">-Policy</span></span>
<span data-ttu-id="c3e43-135">Egy megosztás tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c3e43-135">Specifies the stored access policy for a share.</span></span>

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

### <span data-ttu-id="c3e43-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c3e43-136">-Protocol</span></span>
<span data-ttu-id="c3e43-137">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3e43-137">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c3e43-138">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="c3e43-138">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c3e43-139">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c3e43-139">HttpsOnly</span></span>
* <span data-ttu-id="c3e43-140">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c3e43-140">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c3e43-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c3e43-141">-ShareName</span></span>
<span data-ttu-id="c3e43-142">A tárterület-megosztás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c3e43-142">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e43-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c3e43-143">-StartTime</span></span>
<span data-ttu-id="c3e43-144">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="c3e43-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c3e43-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e43-145">CommonParameters</span></span>
<span data-ttu-id="c3e43-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e43-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e43-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e43-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e43-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3e43-148">INPUTS</span></span>

### <span data-ttu-id="c3e43-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e43-149">System.String</span></span>

### <span data-ttu-id="c3e43-150">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3e43-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c3e43-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3e43-151">OUTPUTS</span></span>

### <span data-ttu-id="c3e43-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e43-152">System.String</span></span>

## <span data-ttu-id="c3e43-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3e43-153">NOTES</span></span>
* <span data-ttu-id="c3e43-154">Kulcsszavak: common, azure, services, data, storage, blob, queue, table</span><span class="sxs-lookup"><span data-stu-id="c3e43-154">Keywords: common, azure, services, data, storage, blob, queue, table</span></span>

## <span data-ttu-id="c3e43-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3e43-155">RELATED LINKS</span></span>

[<span data-ttu-id="c3e43-156">Get-AzstorageShare</span><span class="sxs-lookup"><span data-stu-id="c3e43-156">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="c3e43-157">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="c3e43-157">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)
