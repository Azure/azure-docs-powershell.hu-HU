---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299162"
---
# <span data-ttu-id="42058-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="42058-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="42058-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42058-102">SYNOPSIS</span></span>
<span data-ttu-id="42058-103">CosmosDB Gremlin-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="42058-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="42058-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42058-104">SYNTAX</span></span>

### <span data-ttu-id="42058-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42058-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42058-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42058-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42058-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="42058-107">DESCRIPTION</span></span>
<span data-ttu-id="42058-108">A **Remove-AzCosmosDBGremlinDatabase** parancsmag törli a CosmosDB Gremlin adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="42058-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="42058-109">Példák</span><span class="sxs-lookup"><span data-stu-id="42058-109">EXAMPLES</span></span>

### <span data-ttu-id="42058-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42058-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="42058-111">A parancsmag olyan objektumot ad eredményül, amely a bool (amikor a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="42058-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="42058-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42058-112">PARAMETERS</span></span>

### <span data-ttu-id="42058-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42058-113">-AccountName</span></span>
<span data-ttu-id="42058-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="42058-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42058-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42058-115">-Confirm</span></span>
<span data-ttu-id="42058-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42058-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42058-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42058-117">-DefaultProfile</span></span>
<span data-ttu-id="42058-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42058-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42058-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42058-119">-InputObject</span></span>
<span data-ttu-id="42058-120">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="42058-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="42058-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42058-121">-Name</span></span>
<span data-ttu-id="42058-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="42058-122">Database name.</span></span>

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

### <span data-ttu-id="42058-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42058-123">-PassThru</span></span>
<span data-ttu-id="42058-124">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="42058-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="42058-125">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="42058-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="42058-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42058-126">-ResourceGroupName</span></span>
<span data-ttu-id="42058-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="42058-127">Name of resource group.</span></span>

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

### <span data-ttu-id="42058-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42058-128">-WhatIf</span></span>
<span data-ttu-id="42058-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42058-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42058-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42058-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42058-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42058-131">CommonParameters</span></span>
<span data-ttu-id="42058-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42058-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42058-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="42058-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42058-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42058-134">INPUTS</span></span>

### <span data-ttu-id="42058-135">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="42058-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="42058-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42058-136">OUTPUTS</span></span>

### <span data-ttu-id="42058-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="42058-137">System.Void</span></span>

### <span data-ttu-id="42058-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42058-138">System.Boolean</span></span>

## <span data-ttu-id="42058-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42058-139">NOTES</span></span>

## <span data-ttu-id="42058-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42058-140">RELATED LINKS</span></span>
