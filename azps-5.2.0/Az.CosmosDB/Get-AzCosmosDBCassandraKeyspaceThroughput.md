---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367301"
---
# <span data-ttu-id="43b30-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="43b30-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="43b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43b30-102">SYNOPSIS</span></span>
<span data-ttu-id="43b30-103">A Mintára billentyűtér átviteli sebességét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43b30-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="43b30-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43b30-104">SYNTAX</span></span>

### <span data-ttu-id="43b30-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43b30-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43b30-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43b30-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b30-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43b30-107">DESCRIPTION</span></span>
<span data-ttu-id="43b30-108">A **Get-AzCosmosDBCassandraKeyspaceThroughput** parancsmag az adott Keyspace-nek megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="43b30-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="43b30-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43b30-109">EXAMPLES</span></span>

### <span data-ttu-id="43b30-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="43b30-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="43b30-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43b30-111">PARAMETERS</span></span>

### <span data-ttu-id="43b30-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="43b30-112">-AccountName</span></span>
<span data-ttu-id="43b30-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="43b30-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="43b30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b30-114">-DefaultProfile</span></span>
<span data-ttu-id="43b30-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43b30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43b30-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43b30-116">-InputObject</span></span>
<span data-ttu-id="43b30-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="43b30-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="43b30-118">-Name</span><span class="sxs-lookup"><span data-stu-id="43b30-118">-Name</span></span>
<span data-ttu-id="43b30-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="43b30-119">Cassandra Keyspace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43b30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b30-120">-ResourceGroupName</span></span>
<span data-ttu-id="43b30-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43b30-121">Name of resource group.</span></span>

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

### <span data-ttu-id="43b30-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b30-122">CommonParameters</span></span>
<span data-ttu-id="43b30-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b30-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b30-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43b30-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b30-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43b30-125">INPUTS</span></span>

### <span data-ttu-id="43b30-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="43b30-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="43b30-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43b30-127">OUTPUTS</span></span>

### <span data-ttu-id="43b30-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="43b30-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="43b30-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43b30-129">NOTES</span></span>

## <span data-ttu-id="43b30-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43b30-130">RELATED LINKS</span></span>
