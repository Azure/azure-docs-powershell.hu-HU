---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 3ecea2e4eece9b4e0161a90cc597218d04a29bfc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002405"
---
# <span data-ttu-id="70d99-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="70d99-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="70d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70d99-102">SYNOPSIS</span></span>
<span data-ttu-id="70d99-103">Megosztott hozzáférés aláírási jogkivonatot hoz létre egy Azure-társorhoz.</span><span class="sxs-lookup"><span data-stu-id="70d99-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="70d99-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="70d99-104">SYNTAX</span></span>

### <span data-ttu-id="70d99-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="70d99-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70d99-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="70d99-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70d99-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="70d99-107">DESCRIPTION</span></span>
<span data-ttu-id="70d99-108">A **New-AzStorageQueueSASToken** parancsmag megosztott hozzáférés-aláírási jogkivonatot hoz létre egy Azure-társorhoz.</span><span class="sxs-lookup"><span data-stu-id="70d99-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="70d99-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="70d99-109">EXAMPLES</span></span>

### <span data-ttu-id="70d99-110">1. példa: Várólistás SAS-jogkivonat létrehozása teljes engedéllyel</span><span class="sxs-lookup"><span data-stu-id="70d99-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="70d99-111">Ez a példa teljes engedéllyel rendelkező várólistás SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="70d99-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="70d99-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70d99-112">PARAMETERS</span></span>

### <span data-ttu-id="70d99-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="70d99-113">-Context</span></span>
<span data-ttu-id="70d99-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="70d99-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="70d99-115">A parancsmagot New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="70d99-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="70d99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d99-116">-DefaultProfile</span></span>
<span data-ttu-id="70d99-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70d99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70d99-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="70d99-118">-ExpiryTime</span></span>
<span data-ttu-id="70d99-119">Azt adja meg, hogy a megosztott hozzáférés-aláírás mikor lesz érvényes.</span><span class="sxs-lookup"><span data-stu-id="70d99-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="70d99-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="70d99-120">-FullUri</span></span>
<span data-ttu-id="70d99-121">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="70d99-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="70d99-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="70d99-122">-IPAddressOrRange</span></span>
<span data-ttu-id="70d99-123">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="70d99-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="70d99-124">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="70d99-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="70d99-125">-Name</span><span class="sxs-lookup"><span data-stu-id="70d99-125">-Name</span></span>
<span data-ttu-id="70d99-126">Egy Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d99-126">Specifies an Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70d99-127">-Engedély</span><span class="sxs-lookup"><span data-stu-id="70d99-127">-Permission</span></span>
<span data-ttu-id="70d99-128">Egy tárterület-várólistára vonatkozó engedélyeket ad meg.</span><span class="sxs-lookup"><span data-stu-id="70d99-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="70d99-129">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="70d99-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="70d99-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="70d99-130">-Policy</span></span>
<span data-ttu-id="70d99-131">Egy Azure tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="70d99-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="70d99-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="70d99-132">-Protocol</span></span>
<span data-ttu-id="70d99-133">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="70d99-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="70d99-134">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="70d99-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="70d99-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="70d99-135">HttpsOnly</span></span>
* <span data-ttu-id="70d99-136">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="70d99-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="70d99-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="70d99-137">-StartTime</span></span>
<span data-ttu-id="70d99-138">Azt adja meg, hogy mikor lesz érvényes a megosztott hozzáférés aláírása.</span><span class="sxs-lookup"><span data-stu-id="70d99-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="70d99-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d99-139">CommonParameters</span></span>
<span data-ttu-id="70d99-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d99-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d99-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d99-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d99-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70d99-142">INPUTS</span></span>

### <span data-ttu-id="70d99-143">System.String</span><span class="sxs-lookup"><span data-stu-id="70d99-143">System.String</span></span>

### <span data-ttu-id="70d99-144">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="70d99-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="70d99-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70d99-145">OUTPUTS</span></span>

### <span data-ttu-id="70d99-146">System.String</span><span class="sxs-lookup"><span data-stu-id="70d99-146">System.String</span></span>

## <span data-ttu-id="70d99-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="70d99-147">NOTES</span></span>

## <span data-ttu-id="70d99-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70d99-148">RELATED LINKS</span></span>
