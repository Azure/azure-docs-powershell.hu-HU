---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349517"
---
# <span data-ttu-id="b04b8-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="b04b8-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="b04b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b04b8-103">Sas-tokent hoz létre egy Azure-tár blobhoz.</span><span class="sxs-lookup"><span data-stu-id="b04b8-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="b04b8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b04b8-104">SYNTAX</span></span>

### <span data-ttu-id="b04b8-105">BlobNameWithPermission (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b04b8-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04b8-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="b04b8-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04b8-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="b04b8-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b04b8-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="b04b8-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b04b8-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b04b8-109">DESCRIPTION</span></span>
<span data-ttu-id="b04b8-110">A **New-AzStorageBlobSASToken** parancsmag egy Azure-tár blobhoz létrehoz egy SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="b04b8-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="b04b8-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b04b8-111">EXAMPLES</span></span>

### <span data-ttu-id="b04b8-112">1. példa: Blob SAS-jogkivonat létrehozása teljes blob engedéllyel</span><span class="sxs-lookup"><span data-stu-id="b04b8-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="b04b8-113">Ebben a példában egy blob SAS-jogkivonatot hoz létre teljes blob engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="b04b8-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="b04b8-114">2. példa: Blob SAS-jogkivonat létrehozása az élettartammal</span><span class="sxs-lookup"><span data-stu-id="b04b8-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="b04b8-115">Ez a példa egy blob SAS-jogkivonatot hoz létre az élettartammal.</span><span class="sxs-lookup"><span data-stu-id="b04b8-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="b04b8-116">3. példa: Felhasználói identitású SAS-jogkivonat létrehozása OAuth-hitelesítésen alapuló tárterületkörnyezetben</span><span class="sxs-lookup"><span data-stu-id="b04b8-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="b04b8-117">Ebben a példában egy OAuth-hitelesítésen alapuló tárterületkörnyezetet használó User Identity blob SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b04b8-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="b04b8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b04b8-118">PARAMETERS</span></span>

### <span data-ttu-id="b04b8-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="b04b8-119">-Blob</span></span>
<span data-ttu-id="b04b8-120">A tár blobnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-120">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="b04b8-121">-BlobBaseClient</span></span>
<span data-ttu-id="b04b8-122">BlobBaseClient objektum</span><span class="sxs-lookup"><span data-stu-id="b04b8-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b04b8-123">-CloudBlob</span></span>
<span data-ttu-id="b04b8-124">A **CloudBlob objektumot** adja meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="b04b8-125">**CloudBlob-objektum** beszerzéséhez használja a [Get-AzStorageBlob](./Get-AzStorageBlob.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b04b8-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-126">-Container</span><span class="sxs-lookup"><span data-stu-id="b04b8-126">-Container</span></span>
<span data-ttu-id="b04b8-127">A tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-127">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-128">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b04b8-128">-Context</span></span>
<span data-ttu-id="b04b8-129">A tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-129">Specifies the storage context.</span></span>
<span data-ttu-id="b04b8-130">Amikor a tárterületkörnyezet OAuth-hitelesítésen alapul, felhasználói identitás blob SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b04b8-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="b04b8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04b8-131">-DefaultProfile</span></span>
<span data-ttu-id="b04b8-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b04b8-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04b8-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b04b8-133">-ExpiryTime</span></span>
<span data-ttu-id="b04b8-134">Azt adja meg, hogy mikor jár le a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="b04b8-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="b04b8-135">Ha a tárterület környezete OAuth-hitelesítésen alapul, a lejárati időnek a jelenlegi időponttól 7 napon belül kell lennie, és nem lehet korábbi az aktuális időpontnál.</span><span class="sxs-lookup"><span data-stu-id="b04b8-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="b04b8-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="b04b8-136">-FullUri</span></span>
<span data-ttu-id="b04b8-137">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b04b8-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="b04b8-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b04b8-138">-IPAddressOrRange</span></span>
<span data-ttu-id="b04b8-139">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="b04b8-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="b04b8-140">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="b04b8-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="b04b8-141">-Engedély</span><span class="sxs-lookup"><span data-stu-id="b04b8-141">-Permission</span></span>
<span data-ttu-id="b04b8-142">A tár blob engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="b04b8-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="b04b8-143">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="b04b8-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-144">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b04b8-144">-Policy</span></span>
<span data-ttu-id="b04b8-145">Egy Azure Tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-145">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b04b8-146">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b04b8-146">-Protocol</span></span>
<span data-ttu-id="b04b8-147">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="b04b8-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="b04b8-148">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="b04b8-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="b04b8-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="b04b8-149">HttpsOnly</span></span>
* <span data-ttu-id="b04b8-150">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="b04b8-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="b04b8-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b04b8-151">-StartTime</span></span>
<span data-ttu-id="b04b8-152">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="b04b8-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="b04b8-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b04b8-153">-Confirm</span></span>
<span data-ttu-id="b04b8-154">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b04b8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b04b8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b04b8-155">-WhatIf</span></span>
<span data-ttu-id="b04b8-156">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b04b8-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b04b8-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b04b8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b04b8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04b8-158">CommonParameters</span></span>
<span data-ttu-id="b04b8-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b04b8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04b8-160">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b04b8-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04b8-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b04b8-161">INPUTS</span></span>

### <span data-ttu-id="b04b8-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b04b8-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b04b8-163">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b04b8-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b04b8-164">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b04b8-164">OUTPUTS</span></span>

### <span data-ttu-id="b04b8-165">System.String</span><span class="sxs-lookup"><span data-stu-id="b04b8-165">System.String</span></span>

## <span data-ttu-id="b04b8-166">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b04b8-166">NOTES</span></span>

## <span data-ttu-id="b04b8-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b04b8-167">RELATED LINKS</span></span>

[<span data-ttu-id="b04b8-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b04b8-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b04b8-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="b04b8-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
