---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 0f09c391f63d4d8e1eb0949acb54770e242744a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923233"
---
# <span data-ttu-id="a418e-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a418e-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="a418e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a418e-102">SYNOPSIS</span></span>
<span data-ttu-id="a418e-103">Eltávolít egy tárolótáblát.</span><span class="sxs-lookup"><span data-stu-id="a418e-103">Removes a storage table.</span></span>

## <span data-ttu-id="a418e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a418e-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a418e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a418e-105">DESCRIPTION</span></span>
<span data-ttu-id="a418e-106">A **Remove-AzStorageTable** parancsmag eltávolít egy vagy több tártáblát egy Azure-beli tárfiókból.</span><span class="sxs-lookup"><span data-stu-id="a418e-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="a418e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a418e-107">EXAMPLES</span></span>

### <span data-ttu-id="a418e-108">1. példa: Táblázat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a418e-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="a418e-109">Ez a parancs eltávolít egy táblát.</span><span class="sxs-lookup"><span data-stu-id="a418e-109">This command removes a table.</span></span>

### <span data-ttu-id="a418e-110">2. példa: Több tábla eltávolítása</span><span class="sxs-lookup"><span data-stu-id="a418e-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="a418e-111">Ez a példa egy helyettesítő karaktert használ a *Name* paraméterrel a mintatáblának megfelelő összes táblázat be szerezze, majd átadja az eredményt a folyamatnak a táblák eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="a418e-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="a418e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a418e-112">PARAMETERS</span></span>

### <span data-ttu-id="a418e-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a418e-113">-Context</span></span>
<span data-ttu-id="a418e-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a418e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a418e-115">A parancsmagot a New-AzStorageContext hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="a418e-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a418e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a418e-116">-DefaultProfile</span></span>
<span data-ttu-id="a418e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a418e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a418e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a418e-118">-Force</span></span>
<span data-ttu-id="a418e-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a418e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a418e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a418e-120">-Name</span></span>
<span data-ttu-id="a418e-121">Az eltávolítható tábla neve.</span><span class="sxs-lookup"><span data-stu-id="a418e-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="a418e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a418e-122">-PassThru</span></span>
<span data-ttu-id="a418e-123">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="a418e-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a418e-124">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="a418e-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a418e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a418e-125">-Confirm</span></span>
<span data-ttu-id="a418e-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a418e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a418e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a418e-127">-WhatIf</span></span>
<span data-ttu-id="a418e-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a418e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a418e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a418e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a418e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a418e-130">CommonParameters</span></span>
<span data-ttu-id="a418e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a418e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a418e-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a418e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a418e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a418e-133">INPUTS</span></span>

### <span data-ttu-id="a418e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a418e-134">System.String</span></span>

### <span data-ttu-id="a418e-135">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a418e-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a418e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a418e-136">OUTPUTS</span></span>

### <span data-ttu-id="a418e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a418e-137">System.Boolean</span></span>

## <span data-ttu-id="a418e-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a418e-138">NOTES</span></span>

## <span data-ttu-id="a418e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a418e-139">RELATED LINKS</span></span>

[<span data-ttu-id="a418e-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a418e-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
