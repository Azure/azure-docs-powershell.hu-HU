---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbcollectionthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBCollectionThroughput.md
ms.openlocfilehash: 23a88660bd599b0d317b89a1a7c1dbb1e2d51854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163979"
---
# <span data-ttu-id="02cc7-101">Update-AzCosmosDBMongoDBCollectionThroughput</span><span class="sxs-lookup"><span data-stu-id="02cc7-101">Update-AzCosmosDBMongoDBCollectionThroughput</span></span>

## <span data-ttu-id="02cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="02cc7-103">Frissíti a MintakDB MongoDB gyűjtemény átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="02cc7-103">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="02cc7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02cc7-104">SYNTAX</span></span>

### <span data-ttu-id="02cc7-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02cc7-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput -DatabaseName <String> [-Name <String>]
 -ResourceGroupName <String> -AccountName <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02cc7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02cc7-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -ParentObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02cc7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02cc7-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBCollectionThroughput [-Name <String>] -InputObject <PSMongoDBCollectionGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02cc7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02cc7-108">DESCRIPTION</span></span>
<span data-ttu-id="02cc7-109">Frissíti a MintakDB MongoDB gyűjtemény átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="02cc7-109">Updates the throughput value of a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="02cc7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02cc7-110">EXAMPLES</span></span>

### <span data-ttu-id="02cc7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="02cc7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBCollectionThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -DatabaseName {mydatabaseName} -Name {myCollectionName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabase/{mydatabaseName}/collections/{myCollectionName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

<span data-ttu-id="02cc7-112">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="02cc7-112">{{ Add example description here }}</span></span>

## <span data-ttu-id="02cc7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02cc7-113">PARAMETERS</span></span>

### <span data-ttu-id="02cc7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02cc7-114">-AccountName</span></span>
<span data-ttu-id="02cc7-115">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="02cc7-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="02cc7-116">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="02cc7-116">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="02cc7-117">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="02cc7-117">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="02cc7-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02cc7-118">-Confirm</span></span>
<span data-ttu-id="02cc7-119">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="02cc7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02cc7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="02cc7-120">-DatabaseName</span></span>
<span data-ttu-id="02cc7-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="02cc7-121">Database name.</span></span>

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

### <span data-ttu-id="02cc7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cc7-122">-DefaultProfile</span></span>
<span data-ttu-id="02cc7-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02cc7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02cc7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02cc7-124">-InputObject</span></span>
<span data-ttu-id="02cc7-125">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="02cc7-125">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02cc7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="02cc7-126">-Name</span></span>
<span data-ttu-id="02cc7-127">Gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="02cc7-127">Collection name.</span></span>

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

### <span data-ttu-id="02cc7-128">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02cc7-128">-ParentObject</span></span>
<span data-ttu-id="02cc7-129">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="02cc7-129">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02cc7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02cc7-130">-ResourceGroupName</span></span>
<span data-ttu-id="02cc7-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="02cc7-131">Name of resource group.</span></span>

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

### <span data-ttu-id="02cc7-132">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="02cc7-132">-Throughput</span></span>
<span data-ttu-id="02cc7-133">Az SQL-tároló (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="02cc7-133">The throughput of SQL container (RU/s).</span></span>
<span data-ttu-id="02cc7-134">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="02cc7-134">Default value is 400.</span></span>

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

### <span data-ttu-id="02cc7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02cc7-135">-WhatIf</span></span>
<span data-ttu-id="02cc7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="02cc7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02cc7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="02cc7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02cc7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cc7-138">CommonParameters</span></span>
<span data-ttu-id="02cc7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02cc7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cc7-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02cc7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cc7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02cc7-141">INPUTS</span></span>

### <span data-ttu-id="02cc7-142">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="02cc7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="02cc7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02cc7-143">OUTPUTS</span></span>

### <span data-ttu-id="02cc7-144">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="02cc7-144">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="02cc7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02cc7-145">NOTES</span></span>

## <span data-ttu-id="02cc7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02cc7-146">RELATED LINKS</span></span>
