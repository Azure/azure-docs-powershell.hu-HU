---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162978"
---
# <span data-ttu-id="3a6c4-101">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-101">New-AzStorageAccountSASToken</span></span>

## <span data-ttu-id="3a6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6c4-103">Létrehoz egy fiókszintű SAS-jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-103">Creates an account-level SAS token.</span></span>

## <span data-ttu-id="3a6c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-104">SYNTAX</span></span>

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a6c4-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-105">DESCRIPTION</span></span>
<span data-ttu-id="3a6c4-106">A **New-AzStorageSASToken** parancsmag létrehoz egy fiókszintű megosztott hozzáférés-aláírási (SAS) jogkivonatot egy Azure Storage-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-106">The **New-AzStorageSASToken** cmdlet creates an account-level shared access signature (SAS) token for an Azure Storage account.</span></span>
<span data-ttu-id="3a6c4-107">Az SAS-jogkivonattal delegálhatja több szolgáltatás engedélyét, illetve delegálhatja az objektumszintű SAS-jogkivonattal nem elérhető szolgáltatások engedélyét.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-107">You can use the SAS token to delegate permissions for multiple services, or to delegate permissions for services not available with an object-level SAS token.</span></span>

## <span data-ttu-id="3a6c4-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a6c4-108">EXAMPLES</span></span>

### <span data-ttu-id="3a6c4-109">1. példa: Fiókszintű SAS-jogkivonat létrehozása teljes engedéllyel</span><span class="sxs-lookup"><span data-stu-id="3a6c4-109">Example 1: Create an account-level SAS token with full permission</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

<span data-ttu-id="3a6c4-110">Ez a parancs létrehoz egy fiókszintű SAS-jogkivonatot teljes engedéllyel.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-110">This command creates an account-level SAS token with full permission.</span></span>

### <span data-ttu-id="3a6c4-111">2. példa: Fiókszintű SAS-jogkivonat létrehozása IP-címek tartományhoz</span><span class="sxs-lookup"><span data-stu-id="3a6c4-111">Example 2: Create an account-level SAS token for a range of IP addresses</span></span>
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

<span data-ttu-id="3a6c4-112">Ez a parancs létrehoz egy fiókszintű SAS-jogkivonatot a https-only kérések számára a megadott IP-címtartományból.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-112">This command creates an account-level SAS token for HTTPS-only requests from the specified range of IP addresses.</span></span>

## <span data-ttu-id="3a6c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-113">PARAMETERS</span></span>

### <span data-ttu-id="3a6c4-114">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3a6c4-114">-Context</span></span>
<span data-ttu-id="3a6c4-115">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3a6c4-116">A New-AzStorageContext segítségével **azureStorageContext objektumot** is be tud szerezni.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-116">You can use the New-AzStorageContext cmdlet to get an **AzureStorageContext** object.</span></span>

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

### <span data-ttu-id="3a6c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6c4-117">-DefaultProfile</span></span>
<span data-ttu-id="3a6c4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6c4-119">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3a6c4-119">-ExpiryTime</span></span>
<span data-ttu-id="3a6c4-120">Azt az időt adja meg, amikor a megosztott hozzáférés aláírása érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-120">Specifies the time at which the shared access signature becomes invalid.</span></span>

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

### <span data-ttu-id="3a6c4-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3a6c4-121">-IPAddressOrRange</span></span>
<span data-ttu-id="3a6c4-122">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-122">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3a6c4-123">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-123">The range is inclusive.</span></span>

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

### <span data-ttu-id="3a6c4-124">-Permission</span><span class="sxs-lookup"><span data-stu-id="3a6c4-124">-Permission</span></span>
<span data-ttu-id="3a6c4-125">A Tárfiók engedélyeinek megadása.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-125">Specifies the permissions for Storage account.</span></span>
<span data-ttu-id="3a6c4-126">Az engedélyek csak akkor érvényesek, ha megfelelnek a megadott erőforrástípusnak.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-126">Permissions are valid only if they match the specified resource type.</span></span>
<span data-ttu-id="3a6c4-127">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="3a6c4-127">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>
<span data-ttu-id="3a6c4-128">Az elfogadható engedélyértékekkel kapcsolatos további információkért lásd: Account SAS létrehozása http://go.microsoft.com/fwlink/?LinkId=799514</span><span class="sxs-lookup"><span data-stu-id="3a6c4-128">For more information about acceptable permission values, see Constructing an Account SAS http://go.microsoft.com/fwlink/?LinkId=799514</span></span>

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

