---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185072"
---
# <span data-ttu-id="2cf34-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="2cf34-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="2cf34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cf34-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf34-103">Frissíti a CosmosDB SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="2cf34-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="2cf34-104">Ügyféloldali javítás műveletet hajt végre a meglévő trigger elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="2cf34-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="2cf34-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cf34-105">SYNTAX</span></span>

### <span data-ttu-id="2cf34-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2cf34-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf34-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cf34-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf34-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cf34-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf34-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cf34-109">DESCRIPTION</span></span>
<span data-ttu-id="2cf34-110">Frissíti a CosmosDB SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="2cf34-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="2cf34-111">Ügyféloldali javítás műveletet hajt végre a meglévő trigger elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="2cf34-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="2cf34-112">Példák</span><span class="sxs-lookup"><span data-stu-id="2cf34-112">EXAMPLES</span></span>

### <span data-ttu-id="2cf34-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2cf34-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="2cf34-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cf34-114">PARAMETERS</span></span>

### <span data-ttu-id="2cf34-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2cf34-115">-AccountName</span></span>
<span data-ttu-id="2cf34-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="2cf34-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2cf34-117">-Body</span><span class="sxs-lookup"><span data-stu-id="2cf34-117">-Body</span></span>
<span data-ttu-id="2cf34-118">Az indító törzse.</span><span class="sxs-lookup"><span data-stu-id="2cf34-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="2cf34-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2cf34-119">-Confirm</span></span>
<span data-ttu-id="2cf34-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2cf34-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf34-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2cf34-121">-ContainerName</span></span>
<span data-ttu-id="2cf34-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="2cf34-122">Container name.</span></span>

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

### <span data-ttu-id="2cf34-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cf34-123">-DatabaseName</span></span>
<span data-ttu-id="2cf34-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2cf34-124">Database name.</span></span>

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

### <span data-ttu-id="2cf34-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf34-125">-DefaultProfile</span></span>
<span data-ttu-id="2cf34-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cf34-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf34-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf34-127">-InputObject</span></span>
<span data-ttu-id="2cf34-128">SQL-indító objektum</span><span class="sxs-lookup"><span data-stu-id="2cf34-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="2cf34-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2cf34-129">-Name</span></span>
<span data-ttu-id="2cf34-130">Trigger neve.</span><span class="sxs-lookup"><span data-stu-id="2cf34-130">Trigger name.</span></span>

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

### <span data-ttu-id="2cf34-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2cf34-131">-ParentObject</span></span>
<span data-ttu-id="2cf34-132">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="2cf34-132">Sql Container object.</span></span>

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

### <span data-ttu-id="2cf34-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf34-133">-ResourceGroupName</span></span>
<span data-ttu-id="2cf34-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2cf34-134">Name of resource group.</span></span>

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

### <span data-ttu-id="2cf34-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="2cf34-135">-TriggerOperation</span></span>
<span data-ttu-id="2cf34-136">Az a művelet, amelyhez az trigger társítva van.</span><span class="sxs-lookup"><span data-stu-id="2cf34-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="2cf34-137">A lehetséges értékek a következők: "all", "Create", "Update", "Delete", "csere"</span><span class="sxs-lookup"><span data-stu-id="2cf34-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="2cf34-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="2cf34-138">-TriggerType</span></span>
<span data-ttu-id="2cf34-139">Az indító típusa.</span><span class="sxs-lookup"><span data-stu-id="2cf34-139">Type of the Trigger.</span></span>
<span data-ttu-id="2cf34-140">A lehetséges értékek a következők: "pre", "bejegyzés"</span><span class="sxs-lookup"><span data-stu-id="2cf34-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="2cf34-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf34-141">-WhatIf</span></span>
<span data-ttu-id="2cf34-142">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2cf34-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cf34-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2cf34-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf34-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf34-144">CommonParameters</span></span>
<span data-ttu-id="2cf34-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cf34-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf34-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2cf34-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf34-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf34-147">INPUTS</span></span>

### <span data-ttu-id="2cf34-148">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2cf34-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2cf34-149">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="2cf34-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="2cf34-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cf34-150">OUTPUTS</span></span>

### <span data-ttu-id="2cf34-151">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="2cf34-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="2cf34-152">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="2cf34-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="2cf34-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cf34-153">NOTES</span></span>

## <span data-ttu-id="2cf34-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cf34-154">RELATED LINKS</span></span>
