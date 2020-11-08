---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010550"
---
# <span data-ttu-id="aff0f-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="aff0f-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="aff0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aff0f-102">SYNOPSIS</span></span>
<span data-ttu-id="aff0f-103">Új SQL-CosmosDB hoz létre, vagy frissít egy meglévő SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="aff0f-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="aff0f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aff0f-104">SYNTAX</span></span>

### <span data-ttu-id="aff0f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="aff0f-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aff0f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aff0f-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aff0f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="aff0f-107">DESCRIPTION</span></span>
<span data-ttu-id="aff0f-108">A **set-AzCosmosDBSqlTrigger** parancsmag új SQL-CosmosDB hoz létre, vagy frissít egy meglévő SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="aff0f-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="aff0f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aff0f-109">EXAMPLES</span></span>

### <span data-ttu-id="aff0f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aff0f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="aff0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aff0f-111">PARAMETERS</span></span>

### <span data-ttu-id="aff0f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aff0f-112">-AccountName</span></span>
<span data-ttu-id="aff0f-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="aff0f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aff0f-114">-Body</span><span class="sxs-lookup"><span data-stu-id="aff0f-114">-Body</span></span>
<span data-ttu-id="aff0f-115">Az indító törzse.</span><span class="sxs-lookup"><span data-stu-id="aff0f-115">The body of the Trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff0f-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aff0f-116">-Confirm</span></span>
<span data-ttu-id="aff0f-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aff0f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff0f-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="aff0f-118">-ContainerName</span></span>
<span data-ttu-id="aff0f-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="aff0f-119">Container name.</span></span>

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

### <span data-ttu-id="aff0f-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aff0f-120">-DatabaseName</span></span>
<span data-ttu-id="aff0f-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="aff0f-121">Database name.</span></span>

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

### <span data-ttu-id="aff0f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff0f-122">-DefaultProfile</span></span>
<span data-ttu-id="aff0f-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aff0f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aff0f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aff0f-124">-InputObject</span></span>
<span data-ttu-id="aff0f-125">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="aff0f-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aff0f-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="aff0f-126">-Name</span></span>
<span data-ttu-id="aff0f-127">Trigger neve.</span><span class="sxs-lookup"><span data-stu-id="aff0f-127">Trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff0f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff0f-128">-ResourceGroupName</span></span>
<span data-ttu-id="aff0f-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aff0f-129">Name of resource group.</span></span>

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

### <span data-ttu-id="aff0f-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="aff0f-130">-TriggerOperation</span></span>
<span data-ttu-id="aff0f-131">Az a művelet, amelyhez az trigger társítva van.</span><span class="sxs-lookup"><span data-stu-id="aff0f-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="aff0f-132">A lehetséges értékek a következők: "all", "Create", "Update", "Delete", "csere"</span><span class="sxs-lookup"><span data-stu-id="aff0f-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="aff0f-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="aff0f-133">-TriggerType</span></span>
<span data-ttu-id="aff0f-134">Az indító típusa.</span><span class="sxs-lookup"><span data-stu-id="aff0f-134">Type of the Trigger.</span></span>
<span data-ttu-id="aff0f-135">A lehetséges értékek a következők: "pre", "bejegyzés"</span><span class="sxs-lookup"><span data-stu-id="aff0f-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="aff0f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff0f-136">-WhatIf</span></span>
<span data-ttu-id="aff0f-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aff0f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aff0f-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aff0f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff0f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff0f-139">CommonParameters</span></span>
<span data-ttu-id="aff0f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aff0f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff0f-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aff0f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff0f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff0f-142">INPUTS</span></span>

### <span data-ttu-id="aff0f-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="aff0f-143">None</span></span>

## <span data-ttu-id="aff0f-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aff0f-144">OUTPUTS</span></span>

### <span data-ttu-id="aff0f-145">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="aff0f-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="aff0f-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aff0f-146">NOTES</span></span>

## <span data-ttu-id="aff0f-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aff0f-147">RELATED LINKS</span></span>
