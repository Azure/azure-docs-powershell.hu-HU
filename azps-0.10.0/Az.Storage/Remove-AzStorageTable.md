---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 5d5c5092580c8e86966bb15aaf538702c42483a6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842905"
---
# <span data-ttu-id="ca378-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="ca378-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="ca378-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca378-102">SYNOPSIS</span></span>
<span data-ttu-id="ca378-103">Tároló tábla eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ca378-103">Removes a storage table.</span></span>

## <span data-ttu-id="ca378-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca378-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca378-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca378-105">DESCRIPTION</span></span>
<span data-ttu-id="ca378-106">A **Remove-AzStorageTable** parancsmag egy vagy több tároló táblát eltávolít egy tárterület-fiókból az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ca378-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="ca378-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca378-107">EXAMPLES</span></span>

### <span data-ttu-id="ca378-108">1. példa: táblázat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ca378-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="ca378-109">A parancs eltávolítja a táblázatot.</span><span class="sxs-lookup"><span data-stu-id="ca378-109">This command removes a table.</span></span>

### <span data-ttu-id="ca378-110">2. példa: több tábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ca378-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="ca378-111">Ez a példa egy helyettesítő karaktert használ a *Name* paraméterrel a minta táblázatnak megfelelő összes táblázat beolvasásához, majd átadja az eredményt a csővezetéken a táblák eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="ca378-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="ca378-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca378-112">PARAMETERS</span></span>

### <span data-ttu-id="ca378-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ca378-113">-Context</span></span>
<span data-ttu-id="ca378-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca378-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ca378-115">A New-AzStorageContext parancsmag használatával is létrehozhatja azt.</span><span class="sxs-lookup"><span data-stu-id="ca378-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ca378-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca378-116">-DefaultProfile</span></span>
<span data-ttu-id="ca378-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca378-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca378-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ca378-118">-Force</span></span>
<span data-ttu-id="ca378-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ca378-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca378-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca378-120">-Name</span></span>
<span data-ttu-id="ca378-121">Annak a táblának a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="ca378-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="ca378-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca378-122">-PassThru</span></span>
<span data-ttu-id="ca378-123">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="ca378-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ca378-124">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="ca378-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ca378-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca378-125">-Confirm</span></span>
<span data-ttu-id="ca378-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca378-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca378-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca378-127">-WhatIf</span></span>
<span data-ttu-id="ca378-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca378-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca378-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca378-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca378-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca378-130">CommonParameters</span></span>
<span data-ttu-id="ca378-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca378-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca378-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca378-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca378-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca378-133">INPUTS</span></span>

### <span data-ttu-id="ca378-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ca378-134">System.String</span></span>

### <span data-ttu-id="ca378-135">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca378-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca378-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca378-136">OUTPUTS</span></span>

### <span data-ttu-id="ca378-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca378-137">System.Boolean</span></span>

## <span data-ttu-id="ca378-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca378-138">NOTES</span></span>

## <span data-ttu-id="ca378-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca378-139">RELATED LINKS</span></span>

[<span data-ttu-id="ca378-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="ca378-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
