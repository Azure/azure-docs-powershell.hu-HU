---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: fe98eee14797ff26c39b003d8ab1c9826c8ec687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842853"
---
# <span data-ttu-id="6bc35-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6bc35-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="6bc35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bc35-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc35-103">Egy Azure Storage Table tárolt hozzáférés házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="6bc35-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6bc35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bc35-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bc35-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc35-106">A **set-AzStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table tárolt hozzáférés házirendjének beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bc35-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6bc35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6bc35-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc35-108">1. példa: tárolt hozzáférés-házirend beállítása teljes engedélyekkel rendelkező táblában</span><span class="sxs-lookup"><span data-stu-id="6bc35-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="6bc35-109">Ez a parancs a Policy08 nevű Access-házirendet állítja be a táblanév nevű tárolási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="6bc35-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="6bc35-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bc35-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc35-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6bc35-111">-Context</span></span>
<span data-ttu-id="6bc35-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bc35-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6bc35-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="6bc35-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6bc35-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc35-114">-DefaultProfile</span></span>
<span data-ttu-id="6bc35-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bc35-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc35-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6bc35-116">-ExpiryTime</span></span>
<span data-ttu-id="6bc35-117">Itt adhatja meg, hogy mikor jár le a tárolt hozzáférés-házirend.</span><span class="sxs-lookup"><span data-stu-id="6bc35-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="6bc35-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6bc35-118">-NoExpiryTime</span></span>
<span data-ttu-id="6bc35-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="6bc35-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6bc35-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="6bc35-120">-NoStartTime</span></span>
<span data-ttu-id="6bc35-121">Azt jelzi, hogy a kezdési időpont $Null értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="6bc35-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="6bc35-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="6bc35-122">-Permission</span></span>
<span data-ttu-id="6bc35-123">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="6bc35-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="6bc35-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="6bc35-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6bc35-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="6bc35-125">-Policy</span></span>
<span data-ttu-id="6bc35-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bc35-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="6bc35-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="6bc35-127">-StartTime</span></span>
<span data-ttu-id="6bc35-128">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="6bc35-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6bc35-129">-Table</span><span class="sxs-lookup"><span data-stu-id="6bc35-129">-Table</span></span>
<span data-ttu-id="6bc35-130">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6bc35-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="6bc35-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6bc35-131">-Confirm</span></span>
<span data-ttu-id="6bc35-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bc35-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc35-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc35-133">-WhatIf</span></span>
<span data-ttu-id="6bc35-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6bc35-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bc35-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bc35-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc35-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc35-136">CommonParameters</span></span>
<span data-ttu-id="6bc35-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bc35-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc35-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc35-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc35-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bc35-139">INPUTS</span></span>

### <span data-ttu-id="6bc35-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6bc35-140">System.String</span></span>

### <span data-ttu-id="6bc35-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6bc35-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6bc35-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bc35-142">OUTPUTS</span></span>

### <span data-ttu-id="6bc35-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6bc35-143">System.String</span></span>

## <span data-ttu-id="6bc35-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bc35-144">NOTES</span></span>

## <span data-ttu-id="6bc35-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bc35-145">RELATED LINKS</span></span>

[<span data-ttu-id="6bc35-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6bc35-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6bc35-147">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6bc35-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6bc35-148">Új – AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6bc35-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6bc35-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6bc35-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
