---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184209"
---
# <span data-ttu-id="9dcf6-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="9dcf6-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="9dcf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dcf6-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcf6-103">Megkapja a CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="9dcf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dcf6-104">SYNTAX</span></span>

### <span data-ttu-id="9dcf6-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9dcf6-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="9dcf6-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dcf6-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dcf6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dcf6-107">DESCRIPTION</span></span>
<span data-ttu-id="9dcf6-108">A **Get-AzCosmosDBSqlContainer** parancsmag az adott ResourceGroupName, accountname és databasename minden meglévő CosmosDB SQL-tárolójának listáját kapja, és egy adott CosmosDB, ResourceGroupName, accountname, databasename és ContainerName egyetlen SQL-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="9dcf6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9dcf6-109">EXAMPLES</span></span>

### <span data-ttu-id="9dcf6-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9dcf6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="9dcf6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dcf6-111">PARAMETERS</span></span>

### <span data-ttu-id="9dcf6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9dcf6-112">-AccountName</span></span>
<span data-ttu-id="9dcf6-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9dcf6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dcf6-114">-DatabaseName</span></span>
<span data-ttu-id="9dcf6-115">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-115">Database name.</span></span>

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

### <span data-ttu-id="9dcf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dcf6-116">-DefaultProfile</span></span>
<span data-ttu-id="9dcf6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dcf6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dcf6-118">-Name</span></span>
<span data-ttu-id="9dcf6-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-119">Container name.</span></span>

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

### <span data-ttu-id="9dcf6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9dcf6-120">-ParentObject</span></span>
<span data-ttu-id="9dcf6-121">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-121">Sql Database object.</span></span>

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

### <span data-ttu-id="9dcf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dcf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="9dcf6-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-123">Name of resource group.</span></span>

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

### <span data-ttu-id="9dcf6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dcf6-124">CommonParameters</span></span>
<span data-ttu-id="9dcf6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dcf6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dcf6-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9dcf6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dcf6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dcf6-127">INPUTS</span></span>

### <span data-ttu-id="9dcf6-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="9dcf6-128">None</span></span>

## <span data-ttu-id="9dcf6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dcf6-129">OUTPUTS</span></span>

### <span data-ttu-id="9dcf6-130">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="9dcf6-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="9dcf6-131">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="9dcf6-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="9dcf6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dcf6-132">NOTES</span></span>

## <span data-ttu-id="9dcf6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dcf6-133">RELATED LINKS</span></span>
