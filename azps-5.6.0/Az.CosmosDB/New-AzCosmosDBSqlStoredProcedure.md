---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b088eaf9e09408b8a294965c66acf88ac2715dee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924193"
---
# <span data-ttu-id="86e44-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="86e44-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="86e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e44-102">SYNOPSIS</span></span>
<span data-ttu-id="86e44-103">Létrehoz egy új Táblát. Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="86e44-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="86e44-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="86e44-104">SYNTAX</span></span>

### <span data-ttu-id="86e44-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="86e44-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86e44-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="86e44-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e44-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="86e44-107">DESCRIPTION</span></span>
<span data-ttu-id="86e44-108">Létrehoz egy új Táblát. Sql StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="86e44-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="86e44-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="86e44-109">EXAMPLES</span></span>

### <span data-ttu-id="86e44-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="86e44-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="86e44-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e44-111">PARAMETERS</span></span>

### <span data-ttu-id="86e44-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="86e44-112">-AccountName</span></span>
<span data-ttu-id="86e44-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="86e44-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="86e44-114">-Body</span><span class="sxs-lookup"><span data-stu-id="86e44-114">-Body</span></span>
<span data-ttu-id="86e44-115">A tárolt eljárás törzse.</span><span class="sxs-lookup"><span data-stu-id="86e44-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="86e44-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86e44-116">-Confirm</span></span>
<span data-ttu-id="86e44-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="86e44-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e44-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="86e44-118">-ContainerName</span></span>
<span data-ttu-id="86e44-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="86e44-119">Container name.</span></span>

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

### <span data-ttu-id="86e44-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86e44-120">-DatabaseName</span></span>
<span data-ttu-id="86e44-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="86e44-121">Database name.</span></span>

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

### <span data-ttu-id="86e44-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e44-122">-DefaultProfile</span></span>
<span data-ttu-id="86e44-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="86e44-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e44-124">-Name</span><span class="sxs-lookup"><span data-stu-id="86e44-124">-Name</span></span>
<span data-ttu-id="86e44-125">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="86e44-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="86e44-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="86e44-126">-ParentObject</span></span>
<span data-ttu-id="86e44-127">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="86e44-127">Sql Container object.</span></span>

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

### <span data-ttu-id="86e44-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e44-128">-ResourceGroupName</span></span>
<span data-ttu-id="86e44-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="86e44-129">Name of resource group.</span></span>

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

### <span data-ttu-id="86e44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e44-130">-WhatIf</span></span>
<span data-ttu-id="86e44-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="86e44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e44-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="86e44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e44-133">CommonParameters</span></span>
<span data-ttu-id="86e44-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e44-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e44-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e44-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86e44-136">INPUTS</span></span>

### <span data-ttu-id="86e44-137">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="86e44-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="86e44-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="86e44-138">OUTPUTS</span></span>

### <span data-ttu-id="86e44-139">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="86e44-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="86e44-140">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="86e44-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="86e44-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="86e44-141">NOTES</span></span>

## <span data-ttu-id="86e44-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="86e44-142">RELATED LINKS</span></span>
