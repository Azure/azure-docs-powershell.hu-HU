---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: c52d76889de743a624ce60241a9495ef09ce2c4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299066"
---
# <span data-ttu-id="427e9-101">Update-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="427e9-101">Update-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="427e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="427e9-102">SYNOPSIS</span></span>
<span data-ttu-id="427e9-103">Frissíti a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="427e9-103">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="427e9-104">Ügyféloldali javítás műveletet hajt végre a meglévő adatbázis felolvasásával.</span><span class="sxs-lookup"><span data-stu-id="427e9-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="427e9-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="427e9-105">SYNTAX</span></span>

### <span data-ttu-id="427e9-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="427e9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="427e9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="427e9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="427e9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="427e9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSGremlinDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="427e9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="427e9-109">DESCRIPTION</span></span>
<span data-ttu-id="427e9-110">Frissíti a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="427e9-110">Updates the CosmosDB Gremlin Database.</span></span> <span data-ttu-id="427e9-111">Ügyféloldali javítás műveletet hajt végre a meglévő adatbázis felolvasásával.</span><span class="sxs-lookup"><span data-stu-id="427e9-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="427e9-112">Példák</span><span class="sxs-lookup"><span data-stu-id="427e9-112">EXAMPLES</span></span>

### <span data-ttu-id="427e9-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="427e9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -throughput updatedThroughputValueAsInteger

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="427e9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="427e9-114">PARAMETERS</span></span>

### <span data-ttu-id="427e9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="427e9-115">-AccountName</span></span>
<span data-ttu-id="427e9-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="427e9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="427e9-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="427e9-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="427e9-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="427e9-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="427e9-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="427e9-119">-Confirm</span></span>
<span data-ttu-id="427e9-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="427e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="427e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="427e9-121">-DefaultProfile</span></span>
<span data-ttu-id="427e9-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="427e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="427e9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="427e9-123">-InputObject</span></span>
<span data-ttu-id="427e9-124">Gremlin adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="427e9-124">Gremlin Database object.</span></span>

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

### <span data-ttu-id="427e9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="427e9-125">-Name</span></span>
<span data-ttu-id="427e9-126">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="427e9-126">Database name.</span></span>

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

### <span data-ttu-id="427e9-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="427e9-127">-ParentObject</span></span>
<span data-ttu-id="427e9-128">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="427e9-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="427e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="427e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="427e9-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="427e9-130">Name of resource group.</span></span>

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

### <span data-ttu-id="427e9-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="427e9-131">-Throughput</span></span>
<span data-ttu-id="427e9-132">Az Gremlin-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="427e9-132">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="427e9-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="427e9-133">Default value is 400.</span></span>

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

### <span data-ttu-id="427e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="427e9-134">-WhatIf</span></span>
<span data-ttu-id="427e9-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="427e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="427e9-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="427e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="427e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="427e9-137">CommonParameters</span></span>
<span data-ttu-id="427e9-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="427e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="427e9-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="427e9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="427e9-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="427e9-140">INPUTS</span></span>

### <span data-ttu-id="427e9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="427e9-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="427e9-142">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="427e9-142">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="427e9-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="427e9-143">OUTPUTS</span></span>

### <span data-ttu-id="427e9-144">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="427e9-144">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="427e9-145">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="427e9-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="427e9-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="427e9-146">NOTES</span></span>

## <span data-ttu-id="427e9-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="427e9-147">RELATED LINKS</span></span>
