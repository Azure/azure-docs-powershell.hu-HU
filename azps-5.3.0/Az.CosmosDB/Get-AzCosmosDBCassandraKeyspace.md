---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 30e550ae8670547e6f87ed022053bcbef7927867
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480620"
---
# <span data-ttu-id="5a618-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="5a618-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="5a618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a618-102">SYNOPSIS</span></span>
<span data-ttu-id="5a618-103">2016.01.012.011.010-es kulcsteret kap.</span><span class="sxs-lookup"><span data-stu-id="5a618-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5a618-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a618-104">SYNTAX</span></span>

### <span data-ttu-id="5a618-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a618-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a618-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a618-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a618-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a618-107">DESCRIPTION</span></span>
<span data-ttu-id="5a618-108">A **Get-AzCosmosDBCassandraKeyspace** parancsmag létrehoz egy újat, vagy frissíti a már meglévő, a 2010-es És a 36555555566655444444445500000000000000000000 cmdletet.</span><span class="sxs-lookup"><span data-stu-id="5a618-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="5a618-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a618-109">EXAMPLES</span></span>

### <span data-ttu-id="5a618-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5a618-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="5a618-111">Get-AzCosmosDBCassandraKeyspace a meglévő 1000770000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="5a618-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="5a618-112">Bontsa ki az Erőforrást a _etag, _ts, _rid tulajdonságok be _rid.</span><span class="sxs-lookup"><span data-stu-id="5a618-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="5a618-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a618-113">PARAMETERS</span></span>

### <span data-ttu-id="5a618-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5a618-114">-AccountName</span></span>
<span data-ttu-id="5a618-115">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="5a618-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a618-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a618-116">-DefaultProfile</span></span>
<span data-ttu-id="5a618-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a618-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a618-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5a618-118">-Name</span></span>
<span data-ttu-id="5a618-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="5a618-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="5a618-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5a618-120">-ParentObject</span></span>
<span data-ttu-id="5a618-121">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="5a618-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5a618-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a618-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a618-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a618-123">Name of resource group.</span></span>

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

### <span data-ttu-id="5a618-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a618-124">CommonParameters</span></span>
<span data-ttu-id="5a618-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a618-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a618-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a618-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a618-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a618-127">INPUTS</span></span>

### <span data-ttu-id="5a618-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5a618-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5a618-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a618-129">OUTPUTS</span></span>

### <span data-ttu-id="5a618-130">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="5a618-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="5a618-131">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5a618-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5a618-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a618-132">NOTES</span></span>

## <span data-ttu-id="5a618-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a618-133">RELATED LINKS</span></span>
