---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850489"
---
# <span data-ttu-id="e5aa4-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e5aa4-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="e5aa4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="e5aa4-103">Tároló tábla eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5aa4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5aa4-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5aa4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="e5aa4-106">A **Remove-AzureStorageTable** parancsmag egy vagy több tároló táblát eltávolít egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="e5aa4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5aa4-107">EXAMPLES</span></span>

### <span data-ttu-id="e5aa4-108">1. példa: táblázat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e5aa4-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="e5aa4-109">A parancs eltávolítja a táblázatot.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-109">This command removes a table.</span></span>

### <span data-ttu-id="e5aa4-110">2. példa: több tábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e5aa4-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="e5aa4-111">Ez a példa egy helyettesítő karaktert használ a *Name* paraméterrel a minta táblázatnak megfelelő összes táblázat beolvasásához, majd átadja az eredményt a csővezetéken a táblák eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="e5aa4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5aa4-112">PARAMETERS</span></span>

### <span data-ttu-id="e5aa4-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e5aa4-113">-Context</span></span>
<span data-ttu-id="e5aa4-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e5aa4-115">A New-AzureStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e5aa4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5aa4-116">-DefaultProfile</span></span>
<span data-ttu-id="e5aa4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5aa4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e5aa4-118">-Force</span></span>
<span data-ttu-id="e5aa4-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e5aa4-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5aa4-120">-Name</span></span>
<span data-ttu-id="e5aa4-121">Annak a táblának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5aa4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5aa4-122">-PassThru</span></span>
<span data-ttu-id="e5aa4-123">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e5aa4-124">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e5aa4-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e5aa4-125">-Confirm</span></span>
<span data-ttu-id="e5aa4-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5aa4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5aa4-127">-WhatIf</span></span>
<span data-ttu-id="e5aa4-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5aa4-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e5aa4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5aa4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5aa4-130">CommonParameters</span></span>
<span data-ttu-id="e5aa4-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5aa4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5aa4-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5aa4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5aa4-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5aa4-133">INPUTS</span></span>

### <span data-ttu-id="e5aa4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5aa4-134">System.String</span></span>

### <span data-ttu-id="e5aa4-135">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e5aa4-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e5aa4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5aa4-136">OUTPUTS</span></span>

### <span data-ttu-id="e5aa4-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5aa4-137">System.Boolean</span></span>

## <span data-ttu-id="e5aa4-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5aa4-138">NOTES</span></span>

## <span data-ttu-id="e5aa4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5aa4-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5aa4-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e5aa4-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
