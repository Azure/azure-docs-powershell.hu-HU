---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480519"
---
# <span data-ttu-id="df145-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="df145-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="df145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df145-102">SYNOPSIS</span></span>
<span data-ttu-id="df145-103">Frissíti aFrissítésekDB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df145-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="df145-104">Ügyféloldali javítást hajt végre a meglévő StoredProcedure olvasással.</span><span class="sxs-lookup"><span data-stu-id="df145-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="df145-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df145-105">SYNTAX</span></span>

### <span data-ttu-id="df145-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df145-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df145-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df145-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df145-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df145-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df145-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df145-109">DESCRIPTION</span></span>
<span data-ttu-id="df145-110">Frissíti aFrissítésekDB Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="df145-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="df145-111">Ügyféloldali javítást hajt végre a meglévő StoredProcedure olvasással.</span><span class="sxs-lookup"><span data-stu-id="df145-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="df145-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df145-112">EXAMPLES</span></span>

### <span data-ttu-id="df145-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="df145-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="df145-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df145-114">PARAMETERS</span></span>

### <span data-ttu-id="df145-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df145-115">-AccountName</span></span>
<span data-ttu-id="df145-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="df145-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="df145-117">-Body</span><span class="sxs-lookup"><span data-stu-id="df145-117">-Body</span></span>
<span data-ttu-id="df145-118">A tárolt eljárás törzse.</span><span class="sxs-lookup"><span data-stu-id="df145-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="df145-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df145-119">-Confirm</span></span>
<span data-ttu-id="df145-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df145-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df145-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="df145-121">-ContainerName</span></span>
<span data-ttu-id="df145-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="df145-122">Container name.</span></span>

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

### <span data-ttu-id="df145-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="df145-123">-DatabaseName</span></span>
<span data-ttu-id="df145-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="df145-124">Database name.</span></span>

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

### <span data-ttu-id="df145-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df145-125">-DefaultProfile</span></span>
<span data-ttu-id="df145-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="df145-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df145-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df145-127">-InputObject</span></span>
<span data-ttu-id="df145-128">Sql Tárolt eljárás objektum</span><span class="sxs-lookup"><span data-stu-id="df145-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df145-129">-Name</span><span class="sxs-lookup"><span data-stu-id="df145-129">-Name</span></span>
<span data-ttu-id="df145-130">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="df145-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="df145-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df145-131">-ParentObject</span></span>
<span data-ttu-id="df145-132">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="df145-132">Sql Container object.</span></span>

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

### <span data-ttu-id="df145-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df145-133">-ResourceGroupName</span></span>
<span data-ttu-id="df145-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="df145-134">Name of resource group.</span></span>

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

### <span data-ttu-id="df145-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df145-135">-WhatIf</span></span>
<span data-ttu-id="df145-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df145-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df145-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df145-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df145-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df145-138">CommonParameters</span></span>
<span data-ttu-id="df145-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df145-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df145-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df145-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df145-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df145-141">INPUTS</span></span>

### <span data-ttu-id="df145-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="df145-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="df145-143">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="df145-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="df145-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df145-144">OUTPUTS</span></span>

### <span data-ttu-id="df145-145">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="df145-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="df145-146">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="df145-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="df145-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df145-147">NOTES</span></span>

## <span data-ttu-id="df145-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df145-148">RELATED LINKS</span></span>
