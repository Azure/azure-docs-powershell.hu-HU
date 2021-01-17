---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350489"
---
# <span data-ttu-id="d432f-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="d432f-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="d432f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d432f-102">SYNOPSIS</span></span>
<span data-ttu-id="d432f-103">A 2010-es Éva diagram törlése.</span><span class="sxs-lookup"><span data-stu-id="d432f-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d432f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d432f-104">SYNTAX</span></span>

### <span data-ttu-id="d432f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d432f-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d432f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d432f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d432f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d432f-107">DESCRIPTION</span></span>
<span data-ttu-id="d432f-108">A **Remove-AzCosmosDBGremlinGraph** parancsmag törli a Fogdb Gremlin Graph rekordot.</span><span class="sxs-lookup"><span data-stu-id="d432f-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="d432f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d432f-109">EXAMPLES</span></span>

### <span data-ttu-id="d432f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d432f-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="d432f-111">A parancsmag egy bool (ha -PassThru sikeres) típusú objektumot ad vissza, amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="d432f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="d432f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d432f-112">PARAMETERS</span></span>

### <span data-ttu-id="d432f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d432f-113">-AccountName</span></span>
<span data-ttu-id="d432f-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d432f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d432f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d432f-115">-Confirm</span></span>
<span data-ttu-id="d432f-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d432f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d432f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d432f-117">-DatabaseName</span></span>
<span data-ttu-id="d432f-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d432f-118">Database name.</span></span>

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

### <span data-ttu-id="d432f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d432f-119">-DefaultProfile</span></span>
<span data-ttu-id="d432f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d432f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d432f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d432f-121">-InputObject</span></span>
<span data-ttu-id="d432f-122">Gremlin Graph-objektum.</span><span class="sxs-lookup"><span data-stu-id="d432f-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d432f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d432f-123">-Name</span></span>
<span data-ttu-id="d432f-124">Gremlin Graph-név.</span><span class="sxs-lookup"><span data-stu-id="d432f-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="d432f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d432f-125">-PassThru</span></span>
<span data-ttu-id="d432f-126">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="d432f-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d432f-127">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="d432f-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d432f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d432f-128">-ResourceGroupName</span></span>
<span data-ttu-id="d432f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d432f-129">Name of resource group.</span></span>

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

### <span data-ttu-id="d432f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d432f-130">-WhatIf</span></span>
<span data-ttu-id="d432f-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d432f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d432f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d432f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d432f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d432f-133">CommonParameters</span></span>
<span data-ttu-id="d432f-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d432f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d432f-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d432f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d432f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d432f-136">INPUTS</span></span>

### <span data-ttu-id="d432f-137">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="d432f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="d432f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d432f-138">OUTPUTS</span></span>

### <span data-ttu-id="d432f-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="d432f-139">System.Void</span></span>

### <span data-ttu-id="d432f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d432f-140">System.Boolean</span></span>

## <span data-ttu-id="d432f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d432f-141">NOTES</span></span>

## <span data-ttu-id="d432f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d432f-142">RELATED LINKS</span></span>
