---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 0d422014d3cf2ca2ffa18b60c10b50b21bf91144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936249"
---
# <span data-ttu-id="433b0-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="433b0-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="433b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433b0-102">SYNOPSIS</span></span>
<span data-ttu-id="433b0-103">A 2010-es sql-felhasználó által definiált függvényt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="433b0-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="433b0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="433b0-104">SYNTAX</span></span>

### <span data-ttu-id="433b0-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="433b0-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433b0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="433b0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433b0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="433b0-107">DESCRIPTION</span></span>
<span data-ttu-id="433b0-108">A **Get-AzCosmosDBSqlUserDefinedFunction** parancsmag lekérte az adott ResourceGroupName, AccountName, DatabaseName és ContainerName rekordhoz az összes meglévő Sql UserDefinedFunctions listáját, és egy adott ResourceGroupName, AccountName, ContainerName és UserDefinedFunctionName fájlhoz egyetlen Sql UserDefinedFunction függvényt kap.</span><span class="sxs-lookup"><span data-stu-id="433b0-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="433b0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="433b0-109">EXAMPLES</span></span>

### <span data-ttu-id="433b0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="433b0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="433b0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433b0-111">PARAMETERS</span></span>

### <span data-ttu-id="433b0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="433b0-112">-AccountName</span></span>
<span data-ttu-id="433b0-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="433b0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="433b0-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="433b0-114">-ContainerName</span></span>
<span data-ttu-id="433b0-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="433b0-115">Container name.</span></span>

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

### <span data-ttu-id="433b0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="433b0-116">-DatabaseName</span></span>
<span data-ttu-id="433b0-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="433b0-117">Database name.</span></span>

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

### <span data-ttu-id="433b0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433b0-118">-DefaultProfile</span></span>
<span data-ttu-id="433b0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="433b0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433b0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="433b0-120">-Name</span></span>
<span data-ttu-id="433b0-121">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="433b0-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="433b0-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="433b0-122">-ParentObject</span></span>
<span data-ttu-id="433b0-123">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="433b0-123">Sql Container object.</span></span>

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

### <span data-ttu-id="433b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="433b0-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="433b0-125">Name of resource group.</span></span>

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

### <span data-ttu-id="433b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433b0-126">CommonParameters</span></span>
<span data-ttu-id="433b0-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433b0-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433b0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433b0-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="433b0-129">INPUTS</span></span>

### <span data-ttu-id="433b0-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="433b0-130">None</span></span>

## <span data-ttu-id="433b0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="433b0-131">OUTPUTS</span></span>

### <span data-ttu-id="433b0-132">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="433b0-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="433b0-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="433b0-133">NOTES</span></span>

## <span data-ttu-id="433b0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="433b0-134">RELATED LINKS</span></span>
