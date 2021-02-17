---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164003"
---
# <span data-ttu-id="b4019-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b4019-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b4019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4019-102">SYNOPSIS</span></span>
<span data-ttu-id="b4019-103">Létrehoz egy új TárolóDB Sql StoredProcedure-t.</span><span class="sxs-lookup"><span data-stu-id="b4019-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b4019-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4019-104">SYNTAX</span></span>

### <span data-ttu-id="b4019-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b4019-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4019-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4019-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4019-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4019-107">DESCRIPTION</span></span>
<span data-ttu-id="b4019-108">Létrehoz egy új TárolóDB Sql StoredProcedure-t.</span><span class="sxs-lookup"><span data-stu-id="b4019-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b4019-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4019-109">EXAMPLES</span></span>

### <span data-ttu-id="b4019-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="b4019-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="b4019-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4019-111">PARAMETERS</span></span>

### <span data-ttu-id="b4019-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4019-112">-AccountName</span></span>
<span data-ttu-id="b4019-113">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="b4019-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b4019-114">-Body</span><span class="sxs-lookup"><span data-stu-id="b4019-114">-Body</span></span>
<span data-ttu-id="b4019-115">A tárolt eljárás törzse.</span><span class="sxs-lookup"><span data-stu-id="b4019-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="b4019-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4019-116">-Confirm</span></span>
<span data-ttu-id="b4019-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b4019-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4019-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b4019-118">-ContainerName</span></span>
<span data-ttu-id="b4019-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="b4019-119">Container name.</span></span>

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

### <span data-ttu-id="b4019-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4019-120">-DatabaseName</span></span>
<span data-ttu-id="b4019-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="b4019-121">Database name.</span></span>

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

### <span data-ttu-id="b4019-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4019-122">-DefaultProfile</span></span>
<span data-ttu-id="b4019-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4019-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4019-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b4019-124">-Name</span></span>
<span data-ttu-id="b4019-125">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="b4019-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b4019-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4019-126">-ParentObject</span></span>
<span data-ttu-id="b4019-127">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="b4019-127">Sql Container object.</span></span>

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

### <span data-ttu-id="b4019-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4019-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4019-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b4019-129">Name of resource group.</span></span>

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

### <span data-ttu-id="b4019-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4019-130">-WhatIf</span></span>
<span data-ttu-id="b4019-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b4019-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4019-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4019-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4019-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4019-133">CommonParameters</span></span>
<span data-ttu-id="b4019-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4019-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4019-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4019-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4019-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4019-136">INPUTS</span></span>

### <span data-ttu-id="b4019-137">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="b4019-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="b4019-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4019-138">OUTPUTS</span></span>

### <span data-ttu-id="b4019-139">Microsoft.Azure.Commands.EzresDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b4019-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="b4019-140">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b4019-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b4019-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4019-141">NOTES</span></span>

## <span data-ttu-id="b4019-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4019-142">RELATED LINKS</span></span>
