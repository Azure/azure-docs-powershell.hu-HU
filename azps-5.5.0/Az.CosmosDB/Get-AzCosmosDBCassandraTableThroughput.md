---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandratablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraTableThroughput.md
ms.openlocfilehash: 05304da0a027f66e145ca1c64942b0ffc9fd0936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166275"
---
# <span data-ttu-id="cdbd9-101">Get-AzCosmosDBCassandraTableThroughput</span><span class="sxs-lookup"><span data-stu-id="cdbd9-101">Get-AzCosmosDBCassandraTableThroughput</span></span>

## <span data-ttu-id="cdbd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdbd9-103">A Mintára táblázat átviteli sebességét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-103">Gets the throughput value of the Cassandra Table.</span></span>

## <span data-ttu-id="cdbd9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cdbd9-104">SYNTAX</span></span>

### <span data-ttu-id="cdbd9-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cdbd9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdbd9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdbd9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraTableThroughput -InputObject <PSCassandraKeyspaceGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdbd9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cdbd9-107">DESCRIPTION</span></span>
<span data-ttu-id="cdbd9-108">A **Get-AzCosmosDBCassandraTableThroughput** parancsmag az adott Keyspace-nek megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-108">The **Get-AzCosmosDBCassandraTableThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="cdbd9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cdbd9-109">EXAMPLES</span></span>

### <span data-ttu-id="cdbd9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cdbd9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraTableThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Keyspace {keyspaceName} -Name {tableName}
```

## <span data-ttu-id="cdbd9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdbd9-111">PARAMETERS</span></span>

### <span data-ttu-id="cdbd9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cdbd9-112">-AccountName</span></span>
<span data-ttu-id="cdbd9-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cdbd9-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdbd9-114">-Confirm</span></span>
<span data-ttu-id="cdbd9-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdbd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdbd9-116">-DefaultProfile</span></span>
<span data-ttu-id="cdbd9-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdbd9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdbd9-118">-InputObject</span></span>
<span data-ttu-id="cdbd9-119">A 2010-et a 2010-201</span><span class="sxs-lookup"><span data-stu-id="cdbd9-119">Cassandra Table object.</span></span>

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

### <span data-ttu-id="cdbd9-120">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="cdbd9-120">-KeyspaceName</span></span>
<span data-ttu-id="cdbd9-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-121">Database name.</span></span>

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

### <span data-ttu-id="cdbd9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cdbd9-122">-Name</span></span>
<span data-ttu-id="cdbd9-123">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-123">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="cdbd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdbd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdbd9-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-125">Name of resource group.</span></span>

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

### <span data-ttu-id="cdbd9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdbd9-126">-WhatIf</span></span>
<span data-ttu-id="cdbd9-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdbd9-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdbd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdbd9-129">CommonParameters</span></span>
<span data-ttu-id="cdbd9-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdbd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdbd9-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdbd9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdbd9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdbd9-132">INPUTS</span></span>

### <span data-ttu-id="cdbd9-133">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="cdbd9-133">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="cdbd9-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdbd9-134">OUTPUTS</span></span>

### <span data-ttu-id="cdbd9-135">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cdbd9-135">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cdbd9-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cdbd9-136">NOTES</span></span>

## <span data-ttu-id="cdbd9-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdbd9-137">RELATED LINKS</span></span>
