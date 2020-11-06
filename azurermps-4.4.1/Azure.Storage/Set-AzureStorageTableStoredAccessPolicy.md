---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499319"
---
# <span data-ttu-id="86d44-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86d44-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="86d44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="86d44-102">SYNOPSIS</span></span>
<span data-ttu-id="86d44-103">Egy Azure Storage Table tárolt hozzáférés házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="86d44-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86d44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="86d44-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="86d44-105">DESCRIPTION</span></span>
<span data-ttu-id="86d44-106">A **set-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table tárolt hozzáférés házirendjének beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="86d44-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="86d44-107">Példák</span><span class="sxs-lookup"><span data-stu-id="86d44-107">EXAMPLES</span></span>

### <span data-ttu-id="86d44-108">1. példa: tárolt hozzáférés-házirend beállítása teljes engedélyekkel rendelkező táblában</span><span class="sxs-lookup"><span data-stu-id="86d44-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="86d44-109">Ez a parancs a Policy08 nevű Access-házirendet állítja be a táblanév nevű tárolási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="86d44-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="86d44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="86d44-110">PARAMETERS</span></span>

### <span data-ttu-id="86d44-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="86d44-111">-Context</span></span>
<span data-ttu-id="86d44-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86d44-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="86d44-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="86d44-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="86d44-114">-ExpiryTime</span></span>
<span data-ttu-id="86d44-115">Itt adhatja meg, hogy mikor jár le a tárolt hozzáférés-házirend.</span><span class="sxs-lookup"><span data-stu-id="86d44-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="86d44-116">-NoExpiryTime</span></span>
<span data-ttu-id="86d44-117">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="86d44-117">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="86d44-118">-NoStartTime</span></span>
<span data-ttu-id="86d44-119">Azt jelzi, hogy a kezdési időpont $Null értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="86d44-119">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-120">– Engedély</span><span class="sxs-lookup"><span data-stu-id="86d44-120">-Permission</span></span>
<span data-ttu-id="86d44-121">A tárolt hozzáférési házirend engedélyeit adja meg a tároló tábla eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="86d44-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="86d44-122">-Policy</span></span>
<span data-ttu-id="86d44-123">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86d44-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="86d44-124">-StartTime</span></span>
<span data-ttu-id="86d44-125">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="86d44-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-126">-Table</span><span class="sxs-lookup"><span data-stu-id="86d44-126">-Table</span></span>
<span data-ttu-id="86d44-127">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="86d44-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="86d44-128">-Confirm</span></span>
<span data-ttu-id="86d44-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="86d44-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d44-130">-WhatIf</span></span>
<span data-ttu-id="86d44-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="86d44-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86d44-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86d44-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d44-133">CommonParameters</span></span>
<span data-ttu-id="86d44-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="86d44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d44-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d44-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d44-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d44-136">INPUTS</span></span>

### <span data-ttu-id="86d44-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="86d44-137">IStorageContext</span></span>

<span data-ttu-id="86d44-138">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86d44-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="86d44-139">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="86d44-139">String</span></span>

<span data-ttu-id="86d44-140">A ' Table ' paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="86d44-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="86d44-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86d44-141">OUTPUTS</span></span>

### <span data-ttu-id="86d44-142">System. String</span><span class="sxs-lookup"><span data-stu-id="86d44-142">System.String</span></span>

## <span data-ttu-id="86d44-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="86d44-143">NOTES</span></span>

## <span data-ttu-id="86d44-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86d44-144">RELATED LINKS</span></span>

[<span data-ttu-id="86d44-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86d44-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="86d44-146">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="86d44-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="86d44-147">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86d44-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="86d44-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86d44-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
