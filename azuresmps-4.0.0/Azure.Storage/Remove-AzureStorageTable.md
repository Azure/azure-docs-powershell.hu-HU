---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671712"
---
# <span data-ttu-id="77d7b-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="77d7b-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="77d7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="77d7b-103">Tároló tábla eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="77d7b-103">Removes a storage table.</span></span>

## <span data-ttu-id="77d7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77d7b-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d7b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="77d7b-105">DESCRIPTION</span></span>
<span data-ttu-id="77d7b-106">A **Remove-AzureStorageTable** parancsmag egy vagy több tároló táblát eltávolít egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="77d7b-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="77d7b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="77d7b-107">EXAMPLES</span></span>

### <span data-ttu-id="77d7b-108">1. példa: táblázat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="77d7b-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="77d7b-109">A parancs eltávolítja a táblázatot.</span><span class="sxs-lookup"><span data-stu-id="77d7b-109">This command removes a table.</span></span>

### <span data-ttu-id="77d7b-110">2. példa: több tábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="77d7b-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="77d7b-111">Ez a példa egy helyettesítő karaktert használ a *Name* paraméterrel a minta táblázatnak megfelelő összes táblázat beolvasásához, majd átadja az eredményt a csővezetéken a táblák eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="77d7b-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="77d7b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77d7b-112">PARAMETERS</span></span>

### <span data-ttu-id="77d7b-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="77d7b-113">-Context</span></span>
<span data-ttu-id="77d7b-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="77d7b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="77d7b-115">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="77d7b-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="77d7b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="77d7b-116">-Force</span></span>
<span data-ttu-id="77d7b-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="77d7b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77d7b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77d7b-118">-Name</span></span>
<span data-ttu-id="77d7b-119">Annak a táblának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="77d7b-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="77d7b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77d7b-120">-PassThru</span></span>
<span data-ttu-id="77d7b-121">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="77d7b-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="77d7b-122">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="77d7b-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="77d7b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="77d7b-123">-Confirm</span></span>
<span data-ttu-id="77d7b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="77d7b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d7b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d7b-125">-WhatIf</span></span>
<span data-ttu-id="77d7b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="77d7b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77d7b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77d7b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d7b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d7b-128">CommonParameters</span></span>
<span data-ttu-id="77d7b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77d7b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d7b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d7b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d7b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77d7b-131">INPUTS</span></span>

## <span data-ttu-id="77d7b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77d7b-132">OUTPUTS</span></span>

## <span data-ttu-id="77d7b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77d7b-133">NOTES</span></span>

## <span data-ttu-id="77d7b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77d7b-134">RELATED LINKS</span></span>

[<span data-ttu-id="77d7b-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="77d7b-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
