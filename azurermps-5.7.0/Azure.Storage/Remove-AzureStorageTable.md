---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673069"
---
# <span data-ttu-id="b6b78-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6b78-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="b6b78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6b78-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b78-103">Tároló tábla eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b6b78-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6b78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6b78-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b78-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6b78-105">DESCRIPTION</span></span>
<span data-ttu-id="b6b78-106">A **Remove-AzureStorageTable** parancsmag egy vagy több tároló táblát eltávolít egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="b6b78-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="b6b78-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b6b78-107">EXAMPLES</span></span>

### <span data-ttu-id="b6b78-108">1. példa: táblázat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6b78-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="b6b78-109">A parancs eltávolítja a táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b6b78-109">This command removes a table.</span></span>

### <span data-ttu-id="b6b78-110">2. példa: több tábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="b6b78-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="b6b78-111">Ez a példa egy helyettesítő karaktert használ a *Name* paraméterrel a minta táblázatnak megfelelő összes táblázat beolvasásához, majd átadja az eredményt a csővezetéken a táblák eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="b6b78-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="b6b78-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6b78-112">PARAMETERS</span></span>

### <span data-ttu-id="b6b78-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="b6b78-113">-Context</span></span>
<span data-ttu-id="b6b78-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b6b78-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="b6b78-115">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="b6b78-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b6b78-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b6b78-116">-Force</span></span>
<span data-ttu-id="b6b78-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b6b78-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6b78-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b6b78-118">-Name</span></span>
<span data-ttu-id="b6b78-119">Annak a táblának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="b6b78-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b78-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6b78-120">-PassThru</span></span>
<span data-ttu-id="b6b78-121">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="b6b78-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="b6b78-122">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="b6b78-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b6b78-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b6b78-123">-Confirm</span></span>
<span data-ttu-id="b6b78-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b6b78-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b78-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b78-125">-WhatIf</span></span>
<span data-ttu-id="b6b78-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b6b78-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b78-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b6b78-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b78-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b78-128">CommonParameters</span></span>
<span data-ttu-id="b6b78-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6b78-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b78-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b78-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b78-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6b78-131">INPUTS</span></span>

### <span data-ttu-id="b6b78-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6b78-132">IStorageContext</span></span>

<span data-ttu-id="b6b78-133">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b6b78-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="b6b78-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="b6b78-134">String</span></span>

<span data-ttu-id="b6b78-135">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="b6b78-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b6b78-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6b78-136">OUTPUTS</span></span>

### <span data-ttu-id="b6b78-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6b78-137">System.Boolean</span></span>

## <span data-ttu-id="b6b78-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6b78-138">NOTES</span></span>

## <span data-ttu-id="b6b78-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6b78-139">RELATED LINKS</span></span>

[<span data-ttu-id="b6b78-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="b6b78-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
