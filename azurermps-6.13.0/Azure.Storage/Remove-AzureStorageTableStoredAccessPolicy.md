---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b1e06a31cfbe16cb04a7158cd62858683db6e131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494240"
---
# <span data-ttu-id="4aa11-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4aa11-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4aa11-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4aa11-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa11-103">A tárolt Access-házirendek eltávolítása az Azure Storage-táblájából.</span><span class="sxs-lookup"><span data-stu-id="4aa11-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa11-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4aa11-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4aa11-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4aa11-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa11-106">A **Remove-AzureStorageTableStoredAccessPolicy** parancsmag az Azure Storage Table-ből eltávolítja a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="4aa11-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="4aa11-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4aa11-107">EXAMPLES</span></span>

### <span data-ttu-id="4aa11-108">1. példa: a tárolt Access-házirendek eltávolítása egy tárterület-táblából</span><span class="sxs-lookup"><span data-stu-id="4aa11-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="4aa11-109">Ez a parancs eltávolítja a Policy05 nevű házirendet a táblanév nevű tárterület táblából.</span><span class="sxs-lookup"><span data-stu-id="4aa11-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="4aa11-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4aa11-110">PARAMETERS</span></span>

### <span data-ttu-id="4aa11-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4aa11-111">-Context</span></span>
<span data-ttu-id="4aa11-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4aa11-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4aa11-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="4aa11-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4aa11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa11-114">-DefaultProfile</span></span>
<span data-ttu-id="4aa11-115">kommunikáció az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="4aa11-115">communication with Azure.</span></span>

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

### <span data-ttu-id="4aa11-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aa11-116">-PassThru</span></span>
<span data-ttu-id="4aa11-117">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="4aa11-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4aa11-118">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="4aa11-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4aa11-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="4aa11-119">-Policy</span></span>
<span data-ttu-id="4aa11-120">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4aa11-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4aa11-121">-Table</span><span class="sxs-lookup"><span data-stu-id="4aa11-121">-Table</span></span>
<span data-ttu-id="4aa11-122">Az Azure-táblázat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4aa11-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="4aa11-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4aa11-123">-Confirm</span></span>
<span data-ttu-id="4aa11-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4aa11-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aa11-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa11-125">-WhatIf</span></span>
<span data-ttu-id="4aa11-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4aa11-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa11-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4aa11-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aa11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa11-128">CommonParameters</span></span>
<span data-ttu-id="4aa11-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4aa11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa11-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa11-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa11-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aa11-131">INPUTS</span></span>

### <span data-ttu-id="4aa11-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa11-132">System.String</span></span>

### <span data-ttu-id="4aa11-133">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4aa11-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4aa11-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aa11-134">OUTPUTS</span></span>

### <span data-ttu-id="4aa11-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4aa11-135">System.Boolean</span></span>

## <span data-ttu-id="4aa11-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4aa11-136">NOTES</span></span>

## <span data-ttu-id="4aa11-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aa11-137">RELATED LINKS</span></span>

[<span data-ttu-id="4aa11-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4aa11-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4aa11-139">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4aa11-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4aa11-140">Új – AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4aa11-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4aa11-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4aa11-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
