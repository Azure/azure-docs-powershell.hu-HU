---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350513"
---
# <span data-ttu-id="a5c2f-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="a5c2f-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="a5c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c2f-103">Egy 1277777-es táblát töröl.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a5c2f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5c2f-104">SYNTAX</span></span>

### <span data-ttu-id="a5c2f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5c2f-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c2f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5c2f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c2f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="a5c2f-108">A **Remove-AzCosmosDBCassandraTable törölni** fog egy Olyan Táblát, amelyről az AzCosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a5c2f-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5c2f-109">EXAMPLES</span></span>

### <span data-ttu-id="a5c2f-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5c2f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="a5c2f-111">A parancsmag egy bool (ha -PassThru sikeres) típusú objektumot ad vissza, amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="a5c2f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5c2f-112">PARAMETERS</span></span>

### <span data-ttu-id="a5c2f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5c2f-113">-AccountName</span></span>
<span data-ttu-id="a5c2f-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a5c2f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5c2f-115">-Confirm</span></span>
<span data-ttu-id="a5c2f-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c2f-117">-DefaultProfile</span></span>
<span data-ttu-id="a5c2f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c2f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5c2f-119">-InputObject</span></span>
<span data-ttu-id="a5c2f-120">2010.01.012.01.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c2f-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="a5c2f-121">-KeyspaceName</span></span>
<span data-ttu-id="a5c2f-122">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a5c2f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a5c2f-123">-Name</span></span>
<span data-ttu-id="a5c2f-124">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="a5c2f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c2f-125">-PassThru</span></span>
<span data-ttu-id="a5c2f-126">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a5c2f-127">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a5c2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5c2f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a5c2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c2f-130">-WhatIf</span></span>
<span data-ttu-id="a5c2f-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c2f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c2f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c2f-133">CommonParameters</span></span>
<span data-ttu-id="a5c2f-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5c2f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c2f-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5c2f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c2f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5c2f-136">INPUTS</span></span>

### <span data-ttu-id="a5c2f-137">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a5c2f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="a5c2f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5c2f-138">OUTPUTS</span></span>

### <span data-ttu-id="a5c2f-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="a5c2f-139">System.Void</span></span>

### <span data-ttu-id="a5c2f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c2f-140">System.Boolean</span></span>

## <span data-ttu-id="a5c2f-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5c2f-141">NOTES</span></span>

## <span data-ttu-id="a5c2f-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5c2f-142">RELATED LINKS</span></span>
