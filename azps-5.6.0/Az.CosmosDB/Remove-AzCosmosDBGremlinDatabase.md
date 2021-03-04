---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 2a09582c57cdb06dea955dcbd1c4728b822d229c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928274"
---
# <span data-ttu-id="f8469-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="f8469-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="f8469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8469-102">SYNOPSIS</span></span>
<span data-ttu-id="f8469-103">A 2010-es adatbázis törlése.</span><span class="sxs-lookup"><span data-stu-id="f8469-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f8469-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8469-104">SYNTAX</span></span>

### <span data-ttu-id="f8469-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8469-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8469-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8469-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8469-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8469-107">DESCRIPTION</span></span>
<span data-ttu-id="f8469-108">A **Remove-AzCosmosDBGremlinDatabase** parancsmag törli a Következő adatbázist:</span><span class="sxs-lookup"><span data-stu-id="f8469-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="f8469-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8469-109">EXAMPLES</span></span>

### <span data-ttu-id="f8469-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8469-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="f8469-111">A parancsmag egy bool (ha -PassThru sikeres) típusú objektumot ad vissza, amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f8469-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="f8469-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8469-112">PARAMETERS</span></span>

### <span data-ttu-id="f8469-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f8469-113">-AccountName</span></span>
<span data-ttu-id="f8469-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="f8469-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8469-115">-Confirm</span></span>
<span data-ttu-id="f8469-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8469-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8469-117">-DefaultProfile</span></span>
<span data-ttu-id="f8469-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8469-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8469-119">-InputObject</span></span>
<span data-ttu-id="f8469-120">Gremlin-adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="f8469-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8469-121">-Name</span></span>
<span data-ttu-id="f8469-122">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f8469-122">Database name.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8469-123">-PassThru</span></span>
<span data-ttu-id="f8469-124">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="f8469-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f8469-125">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="f8469-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f8469-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8469-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8469-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8469-127">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8469-128">-WhatIf</span></span>
<span data-ttu-id="f8469-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8469-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8469-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8469-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8469-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8469-131">CommonParameters</span></span>
<span data-ttu-id="f8469-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8469-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8469-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8469-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8469-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8469-134">INPUTS</span></span>

### <span data-ttu-id="f8469-135">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f8469-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="f8469-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8469-136">OUTPUTS</span></span>

### <span data-ttu-id="f8469-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="f8469-137">System.Void</span></span>

### <span data-ttu-id="f8469-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8469-138">System.Boolean</span></span>

## <span data-ttu-id="f8469-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8469-139">NOTES</span></span>

## <span data-ttu-id="f8469-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8469-140">RELATED LINKS</span></span>
