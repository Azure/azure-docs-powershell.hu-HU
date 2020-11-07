---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 88b9d395cca2e548e3c70d55267b7c1b3854a750
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668619"
---
# <span data-ttu-id="d7770-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="d7770-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="d7770-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7770-102">SYNOPSIS</span></span>
<span data-ttu-id="d7770-103">Létrehoz egy SAS-jogkivonatot az Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="d7770-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="d7770-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7770-104">SYNTAX</span></span>

### <span data-ttu-id="d7770-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="d7770-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7770-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="d7770-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7770-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7770-107">DESCRIPTION</span></span>
<span data-ttu-id="d7770-108">A **New-AzStorageContainerSASToken** parancsmag létrehoz egy Access-aláírási (SAS) tokent egy Azure-tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="d7770-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="d7770-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7770-109">EXAMPLES</span></span>

### <span data-ttu-id="d7770-110">1. példa: a Container SAS-token létrehozása teljes tároló engedéllyel</span><span class="sxs-lookup"><span data-stu-id="d7770-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="d7770-111">Ebben a példában egy tároló SAS-tokent hoz létre teljes tároló engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="d7770-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="d7770-112">2. példa: több Container SAS-token létrehozása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d7770-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="d7770-113">Ez a példa több Container SAS-tokent hoz létre a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="d7770-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="d7770-114">3. példa: a Container SAS-token létrehozása megosztott hozzáférési házirenddel</span><span class="sxs-lookup"><span data-stu-id="d7770-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="d7770-115">Ebben a példában egy tároló SAS-tokent hoz létre a megosztott hozzáférés házirendjével.</span><span class="sxs-lookup"><span data-stu-id="d7770-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="d7770-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7770-116">PARAMETERS</span></span>

### <span data-ttu-id="d7770-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d7770-117">-Context</span></span>
<span data-ttu-id="d7770-118">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7770-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d7770-119">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="d7770-119">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d7770-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7770-120">-DefaultProfile</span></span>
<span data-ttu-id="d7770-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7770-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7770-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d7770-122">-ExpiryTime</span></span>
<span data-ttu-id="d7770-123">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="d7770-123">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="d7770-124">Ha a felhasználó a kezdési időpontot állítja be, de nem a lejárati időt, a lejárati idő a kezdési időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="d7770-124">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="d7770-125">Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="d7770-125">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="d7770-126">-FullUri</span><span class="sxs-lookup"><span data-stu-id="d7770-126">-FullUri</span></span>
<span data-ttu-id="d7770-127">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d7770-127">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="d7770-128">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="d7770-128">-IPAddressOrRange</span></span>
<span data-ttu-id="d7770-129">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="d7770-129">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="d7770-130">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="d7770-130">The range is inclusive.</span></span>

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

### <span data-ttu-id="d7770-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7770-131">-Name</span></span>
<span data-ttu-id="d7770-132">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7770-132">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="d7770-133">– Engedély</span><span class="sxs-lookup"><span data-stu-id="d7770-133">-Permission</span></span>
<span data-ttu-id="d7770-134">Megadhatja a tároló tároló engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="d7770-134">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="d7770-135">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="d7770-135">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="d7770-136">-Házirend</span><span class="sxs-lookup"><span data-stu-id="d7770-136">-Policy</span></span>
<span data-ttu-id="d7770-137">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7770-137">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="d7770-138">-Protocol</span><span class="sxs-lookup"><span data-stu-id="d7770-138">-Protocol</span></span>
<span data-ttu-id="d7770-139">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7770-139">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="d7770-140">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d7770-140">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="d7770-141">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d7770-141">HttpsOnly</span></span>
* <span data-ttu-id="d7770-142">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="d7770-142">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7770-143">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="d7770-143">-StartTime</span></span>
<span data-ttu-id="d7770-144">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="d7770-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="d7770-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7770-145">CommonParameters</span></span>
<span data-ttu-id="d7770-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7770-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7770-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7770-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7770-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7770-148">INPUTS</span></span>

### <span data-ttu-id="d7770-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d7770-149">System.String</span></span>

### <span data-ttu-id="d7770-150">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d7770-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d7770-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7770-151">OUTPUTS</span></span>

### <span data-ttu-id="d7770-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d7770-152">System.String</span></span>

## <span data-ttu-id="d7770-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7770-153">NOTES</span></span>

## <span data-ttu-id="d7770-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7770-154">RELATED LINKS</span></span>

[<span data-ttu-id="d7770-155">Új – AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="d7770-155">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
