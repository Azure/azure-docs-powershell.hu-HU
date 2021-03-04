---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: fb387adafa1a1a71d9a42b09b8c7255955eccd9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931986"
---
# <span data-ttu-id="99d68-101">Get-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="99d68-101">Get-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="99d68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99d68-102">SYNOPSIS</span></span>
<span data-ttu-id="99d68-103">A 2010-es évtől a 2010-es évtől a 2010-es évtől a 2016.</span><span class="sxs-lookup"><span data-stu-id="99d68-103">Gets a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="99d68-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="99d68-104">SYNTAX</span></span>

### <span data-ttu-id="99d68-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99d68-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspace -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d68-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99d68-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspace [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d68-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="99d68-107">DESCRIPTION</span></span>
<span data-ttu-id="99d68-108">A **Get-AzCosmosDBCassandraKeyspace** parancsmag létrehoz egy újat, vagy frissíti a már meglévő, a 2010-es És a 36555555566655444444445500000000000000000000 cmdletet.</span><span class="sxs-lookup"><span data-stu-id="99d68-108">The **Get-AzCosmosDBCassandraKeyspace** cmdlet creates a new or updates an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="99d68-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="99d68-109">EXAMPLES</span></span>

### <span data-ttu-id="99d68-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="99d68-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}

Name    Id   Resource
{name}  {id} {resourceObject}
```

<span data-ttu-id="99d68-111">Get-AzCosmosDBCassandraKeyspace a meglévő 1000770000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="99d68-111">Get-AzCosmosDBCassandraKeyspace gets the properties of an existing CassandraKeyspace.</span></span> <span data-ttu-id="99d68-112">Bontsa ki az Erőforrást a _etag, _ts, _rid tulajdonságok be _rid.</span><span class="sxs-lookup"><span data-stu-id="99d68-112">You can expand the Resource to get the _etag, _ts, _rid properties.</span></span>

## <span data-ttu-id="99d68-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99d68-113">PARAMETERS</span></span>

### <span data-ttu-id="99d68-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="99d68-114">-AccountName</span></span>
<span data-ttu-id="99d68-115">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="99d68-115">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="99d68-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d68-116">-DefaultProfile</span></span>
<span data-ttu-id="99d68-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99d68-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99d68-118">-Name</span><span class="sxs-lookup"><span data-stu-id="99d68-118">-Name</span></span>
<span data-ttu-id="99d68-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="99d68-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="99d68-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="99d68-120">-ParentObject</span></span>
<span data-ttu-id="99d68-121">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="99d68-121">CosmosDB Account object</span></span>

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

### <span data-ttu-id="99d68-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d68-122">-ResourceGroupName</span></span>
<span data-ttu-id="99d68-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="99d68-123">Name of resource group.</span></span>

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

### <span data-ttu-id="99d68-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d68-124">CommonParameters</span></span>
<span data-ttu-id="99d68-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d68-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d68-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99d68-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d68-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99d68-127">INPUTS</span></span>

### <span data-ttu-id="99d68-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="99d68-128">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="99d68-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99d68-129">OUTPUTS</span></span>

### <span data-ttu-id="99d68-130">Microsoft.Azure.Commands.EzresDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="99d68-130">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

### <span data-ttu-id="99d68-131">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="99d68-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="99d68-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="99d68-132">NOTES</span></span>

## <span data-ttu-id="99d68-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99d68-133">RELATED LINKS</span></span>
