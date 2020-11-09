---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299471"
---
# <span data-ttu-id="dfc84-101">Get-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="dfc84-101">Get-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="dfc84-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfc84-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc84-103">Megkapja a CosmosDB SQL-felhasználó által definiált függvényt.</span><span class="sxs-lookup"><span data-stu-id="dfc84-103">Gets the CosmosDB Sql User Defined Function.</span></span>

## <span data-ttu-id="dfc84-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfc84-104">SYNTAX</span></span>

### <span data-ttu-id="dfc84-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfc84-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfc84-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfc84-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfc84-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfc84-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc84-108">A **Get-AzCosmosDBSqlUserDefinedFunction** parancsmag minden létező SQL-UserDefinedFunctions-CosmosDB megjelenik egy adott ResourceGroupName, accountname, databasename és ContainerName, és egy CosmosDB-UserDefinedFunction, ResourceGroupName, accountname, databasename, ContainerName, UserDefinedFunctionName és.</span><span class="sxs-lookup"><span data-stu-id="dfc84-108">The **Get-AzCosmosDBSqlUserDefinedFunction** cmdlet gets the list of all existing CosmosDB Sql UserDefinedFunctions for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql UserDefinedFunction for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and UserDefinedFunctionName.</span></span>

## <span data-ttu-id="dfc84-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dfc84-109">EXAMPLES</span></span>

### <span data-ttu-id="dfc84-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfc84-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## <span data-ttu-id="dfc84-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfc84-111">PARAMETERS</span></span>

### <span data-ttu-id="dfc84-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dfc84-112">-AccountName</span></span>
<span data-ttu-id="dfc84-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="dfc84-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dfc84-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dfc84-114">-ContainerName</span></span>
<span data-ttu-id="dfc84-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="dfc84-115">Container name.</span></span>

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

### <span data-ttu-id="dfc84-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dfc84-116">-DatabaseName</span></span>
<span data-ttu-id="dfc84-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="dfc84-117">Database name.</span></span>

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

### <span data-ttu-id="dfc84-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc84-118">-DefaultProfile</span></span>
<span data-ttu-id="dfc84-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfc84-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfc84-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfc84-120">-Name</span></span>
<span data-ttu-id="dfc84-121">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="dfc84-121">User Defined Function Name.</span></span>

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

### <span data-ttu-id="dfc84-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dfc84-122">-ParentObject</span></span>
<span data-ttu-id="dfc84-123">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="dfc84-123">Sql Container object.</span></span>

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

### <span data-ttu-id="dfc84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc84-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfc84-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dfc84-125">Name of resource group.</span></span>

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

### <span data-ttu-id="dfc84-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc84-126">CommonParameters</span></span>
<span data-ttu-id="dfc84-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfc84-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc84-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dfc84-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc84-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfc84-129">INPUTS</span></span>

### <span data-ttu-id="dfc84-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="dfc84-130">None</span></span>

## <span data-ttu-id="dfc84-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfc84-131">OUTPUTS</span></span>

### <span data-ttu-id="dfc84-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="dfc84-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="dfc84-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfc84-133">NOTES</span></span>

## <span data-ttu-id="dfc84-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfc84-134">RELATED LINKS</span></span>
