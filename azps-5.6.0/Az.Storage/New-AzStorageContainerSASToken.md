---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 09cbfb953118e5d6e29f2af25cd4653939135f07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002502"
---
# <span data-ttu-id="29732-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="29732-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="29732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29732-102">SYNOPSIS</span></span>
<span data-ttu-id="29732-103">Egy Azure-tárolóhoz egy SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29732-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="29732-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="29732-104">SYNTAX</span></span>

### <span data-ttu-id="29732-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="29732-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29732-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="29732-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29732-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="29732-107">DESCRIPTION</span></span>
<span data-ttu-id="29732-108">A **New-AzStorageContainerSASToken** parancsmag létrehoz egy SAS-jogkivonatot egy Azure-tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="29732-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="29732-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="29732-109">EXAMPLES</span></span>

### <span data-ttu-id="29732-110">1. példa: Tároló SAS-jogkivonat létrehozása teljes tároló engedéllyel</span><span class="sxs-lookup"><span data-stu-id="29732-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="29732-111">Ez a példa egy teljes tároló engedéllyel rendelkező tároló SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29732-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="29732-112">2. példa: Több tároló SAS-jogkivonat létrehozása folyamat szerint</span><span class="sxs-lookup"><span data-stu-id="29732-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="29732-113">Ez a példa több tároló SAS-jogkivonatot hoz létre a folyamat használatával.</span><span class="sxs-lookup"><span data-stu-id="29732-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="29732-114">3. példa: Tároló SAS-jogkivonat létrehozása megosztott hozzáférési házirend használatával</span><span class="sxs-lookup"><span data-stu-id="29732-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="29732-115">Ez a példa megosztott hozzáférési házirendet tartalmazó tároló SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29732-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="29732-116">3. példa: Felhasználói identitás tároló SAS-jogkivonat létrehozása OAuth-hitelesítésen alapuló tárterületkörnyezetben</span><span class="sxs-lookup"><span data-stu-id="29732-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="29732-117">Ebben a példában egy OAuth-hitelesítésen alapuló tárterületkörnyezetet tartalmazó Felhasználói identitás tároló SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="29732-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="29732-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29732-118">PARAMETERS</span></span>

### <span data-ttu-id="29732-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="29732-119">-Context</span></span>
<span data-ttu-id="29732-120">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="29732-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="29732-121">A parancsmagot a New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="29732-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="29732-122">Amikor a tárterületkörnyezet OAuth-hitelesítésen alapul, létrehoz egy Felhasználói identitás tároló SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="29732-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="29732-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29732-123">-DefaultProfile</span></span>
<span data-ttu-id="29732-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29732-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29732-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="29732-125">-ExpiryTime</span></span>
<span data-ttu-id="29732-126">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="29732-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="29732-127">Ha a felhasználó beállítja a kezdési időt, de nem a lejárati időt, a lejárati idő a kezdési időpontra plusz egy órával van megállítva.</span><span class="sxs-lookup"><span data-stu-id="29732-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="29732-128">Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális idő plusz egy óra lesz.</span><span class="sxs-lookup"><span data-stu-id="29732-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="29732-129">Ha a tárterület környezete OAuth-hitelesítésen alapul, a lejárati időnek a jelenlegi időponttól 7 napon belül kell lennie, és nem lehet korábbi az aktuális időpontnál.</span><span class="sxs-lookup"><span data-stu-id="29732-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="29732-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="29732-130">-FullUri</span></span>
<span data-ttu-id="29732-131">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="29732-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="29732-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="29732-132">-IPAddressOrRange</span></span>
<span data-ttu-id="29732-133">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="29732-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="29732-134">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="29732-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="29732-135">-Name</span><span class="sxs-lookup"><span data-stu-id="29732-135">-Name</span></span>
<span data-ttu-id="29732-136">Egy Azure-tároló tárolónevet ad meg.</span><span class="sxs-lookup"><span data-stu-id="29732-136">Specifies an Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29732-137">-Engedély</span><span class="sxs-lookup"><span data-stu-id="29732-137">-Permission</span></span>
<span data-ttu-id="29732-138">Egy tároló engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="29732-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="29732-139">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="29732-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="29732-140">-Házirend</span><span class="sxs-lookup"><span data-stu-id="29732-140">-Policy</span></span>
<span data-ttu-id="29732-141">Egy Azure Tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="29732-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="29732-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="29732-142">-Protocol</span></span>
<span data-ttu-id="29732-143">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="29732-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="29732-144">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="29732-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="29732-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="29732-145">HttpsOnly</span></span>
* <span data-ttu-id="29732-146">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="29732-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="29732-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="29732-147">-StartTime</span></span>
<span data-ttu-id="29732-148">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="29732-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="29732-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29732-149">-Confirm</span></span>
<span data-ttu-id="29732-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="29732-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29732-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29732-151">-WhatIf</span></span>
<span data-ttu-id="29732-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="29732-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29732-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29732-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29732-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29732-154">CommonParameters</span></span>
<span data-ttu-id="29732-155">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29732-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29732-156">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29732-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29732-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29732-157">INPUTS</span></span>

### <span data-ttu-id="29732-158">System.String</span><span class="sxs-lookup"><span data-stu-id="29732-158">System.String</span></span>

### <span data-ttu-id="29732-159">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="29732-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="29732-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29732-160">OUTPUTS</span></span>

### <span data-ttu-id="29732-161">System.String</span><span class="sxs-lookup"><span data-stu-id="29732-161">System.String</span></span>

## <span data-ttu-id="29732-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="29732-162">NOTES</span></span>

## <span data-ttu-id="29732-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29732-163">RELATED LINKS</span></span>

[<span data-ttu-id="29732-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="29732-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
