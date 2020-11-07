---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageaccountsastoken
schema: 2.0.0
ms.openlocfilehash: 4addd74f4a57c261886ef3323517663d02ffbcba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849834"
---
# <span data-ttu-id="dfaeb-101">New-AzureStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-101">New-AzureStorageAccountSASToken</span></span>

## <span data-ttu-id="dfaeb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfaeb-103">Ügyfél szintű SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-103">Creates an account-level SAS token.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfaeb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfaeb-104">SYNTAX</span></span>

```
New-AzureStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfaeb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfaeb-105">DESCRIPTION</span></span>
<span data-ttu-id="dfaeb-106">A **New-AzureStorageSASToken** parancsmag létrehoz egy ügyfél szintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-106">The **New-AzureStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="dfaeb-107">A SAS-tokent használhatja több szolgáltatás engedélyeinek meghatalmazására, illetve a szolgáltatások engedélyeinek meghatalmazására, ha az objektum szintű SAS-tokent használja.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="dfaeb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dfaeb-108">EXAMPLES</span></span>

### <span data-ttu-id="dfaeb-109">Példa 1: egy fiók szintű SAS-token létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="dfaeb-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="dfaeb-110">A parancs teljes hozzáféréssel létrehoz egy fiók szintű SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="dfaeb-111">2. példa: fiók szintű SAS-token létrehozása IP-címekhez</span><span class="sxs-lookup"><span data-stu-id="dfaeb-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzureStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="dfaeb-112">Ez a parancs egy fiók szintű SAS-jogkivonatot hoz létre a HTTPS-only kérelmekhez a megadott IP-címtartományból.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="dfaeb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfaeb-113">PARAMETERS</span></span>

### <span data-ttu-id="dfaeb-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="dfaeb-114">-Context</span></span>
<span data-ttu-id="dfaeb-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dfaeb-116">A New-AzureStorageContext parancsmaggal **AzureStorageContext** -objektumokat lehet kikeresni.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-116">You can use the New-AzureStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="dfaeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfaeb-117">-DefaultProfile</span></span>
<span data-ttu-id="dfaeb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfaeb-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dfaeb-119">-ExpiryTime</span></span>
<span data-ttu-id="dfaeb-120">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="dfaeb-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="dfaeb-121">-IPAddressOrRange</span></span>
<span data-ttu-id="dfaeb-122">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="dfaeb-123">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="dfaeb-124">– Engedély</span><span class="sxs-lookup"><span data-stu-id="dfaeb-124">-Permission</span></span>
<span data-ttu-id="dfaeb-125">A tárolási fiók engedélyei.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="dfaeb-126">Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrás-típusnak.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="dfaeb-127">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="dfaeb-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="dfaeb-128">Az elfogadható jogosultsági értékekről további információt a fiók-SAS létrehozása című témakörben talál. https://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="dfaeb-128">For more information about acceptable permission values, see Constructing an Account SAS https://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="dfaeb-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dfaeb-129">-Protocol</span></span>
<span data-ttu-id="dfaeb-130">Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="dfaeb-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dfaeb-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfaeb-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="dfaeb-132">HttpsOnly</span></span>
- <span data-ttu-id="dfaeb-133">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="dfaeb-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="dfaeb-134">-ResourceType</span></span>
<span data-ttu-id="dfaeb-135">A SAS-tokenhez elérhető erőforrás-típusokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="dfaeb-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dfaeb-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfaeb-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="dfaeb-137">None</span></span>
- <span data-ttu-id="dfaeb-138">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="dfaeb-138">Service</span></span>
- <span data-ttu-id="dfaeb-139">Konténer</span><span class="sxs-lookup"><span data-stu-id="dfaeb-139">Container</span></span>
- <span data-ttu-id="dfaeb-140">Objektum</span><span class="sxs-lookup"><span data-stu-id="dfaeb-140">Object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfaeb-141">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="dfaeb-141">-Service</span></span>
<span data-ttu-id="dfaeb-142">A szolgáltatást adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-142">Specifies the service.</span></span>
<span data-ttu-id="dfaeb-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="dfaeb-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfaeb-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="dfaeb-144">None</span></span>
- <span data-ttu-id="dfaeb-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="dfaeb-145">Blob</span></span>
- <span data-ttu-id="dfaeb-146">Fájl</span><span class="sxs-lookup"><span data-stu-id="dfaeb-146">File</span></span>
- <span data-ttu-id="dfaeb-147">Várólista</span><span class="sxs-lookup"><span data-stu-id="dfaeb-147">Queue</span></span>
- <span data-ttu-id="dfaeb-148">Táblázat</span><span class="sxs-lookup"><span data-stu-id="dfaeb-148">Table</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfaeb-149">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="dfaeb-149">-StartTime</span></span>
<span data-ttu-id="dfaeb-150">Itt adhatja meg **datetime** -objektumként az időt, amelyen a biztonsági társítás érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="dfaeb-151">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="dfaeb-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="dfaeb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfaeb-152">CommonParameters</span></span>
<span data-ttu-id="dfaeb-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfaeb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfaeb-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfaeb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfaeb-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfaeb-155">INPUTS</span></span>

### <span data-ttu-id="dfaeb-156">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dfaeb-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dfaeb-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfaeb-157">OUTPUTS</span></span>

### <span data-ttu-id="dfaeb-158">System. String</span><span class="sxs-lookup"><span data-stu-id="dfaeb-158">System.String</span></span>

## <span data-ttu-id="dfaeb-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfaeb-159">NOTES</span></span>

## <span data-ttu-id="dfaeb-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfaeb-160">RELATED LINKS</span></span>

[<span data-ttu-id="dfaeb-161">Új – AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-161">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)

[<span data-ttu-id="dfaeb-162">Új – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-162">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)

[<span data-ttu-id="dfaeb-163">Új – AzureStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-163">New-AzureStorageFileSASToken</span></span>](./New-AzureStorageFileSASToken.md)

[<span data-ttu-id="dfaeb-164">Új – AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-164">New-AzureStorageQueueSASToken</span></span>](./New-AzureStorageQueueSASToken.md)

[<span data-ttu-id="dfaeb-165">Új – AzureStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-165">New-AzureStorageShareSASToken</span></span>](./New-AzureStorageShareSASToken.md)

[<span data-ttu-id="dfaeb-166">Új – AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="dfaeb-166">New-AzureStorageTableSASToken</span></span>](./New-AzureStorageTableSASToken.md)


