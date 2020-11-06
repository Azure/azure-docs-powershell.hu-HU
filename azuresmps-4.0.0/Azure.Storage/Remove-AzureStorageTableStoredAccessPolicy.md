---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490992"
---
# <span data-ttu-id="e43b2-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e43b2-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="e43b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e43b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e43b2-103">A tárolt Access-házirendek eltávolítása az Azure Storage-táblájából.</span><span class="sxs-lookup"><span data-stu-id="e43b2-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="e43b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e43b2-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e43b2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e43b2-105">DESCRIPTION</span></span>
<span data-ttu-id="e43b2-106">A **Remove-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table-ből eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="e43b2-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="e43b2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e43b2-107">EXAMPLES</span></span>

### <span data-ttu-id="e43b2-108">1. példa: a tárolt Access-házirendek eltávolítása egy tárterület-táblából</span><span class="sxs-lookup"><span data-stu-id="e43b2-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="e43b2-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a táblanév nevű tárterület táblából.</span><span class="sxs-lookup"><span data-stu-id="e43b2-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="e43b2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e43b2-110">PARAMETERS</span></span>

### <span data-ttu-id="e43b2-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e43b2-111">-Context</span></span>
<span data-ttu-id="e43b2-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e43b2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e43b2-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e43b2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e43b2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e43b2-114">-PassThru</span></span>
<span data-ttu-id="e43b2-115">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="e43b2-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e43b2-116">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="e43b2-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e43b2-117">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e43b2-117">-Policy</span></span>
<span data-ttu-id="e43b2-118">A tárolt elérési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="e43b2-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43b2-119">-Table</span><span class="sxs-lookup"><span data-stu-id="e43b2-119">-Table</span></span>
<span data-ttu-id="e43b2-120">Az Azure-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e43b2-120">Specifies the Azure table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43b2-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e43b2-121">-Confirm</span></span>
<span data-ttu-id="e43b2-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e43b2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43b2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43b2-123">-WhatIf</span></span>
<span data-ttu-id="e43b2-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e43b2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e43b2-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e43b2-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43b2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43b2-126">CommonParameters</span></span>
<span data-ttu-id="e43b2-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e43b2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43b2-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e43b2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43b2-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43b2-129">INPUTS</span></span>

## <span data-ttu-id="e43b2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e43b2-130">OUTPUTS</span></span>

## <span data-ttu-id="e43b2-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e43b2-131">NOTES</span></span>

## <span data-ttu-id="e43b2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e43b2-132">RELATED LINKS</span></span>

[<span data-ttu-id="e43b2-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e43b2-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e43b2-134">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e43b2-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e43b2-135">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e43b2-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e43b2-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e43b2-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
