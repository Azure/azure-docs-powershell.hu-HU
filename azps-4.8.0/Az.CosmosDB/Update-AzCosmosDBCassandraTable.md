---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 6fad5017dbd7dd258e44e69638a919e53597ec9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184608"
---
# <span data-ttu-id="045f2-101">Update-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="045f2-101">Update-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="045f2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="045f2-102">SYNOPSIS</span></span>
<span data-ttu-id="045f2-103">A CosmosDB Cassandra táblázat frissítése</span><span class="sxs-lookup"><span data-stu-id="045f2-103">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="045f2-104">Ügyféloldali javítás műveletet hajt végre a meglévő tábla olvasásával.</span><span class="sxs-lookup"><span data-stu-id="045f2-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="045f2-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="045f2-105">SYNTAX</span></span>

### <span data-ttu-id="045f2-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="045f2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-TtlInSeconds <Int32>]
 [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="045f2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="045f2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -ParentObject <PSCassandraKeyspaceGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="045f2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="045f2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBCassandraTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 [-TtlInSeconds <Int32>] [-AnalyticalStorageTtl <Int32>] [-Schema <PSCassandraSchema>]
 -InputObject <PSCassandraTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="045f2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="045f2-109">DESCRIPTION</span></span>
<span data-ttu-id="045f2-110">A CosmosDB Cassandra táblázat frissítése</span><span class="sxs-lookup"><span data-stu-id="045f2-110">Updates the CosmosDB Cassandra Table.</span></span> <span data-ttu-id="045f2-111">Ügyféloldali javítás műveletet hajt végre a meglévő tábla olvasásával.</span><span class="sxs-lookup"><span data-stu-id="045f2-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="045f2-112">Példák</span><span class="sxs-lookup"><span data-stu-id="045f2-112">EXAMPLES</span></span>

### <span data-ttu-id="045f2-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="045f2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBCassandraTable -AccountName myAccountName -ResourceGroupName myRgName -KeyspaceName myKeyspaceName -Name myTableName -Schema updatedSchema
        Name     : myTable
        Id       : /subscriptions/mySubId/resourceGroups/myRgName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/cassandraKeyspaces/myKeyspaceName/t
                ables/myTableName
        Location :
        Tags     :
        Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetPropertiesResource
```

<span data-ttu-id="045f2-114">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="045f2-114">{{ Add example description here }}</span></span>

## <span data-ttu-id="045f2-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="045f2-115">PARAMETERS</span></span>

### <span data-ttu-id="045f2-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="045f2-116">-AccountName</span></span>
<span data-ttu-id="045f2-117">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="045f2-117">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="045f2-118">-AnalyticalStorageTtl</span><span class="sxs-lookup"><span data-stu-id="045f2-118">-AnalyticalStorageTtl</span></span>
<span data-ttu-id="045f2-119">Analitikai tárterület ÉLETTARTAMa.</span><span class="sxs-lookup"><span data-stu-id="045f2-119">Analytical Storage TTL.</span></span>

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

### <span data-ttu-id="045f2-120">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="045f2-120">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="045f2-121">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="045f2-121">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="045f2-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="045f2-122">-Confirm</span></span>
<span data-ttu-id="045f2-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="045f2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="045f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="045f2-124">-DefaultProfile</span></span>
<span data-ttu-id="045f2-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="045f2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="045f2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="045f2-126">-InputObject</span></span>
<span data-ttu-id="045f2-127">Cassandra Table objektum.</span><span class="sxs-lookup"><span data-stu-id="045f2-127">Cassandra Table object.</span></span>

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

### <span data-ttu-id="045f2-128">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="045f2-128">-KeyspaceName</span></span>
<span data-ttu-id="045f2-129">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="045f2-129">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="045f2-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="045f2-130">-Name</span></span>
<span data-ttu-id="045f2-131">A táblázat neve: Cassandra.</span><span class="sxs-lookup"><span data-stu-id="045f2-131">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="045f2-132">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="045f2-132">-ParentObject</span></span>
<span data-ttu-id="045f2-133">A billentyűk Cassandra Space objektum</span><span class="sxs-lookup"><span data-stu-id="045f2-133">Cassandra Keyspace object.</span></span>

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

### <span data-ttu-id="045f2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="045f2-134">-ResourceGroupName</span></span>
<span data-ttu-id="045f2-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="045f2-135">Name of resource group.</span></span>

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

### <span data-ttu-id="045f2-136">-Schema (séma)</span><span class="sxs-lookup"><span data-stu-id="045f2-136">-Schema</span></span>
<span data-ttu-id="045f2-137">PSCassandraSchema objektum</span><span class="sxs-lookup"><span data-stu-id="045f2-137">PSCassandraSchema object.</span></span>
<span data-ttu-id="045f2-138">Az objektum létrehozásához használja a New-AzCosmosDBCassandraSchema.</span><span class="sxs-lookup"><span data-stu-id="045f2-138">Use New-AzCosmosDBCassandraSchema to create this object.</span></span>

```yaml
Type: PSCassandraSchema
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="045f2-139">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="045f2-139">-Throughput</span></span>
<span data-ttu-id="045f2-140">A szóköz (RU/s) méretének átvitele.</span><span class="sxs-lookup"><span data-stu-id="045f2-140">The throughput of Cassandra Keyspace (RU/s).</span></span>
<span data-ttu-id="045f2-141">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="045f2-141">Default value is 400.</span></span>

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

### <span data-ttu-id="045f2-142">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="045f2-142">-TtlInSeconds</span></span>
<span data-ttu-id="045f2-143">Az alapértelmezett élettartam másodpercben</span><span class="sxs-lookup"><span data-stu-id="045f2-143">Default Ttl in seconds.</span></span>
<span data-ttu-id="045f2-144">Ha az érték hiányzik vagy a-1 érték van megadva, az elemek nem járnak le.</span><span class="sxs-lookup"><span data-stu-id="045f2-144">If the value is missing or set to  - 1, items don't expire.</span></span>
<span data-ttu-id="045f2-145">Ha az érték n értékre van állítva, az elemek a legutóbbi módosítási idő után lejárnak.</span><span class="sxs-lookup"><span data-stu-id="045f2-145">If the value is set to n, items will expire n seconds after last modified time.</span></span>

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

### <span data-ttu-id="045f2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="045f2-146">-WhatIf</span></span>
<span data-ttu-id="045f2-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="045f2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="045f2-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="045f2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="045f2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="045f2-149">CommonParameters</span></span>
<span data-ttu-id="045f2-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="045f2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="045f2-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="045f2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="045f2-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="045f2-152">INPUTS</span></span>

### <span data-ttu-id="045f2-153">Microsoft. Azure. Command. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="045f2-153">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

### <span data-ttu-id="045f2-154">Microsoft. Azure. Command. CosmosDB. models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="045f2-154">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="045f2-155">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="045f2-155">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="045f2-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="045f2-156">OUTPUTS</span></span>

### <span data-ttu-id="045f2-157">Microsoft. Azure. Command. CosmosDB. models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="045f2-157">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

### <span data-ttu-id="045f2-158">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="045f2-158">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="045f2-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="045f2-159">NOTES</span></span>

## <span data-ttu-id="045f2-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="045f2-160">RELATED LINKS</span></span>
