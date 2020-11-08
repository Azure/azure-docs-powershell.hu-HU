---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013137"
---
# <span data-ttu-id="c72fb-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="c72fb-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="c72fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c72fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c72fb-103">Egy, az Azure Storage blob-hoz generált SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c72fb-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="c72fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c72fb-104">SYNTAX</span></span>

### <span data-ttu-id="c72fb-105">BlobNameWithPermission (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c72fb-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c72fb-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="c72fb-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c72fb-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="c72fb-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c72fb-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="c72fb-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c72fb-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c72fb-109">DESCRIPTION</span></span>
<span data-ttu-id="c72fb-110">A **New-AzStorageBlobSASToken** parancsmag létrehoz egy megosztott hozzáférés-aláírási (SAS) tokent egy Azure Storage blob számára.</span><span class="sxs-lookup"><span data-stu-id="c72fb-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="c72fb-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c72fb-111">EXAMPLES</span></span>

### <span data-ttu-id="c72fb-112">1. példa: blob SAS-jogkivonat létrehozása teljes blob-engedély birtokában</span><span class="sxs-lookup"><span data-stu-id="c72fb-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="c72fb-113">Ez a példa blob SAS-jogkivonatot hoz létre teljes blob-engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="c72fb-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="c72fb-114">2. példa: blob SAS-token létrehozása a Life Time szolgáltatóval</span><span class="sxs-lookup"><span data-stu-id="c72fb-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="c72fb-115">Ez a példa blob SAS-tokent hoz létre a Life Time szolgáltatóval.</span><span class="sxs-lookup"><span data-stu-id="c72fb-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="c72fb-116">3. példa: a felhasználói identitás biztonsági társításának létrehozása a OAuth-hitelesítésen alapuló tárolási környezettel</span><span class="sxs-lookup"><span data-stu-id="c72fb-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="c72fb-117">Ez a példa a felhasználói identitás blob SAS-jogkivonatát OAuth-hitelesítésen alapuló tárolási környezettel hozza létre</span><span class="sxs-lookup"><span data-stu-id="c72fb-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="c72fb-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c72fb-118">PARAMETERS</span></span>

### <span data-ttu-id="c72fb-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="c72fb-119">-Blob</span></span>
<span data-ttu-id="c72fb-120">A Storage blob nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="c72fb-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c72fb-121">-CloudBlob</span></span>
<span data-ttu-id="c72fb-122">A **CloudBlob** objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="c72fb-123">Ha **CloudBlob** objektumot szeretne beolvasni, használja a [Get-AzStorageBlob](./Get-AzStorageBlob.md) parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c72fb-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="c72fb-124">-Container</span><span class="sxs-lookup"><span data-stu-id="c72fb-124">-Container</span></span>
<span data-ttu-id="c72fb-125">A tároló tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="c72fb-126">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c72fb-126">-Context</span></span>
<span data-ttu-id="c72fb-127">A tárolási környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-127">Specifies the storage context.</span></span>
<span data-ttu-id="c72fb-128">Ha a tárolási környezet a OAuth-hitelesítésen alapul, a felhasználói identitás blob SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c72fb-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="c72fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72fb-129">-DefaultProfile</span></span>
<span data-ttu-id="c72fb-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c72fb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c72fb-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c72fb-131">-ExpiryTime</span></span>
<span data-ttu-id="c72fb-132">Azt adja meg, hogy mikor jár le a megosztott Access-aláírás.</span><span class="sxs-lookup"><span data-stu-id="c72fb-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="c72fb-133">Ha a tárolási környezet a OAuth-hitelesítésen alapul, a lejárati idő az aktuális időponttól 7 napig tart, és nem lehet korábbi az aktuális időpontnál.</span><span class="sxs-lookup"><span data-stu-id="c72fb-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="c72fb-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="c72fb-134">-FullUri</span></span>
<span data-ttu-id="c72fb-135">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="c72fb-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="c72fb-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c72fb-136">-IPAddressOrRange</span></span>
<span data-ttu-id="c72fb-137">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="c72fb-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="c72fb-138">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="c72fb-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="c72fb-139">– Engedély</span><span class="sxs-lookup"><span data-stu-id="c72fb-139">-Permission</span></span>
<span data-ttu-id="c72fb-140">A tárterület-blob engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="c72fb-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="c72fb-141">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="c72fb-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="c72fb-142">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c72fb-142">-Policy</span></span>
<span data-ttu-id="c72fb-143">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="c72fb-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c72fb-144">-Protocol</span></span>
<span data-ttu-id="c72fb-145">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c72fb-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="c72fb-146">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c72fb-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="c72fb-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c72fb-147">HttpsOnly</span></span>
* <span data-ttu-id="c72fb-148">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="c72fb-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="c72fb-149">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="c72fb-149">-StartTime</span></span>
<span data-ttu-id="c72fb-150">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="c72fb-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="c72fb-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c72fb-151">-Confirm</span></span>
<span data-ttu-id="c72fb-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c72fb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c72fb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c72fb-153">-WhatIf</span></span>
<span data-ttu-id="c72fb-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c72fb-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c72fb-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c72fb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c72fb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72fb-156">CommonParameters</span></span>
<span data-ttu-id="c72fb-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c72fb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72fb-158">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72fb-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72fb-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c72fb-159">INPUTS</span></span>

### <span data-ttu-id="c72fb-160">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="c72fb-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="c72fb-161">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c72fb-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c72fb-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c72fb-162">OUTPUTS</span></span>

### <span data-ttu-id="c72fb-163">System. String</span><span class="sxs-lookup"><span data-stu-id="c72fb-163">System.String</span></span>

## <span data-ttu-id="c72fb-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c72fb-164">NOTES</span></span>

## <span data-ttu-id="c72fb-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c72fb-165">RELATED LINKS</span></span>

[<span data-ttu-id="c72fb-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="c72fb-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="c72fb-167">Új – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="c72fb-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
