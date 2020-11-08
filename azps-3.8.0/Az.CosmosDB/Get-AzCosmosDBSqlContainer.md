---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014108"
---
# <span data-ttu-id="dc7fb-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="dc7fb-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="dc7fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7fb-103">Megkapja a CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="dc7fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc7fb-104">SYNTAX</span></span>

### <span data-ttu-id="dc7fb-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc7fb-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="dc7fb-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc7fb-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc7fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc7fb-107">DESCRIPTION</span></span>
<span data-ttu-id="dc7fb-108">A **Get-AzCosmosDBSqlContainer** parancsmag az adott ResourceGroupName, accountname és databasename minden meglévő CosmosDB SQL-tárolójának listáját kapja, és egy adott CosmosDB, ResourceGroupName, accountname, databasename és ContainerName egyetlen SQL-tárolót kap.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="dc7fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dc7fb-109">EXAMPLES</span></span>

### <span data-ttu-id="dc7fb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dc7fb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="dc7fb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc7fb-111">PARAMETERS</span></span>

### <span data-ttu-id="dc7fb-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dc7fb-112">-AccountName</span></span>
<span data-ttu-id="dc7fb-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dc7fb-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc7fb-114">-DatabaseName</span></span>
<span data-ttu-id="dc7fb-115">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-115">Database name.</span></span>

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

### <span data-ttu-id="dc7fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7fb-116">-DefaultProfile</span></span>
<span data-ttu-id="dc7fb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc7fb-118">– Részletes</span><span class="sxs-lookup"><span data-stu-id="dc7fb-118">-Detailed</span></span>
<span data-ttu-id="dc7fb-119">Ha meg van határozva, akkor a parancsmag a megadott átviteli értékkel rendelkező tárolót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc7fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc7fb-120">-InputObject</span></span>
<span data-ttu-id="dc7fb-121">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-121">Sql Database object.</span></span>

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

### <span data-ttu-id="dc7fb-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc7fb-122">-Name</span></span>
<span data-ttu-id="dc7fb-123">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-123">Container name.</span></span>

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

### <span data-ttu-id="dc7fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc7fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc7fb-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-125">Name of resource group.</span></span>

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

### <span data-ttu-id="dc7fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7fb-126">CommonParameters</span></span>
<span data-ttu-id="dc7fb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc7fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7fb-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc7fb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7fb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc7fb-129">INPUTS</span></span>

### <span data-ttu-id="dc7fb-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="dc7fb-130">None</span></span>

## <span data-ttu-id="dc7fb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc7fb-131">OUTPUTS</span></span>

### <span data-ttu-id="dc7fb-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="dc7fb-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="dc7fb-133">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="dc7fb-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="dc7fb-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc7fb-134">NOTES</span></span>

## <span data-ttu-id="dc7fb-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc7fb-135">RELATED LINKS</span></span>
