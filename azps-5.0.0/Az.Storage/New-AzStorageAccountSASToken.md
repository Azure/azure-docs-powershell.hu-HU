---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187177"
---
# <span data-ttu-id="f10cc-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="f10cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f10cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f10cc-103">Ügyfél szintű SAS-tokent hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f10cc-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="f10cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f10cc-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f10cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f10cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f10cc-106">A **New-AzStorageSASToken** parancsmag létrehoz egy ügyfél szintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure-tárterülethez.</span><span class="sxs-lookup"><span data-stu-id="f10cc-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="f10cc-107">A SAS-tokent használhatja több szolgáltatás engedélyeinek meghatalmazására, illetve a szolgáltatások engedélyeinek meghatalmazására, ha az objektum szintű SAS-tokent használja.</span><span class="sxs-lookup"><span data-stu-id="f10cc-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="f10cc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f10cc-108">EXAMPLES</span></span>

### <span data-ttu-id="f10cc-109">Példa 1: egy fiók szintű SAS-token létrehozása teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="f10cc-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="f10cc-110">A parancs teljes hozzáféréssel létrehoz egy fiók szintű SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="f10cc-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="f10cc-111">2. példa: fiók szintű SAS-token létrehozása IP-címekhez</span><span class="sxs-lookup"><span data-stu-id="f10cc-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="f10cc-112">Ez a parancs egy fiók szintű SAS-jogkivonatot hoz létre a HTTPS-only kérelmekhez a megadott IP-címtartományból.</span><span class="sxs-lookup"><span data-stu-id="f10cc-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="f10cc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f10cc-113">PARAMETERS</span></span>

### <span data-ttu-id="f10cc-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f10cc-114">-Context</span></span>
<span data-ttu-id="f10cc-115">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f10cc-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f10cc-116">A New-AzStorageContext parancsmaggal **AzureStorageContext** -objektumokat lehet kikeresni.</span><span class="sxs-lookup"><span data-stu-id="f10cc-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="f10cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10cc-117">-DefaultProfile</span></span>
<span data-ttu-id="f10cc-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f10cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f10cc-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f10cc-119">-ExpiryTime</span></span>
<span data-ttu-id="f10cc-120">Azt az időpontot adja meg, amikor a megosztott elérési aláírás érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="f10cc-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="f10cc-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f10cc-121">-IPAddressOrRange</span></span>
<span data-ttu-id="f10cc-122">Adja meg az IP-címet vagy az IP-címeket, amelyekből el szeretné fogadni a kéréseket, például a 168.1.5.65 vagy a 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f10cc-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f10cc-123">A tartomány bezárólag.</span><span class="sxs-lookup"><span data-stu-id="f10cc-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="f10cc-124">– Engedély</span><span class="sxs-lookup"><span data-stu-id="f10cc-124">-Permission</span></span>
<span data-ttu-id="f10cc-125">A tárolási fiók engedélyei.</span><span class="sxs-lookup"><span data-stu-id="f10cc-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="f10cc-126">Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrás-típusnak.</span><span class="sxs-lookup"><span data-stu-id="f10cc-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="f10cc-127">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="f10cc-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="f10cc-128">Az elfogadható jogosultsági értékekről további információt a fiók-SAS létrehozása című témakörben talál. http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="f10cc-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="f10cc-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f10cc-129">-Protocol</span></span>
<span data-ttu-id="f10cc-130">Annak a protokollnak a használatát adja meg, amely a biztonsági fiókkezelő fiókkal végzett kéréshez engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="f10cc-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="f10cc-131">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f10cc-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f10cc-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f10cc-132">HttpsOnly</span></span>
- <span data-ttu-id="f10cc-133">HttpsOrHttp: az alapértelmezett érték a HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f10cc-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f10cc-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f10cc-134">-ResourceType</span></span>
<span data-ttu-id="f10cc-135">A SAS-tokenhez elérhető erőforrás-típusokat adja meg.</span><span class="sxs-lookup"><span data-stu-id="f10cc-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="f10cc-136">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f10cc-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f10cc-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="f10cc-137">None</span></span>
- <span data-ttu-id="f10cc-138">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="f10cc-138">Service</span></span>
- <span data-ttu-id="f10cc-139">Konténer</span><span class="sxs-lookup"><span data-stu-id="f10cc-139">Container</span></span>
- <span data-ttu-id="f10cc-140">Objektum</span><span class="sxs-lookup"><span data-stu-id="f10cc-140">Object</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f10cc-141">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="f10cc-141">-Service</span></span>
<span data-ttu-id="f10cc-142">A szolgáltatást adja meg.</span><span class="sxs-lookup"><span data-stu-id="f10cc-142">Specifies the service.</span></span>
<span data-ttu-id="f10cc-143">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f10cc-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f10cc-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="f10cc-144">None</span></span>
- <span data-ttu-id="f10cc-145">BLOB</span><span class="sxs-lookup"><span data-stu-id="f10cc-145">Blob</span></span>
- <span data-ttu-id="f10cc-146">Fájl</span><span class="sxs-lookup"><span data-stu-id="f10cc-146">File</span></span>
- <span data-ttu-id="f10cc-147">Várólista</span><span class="sxs-lookup"><span data-stu-id="f10cc-147">Queue</span></span>
- <span data-ttu-id="f10cc-148">Táblázat</span><span class="sxs-lookup"><span data-stu-id="f10cc-148">Table</span></span>

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f10cc-149">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="f10cc-149">-StartTime</span></span>
<span data-ttu-id="f10cc-150">Itt adhatja meg **datetime** -objektumként az időt, amelyen a biztonsági társítás érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="f10cc-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="f10cc-151">A **datetime** objektum beszerzéséhez használja az Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f10cc-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="f10cc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10cc-152">CommonParameters</span></span>
<span data-ttu-id="f10cc-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f10cc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10cc-154">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10cc-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10cc-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10cc-155">INPUTS</span></span>

### <span data-ttu-id="f10cc-156">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f10cc-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f10cc-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f10cc-157">OUTPUTS</span></span>

### <span data-ttu-id="f10cc-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f10cc-158">System.String</span></span>

## <span data-ttu-id="f10cc-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f10cc-159">NOTES</span></span>

## <span data-ttu-id="f10cc-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f10cc-160">RELATED LINKS</span></span>

[<span data-ttu-id="f10cc-161">Új – AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="f10cc-162">Új – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="f10cc-163">Új – AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="f10cc-164">Új – AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="f10cc-165">Új – AzStorageShareSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="f10cc-166">Új – AzStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="f10cc-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)

