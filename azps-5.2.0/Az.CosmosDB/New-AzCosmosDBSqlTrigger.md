---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366979"
---
# <span data-ttu-id="989dd-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="989dd-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="989dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989dd-102">SYNOPSIS</span></span>
<span data-ttu-id="989dd-103">Létrehoz egy új TárolóB SQL-eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="989dd-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="989dd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="989dd-104">SYNTAX</span></span>

### <span data-ttu-id="989dd-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="989dd-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="989dd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="989dd-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="989dd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="989dd-107">DESCRIPTION</span></span>
<span data-ttu-id="989dd-108">Létrehoz egy új TárolóB SQL-eseményindítót.</span><span class="sxs-lookup"><span data-stu-id="989dd-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="989dd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="989dd-109">EXAMPLES</span></span>

### <span data-ttu-id="989dd-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="989dd-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="989dd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="989dd-111">PARAMETERS</span></span>

### <span data-ttu-id="989dd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="989dd-112">-AccountName</span></span>
<span data-ttu-id="989dd-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="989dd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="989dd-114">-Body</span><span class="sxs-lookup"><span data-stu-id="989dd-114">-Body</span></span>
<span data-ttu-id="989dd-115">Az eseményindító törzse.</span><span class="sxs-lookup"><span data-stu-id="989dd-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="989dd-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="989dd-116">-Confirm</span></span>
<span data-ttu-id="989dd-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="989dd-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="989dd-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="989dd-118">-ContainerName</span></span>
<span data-ttu-id="989dd-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="989dd-119">Container name.</span></span>

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

### <span data-ttu-id="989dd-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="989dd-120">-DatabaseName</span></span>
<span data-ttu-id="989dd-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="989dd-121">Database name.</span></span>

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

### <span data-ttu-id="989dd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989dd-122">-DefaultProfile</span></span>
<span data-ttu-id="989dd-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="989dd-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989dd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="989dd-124">-Name</span></span>
<span data-ttu-id="989dd-125">Eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="989dd-125">Trigger name.</span></span>

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

### <span data-ttu-id="989dd-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="989dd-126">-ParentObject</span></span>
<span data-ttu-id="989dd-127">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="989dd-127">Sql Container object.</span></span>

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

### <span data-ttu-id="989dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="989dd-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="989dd-129">Name of resource group.</span></span>

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

### <span data-ttu-id="989dd-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="989dd-130">-TriggerOperation</span></span>
<span data-ttu-id="989dd-131">A művelet, amelyhez az eseményindító társítva van.</span><span class="sxs-lookup"><span data-stu-id="989dd-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="989dd-132">Lehetséges értékek: "Mind", "Létrehozás", "Frissítés", "Törlés", "Csere"</span><span class="sxs-lookup"><span data-stu-id="989dd-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="989dd-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="989dd-133">-TriggerType</span></span>
<span data-ttu-id="989dd-134">Az eseményindító típusa.</span><span class="sxs-lookup"><span data-stu-id="989dd-134">Type of the Trigger.</span></span>
<span data-ttu-id="989dd-135">Lehetséges értékek: "Elő", "Bejegyzés"</span><span class="sxs-lookup"><span data-stu-id="989dd-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="989dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989dd-136">-WhatIf</span></span>
<span data-ttu-id="989dd-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="989dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="989dd-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="989dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="989dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989dd-139">CommonParameters</span></span>
<span data-ttu-id="989dd-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989dd-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="989dd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989dd-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="989dd-142">INPUTS</span></span>

### <span data-ttu-id="989dd-143">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="989dd-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="989dd-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="989dd-144">OUTPUTS</span></span>

### <span data-ttu-id="989dd-145">Microsoft.Azure.Commands.CossDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="989dd-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="989dd-146">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="989dd-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="989dd-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="989dd-147">NOTES</span></span>

## <span data-ttu-id="989dd-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="989dd-148">RELATED LINKS</span></span>
