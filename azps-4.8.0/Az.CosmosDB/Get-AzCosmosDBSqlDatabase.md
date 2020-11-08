---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184198"
---
# <span data-ttu-id="f95bb-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f95bb-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f95bb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f95bb-102">SYNOPSIS</span></span>
<span data-ttu-id="f95bb-103">Megkapja a CosmosDB SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="f95bb-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f95bb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f95bb-104">SYNTAX</span></span>

### <span data-ttu-id="f95bb-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f95bb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95bb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95bb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f95bb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f95bb-107">DESCRIPTION</span></span>
<span data-ttu-id="f95bb-108">A **Get-AzCosmosDBSqlDatabase parancsmag beolvassa** az adott ResourceGroupName tartozó összes meglévő CosmosDB-SQL-adatbázis listáját, és egy adott CosmosDB, ResourceGroupName, accountname, databasename és ContainerName egyetlen SQL-adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="f95bb-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="f95bb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f95bb-109">EXAMPLES</span></span>

### <span data-ttu-id="f95bb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f95bb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="f95bb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f95bb-111">PARAMETERS</span></span>

### <span data-ttu-id="f95bb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f95bb-112">-AccountName</span></span>
<span data-ttu-id="f95bb-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f95bb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f95bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95bb-114">-DefaultProfile</span></span>
<span data-ttu-id="f95bb-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f95bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f95bb-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f95bb-116">-Name</span></span>
<span data-ttu-id="f95bb-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f95bb-117">Database name.</span></span>

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

### <span data-ttu-id="f95bb-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f95bb-118">-ParentObject</span></span>
<span data-ttu-id="f95bb-119">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="f95bb-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f95bb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95bb-120">-ResourceGroupName</span></span>
<span data-ttu-id="f95bb-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f95bb-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f95bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95bb-122">CommonParameters</span></span>
<span data-ttu-id="f95bb-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f95bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95bb-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f95bb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95bb-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95bb-125">INPUTS</span></span>

### <span data-ttu-id="f95bb-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="f95bb-126">None</span></span>

## <span data-ttu-id="f95bb-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f95bb-127">OUTPUTS</span></span>

### <span data-ttu-id="f95bb-128">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f95bb-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f95bb-129">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f95bb-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f95bb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f95bb-130">NOTES</span></span>

## <span data-ttu-id="f95bb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f95bb-131">RELATED LINKS</span></span>
