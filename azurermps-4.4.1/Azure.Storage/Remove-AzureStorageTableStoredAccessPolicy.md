---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7ee384fb26ed8e16b377800fc7e3912f33b81669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493900"
---
# <span data-ttu-id="c9e16-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e16-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="c9e16-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9e16-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e16-103">A tárolt Access-házirendek eltávolítása az Azure Storage-táblájából.</span><span class="sxs-lookup"><span data-stu-id="c9e16-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9e16-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9e16-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9e16-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9e16-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e16-106">A **Remove-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table-ből eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="c9e16-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="c9e16-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9e16-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e16-108">1. példa: a tárolt Access-házirendek eltávolítása egy tárterület-táblából</span><span class="sxs-lookup"><span data-stu-id="c9e16-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="c9e16-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a táblanév nevű tárterület táblából.</span><span class="sxs-lookup"><span data-stu-id="c9e16-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="c9e16-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9e16-110">PARAMETERS</span></span>

### <span data-ttu-id="c9e16-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="c9e16-111">-Context</span></span>
<span data-ttu-id="c9e16-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9e16-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c9e16-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="c9e16-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c9e16-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9e16-114">-PassThru</span></span>
<span data-ttu-id="c9e16-115">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="c9e16-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c9e16-116">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="c9e16-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c9e16-117">-Házirend</span><span class="sxs-lookup"><span data-stu-id="c9e16-117">-Policy</span></span>
<span data-ttu-id="c9e16-118">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="c9e16-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9e16-119">-Table</span><span class="sxs-lookup"><span data-stu-id="c9e16-119">-Table</span></span>
<span data-ttu-id="c9e16-120">Az Azure-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c9e16-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="c9e16-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c9e16-121">-Confirm</span></span>
<span data-ttu-id="c9e16-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c9e16-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9e16-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e16-123">-WhatIf</span></span>
<span data-ttu-id="c9e16-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c9e16-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e16-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9e16-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9e16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e16-126">CommonParameters</span></span>
<span data-ttu-id="c9e16-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9e16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e16-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e16-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e16-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9e16-129">INPUTS</span></span>

### <span data-ttu-id="c9e16-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9e16-130">IStorageContext</span></span>

<span data-ttu-id="c9e16-131">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c9e16-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="c9e16-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9e16-132">OUTPUTS</span></span>

### <span data-ttu-id="c9e16-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9e16-133">System.Boolean</span></span>

## <span data-ttu-id="c9e16-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9e16-134">NOTES</span></span>

## <span data-ttu-id="c9e16-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9e16-135">RELATED LINKS</span></span>

[<span data-ttu-id="c9e16-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e16-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c9e16-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9e16-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c9e16-138">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e16-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="c9e16-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e16-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
