---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324642"
---
# <span data-ttu-id="f17d8-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f17d8-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f17d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f17d8-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárolótáblához.</span><span class="sxs-lookup"><span data-stu-id="f17d8-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f17d8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f17d8-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f17d8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f17d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f17d8-106">A **New-AzStorageTableStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárolótáblához.</span><span class="sxs-lookup"><span data-stu-id="f17d8-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f17d8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f17d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f17d8-108">1. példa: Tárolt hozzáférési házirend létrehozása táblában</span><span class="sxs-lookup"><span data-stu-id="f17d8-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="f17d8-109">Ez a parancs létrehoz egy Policy02 nevű hozzáférési házirendet a MyTable nevű tárolótáblában.</span><span class="sxs-lookup"><span data-stu-id="f17d8-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="f17d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f17d8-110">PARAMETERS</span></span>

### <span data-ttu-id="f17d8-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="f17d8-111">-Context</span></span>
<span data-ttu-id="f17d8-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f17d8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f17d8-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f17d8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f17d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17d8-114">-DefaultProfile</span></span>
<span data-ttu-id="f17d8-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f17d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f17d8-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f17d8-116">-ExpiryTime</span></span>
<span data-ttu-id="f17d8-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="f17d8-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f17d8-118">-Engedély</span><span class="sxs-lookup"><span data-stu-id="f17d8-118">-Permission</span></span>
<span data-ttu-id="f17d8-119">A tártábla eléréséhez szükséges engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="f17d8-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="f17d8-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="f17d8-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f17d8-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="f17d8-121">-Policy</span></span>
<span data-ttu-id="f17d8-122">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="f17d8-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17d8-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f17d8-123">-StartTime</span></span>
<span data-ttu-id="f17d8-124">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="f17d8-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f17d8-125">-Table</span><span class="sxs-lookup"><span data-stu-id="f17d8-125">-Table</span></span>
<span data-ttu-id="f17d8-126">Az Azure-tártábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f17d8-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f17d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17d8-127">CommonParameters</span></span>
<span data-ttu-id="f17d8-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17d8-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17d8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17d8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f17d8-130">INPUTS</span></span>

### <span data-ttu-id="f17d8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f17d8-131">System.String</span></span>

### <span data-ttu-id="f17d8-132">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f17d8-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f17d8-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f17d8-133">OUTPUTS</span></span>

### <span data-ttu-id="f17d8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f17d8-134">System.String</span></span>

## <span data-ttu-id="f17d8-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f17d8-135">NOTES</span></span>

## <span data-ttu-id="f17d8-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f17d8-136">RELATED LINKS</span></span>

[<span data-ttu-id="f17d8-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f17d8-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f17d8-138">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="f17d8-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f17d8-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f17d8-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f17d8-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f17d8-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


