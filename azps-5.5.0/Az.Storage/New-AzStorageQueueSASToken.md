---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueSASToken.md
ms.openlocfilehash: 17a7e32d0686e68b70f2129edfbb617661057218
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162963"
---
# <span data-ttu-id="f31fb-101">New-AzStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="f31fb-101">New-AzStorageQueueSASToken</span></span>

## <span data-ttu-id="f31fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f31fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f31fb-103">Megosztott hozzáférés aláírási jogkivonatot hoz létre egy Azure-társorhoz.</span><span class="sxs-lookup"><span data-stu-id="f31fb-103">Generates a shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f31fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f31fb-104">SYNTAX</span></span>

### <span data-ttu-id="f31fb-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="f31fb-105">SasPolicy</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f31fb-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="f31fb-106">SasPermission</span></span>
```
New-AzStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f31fb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f31fb-107">DESCRIPTION</span></span>
<span data-ttu-id="f31fb-108">A **New-AzStorageQueueSASToken** parancsmag megosztott hozzáférés-aláírási jogkivonatot hoz létre egy Azure-társorhoz.</span><span class="sxs-lookup"><span data-stu-id="f31fb-108">The **New-AzStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="f31fb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f31fb-109">EXAMPLES</span></span>

### <span data-ttu-id="f31fb-110">1. példa: Várólistás SAS-jogkivonat létrehozása teljes engedéllyel</span><span class="sxs-lookup"><span data-stu-id="f31fb-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="f31fb-111">Ez a példa teljes engedéllyel rendelkező várólistás SAS-jogkivonatot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f31fb-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="f31fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f31fb-112">PARAMETERS</span></span>

### <span data-ttu-id="f31fb-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f31fb-113">-Context</span></span>
<span data-ttu-id="f31fb-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f31fb-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f31fb-115">A parancsmagot New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="f31fb-115">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f31fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31fb-116">-DefaultProfile</span></span>
<span data-ttu-id="f31fb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f31fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31fb-118">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f31fb-118">-ExpiryTime</span></span>
<span data-ttu-id="f31fb-119">Azt adja meg, hogy a megosztott hozzáférés-aláírás mikor lesz érvényes.</span><span class="sxs-lookup"><span data-stu-id="f31fb-119">Specifies when the shared access signature is no longer valid.</span></span>

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

### <span data-ttu-id="f31fb-120">-FullUri</span><span class="sxs-lookup"><span data-stu-id="f31fb-120">-FullUri</span></span>
<span data-ttu-id="f31fb-121">Azt jelzi, hogy ez a parancsmag a teljes blob URI-t és a megosztott hozzáférés-aláírási jogkivonatot adja vissza.</span><span class="sxs-lookup"><span data-stu-id="f31fb-121">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="f31fb-122">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f31fb-122">-IPAddressOrRange</span></span>
<span data-ttu-id="f31fb-123">Megadja azt az IP-címet vagy IP-címtartományt, amelyből a kérelmeket el kell fogadni( például 168.1.5.65 vagy 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="f31fb-123">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="f31fb-124">A tartomány magában foglalja a teljes tartományt is.</span><span class="sxs-lookup"><span data-stu-id="f31fb-124">The range is inclusive.</span></span>

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

### <span data-ttu-id="f31fb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f31fb-125">-Name</span></span>
<span data-ttu-id="f31fb-126">Egy Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f31fb-126">Specifies an Azure storage queue name.</span></span>

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

### <span data-ttu-id="f31fb-127">-Permission</span><span class="sxs-lookup"><span data-stu-id="f31fb-127">-Permission</span></span>
<span data-ttu-id="f31fb-128">Egy tárterület-várólistára vonatkozó engedélyeket ad meg.</span><span class="sxs-lookup"><span data-stu-id="f31fb-128">Specifies permissions for a storage queue.</span></span>
<span data-ttu-id="f31fb-129">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="f31fb-129">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f31fb-130">-Házirend</span><span class="sxs-lookup"><span data-stu-id="f31fb-130">-Policy</span></span>
<span data-ttu-id="f31fb-131">Egy Azure tárolt hozzáférési házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="f31fb-131">Specifies an Azure stored access policy.</span></span>

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

### <span data-ttu-id="f31fb-132">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f31fb-132">-Protocol</span></span>
<span data-ttu-id="f31fb-133">A kéréshez engedélyezett protokollt adja meg.</span><span class="sxs-lookup"><span data-stu-id="f31fb-133">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="f31fb-134">A paraméter elfogadható értékei a következőek:</span><span class="sxs-lookup"><span data-stu-id="f31fb-134">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="f31fb-135">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="f31fb-135">HttpsOnly</span></span>
* <span data-ttu-id="f31fb-136">HttpsOrHttp Az alapértelmezett érték a httpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="f31fb-136">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="f31fb-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f31fb-137">-StartTime</span></span>
<span data-ttu-id="f31fb-138">Azt adja meg, hogy a megosztott hozzáférés-aláírás mikor lesz érvényes.</span><span class="sxs-lookup"><span data-stu-id="f31fb-138">Specifies when the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="f31fb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31fb-139">CommonParameters</span></span>
<span data-ttu-id="f31fb-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31fb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31fb-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f31fb-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31fb-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f31fb-142">INPUTS</span></span>

### <span data-ttu-id="f31fb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f31fb-143">System.String</span></span>

### <span data-ttu-id="f31fb-144">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f31fb-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f31fb-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f31fb-145">OUTPUTS</span></span>

### <span data-ttu-id="f31fb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f31fb-146">System.String</span></span>

## <span data-ttu-id="f31fb-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f31fb-147">NOTES</span></span>

## <span data-ttu-id="f31fb-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f31fb-148">RELATED LINKS</span></span>
