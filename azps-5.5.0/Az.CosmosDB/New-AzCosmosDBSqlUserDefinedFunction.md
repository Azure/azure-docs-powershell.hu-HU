---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204614"
---
# <span data-ttu-id="cabb7-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="cabb7-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="cabb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cabb7-102">SYNOPSIS</span></span>
<span data-ttu-id="cabb7-103">Létrehoz egy új ParancsbélB Sql UserDefinedFunctiont.</span><span class="sxs-lookup"><span data-stu-id="cabb7-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="cabb7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cabb7-104">SYNTAX</span></span>

### <span data-ttu-id="cabb7-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cabb7-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cabb7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cabb7-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cabb7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cabb7-107">DESCRIPTION</span></span>
<span data-ttu-id="cabb7-108">Létrehoz egy új ParancsbélB Sql UserDefinedFunctiont.</span><span class="sxs-lookup"><span data-stu-id="cabb7-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="cabb7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cabb7-109">EXAMPLES</span></span>

### <span data-ttu-id="cabb7-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="cabb7-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="cabb7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cabb7-111">PARAMETERS</span></span>

### <span data-ttu-id="cabb7-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cabb7-112">-AccountName</span></span>
<span data-ttu-id="cabb7-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="cabb7-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cabb7-114">-Body</span><span class="sxs-lookup"><span data-stu-id="cabb7-114">-Body</span></span>
<span data-ttu-id="cabb7-115">A Felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="cabb7-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="cabb7-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cabb7-116">-Confirm</span></span>
<span data-ttu-id="cabb7-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cabb7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cabb7-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cabb7-118">-ContainerName</span></span>
<span data-ttu-id="cabb7-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="cabb7-119">Container name.</span></span>

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

### <span data-ttu-id="cabb7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cabb7-120">-DatabaseName</span></span>
<span data-ttu-id="cabb7-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="cabb7-121">Database name.</span></span>

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

### <span data-ttu-id="cabb7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cabb7-122">-DefaultProfile</span></span>
<span data-ttu-id="cabb7-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cabb7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cabb7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cabb7-124">-Name</span></span>
<span data-ttu-id="cabb7-125">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="cabb7-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="cabb7-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="cabb7-126">-ParentObject</span></span>
<span data-ttu-id="cabb7-127">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="cabb7-127">Sql Container object.</span></span>

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

### <span data-ttu-id="cabb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cabb7-128">-ResourceGroupName</span></span>
<span data-ttu-id="cabb7-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cabb7-129">Name of resource group.</span></span>

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

### <span data-ttu-id="cabb7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cabb7-130">-WhatIf</span></span>
<span data-ttu-id="cabb7-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cabb7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cabb7-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cabb7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cabb7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cabb7-133">CommonParameters</span></span>
<span data-ttu-id="cabb7-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cabb7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cabb7-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cabb7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cabb7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cabb7-136">INPUTS</span></span>

### <span data-ttu-id="cabb7-137">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="cabb7-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="cabb7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cabb7-138">OUTPUTS</span></span>

### <span data-ttu-id="cabb7-139">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="cabb7-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="cabb7-140">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="cabb7-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="cabb7-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cabb7-141">NOTES</span></span>

## <span data-ttu-id="cabb7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cabb7-142">RELATED LINKS</span></span>
