---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182554"
---
# <span data-ttu-id="d3337-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="d3337-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="d3337-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3337-102">SYNOPSIS</span></span>
<span data-ttu-id="d3337-103">Frissíti a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="d3337-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="d3337-104">Ügyféloldali javítás műveletet hajt végre a meglévő adatbázis felolvasásával.</span><span class="sxs-lookup"><span data-stu-id="d3337-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d3337-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3337-105">SYNTAX</span></span>

### <span data-ttu-id="d3337-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3337-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3337-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3337-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3337-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3337-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3337-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3337-109">DESCRIPTION</span></span>
<span data-ttu-id="d3337-110">Frissíti a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="d3337-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="d3337-111">Ügyféloldali javítás műveletet hajt végre a meglévő adatbázis felolvasásával.</span><span class="sxs-lookup"><span data-stu-id="d3337-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="d3337-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d3337-112">EXAMPLES</span></span>

### <span data-ttu-id="d3337-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3337-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="d3337-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3337-114">PARAMETERS</span></span>

### <span data-ttu-id="d3337-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d3337-115">-AccountName</span></span>
<span data-ttu-id="d3337-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d3337-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d3337-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d3337-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d3337-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d3337-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3337-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d3337-119">-Confirm</span></span>
<span data-ttu-id="d3337-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d3337-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3337-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3337-121">-DefaultProfile</span></span>
<span data-ttu-id="d3337-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3337-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3337-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3337-123">-InputObject</span></span>
<span data-ttu-id="d3337-124">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="d3337-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="d3337-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3337-125">-Name</span></span>
<span data-ttu-id="d3337-126">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d3337-126">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3337-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d3337-127">-ParentObject</span></span>
<span data-ttu-id="d3337-128">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d3337-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3337-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3337-129">-ResourceGroupName</span></span>
<span data-ttu-id="d3337-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d3337-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d3337-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="d3337-131">-Throughput</span></span>
<span data-ttu-id="d3337-132">Az Gremlin-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="d3337-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="d3337-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="d3337-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3337-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3337-134">-WhatIf</span></span>
<span data-ttu-id="d3337-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d3337-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3337-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d3337-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3337-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3337-137">CommonParameters</span></span>
<span data-ttu-id="d3337-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3337-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3337-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d3337-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3337-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3337-140">INPUTS</span></span>

### <span data-ttu-id="d3337-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d3337-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="d3337-142">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d3337-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="d3337-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3337-143">OUTPUTS</span></span>

### <span data-ttu-id="d3337-144">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d3337-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="d3337-145">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d3337-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d3337-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3337-146">NOTES</span></span>

## <span data-ttu-id="d3337-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3337-147">RELATED LINKS</span></span>
