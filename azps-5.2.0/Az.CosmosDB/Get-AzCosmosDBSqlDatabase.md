---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333737"
---
# <span data-ttu-id="477db-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="477db-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="477db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477db-102">SYNOPSIS</span></span>
<span data-ttu-id="477db-103">Beveszi a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="477db-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="477db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="477db-104">SYNTAX</span></span>

### <span data-ttu-id="477db-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="477db-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477db-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="477db-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="477db-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="477db-107">DESCRIPTION</span></span>
<span data-ttu-id="477db-108">A **Get-AzCosmosDBSqlDatabase** parancsmag egy adott ResourceGroupName, AccountName és Egy adott ResourceGroupName, AccountName és Egy Adott ResourceGroupName, AccountName és ContainerName típusú ErőforrásCsoportNév, AccountName és ContainerName esetén az összes meglévő Táblát megkapja.</span><span class="sxs-lookup"><span data-stu-id="477db-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="477db-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="477db-109">EXAMPLES</span></span>

### <span data-ttu-id="477db-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="477db-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="477db-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="477db-111">PARAMETERS</span></span>

### <span data-ttu-id="477db-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="477db-112">-AccountName</span></span>
<span data-ttu-id="477db-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="477db-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="477db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477db-114">-DefaultProfile</span></span>
<span data-ttu-id="477db-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="477db-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477db-116">-Name</span><span class="sxs-lookup"><span data-stu-id="477db-116">-Name</span></span>
<span data-ttu-id="477db-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="477db-117">Database name.</span></span>

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

### <span data-ttu-id="477db-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="477db-118">-ParentObject</span></span>
<span data-ttu-id="477db-119">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="477db-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="477db-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477db-120">-ResourceGroupName</span></span>
<span data-ttu-id="477db-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="477db-121">Name of resource group.</span></span>

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

### <span data-ttu-id="477db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477db-122">CommonParameters</span></span>
<span data-ttu-id="477db-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="477db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477db-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="477db-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477db-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="477db-125">INPUTS</span></span>

### <span data-ttu-id="477db-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="477db-126">None</span></span>

## <span data-ttu-id="477db-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="477db-127">OUTPUTS</span></span>

### <span data-ttu-id="477db-128">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="477db-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="477db-129">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="477db-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="477db-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="477db-130">NOTES</span></span>

## <span data-ttu-id="477db-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="477db-131">RELATED LINKS</span></span>
