---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491778"
---
# <span data-ttu-id="b3e2d-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3e2d-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="b3e2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b3e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e2d-103">Egy Azure Storage Table tárolt hozzáférés házirendjének beállítása.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="b3e2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b3e2d-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b3e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e2d-106">A **set-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table tárolt hozzáférés házirendjének beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="b3e2d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b3e2d-107">EXAMPLES</span></span>

### <span data-ttu-id="b3e2d-108">1. példa: tárolt hozzáférés-házirend beállítása teljes engedélyekkel rendelkező táblában</span><span class="sxs-lookup"><span data-stu-id="b3e2d-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="b3e2d-109">Ez a parancs a Policy08 nevű Access-házirendet állítja be a táblanév nevű tárolási táblázathoz.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="b3e2d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b3e2d-110">PARAMETERS</span></span>

### <span data-ttu-id="b3e2d-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b3e2d-111">-Context</span></span>
<span data-ttu-id="b3e2d-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b3e2d-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3e2d-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b3e2d-114">-ExpiryTime</span></span>
<span data-ttu-id="b3e2d-115">Itt adhatja meg, hogy mikor jár le a tárolt hozzáférés-házirend.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="b3e2d-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b3e2d-116">-NoExpiryTime</span></span>
<span data-ttu-id="b3e2d-117">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="b3e2d-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="b3e2d-118">-NoStartTime</span></span>
<span data-ttu-id="b3e2d-119">Azt jelzi, hogy a kezdési időpont $Null értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="b3e2d-120">– Engedély</span><span class="sxs-lookup"><span data-stu-id="b3e2d-120">-Permission</span></span>
<span data-ttu-id="b3e2d-121">A tárterület-tábla nyilvános hozzáférésének szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-121">Specifies the level of public access to this storage table.</span></span>

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

### <span data-ttu-id="b3e2d-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="b3e2d-122">-Policy</span></span>
<span data-ttu-id="b3e2d-123">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="b3e2d-124">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="b3e2d-124">-StartTime</span></span>
<span data-ttu-id="b3e2d-125">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b3e2d-126">-Table</span><span class="sxs-lookup"><span data-stu-id="b3e2d-126">-Table</span></span>
<span data-ttu-id="b3e2d-127">Az Azure Storage táblanév nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="b3e2d-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b3e2d-128">-Confirm</span></span>
<span data-ttu-id="b3e2d-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e2d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e2d-130">-WhatIf</span></span>
<span data-ttu-id="b3e2d-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3e2d-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3e2d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e2d-133">CommonParameters</span></span>
<span data-ttu-id="b3e2d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b3e2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e2d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e2d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3e2d-136">INPUTS</span></span>

## <span data-ttu-id="b3e2d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3e2d-137">OUTPUTS</span></span>

## <span data-ttu-id="b3e2d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b3e2d-138">NOTES</span></span>

## <span data-ttu-id="b3e2d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3e2d-139">RELATED LINKS</span></span>

[<span data-ttu-id="b3e2d-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3e2d-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3e2d-141">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b3e2d-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b3e2d-142">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3e2d-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="b3e2d-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b3e2d-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
