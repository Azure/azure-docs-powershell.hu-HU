---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477334"
---
# <span data-ttu-id="f8d7c-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f8d7c-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f8d7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d7c-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d7c-103">Frissíti aFrissítésekDB sql triggert.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="f8d7c-104">Ügyféloldali javítást hajt végre a meglévő eseményindító elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="f8d7c-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8d7c-105">SYNTAX</span></span>

### <span data-ttu-id="f8d7c-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8d7c-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d7c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8d7c-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8d7c-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8d7c-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8d7c-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8d7c-109">DESCRIPTION</span></span>
<span data-ttu-id="f8d7c-110">Frissíti aFrissítésekDB sql triggert.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="f8d7c-111">Ügyféloldali javítást hajt végre a meglévő eseményindító elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="f8d7c-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8d7c-112">EXAMPLES</span></span>

### <span data-ttu-id="f8d7c-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8d7c-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="f8d7c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8d7c-114">PARAMETERS</span></span>

### <span data-ttu-id="f8d7c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-115">-AccountName</span></span>
<span data-ttu-id="f8d7c-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f8d7c-117">-Body</span><span class="sxs-lookup"><span data-stu-id="f8d7c-117">-Body</span></span>
<span data-ttu-id="f8d7c-118">Az eseményindító törzse.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="f8d7c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8d7c-119">-Confirm</span></span>
<span data-ttu-id="f8d7c-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8d7c-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-121">-ContainerName</span></span>
<span data-ttu-id="f8d7c-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-122">Container name.</span></span>

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

### <span data-ttu-id="f8d7c-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-123">-DatabaseName</span></span>
<span data-ttu-id="f8d7c-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-124">Database name.</span></span>

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

### <span data-ttu-id="f8d7c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d7c-125">-DefaultProfile</span></span>
<span data-ttu-id="f8d7c-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8d7c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8d7c-127">-InputObject</span></span>
<span data-ttu-id="f8d7c-128">Sql trigger objektum</span><span class="sxs-lookup"><span data-stu-id="f8d7c-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d7c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f8d7c-129">-Name</span></span>
<span data-ttu-id="f8d7c-130">Eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-130">Trigger name.</span></span>

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

### <span data-ttu-id="f8d7c-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f8d7c-131">-ParentObject</span></span>
<span data-ttu-id="f8d7c-132">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-132">Sql Container object.</span></span>

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

### <span data-ttu-id="f8d7c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d7c-133">-ResourceGroupName</span></span>
<span data-ttu-id="f8d7c-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-134">Name of resource group.</span></span>

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

### <span data-ttu-id="f8d7c-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="f8d7c-135">-TriggerOperation</span></span>
<span data-ttu-id="f8d7c-136">A művelet, amelyhez az eseményindító társítva van.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="f8d7c-137">Lehetséges értékek: "Mind", "Létrehozás", "Frissítés", "Törlés", "Csere"</span><span class="sxs-lookup"><span data-stu-id="f8d7c-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="f8d7c-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="f8d7c-138">-TriggerType</span></span>
<span data-ttu-id="f8d7c-139">Az eseményindító típusa.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-139">Type of the Trigger.</span></span>
<span data-ttu-id="f8d7c-140">Lehetséges értékek: "Elő", "Bejegyzés"</span><span class="sxs-lookup"><span data-stu-id="f8d7c-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="f8d7c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8d7c-141">-WhatIf</span></span>
<span data-ttu-id="f8d7c-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8d7c-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8d7c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d7c-144">CommonParameters</span></span>
<span data-ttu-id="f8d7c-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d7c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d7c-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8d7c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d7c-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8d7c-147">INPUTS</span></span>

### <span data-ttu-id="f8d7c-148">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="f8d7c-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="f8d7c-149">Microsoft.Azure.Commands.CossDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f8d7c-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="f8d7c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8d7c-150">OUTPUTS</span></span>

### <span data-ttu-id="f8d7c-151">Microsoft.Azure.Commands.CossDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f8d7c-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="f8d7c-152">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f8d7c-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f8d7c-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8d7c-153">NOTES</span></span>

## <span data-ttu-id="f8d7c-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8d7c-154">RELATED LINKS</span></span>
