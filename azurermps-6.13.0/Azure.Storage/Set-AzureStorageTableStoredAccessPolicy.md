---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 80fe36072840d112c4c8849e72deedd0a7f49d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498583"
---
# <span data-ttu-id="8f8d0-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f8d0-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="8f8d0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8f8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8d0-103">Egy Azure Storage Table tárolt hozzáférés házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f8d0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8f8d0-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f8d0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8f8d0-105">DESCRIPTION</span></span>
<span data-ttu-id="8f8d0-106">A **set-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table tárolt hozzáférés házirendjének beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="8f8d0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8f8d0-107">EXAMPLES</span></span>

### <span data-ttu-id="8f8d0-108">1. példa: tárolt hozzáférés-házirend beállítása teljes engedélyekkel rendelkező táblában</span><span class="sxs-lookup"><span data-stu-id="8f8d0-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="8f8d0-109">Ez a parancs a Policy08 nevű Access-házirendet állítja be a táblanév nevű tárolási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="8f8d0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8f8d0-110">PARAMETERS</span></span>

### <span data-ttu-id="8f8d0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="8f8d0-111">-Context</span></span>
<span data-ttu-id="8f8d0-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8f8d0-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8f8d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8d0-114">-DefaultProfile</span></span>
<span data-ttu-id="8f8d0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f8d0-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f8d0-116">-ExpiryTime</span></span>
<span data-ttu-id="8f8d0-117">Itt adhatja meg, hogy mikor jár le a tárolt hozzáférés-házirend.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="8f8d0-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="8f8d0-118">-NoExpiryTime</span></span>
<span data-ttu-id="8f8d0-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="8f8d0-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="8f8d0-120">-NoStartTime</span></span>
<span data-ttu-id="8f8d0-121">Azt jelzi, hogy a kezdési időpont $Null értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="8f8d0-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="8f8d0-122">-Permission</span></span>
<span data-ttu-id="8f8d0-123">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="8f8d0-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="8f8d0-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="8f8d0-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8f8d0-125">-Policy</span></span>
<span data-ttu-id="8f8d0-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="8f8d0-127">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="8f8d0-127">-StartTime</span></span>
<span data-ttu-id="8f8d0-128">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="8f8d0-129">-Table</span><span class="sxs-lookup"><span data-stu-id="8f8d0-129">-Table</span></span>
<span data-ttu-id="8f8d0-130">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="8f8d0-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8f8d0-131">-Confirm</span></span>
<span data-ttu-id="8f8d0-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f8d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f8d0-133">-WhatIf</span></span>
<span data-ttu-id="8f8d0-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f8d0-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f8d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f8d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8d0-136">CommonParameters</span></span>
<span data-ttu-id="8f8d0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8f8d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8d0-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f8d0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8d0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f8d0-139">INPUTS</span></span>

### <span data-ttu-id="8f8d0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8f8d0-140">System.String</span></span>

### <span data-ttu-id="8f8d0-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f8d0-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8f8d0-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f8d0-142">OUTPUTS</span></span>

### <span data-ttu-id="8f8d0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8f8d0-143">System.String</span></span>

## <span data-ttu-id="8f8d0-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8f8d0-144">NOTES</span></span>

## <span data-ttu-id="8f8d0-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f8d0-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f8d0-146">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f8d0-146">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8f8d0-147">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8f8d0-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="8f8d0-148">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f8d0-148">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="8f8d0-149">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8f8d0-149">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
