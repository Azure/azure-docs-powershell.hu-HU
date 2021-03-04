---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 576b347ad260fc95cdafe7c4a11e42246feb09ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928466"
---
# <span data-ttu-id="0488b-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0488b-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="0488b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0488b-102">SYNOPSIS</span></span>
<span data-ttu-id="0488b-103">Beállítja egy Azure-tárhelytáblához a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="0488b-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="0488b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0488b-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0488b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0488b-105">DESCRIPTION</span></span>
<span data-ttu-id="0488b-106">A **Set-AzStorageTableStoredAccessPolicy** parancsmag egy Azure-tárolótábla tárolt hozzáférési házirendjeként szolgál.</span><span class="sxs-lookup"><span data-stu-id="0488b-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="0488b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0488b-107">EXAMPLES</span></span>

### <span data-ttu-id="0488b-108">1. példa: Tárolt hozzáférési házirend beállítása teljes engedéllyel rendelkező táblában</span><span class="sxs-lookup"><span data-stu-id="0488b-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="0488b-109">Ez a parancs beállítja a MyTable nevű tárterülettáblához a Policy08 nevű hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="0488b-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="0488b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0488b-110">PARAMETERS</span></span>

### <span data-ttu-id="0488b-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0488b-111">-Context</span></span>
<span data-ttu-id="0488b-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0488b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0488b-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0488b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0488b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0488b-114">-DefaultProfile</span></span>
<span data-ttu-id="0488b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0488b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0488b-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0488b-116">-ExpiryTime</span></span>
<span data-ttu-id="0488b-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend lejár.</span><span class="sxs-lookup"><span data-stu-id="0488b-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="0488b-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0488b-118">-NoExpiryTime</span></span>
<span data-ttu-id="0488b-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="0488b-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="0488b-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="0488b-120">-NoStartTime</span></span>
<span data-ttu-id="0488b-121">Azt jelzi, hogy a kezdési időpont $Null.</span><span class="sxs-lookup"><span data-stu-id="0488b-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="0488b-122">-Engedély</span><span class="sxs-lookup"><span data-stu-id="0488b-122">-Permission</span></span>
<span data-ttu-id="0488b-123">A tártábla eléréséhez szükséges engedélyeket adja meg a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="0488b-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="0488b-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="0488b-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0488b-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="0488b-125">-Policy</span></span>
<span data-ttu-id="0488b-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0488b-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="0488b-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0488b-127">-StartTime</span></span>
<span data-ttu-id="0488b-128">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="0488b-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="0488b-129">-Table</span><span class="sxs-lookup"><span data-stu-id="0488b-129">-Table</span></span>
<span data-ttu-id="0488b-130">Az Azure-tártábla nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0488b-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="0488b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0488b-131">-Confirm</span></span>
<span data-ttu-id="0488b-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0488b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0488b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0488b-133">-WhatIf</span></span>
<span data-ttu-id="0488b-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0488b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0488b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0488b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0488b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0488b-136">CommonParameters</span></span>
<span data-ttu-id="0488b-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0488b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0488b-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0488b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0488b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0488b-139">INPUTS</span></span>

### <span data-ttu-id="0488b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0488b-140">System.String</span></span>

### <span data-ttu-id="0488b-141">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0488b-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0488b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0488b-142">OUTPUTS</span></span>

### <span data-ttu-id="0488b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0488b-143">System.String</span></span>

## <span data-ttu-id="0488b-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0488b-144">NOTES</span></span>

## <span data-ttu-id="0488b-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0488b-145">RELATED LINKS</span></span>

[<span data-ttu-id="0488b-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0488b-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="0488b-147">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="0488b-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0488b-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0488b-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="0488b-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0488b-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
