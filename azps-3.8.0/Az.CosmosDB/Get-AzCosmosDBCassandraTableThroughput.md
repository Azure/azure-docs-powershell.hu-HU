---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014126"
---
# <span data-ttu-id="5a70c-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="5a70c-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="5a70c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5a70c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a70c-103">Megkapja a Cassandra (Cassandra) táblázat átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="5a70c-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="5a70c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5a70c-104">SYNTAX</span></span>

### <span data-ttu-id="5a70c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a70c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a70c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a70c-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a70c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5a70c-107">DESCRIPTION</span></span>
<span data-ttu-id="5a70c-108">A **Get-AzCosmosDBCassandraTableThroughput** parancsmag az adott térköznek megfelelő átviteli objektumot kapja.</span><span class="sxs-lookup"><span data-stu-id="5a70c-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="5a70c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5a70c-109">EXAMPLES</span></span>

### <span data-ttu-id="5a70c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5a70c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="5a70c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5a70c-111">PARAMETERS</span></span>

### <span data-ttu-id="5a70c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a70c-112">-AccountName</span></span>
<span data-ttu-id="5a70c-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5a70c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a70c-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5a70c-114">-Confirm</span></span>
<span data-ttu-id="5a70c-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5a70c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a70c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a70c-116">-DefaultProfile</span></span>
<span data-ttu-id="5a70c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a70c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a70c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a70c-118">-InputObject</span></span>
<span data-ttu-id="5a70c-119">Cassandra Table objektum.</span><span class="sxs-lookup"><span data-stu-id="5a70c-119">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a70c-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="5a70c-120">-KeyspaceName</span></span>
<span data-ttu-id="5a70c-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5a70c-121">Database name.</span></span>

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

### <span data-ttu-id="5a70c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5a70c-122">-Name</span></span>
<span data-ttu-id="5a70c-123">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="5a70c-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="5a70c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a70c-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a70c-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a70c-125">Name of resource group.</span></span>

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

### <span data-ttu-id="5a70c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a70c-126">-WhatIf</span></span>
<span data-ttu-id="5a70c-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5a70c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a70c-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5a70c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a70c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a70c-129">CommonParameters</span></span>
<span data-ttu-id="5a70c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5a70c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a70c-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5a70c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a70c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a70c-132">INPUTS</span></span>

### <span data-ttu-id="5a70c-133">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5a70c-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="5a70c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a70c-134">OUTPUTS</span></span>

### <span data-ttu-id="5a70c-135">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5a70c-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5a70c-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5a70c-136">NOTES</span></span>

## <span data-ttu-id="5a70c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a70c-137">RELATED LINKS</span></span>
