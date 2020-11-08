---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187171"
---
# <span data-ttu-id="41021-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="41021-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="41021-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41021-102">SYNOPSIS</span></span>
<span data-ttu-id="41021-103">Létrehoz egy SAS-jogkivonatot az Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="41021-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="41021-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41021-104">SYNTAX</span></span>

### <span data-ttu-id="41021-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="41021-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41021-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="41021-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41021-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41021-107">DESCRIPTION</span></span>
<span data-ttu-id="41021-108">A **New-AzStorageContainerSASToken** parancsmag létrehoz egy Access-aláírási (SAS) tokent egy Azure-tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="41021-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="41021-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41021-109">EXAMPLES</span></span>

### <span data-ttu-id="41021-110">1. példa: a Container SAS-token létrehozása teljes tároló engedéllyel</span><span class="sxs-lookup"><span data-stu-id="41021-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="41021-111">Ebben a példában egy tároló SAS-tokent hoz létre teljes tároló engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="41021-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="41021-112">2. példa: több Container SAS-token létrehozása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="41021-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="41021-113">Ez a példa több Container SAS-tokent hoz létre a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="41021-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="41021-114">3. példa: a Container SAS-token létrehozása megosztott hozzáférési házirenddel</span><span class="sxs-lookup"><span data-stu-id="41021-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="41021-115">Ebben a példában egy tároló SAS-tokent hoz létre a megosztott hozzáférés házirendjével.</span><span class="sxs-lookup"><span data-stu-id="41021-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="41021-116">3. példa: a felhasználó személyazonosságát tároló SAS-token létrehozása OAuth-hitelesítésen alapuló tárolási környezettel</span><span class="sxs-lookup"><span data-stu-id="41021-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="41021-117">Ez a példa a felhasználói identitás tárolóját a OAuth-hitelesítés alapján tároló környezettel hozza létre.</span><span class="sxs-lookup"><span data-stu-id="41021-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="41021-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41021-118">PARAMETERS</span></span>

### <span data-ttu-id="41021-119">-Környezet</span><span class="sxs-lookup"><span data-stu-id="41021-119">-Context</span></span>
<span data-ttu-id="41021-120">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41021-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="41021-121">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="41021-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="41021-122">Ha a tárolási környezet a OAuth-hitelesítésen alapul, létrejön egy user identity Container SAS-token.</span><span class="sxs-lookup"><span data-stu-id="41021-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="41021-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41021-123">-DefaultProfile</span></span>
<span data-ttu-id="41021-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41021-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41021-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="41021-125">-ExpiryTime</span></span>
<span data-ttu-id="41021-126">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="41021-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="41021-127">Ha a felhasználó a kezdési időpontot állítja be, de nem a lejárati időt, a lejárati idő a kezdési időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="41021-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="41021-128">Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="41021-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="41021-129">Ha a tárolási környezet a OAuth-hitelesítésen alapul, a lejárati idő az aktuális időponttól 7 napig tart, és nem lehet korábbi az aktuális időpontnál.</span><span class="sxs-lookup"><span data-stu-id="41021-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="41021-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="41021-130">-FullUri</span></span>
<span data-ttu-id="41021-131">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="41021-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="41021-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="41021-132">-IPAddressOrRange</span></span>
<span data-ttu-id="41021-133">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="41021-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="41021-134">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="41021-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="41021-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41021-135">-Name</span></span>
<span data-ttu-id="41021-136">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="41021-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="41021-137">– Engedély</span><span class="sxs-lookup"><span data-stu-id="41021-137">-Permission</span></span>
<span data-ttu-id="41021-138">Megadhatja a tároló tároló engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="41021-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="41021-139">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="41021-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="41021-140">-Házirend</span><span class="sxs-lookup"><span data-stu-id="41021-140">-Policy</span></span>
<span data-ttu-id="41021-141">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="41021-141">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="41021-142">-Protocol</span><span class="sxs-lookup"><span data-stu-id="41021-142">-Protocol</span></span>
<span data-ttu-id="41021-143">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="41021-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="41021-144">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="41021-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="41021-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="41021-145">HttpsOnly</span></span>
* <span data-ttu-id="41021-146">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="41021-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="41021-147">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="41021-147">-StartTime</span></span>
<span data-ttu-id="41021-148">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="41021-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="41021-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41021-149">-Confirm</span></span>
<span data-ttu-id="41021-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41021-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41021-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41021-151">-WhatIf</span></span>
<span data-ttu-id="41021-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41021-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41021-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41021-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41021-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41021-154">CommonParameters</span></span>
<span data-ttu-id="41021-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41021-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41021-156">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41021-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41021-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41021-157">INPUTS</span></span>

### <span data-ttu-id="41021-158">System. String</span><span class="sxs-lookup"><span data-stu-id="41021-158">System.String</span></span>

### <span data-ttu-id="41021-159">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="41021-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="41021-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41021-160">OUTPUTS</span></span>

### <span data-ttu-id="41021-161">System. String</span><span class="sxs-lookup"><span data-stu-id="41021-161">System.String</span></span>

## <span data-ttu-id="41021-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41021-162">NOTES</span></span>

## <span data-ttu-id="41021-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41021-163">RELATED LINKS</span></span>

[<span data-ttu-id="41021-164">Új – AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="41021-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
