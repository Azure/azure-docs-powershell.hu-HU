---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480605"
---
# <span data-ttu-id="d25c4-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="d25c4-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="d25c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d25c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d25c4-103">A 2012-es sql tárolót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c4-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d25c4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d25c4-104">SYNTAX</span></span>

### <span data-ttu-id="d25c4-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d25c4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="d25c4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d25c4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d25c4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d25c4-107">DESCRIPTION</span></span>
<span data-ttu-id="d25c4-108">A **Get-AzCosmosDBSqlContainer** parancsmag lekérte az adott ResourceGroupName, AccountName és DatabaseName erőforráscsoport összes meglévő Tárolóját, és egy Adott ResourceGroupName, AccountName és ContainerName rekordhoz egyetlen Tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="d25c4-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="d25c4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d25c4-109">EXAMPLES</span></span>

### <span data-ttu-id="d25c4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="d25c4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="d25c4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d25c4-111">PARAMETERS</span></span>

### <span data-ttu-id="d25c4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d25c4-112">-AccountName</span></span>
<span data-ttu-id="d25c4-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d25c4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d25c4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d25c4-114">-DatabaseName</span></span>
<span data-ttu-id="d25c4-115">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d25c4-115">Database name.</span></span>

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

### <span data-ttu-id="d25c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25c4-116">-DefaultProfile</span></span>
<span data-ttu-id="d25c4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d25c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25c4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d25c4-118">-Name</span></span>
<span data-ttu-id="d25c4-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d25c4-119">Container name.</span></span>

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

### <span data-ttu-id="d25c4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d25c4-120">-ParentObject</span></span>
<span data-ttu-id="d25c4-121">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="d25c4-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d25c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="d25c4-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d25c4-123">Name of resource group.</span></span>

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

### <span data-ttu-id="d25c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25c4-124">CommonParameters</span></span>
<span data-ttu-id="d25c4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25c4-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d25c4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25c4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d25c4-127">INPUTS</span></span>

### <span data-ttu-id="d25c4-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="d25c4-128">None</span></span>

## <span data-ttu-id="d25c4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25c4-129">OUTPUTS</span></span>

### <span data-ttu-id="d25c4-130">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d25c4-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d25c4-131">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d25c4-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d25c4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d25c4-132">NOTES</span></span>

## <span data-ttu-id="d25c4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d25c4-133">RELATED LINKS</span></span>
