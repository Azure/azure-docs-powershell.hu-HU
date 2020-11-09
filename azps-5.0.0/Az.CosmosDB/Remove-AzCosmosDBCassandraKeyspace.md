---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299174"
---
# <span data-ttu-id="93bc4-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="93bc4-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="93bc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="93bc4-103">Törli a CosmosDB Cassandra szóköz billentyűt.</span><span class="sxs-lookup"><span data-stu-id="93bc4-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="93bc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93bc4-104">SYNTAX</span></span>

### <span data-ttu-id="93bc4-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bc4-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93bc4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bc4-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93bc4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="93bc4-107">DESCRIPTION</span></span>
<span data-ttu-id="93bc4-108">A **Remove-AzCosmosDBCassandraKeyspace** parancsmag törli a meglévő CosmosDB a Cassandra szóköz billentyűkombinációval.</span><span class="sxs-lookup"><span data-stu-id="93bc4-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="93bc4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="93bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="93bc4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="93bc4-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="93bc4-111">A parancsmag olyan objektumot ad eredményül, amely bool (ha a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="93bc4-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="93bc4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93bc4-112">PARAMETERS</span></span>

### <span data-ttu-id="93bc4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="93bc4-113">-AccountName</span></span>
<span data-ttu-id="93bc4-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="93bc4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="93bc4-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93bc4-115">-Confirm</span></span>
<span data-ttu-id="93bc4-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93bc4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93bc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bc4-117">-DefaultProfile</span></span>
<span data-ttu-id="93bc4-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93bc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93bc4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93bc4-119">-InputObject</span></span>
<span data-ttu-id="93bc4-120">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="93bc4-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93bc4-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93bc4-121">-Name</span></span>
<span data-ttu-id="93bc4-122">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="93bc4-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="93bc4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93bc4-123">-PassThru</span></span>
<span data-ttu-id="93bc4-124">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="93bc4-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="93bc4-125">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="93bc4-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="93bc4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bc4-126">-ResourceGroupName</span></span>
<span data-ttu-id="93bc4-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93bc4-127">Name of resource group.</span></span>

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

### <span data-ttu-id="93bc4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bc4-128">-WhatIf</span></span>
<span data-ttu-id="93bc4-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93bc4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93bc4-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93bc4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93bc4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bc4-131">CommonParameters</span></span>
<span data-ttu-id="93bc4-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93bc4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bc4-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="93bc4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bc4-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bc4-134">INPUTS</span></span>

### <span data-ttu-id="93bc4-135">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="93bc4-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="93bc4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93bc4-136">OUTPUTS</span></span>

### <span data-ttu-id="93bc4-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="93bc4-137">System.Void</span></span>

### <span data-ttu-id="93bc4-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93bc4-138">System.Boolean</span></span>

## <span data-ttu-id="93bc4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93bc4-139">NOTES</span></span>

## <span data-ttu-id="93bc4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93bc4-140">RELATED LINKS</span></span>
