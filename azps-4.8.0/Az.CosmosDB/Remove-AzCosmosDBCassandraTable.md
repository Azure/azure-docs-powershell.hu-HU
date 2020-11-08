---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185082"
---
# <span data-ttu-id="875c2-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="875c2-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="875c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="875c2-102">SYNOPSIS</span></span>
<span data-ttu-id="875c2-103">CosmosDB Cassandra-táblázat törlése</span><span class="sxs-lookup"><span data-stu-id="875c2-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="875c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="875c2-104">SYNTAX</span></span>

### <span data-ttu-id="875c2-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="875c2-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="875c2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="875c2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="875c2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="875c2-107">DESCRIPTION</span></span>
<span data-ttu-id="875c2-108">A **Remove-AzCosmosDBCassandraTable** CosmosDB: Cassandra-táblázat törlése</span><span class="sxs-lookup"><span data-stu-id="875c2-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="875c2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="875c2-109">EXAMPLES</span></span>

### <span data-ttu-id="875c2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="875c2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="875c2-111">A parancsmag olyan objektumot ad eredményül, amely a bool (amikor a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="875c2-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="875c2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="875c2-112">PARAMETERS</span></span>

### <span data-ttu-id="875c2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="875c2-113">-AccountName</span></span>
<span data-ttu-id="875c2-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="875c2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="875c2-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="875c2-115">-Confirm</span></span>
<span data-ttu-id="875c2-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="875c2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875c2-117">-DefaultProfile</span></span>
<span data-ttu-id="875c2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="875c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="875c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="875c2-119">-InputObject</span></span>
<span data-ttu-id="875c2-120">Cassandra Table objektum.</span><span class="sxs-lookup"><span data-stu-id="875c2-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="875c2-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="875c2-121">-KeyspaceName</span></span>
<span data-ttu-id="875c2-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="875c2-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="875c2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="875c2-123">-Name</span></span>
<span data-ttu-id="875c2-124">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="875c2-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="875c2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="875c2-125">-PassThru</span></span>
<span data-ttu-id="875c2-126">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="875c2-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="875c2-127">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="875c2-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="875c2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875c2-128">-ResourceGroupName</span></span>
<span data-ttu-id="875c2-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="875c2-129">Name of resource group.</span></span>

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

### <span data-ttu-id="875c2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875c2-130">-WhatIf</span></span>
<span data-ttu-id="875c2-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="875c2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875c2-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="875c2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875c2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875c2-133">CommonParameters</span></span>
<span data-ttu-id="875c2-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="875c2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875c2-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="875c2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875c2-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="875c2-136">INPUTS</span></span>

### <span data-ttu-id="875c2-137">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="875c2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="875c2-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="875c2-138">OUTPUTS</span></span>

### <span data-ttu-id="875c2-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="875c2-139">System.Void</span></span>

### <span data-ttu-id="875c2-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="875c2-140">System.Boolean</span></span>

## <span data-ttu-id="875c2-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="875c2-141">NOTES</span></span>

## <span data-ttu-id="875c2-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="875c2-142">RELATED LINKS</span></span>
