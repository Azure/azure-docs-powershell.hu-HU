---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 76f36fa6cc7b2ab51604f59fb40170734f5ce99f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668557"
---
# <span data-ttu-id="96cb6-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb6-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="96cb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="96cb6-103">A tárolt Access-házirendek eltávolítása az Azure Storage-táblájából.</span><span class="sxs-lookup"><span data-stu-id="96cb6-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="96cb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96cb6-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96cb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="96cb6-106">A **Remove-AzStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table-ből eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="96cb6-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="96cb6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="96cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="96cb6-108">1. példa: a tárolt Access-házirendek eltávolítása egy tárterület-táblából</span><span class="sxs-lookup"><span data-stu-id="96cb6-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="96cb6-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a táblanév nevű tárterület táblából.</span><span class="sxs-lookup"><span data-stu-id="96cb6-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="96cb6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96cb6-110">PARAMETERS</span></span>

### <span data-ttu-id="96cb6-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="96cb6-111">-Context</span></span>
<span data-ttu-id="96cb6-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96cb6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="96cb6-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="96cb6-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="96cb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cb6-114">-DefaultProfile</span></span>
<span data-ttu-id="96cb6-115">kommunikáció az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="96cb6-115">communication with Azure.</span></span>

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

### <span data-ttu-id="96cb6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96cb6-116">-PassThru</span></span>
<span data-ttu-id="96cb6-117">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="96cb6-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="96cb6-118">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="96cb6-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="96cb6-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="96cb6-119">-Policy</span></span>
<span data-ttu-id="96cb6-120">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="96cb6-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96cb6-121">-Table</span><span class="sxs-lookup"><span data-stu-id="96cb6-121">-Table</span></span>
<span data-ttu-id="96cb6-122">Az Azure-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96cb6-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="96cb6-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96cb6-123">-Confirm</span></span>
<span data-ttu-id="96cb6-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96cb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96cb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cb6-125">-WhatIf</span></span>
<span data-ttu-id="96cb6-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96cb6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96cb6-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96cb6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96cb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cb6-128">CommonParameters</span></span>
<span data-ttu-id="96cb6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96cb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cb6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cb6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96cb6-131">INPUTS</span></span>

### <span data-ttu-id="96cb6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="96cb6-132">System.String</span></span>

### <span data-ttu-id="96cb6-133">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cb6-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="96cb6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96cb6-134">OUTPUTS</span></span>

### <span data-ttu-id="96cb6-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96cb6-135">System.Boolean</span></span>

## <span data-ttu-id="96cb6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96cb6-136">NOTES</span></span>

## <span data-ttu-id="96cb6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96cb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="96cb6-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb6-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="96cb6-139">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="96cb6-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="96cb6-140">Új – AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb6-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="96cb6-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb6-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
