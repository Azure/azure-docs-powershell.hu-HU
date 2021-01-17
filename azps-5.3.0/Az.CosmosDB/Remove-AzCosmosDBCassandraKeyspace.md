---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477401"
---
# <span data-ttu-id="f720e-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="f720e-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="f720e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f720e-102">SYNOPSIS</span></span>
<span data-ttu-id="f720e-103">Egy 127777-es kulcsteret töröl.</span><span class="sxs-lookup"><span data-stu-id="f720e-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f720e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f720e-104">SYNTAX</span></span>

### <span data-ttu-id="f720e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f720e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f720e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f720e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f720e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f720e-107">DESCRIPTION</span></span>
<span data-ttu-id="f720e-108">A **Remove-AzCosmosDBCassandraKeyspace** parancsmag törli a már meglévő, A1177772255000000000022-et.</span><span class="sxs-lookup"><span data-stu-id="f720e-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="f720e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f720e-109">EXAMPLES</span></span>

### <span data-ttu-id="f720e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f720e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="f720e-111">A parancsmag egy bool típusú objektumot (a -PassThru-sikeresség esetén) ad vissza, amely akkor igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f720e-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="f720e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f720e-112">PARAMETERS</span></span>

### <span data-ttu-id="f720e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f720e-113">-AccountName</span></span>
<span data-ttu-id="f720e-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="f720e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f720e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f720e-115">-Confirm</span></span>
<span data-ttu-id="f720e-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f720e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f720e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f720e-117">-DefaultProfile</span></span>
<span data-ttu-id="f720e-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f720e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f720e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f720e-119">-InputObject</span></span>
<span data-ttu-id="f720e-120">A 2016-2013-2013-201</span><span class="sxs-lookup"><span data-stu-id="f720e-120">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="f720e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f720e-121">-Name</span></span>
<span data-ttu-id="f720e-122">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="f720e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f720e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f720e-123">-PassThru</span></span>
<span data-ttu-id="f720e-124">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="f720e-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f720e-125">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="f720e-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f720e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f720e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f720e-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f720e-127">Name of resource group.</span></span>

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

### <span data-ttu-id="f720e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f720e-128">-WhatIf</span></span>
<span data-ttu-id="f720e-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f720e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f720e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f720e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f720e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f720e-131">CommonParameters</span></span>
<span data-ttu-id="f720e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f720e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f720e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f720e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f720e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f720e-134">INPUTS</span></span>

### <span data-ttu-id="f720e-135">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="f720e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="f720e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f720e-136">OUTPUTS</span></span>

### <span data-ttu-id="f720e-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="f720e-137">System.Void</span></span>

### <span data-ttu-id="f720e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f720e-138">System.Boolean</span></span>

## <span data-ttu-id="f720e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f720e-139">NOTES</span></span>

## <span data-ttu-id="f720e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f720e-140">RELATED LINKS</span></span>
