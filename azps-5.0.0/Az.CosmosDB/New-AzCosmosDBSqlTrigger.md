---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299216"
---
# <span data-ttu-id="49458-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="49458-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="49458-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49458-102">SYNOPSIS</span></span>
<span data-ttu-id="49458-103">Új CosmosDB SQL-triggert hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49458-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="49458-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49458-104">SYNTAX</span></span>

### <span data-ttu-id="49458-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="49458-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49458-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49458-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49458-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="49458-107">DESCRIPTION</span></span>
<span data-ttu-id="49458-108">Új CosmosDB SQL-triggert hoz létre.</span><span class="sxs-lookup"><span data-stu-id="49458-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="49458-109">Példák</span><span class="sxs-lookup"><span data-stu-id="49458-109">EXAMPLES</span></span>

### <span data-ttu-id="49458-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49458-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="49458-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49458-111">PARAMETERS</span></span>

### <span data-ttu-id="49458-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="49458-112">-AccountName</span></span>
<span data-ttu-id="49458-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="49458-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="49458-114">-Body</span><span class="sxs-lookup"><span data-stu-id="49458-114">-Body</span></span>
<span data-ttu-id="49458-115">Az indító törzse.</span><span class="sxs-lookup"><span data-stu-id="49458-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="49458-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49458-116">-Confirm</span></span>
<span data-ttu-id="49458-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49458-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49458-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="49458-118">-ContainerName</span></span>
<span data-ttu-id="49458-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="49458-119">Container name.</span></span>

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

### <span data-ttu-id="49458-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49458-120">-DatabaseName</span></span>
<span data-ttu-id="49458-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="49458-121">Database name.</span></span>

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

### <span data-ttu-id="49458-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49458-122">-DefaultProfile</span></span>
<span data-ttu-id="49458-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49458-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49458-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49458-124">-Name</span></span>
<span data-ttu-id="49458-125">Trigger neve.</span><span class="sxs-lookup"><span data-stu-id="49458-125">Trigger name.</span></span>

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

### <span data-ttu-id="49458-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="49458-126">-ParentObject</span></span>
<span data-ttu-id="49458-127">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="49458-127">Sql Container object.</span></span>

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

### <span data-ttu-id="49458-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49458-128">-ResourceGroupName</span></span>
<span data-ttu-id="49458-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="49458-129">Name of resource group.</span></span>

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

### <span data-ttu-id="49458-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="49458-130">-TriggerOperation</span></span>
<span data-ttu-id="49458-131">Az a művelet, amelyhez az trigger társítva van.</span><span class="sxs-lookup"><span data-stu-id="49458-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="49458-132">A lehetséges értékek a következők: "all", "Create", "Update", "Delete", "csere"</span><span class="sxs-lookup"><span data-stu-id="49458-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="49458-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="49458-133">-TriggerType</span></span>
<span data-ttu-id="49458-134">Az indító típusa.</span><span class="sxs-lookup"><span data-stu-id="49458-134">Type of the Trigger.</span></span>
<span data-ttu-id="49458-135">A lehetséges értékek a következők: "pre", "bejegyzés"</span><span class="sxs-lookup"><span data-stu-id="49458-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="49458-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49458-136">-WhatIf</span></span>
<span data-ttu-id="49458-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49458-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49458-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49458-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49458-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49458-139">CommonParameters</span></span>
<span data-ttu-id="49458-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49458-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49458-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="49458-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49458-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49458-142">INPUTS</span></span>

### <span data-ttu-id="49458-143">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="49458-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="49458-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49458-144">OUTPUTS</span></span>

### <span data-ttu-id="49458-145">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="49458-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="49458-146">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="49458-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="49458-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49458-147">NOTES</span></span>

## <span data-ttu-id="49458-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49458-148">RELATED LINKS</span></span>
