---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365132"
---
# <span data-ttu-id="bc8d3-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="bc8d3-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="bc8d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc8d3-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8d3-103">Létrehoz egy új Táblát. Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bc8d3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bc8d3-104">SYNTAX</span></span>

### <span data-ttu-id="bc8d3-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bc8d3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc8d3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc8d3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc8d3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bc8d3-107">DESCRIPTION</span></span>
<span data-ttu-id="bc8d3-108">Létrehoz egy új Táblát. Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bc8d3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bc8d3-109">EXAMPLES</span></span>

### <span data-ttu-id="bc8d3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bc8d3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="bc8d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc8d3-111">PARAMETERS</span></span>

### <span data-ttu-id="bc8d3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bc8d3-112">-AccountName</span></span>
<span data-ttu-id="bc8d3-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc8d3-114">-Body</span><span class="sxs-lookup"><span data-stu-id="bc8d3-114">-Body</span></span>
<span data-ttu-id="bc8d3-115">A tárolt eljárás törzse.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="bc8d3-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc8d3-116">-Confirm</span></span>
<span data-ttu-id="bc8d3-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc8d3-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bc8d3-118">-ContainerName</span></span>
<span data-ttu-id="bc8d3-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-119">Container name.</span></span>

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

### <span data-ttu-id="bc8d3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc8d3-120">-DatabaseName</span></span>
<span data-ttu-id="bc8d3-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-121">Database name.</span></span>

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

### <span data-ttu-id="bc8d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8d3-122">-DefaultProfile</span></span>
<span data-ttu-id="bc8d3-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc8d3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bc8d3-124">-Name</span></span>
<span data-ttu-id="bc8d3-125">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="bc8d3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bc8d3-126">-ParentObject</span></span>
<span data-ttu-id="bc8d3-127">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-127">Sql Container object.</span></span>

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

### <span data-ttu-id="bc8d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="bc8d3-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="bc8d3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc8d3-130">-WhatIf</span></span>
<span data-ttu-id="bc8d3-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc8d3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc8d3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8d3-133">CommonParameters</span></span>
<span data-ttu-id="bc8d3-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc8d3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8d3-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc8d3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8d3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc8d3-136">INPUTS</span></span>

### <span data-ttu-id="bc8d3-137">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bc8d3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="bc8d3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bc8d3-138">OUTPUTS</span></span>

### <span data-ttu-id="bc8d3-139">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="bc8d3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="bc8d3-140">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bc8d3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bc8d3-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bc8d3-141">NOTES</span></span>

## <span data-ttu-id="bc8d3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bc8d3-142">RELATED LINKS</span></span>
