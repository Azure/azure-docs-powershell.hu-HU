---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184614"
---
# <span data-ttu-id="bfbd3-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="bfbd3-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="bfbd3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bfbd3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfbd3-103">Új CosmosDB SQL-UserDefinedFunction hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="bfbd3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bfbd3-104">SYNTAX</span></span>

### <span data-ttu-id="bfbd3-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bfbd3-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfbd3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfbd3-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfbd3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bfbd3-107">DESCRIPTION</span></span>
<span data-ttu-id="bfbd3-108">Új CosmosDB SQL-UserDefinedFunction hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="bfbd3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bfbd3-109">EXAMPLES</span></span>

### <span data-ttu-id="bfbd3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bfbd3-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="bfbd3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bfbd3-111">PARAMETERS</span></span>

### <span data-ttu-id="bfbd3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bfbd3-112">-AccountName</span></span>
<span data-ttu-id="bfbd3-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bfbd3-114">-Body</span><span class="sxs-lookup"><span data-stu-id="bfbd3-114">-Body</span></span>
<span data-ttu-id="bfbd3-115">A felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="bfbd3-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bfbd3-116">-Confirm</span></span>
<span data-ttu-id="bfbd3-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfbd3-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bfbd3-118">-ContainerName</span></span>
<span data-ttu-id="bfbd3-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-119">Container name.</span></span>

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

### <span data-ttu-id="bfbd3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bfbd3-120">-DatabaseName</span></span>
<span data-ttu-id="bfbd3-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-121">Database name.</span></span>

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

### <span data-ttu-id="bfbd3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfbd3-122">-DefaultProfile</span></span>
<span data-ttu-id="bfbd3-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfbd3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bfbd3-124">-Name</span></span>
<span data-ttu-id="bfbd3-125">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="bfbd3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bfbd3-126">-ParentObject</span></span>
<span data-ttu-id="bfbd3-127">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-127">Sql Container object.</span></span>

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

### <span data-ttu-id="bfbd3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfbd3-128">-ResourceGroupName</span></span>
<span data-ttu-id="bfbd3-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="bfbd3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfbd3-130">-WhatIf</span></span>
<span data-ttu-id="bfbd3-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfbd3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfbd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfbd3-133">CommonParameters</span></span>
<span data-ttu-id="bfbd3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bfbd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfbd3-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bfbd3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfbd3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfbd3-136">INPUTS</span></span>

### <span data-ttu-id="bfbd3-137">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bfbd3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="bfbd3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bfbd3-138">OUTPUTS</span></span>

### <span data-ttu-id="bfbd3-139">Microsoft. Azure. Command. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bfbd3-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="bfbd3-140">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="bfbd3-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="bfbd3-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bfbd3-141">NOTES</span></span>

## <span data-ttu-id="bfbd3-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bfbd3-142">RELATED LINKS</span></span>
