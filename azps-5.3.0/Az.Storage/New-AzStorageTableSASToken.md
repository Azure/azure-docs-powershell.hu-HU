---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableSASToken.md
ms.openlocfilehash: bf17a44b4f67d545ed464670776a5fc4c81b315a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479410"
---
# <span data-ttu-id="9adc7-101">New-AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="9adc7-101">New-AzStorageTableSASToken</span></span>

## <span data-ttu-id="9adc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adc7-102">SYNOPSIS</span></span>
<span data-ttu-id="9adc7-103">Egy Azure Storage-táblához létrehoz egy SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="9adc7-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="9adc7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9adc7-104">SYNTAX</span></span>

### <span data-ttu-id="9adc7-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="9adc7-105">SasPolicy</span></span>
```
New-AzStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9adc7-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="9adc7-106">SasPermission</span></span>
```
New-AzStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9adc7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9adc7-107">DESCRIPTION</span></span>
<span data-ttu-id="9adc7-108">A **New-AzStorageTableSASToken** parancsmag egy Azure Storage-táblához létrehoz egy SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="9adc7-108">The **New-AzStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="9adc7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9adc7-109">EXAMPLES</span></span>

### <span data-ttu-id="9adc7-110">1. példa: Egy tábla teljes engedélyekkel rendelkező SAS-jogkivonat létrehozása</span><span class="sxs-lookup"><span data-stu-id="9adc7-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="9adc7-111">Ez a parancs létrehoz egy TELJES engedélyekkel rendelkező SAS-jogkivonatot a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="9adc7-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="9adc7-112">Ez a jogkivonat olvasási, hozzáadási, frissítési és törlési engedélyekhez szükséges.</span><span class="sxs-lookup"><span data-stu-id="9adc7-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="9adc7-113">2. példa: SAS-jogkivonat létrehozása egy partíciótartományhoz</span><span class="sxs-lookup"><span data-stu-id="9adc7-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="9adc7-114">Ez a parancs a ContosoResources nevű tábla teljes engedélyekkel rendelkező SAS-jogkivonatát generálja.</span><span class="sxs-lookup"><span data-stu-id="9adc7-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="9adc7-115">A parancs a tokent a *StartPartitionKey* és *az EndPartitionKey* paraméter által megadott tartományra korlátozza.</span><span class="sxs-lookup"><span data-stu-id="9adc7-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="9adc7-116">3. példa: OLYAN SAS-jogkivonat létrehozása, amely egy táblához tárolt hozzáférési házirendet biztosít</span><span class="sxs-lookup"><span data-stu-id="9adc7-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="9adc7-117">Ez a parancs egy SAS-jogkivonatot hoz létre a ContosoResources nevű táblához.</span><span class="sxs-lookup"><span data-stu-id="9adc7-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="9adc7-118">A parancs a ClientPolicy01 nevű tárolt hozzáférési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="9adc7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9adc7-119">PARAMETERS</span></span>

### <span data-ttu-id="9adc7-120">-Környezet</span><span class="sxs-lookup"><span data-stu-id="9adc7-120">-Context</span></span>
<span data-ttu-id="9adc7-121">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9adc7-122">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="9adc7-122">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9adc7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adc7-123">-DefaultProfile</span></span>
<span data-ttu-id="9adc7-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9adc7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adc7-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="9adc7-125">-EndPartitionKey</span></span>
<span data-ttu-id="9adc7-126">A parancsmag által létrehozott jogkivonat tartománya végének partíciókulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="9adc7-127">-EndRowKey</span></span>
<span data-ttu-id="9adc7-128">A parancsmag által létrehozott jogkivonat tartományának végének sorkulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9adc7-129">-ExpiryTime</span></span>
<span data-ttu-id="9adc7-130">Azt adja meg, hogy mikor jár le az SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="9adc7-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="9adc7-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="9adc7-131">-FullUri</span></span>
<span data-ttu-id="9adc7-132">Azt jelzi, hogy ez a parancsmag az SAS-jogkivonattal együtt a teljes várólistás URI-t adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9adc7-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="9adc7-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9adc7-133">-IPAddressOrRange</span></span>
<span data-ttu-id="9adc7-134">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="9adc7-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="9adc7-135">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="9adc7-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="9adc7-136">-Name</span><span class="sxs-lookup"><span data-stu-id="9adc7-136">-Name</span></span>
<span data-ttu-id="9adc7-137">Egy Azure Storage-tábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="9adc7-138">Ez a parancsmag létrehoz egy SAS-jogkivonatot a paraméter által megadott táblához.</span><span class="sxs-lookup"><span data-stu-id="9adc7-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-139">-Engedély</span><span class="sxs-lookup"><span data-stu-id="9adc7-139">-Permission</span></span>
<span data-ttu-id="9adc7-140">Engedélyeket ad meg egy Azure Storage-táblához.</span><span class="sxs-lookup"><span data-stu-id="9adc7-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="9adc7-141">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="9adc7-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="9adc7-142">-Házirend</span><span class="sxs-lookup"><span data-stu-id="9adc7-142">-Policy</span></span>
<span data-ttu-id="9adc7-143">Egy tárolt hozzáférési házirendet ad meg, amely tartalmazza az SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="9adc7-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="9adc7-144">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9adc7-144">-Protocol</span></span>
<span data-ttu-id="9adc7-145">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="9adc7-146">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="9adc7-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="9adc7-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9adc7-147">HttpsOnly</span></span>
* <span data-ttu-id="9adc7-148">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="9adc7-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Cosmos.Table.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="9adc7-149">-StartPartitionKey</span></span>
<span data-ttu-id="9adc7-150">A parancsmag által létrehozott token tartományának kezdő partíciókulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="9adc7-151">-StartRowKey</span></span>
<span data-ttu-id="9adc7-152">A parancsmag által létrehozott token tartományának kezdő sorkulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9adc7-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adc7-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9adc7-153">-StartTime</span></span>
<span data-ttu-id="9adc7-154">Azt adja meg, hogy mikor lesz érvényes az SAS-jogkivonat.</span><span class="sxs-lookup"><span data-stu-id="9adc7-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="9adc7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adc7-155">CommonParameters</span></span>
<span data-ttu-id="9adc7-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9adc7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adc7-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9adc7-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adc7-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9adc7-158">INPUTS</span></span>

### <span data-ttu-id="9adc7-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9adc7-159">System.String</span></span>

### <span data-ttu-id="9adc7-160">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9adc7-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9adc7-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9adc7-161">OUTPUTS</span></span>

### <span data-ttu-id="9adc7-162">System.String</span><span class="sxs-lookup"><span data-stu-id="9adc7-162">System.String</span></span>

## <span data-ttu-id="9adc7-163">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9adc7-163">NOTES</span></span>

## <span data-ttu-id="9adc7-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9adc7-164">RELATED LINKS</span></span>

[<span data-ttu-id="9adc7-165">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="9adc7-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
