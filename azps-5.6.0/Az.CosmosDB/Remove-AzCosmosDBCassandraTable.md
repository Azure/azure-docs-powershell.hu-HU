---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: d860e9f5992cb1bd8df9a3f7f14e51565412284b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930569"
---
# <span data-ttu-id="65547-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="65547-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="65547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65547-102">SYNOPSIS</span></span>
<span data-ttu-id="65547-103">Egy 127777777223336777444-táblázatot töröl.</span><span class="sxs-lookup"><span data-stu-id="65547-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="65547-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="65547-104">SYNTAX</span></span>

### <span data-ttu-id="65547-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="65547-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65547-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65547-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65547-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="65547-107">DESCRIPTION</span></span>
<span data-ttu-id="65547-108">A **Remove-AzCosmosDBCassandraTable törölni** fog egy Olyan Táblát, amelyről az AzCosmosDB.</span><span class="sxs-lookup"><span data-stu-id="65547-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="65547-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="65547-109">EXAMPLES</span></span>

### <span data-ttu-id="65547-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="65547-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="65547-111">A parancsmag egy bool (ha -PassThru sikeres) típusú objektumot ad vissza, amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="65547-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="65547-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65547-112">PARAMETERS</span></span>

### <span data-ttu-id="65547-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="65547-113">-AccountName</span></span>
<span data-ttu-id="65547-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="65547-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="65547-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65547-115">-Confirm</span></span>
<span data-ttu-id="65547-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="65547-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65547-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65547-117">-DefaultProfile</span></span>
<span data-ttu-id="65547-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65547-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65547-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65547-119">-InputObject</span></span>
<span data-ttu-id="65547-120">2010.01.012.01.</span><span class="sxs-lookup"><span data-stu-id="65547-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="65547-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="65547-121">-KeyspaceName</span></span>
<span data-ttu-id="65547-122">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="65547-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="65547-123">-Name</span><span class="sxs-lookup"><span data-stu-id="65547-123">-Name</span></span>
<span data-ttu-id="65547-124">Kéttáblás tábla neve.</span><span class="sxs-lookup"><span data-stu-id="65547-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="65547-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65547-125">-PassThru</span></span>
<span data-ttu-id="65547-126">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="65547-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="65547-127">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="65547-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="65547-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65547-128">-ResourceGroupName</span></span>
<span data-ttu-id="65547-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="65547-129">Name of resource group.</span></span>

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

### <span data-ttu-id="65547-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65547-130">-WhatIf</span></span>
<span data-ttu-id="65547-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="65547-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65547-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65547-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65547-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65547-133">CommonParameters</span></span>
<span data-ttu-id="65547-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65547-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65547-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65547-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65547-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65547-136">INPUTS</span></span>

### <span data-ttu-id="65547-137">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="65547-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="65547-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65547-138">OUTPUTS</span></span>

### <span data-ttu-id="65547-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="65547-139">System.Void</span></span>

### <span data-ttu-id="65547-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="65547-140">System.Boolean</span></span>

## <span data-ttu-id="65547-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="65547-141">NOTES</span></span>

## <span data-ttu-id="65547-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65547-142">RELATED LINKS</span></span>
