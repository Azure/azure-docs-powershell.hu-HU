---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924377"
---
# <span data-ttu-id="05208-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="05208-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="05208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05208-102">SYNOPSIS</span></span>
<span data-ttu-id="05208-103">Tárolt hozzáférési házirendet hoz létre egy Azure-tárolótáblához.</span><span class="sxs-lookup"><span data-stu-id="05208-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="05208-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="05208-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05208-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="05208-105">DESCRIPTION</span></span>
<span data-ttu-id="05208-106">A **New-AzStorageTableStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet hoz létre egy Azure-tárolótáblához.</span><span class="sxs-lookup"><span data-stu-id="05208-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="05208-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="05208-107">EXAMPLES</span></span>

### <span data-ttu-id="05208-108">1. példa: Tárolt hozzáférési házirend létrehozása táblában</span><span class="sxs-lookup"><span data-stu-id="05208-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="05208-109">Ez a parancs létrehoz egy Policy02 nevű hozzáférési házirendet a MyTable nevű tárolótáblában.</span><span class="sxs-lookup"><span data-stu-id="05208-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="05208-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05208-110">PARAMETERS</span></span>

### <span data-ttu-id="05208-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="05208-111">-Context</span></span>
<span data-ttu-id="05208-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05208-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="05208-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="05208-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="05208-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05208-114">-DefaultProfile</span></span>
<span data-ttu-id="05208-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05208-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05208-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="05208-116">-ExpiryTime</span></span>
<span data-ttu-id="05208-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="05208-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="05208-118">-Engedély</span><span class="sxs-lookup"><span data-stu-id="05208-118">-Permission</span></span>
<span data-ttu-id="05208-119">A tártábla eléréséhez szükséges engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="05208-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="05208-120">Fontos megjegyezni, hogy ez egy karakterlánc, például `raud` (Olvasás, Hozzáadás, Frissítés és Törlés).</span><span class="sxs-lookup"><span data-stu-id="05208-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

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

### <span data-ttu-id="05208-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="05208-121">-Policy</span></span>
<span data-ttu-id="05208-122">Megadja a tárolt hozzáférési házirend nevét.</span><span class="sxs-lookup"><span data-stu-id="05208-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="05208-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05208-123">-StartTime</span></span>
<span data-ttu-id="05208-124">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="05208-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="05208-125">-Table</span><span class="sxs-lookup"><span data-stu-id="05208-125">-Table</span></span>
<span data-ttu-id="05208-126">Az Azure-tártábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05208-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="05208-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05208-127">CommonParameters</span></span>
<span data-ttu-id="05208-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05208-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05208-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05208-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05208-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05208-130">INPUTS</span></span>

### <span data-ttu-id="05208-131">System.String</span><span class="sxs-lookup"><span data-stu-id="05208-131">System.String</span></span>

### <span data-ttu-id="05208-132">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="05208-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="05208-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05208-133">OUTPUTS</span></span>

### <span data-ttu-id="05208-134">System.String</span><span class="sxs-lookup"><span data-stu-id="05208-134">System.String</span></span>

## <span data-ttu-id="05208-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="05208-135">NOTES</span></span>

## <span data-ttu-id="05208-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05208-136">RELATED LINKS</span></span>

[<span data-ttu-id="05208-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="05208-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="05208-138">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="05208-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="05208-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="05208-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="05208-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="05208-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


