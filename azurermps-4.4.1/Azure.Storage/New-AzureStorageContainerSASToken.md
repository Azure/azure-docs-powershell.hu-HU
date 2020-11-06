---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: d7c7847a92c7bbb241046479c70d1dabb75ea685
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492637"
---
# <span data-ttu-id="97b4e-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="97b4e-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="97b4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="97b4e-103">Létrehoz egy SAS-jogkivonatot az Azure Storage tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="97b4e-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97b4e-104">SYNTAX</span></span>

### <span data-ttu-id="97b4e-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="97b4e-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="97b4e-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="97b4e-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="97b4e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="97b4e-107">DESCRIPTION</span></span>
<span data-ttu-id="97b4e-108">A **New-AzureStorageContainerSASToken** parancsmag létrehoz egy Access-aláírási (SAS) tokent egy Azure-tároló tárolóhoz.</span><span class="sxs-lookup"><span data-stu-id="97b4e-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="97b4e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="97b4e-109">EXAMPLES</span></span>

### <span data-ttu-id="97b4e-110">1. példa: a Container SAS-token létrehozása teljes tároló engedéllyel</span><span class="sxs-lookup"><span data-stu-id="97b4e-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="97b4e-111">Ebben a példában egy tároló SAS-tokent hoz létre teljes tároló engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="97b4e-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="97b4e-112">2. példa: több Container SAS-token létrehozása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="97b4e-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="97b4e-113">Ez a példa több Container SAS-tokent hoz létre a csővezeték használatával.</span><span class="sxs-lookup"><span data-stu-id="97b4e-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="97b4e-114">3. példa: a Container SAS-token létrehozása megosztott hozzáférési házirenddel</span><span class="sxs-lookup"><span data-stu-id="97b4e-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="97b4e-115">Ebben a példában egy tároló SAS-tokent hoz létre a megosztott hozzáférés házirendjével.</span><span class="sxs-lookup"><span data-stu-id="97b4e-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="97b4e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97b4e-116">PARAMETERS</span></span>

### <span data-ttu-id="97b4e-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="97b4e-117">-Context</span></span>
<span data-ttu-id="97b4e-118">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b4e-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="97b4e-119">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="97b4e-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b4e-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="97b4e-120">-ExpiryTime</span></span>
<span data-ttu-id="97b4e-121">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="97b4e-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="97b4e-122">Ha a felhasználó a kezdési időpontot állítja be, de nem a lejárati időt, a lejárati idő a kezdési időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="97b4e-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="97b4e-123">Ha sem a kezdési időpont, sem a lejárati idő nincs megadva, a lejárati idő az aktuális időpontra és egy órára van állítva.</span><span class="sxs-lookup"><span data-stu-id="97b4e-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="97b4e-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="97b4e-124">-FullUri</span></span>
<span data-ttu-id="97b4e-125">Jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási tokent adja vissza.</span><span class="sxs-lookup"><span data-stu-id="97b4e-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="97b4e-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="97b4e-126">-IPAddressOrRange</span></span>
<span data-ttu-id="97b4e-127">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="97b4e-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="97b4e-128">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="97b4e-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="97b4e-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="97b4e-129">-Name</span></span>
<span data-ttu-id="97b4e-130">Az Azure Storage Container nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b4e-130">Specifies an Azure storage container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97b4e-131">– Engedély</span><span class="sxs-lookup"><span data-stu-id="97b4e-131">-Permission</span></span>
<span data-ttu-id="97b4e-132">Megadhatja a tároló tároló engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="97b4e-132">Specifies permissions for a storage container.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4e-133">-Házirend</span><span class="sxs-lookup"><span data-stu-id="97b4e-133">-Policy</span></span>
<span data-ttu-id="97b4e-134">Egy, az Azure által tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b4e-134">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b4e-135">-Protocol</span><span class="sxs-lookup"><span data-stu-id="97b4e-135">-Protocol</span></span>
<span data-ttu-id="97b4e-136">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b4e-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="97b4e-137">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="97b4e-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="97b4e-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="97b4e-138">HttpsOnly</span></span>
* <span data-ttu-id="97b4e-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="97b4e-139">HttpsOrHttp</span></span>

<span data-ttu-id="97b4e-140">Az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="97b4e-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="97b4e-141">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="97b4e-141">-StartTime</span></span>
<span data-ttu-id="97b4e-142">Azt az időpontot adja meg, amikor a megosztott hozzáférés aláírása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="97b4e-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="97b4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b4e-143">CommonParameters</span></span>
<span data-ttu-id="97b4e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97b4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b4e-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b4e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b4e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b4e-146">INPUTS</span></span>

### <span data-ttu-id="97b4e-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="97b4e-147">IStorageContext</span></span>

<span data-ttu-id="97b4e-148">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="97b4e-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="97b4e-149">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="97b4e-149">String</span></span>

<span data-ttu-id="97b4e-150">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="97b4e-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="97b4e-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b4e-151">OUTPUTS</span></span>

### <span data-ttu-id="97b4e-152">System. String</span><span class="sxs-lookup"><span data-stu-id="97b4e-152">System.String</span></span>

## <span data-ttu-id="97b4e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97b4e-153">NOTES</span></span>

## <span data-ttu-id="97b4e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97b4e-154">RELATED LINKS</span></span>

[<span data-ttu-id="97b4e-155">Új – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="97b4e-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)