### <span data-ttu-id="3a6c4-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="3a6c4-129">-Protocol</span></span>
<span data-ttu-id="3a6c4-130">A fiók SAS-hez való kérése esetén engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-130">Specifies the protocol permitted for a request made with the account SAS.</span></span>
<span data-ttu-id="3a6c4-131">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3a6c4-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a6c4-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3a6c4-132">HttpsOnly</span></span>
- <span data-ttu-id="3a6c4-133">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-133">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3a6c4-134">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3a6c4-134">-ResourceType</span></span>
<span data-ttu-id="3a6c4-135">Megadja az SAS-jogkivonattal elérhető erőforrástípusokat.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-135">Specifies the resource types that are available with the SAS token.</span></span>
<span data-ttu-id="3a6c4-136">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3a6c4-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a6c4-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a6c4-137">None</span></span>
- <span data-ttu-id="3a6c4-138">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="3a6c4-138">Service</span></span>
- <span data-ttu-id="3a6c4-139">Tároló</span><span class="sxs-lookup"><span data-stu-id="3a6c4-139">Container</span></span>
- <span data-ttu-id="3a6c4-140">Objektum</span><span class="sxs-lookup"><span data-stu-id="3a6c4-140">Object</span></span>

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

### <span data-ttu-id="3a6c4-141">-Service</span><span class="sxs-lookup"><span data-stu-id="3a6c4-141">-Service</span></span>
<span data-ttu-id="3a6c4-142">A szolgáltatást határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-142">Specifies the service.</span></span>
<span data-ttu-id="3a6c4-143">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="3a6c4-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3a6c4-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a6c4-144">None</span></span>
- <span data-ttu-id="3a6c4-145">Blob</span><span class="sxs-lookup"><span data-stu-id="3a6c4-145">Blob</span></span>
- <span data-ttu-id="3a6c4-146">Fájl</span><span class="sxs-lookup"><span data-stu-id="3a6c4-146">File</span></span>
- <span data-ttu-id="3a6c4-147">Várólistán</span><span class="sxs-lookup"><span data-stu-id="3a6c4-147">Queue</span></span>
- <span data-ttu-id="3a6c4-148">Táblázat</span><span class="sxs-lookup"><span data-stu-id="3a6c4-148">Table</span></span>

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

### <span data-ttu-id="3a6c4-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3a6c4-149">-StartTime</span></span>
<span data-ttu-id="3a6c4-150">Azt az időpontot adja meg **DateTime-objektumként,** amikorra az SAS érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-150">Specifies the time, as a **DateTime** object, at which the SAS becomes valid.</span></span>
<span data-ttu-id="3a6c4-151">**DateTime-objektum** betöltéshez használja a Get-Date parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-151">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="3a6c4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6c4-152">CommonParameters</span></span>
<span data-ttu-id="3a6c4-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a6c4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6c4-154">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a6c4-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6c4-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a6c4-155">INPUTS</span></span>

### <span data-ttu-id="3a6c4-156">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3a6c4-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3a6c4-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a6c4-157">OUTPUTS</span></span>

### <span data-ttu-id="3a6c4-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3a6c4-158">System.String</span></span>

## <span data-ttu-id="3a6c4-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a6c4-159">NOTES</span></span>

## <span data-ttu-id="3a6c4-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a6c4-160">RELATED LINKS</span></span>

[<span data-ttu-id="3a6c4-161">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-161">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)

[<span data-ttu-id="3a6c4-162">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-162">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)

[<span data-ttu-id="3a6c4-163">New-AzStorageFileSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-163">New-AzStorageFileSASToken</span></span>](./New-AzStorageFileSASToken.md)

[<span data-ttu-id="3a6c4-164">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-164">New-AzStorageQueueSASToken</span></span>](./New-AzStorageQueueSASToken.md)

[<span data-ttu-id="3a6c4-165">New-AzstorageSharesASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-165">New-AzStorageShareSASToken</span></span>](./New-AzStorageShareSASToken.md)

[<span data-ttu-id="3a6c4-166">New-AzstorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="3a6c4-166">New-AzStorageTableSASToken</span></span>](./New-AzStorageTableSASToken.md)


