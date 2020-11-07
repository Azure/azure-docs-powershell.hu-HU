---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850486"
---
# <span data-ttu-id="53359-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53359-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="53359-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53359-102">SYNOPSIS</span></span>
<span data-ttu-id="53359-103">A tárolt Access-házirendek eltávolítása az Azure Storage-táblájából.</span><span class="sxs-lookup"><span data-stu-id="53359-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53359-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53359-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53359-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="53359-105">DESCRIPTION</span></span>
<span data-ttu-id="53359-106">A **Remove-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table-ből eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="53359-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="53359-107">Példák</span><span class="sxs-lookup"><span data-stu-id="53359-107">EXAMPLES</span></span>

### <span data-ttu-id="53359-108">1. példa: a tárolt Access-házirendek eltávolítása egy tárterület-táblából</span><span class="sxs-lookup"><span data-stu-id="53359-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="53359-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a táblanév nevű tárterület táblából.</span><span class="sxs-lookup"><span data-stu-id="53359-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="53359-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53359-110">PARAMETERS</span></span>

### <span data-ttu-id="53359-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="53359-111">-Context</span></span>
<span data-ttu-id="53359-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53359-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="53359-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="53359-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="53359-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53359-114">-DefaultProfile</span></span>
<span data-ttu-id="53359-115">kommunikáció az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="53359-115">communication with Azure.</span></span>

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

### <span data-ttu-id="53359-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53359-116">-PassThru</span></span>
<span data-ttu-id="53359-117">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="53359-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="53359-118">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="53359-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="53359-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="53359-119">-Policy</span></span>
<span data-ttu-id="53359-120">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="53359-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53359-121">-Table</span><span class="sxs-lookup"><span data-stu-id="53359-121">-Table</span></span>
<span data-ttu-id="53359-122">Az Azure-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="53359-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53359-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="53359-123">-Confirm</span></span>
<span data-ttu-id="53359-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="53359-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53359-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53359-125">-WhatIf</span></span>
<span data-ttu-id="53359-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="53359-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53359-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="53359-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53359-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53359-128">CommonParameters</span></span>
<span data-ttu-id="53359-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53359-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53359-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53359-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53359-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53359-131">INPUTS</span></span>

### <span data-ttu-id="53359-132">System. String</span><span class="sxs-lookup"><span data-stu-id="53359-132">System.String</span></span>

### <span data-ttu-id="53359-133">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="53359-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="53359-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53359-134">OUTPUTS</span></span>

### <span data-ttu-id="53359-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53359-135">System.Boolean</span></span>

## <span data-ttu-id="53359-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53359-136">NOTES</span></span>

## <span data-ttu-id="53359-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53359-137">RELATED LINKS</span></span>

[<span data-ttu-id="53359-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53359-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="53359-139">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="53359-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="53359-140">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53359-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="53359-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53359-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
