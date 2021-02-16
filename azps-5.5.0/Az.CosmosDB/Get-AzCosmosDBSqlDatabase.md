---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166243"
---
# <span data-ttu-id="60824-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="60824-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="60824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60824-102">SYNOPSIS</span></span>
<span data-ttu-id="60824-103">Beveszi a 2010-es sqladatbázist.</span><span class="sxs-lookup"><span data-stu-id="60824-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="60824-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60824-104">SYNTAX</span></span>

### <span data-ttu-id="60824-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60824-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60824-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60824-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60824-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60824-107">DESCRIPTION</span></span>
<span data-ttu-id="60824-108">A **Get-AzCosmosDBSqlDatabase** parancsmag egy adott ResourceGroupName, AccountName és Egy Adott ResourceGroupName, AccountName és DatabaseName típusú Erőforráscsoportnév, AccountName és ContainerName esetén az összes meglévő Naplódb Sql-adatbázis listáját lekérte.</span><span class="sxs-lookup"><span data-stu-id="60824-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="60824-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60824-109">EXAMPLES</span></span>

### <span data-ttu-id="60824-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="60824-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="60824-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60824-111">PARAMETERS</span></span>

### <span data-ttu-id="60824-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="60824-112">-AccountName</span></span>
<span data-ttu-id="60824-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="60824-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="60824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60824-114">-DefaultProfile</span></span>
<span data-ttu-id="60824-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60824-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60824-116">-Name</span><span class="sxs-lookup"><span data-stu-id="60824-116">-Name</span></span>
<span data-ttu-id="60824-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="60824-117">Database name.</span></span>

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

### <span data-ttu-id="60824-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="60824-118">-ParentObject</span></span>
<span data-ttu-id="60824-119">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="60824-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="60824-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60824-120">-ResourceGroupName</span></span>
<span data-ttu-id="60824-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="60824-121">Name of resource group.</span></span>

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

### <span data-ttu-id="60824-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60824-122">CommonParameters</span></span>
<span data-ttu-id="60824-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60824-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60824-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60824-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60824-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60824-125">INPUTS</span></span>

### <span data-ttu-id="60824-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="60824-126">None</span></span>

## <span data-ttu-id="60824-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60824-127">OUTPUTS</span></span>

### <span data-ttu-id="60824-128">Microsoft.Azure.Commands.CossDB.Models.PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="60824-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="60824-129">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="60824-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="60824-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60824-130">NOTES</span></span>

## <span data-ttu-id="60824-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60824-131">RELATED LINKS</span></span>
