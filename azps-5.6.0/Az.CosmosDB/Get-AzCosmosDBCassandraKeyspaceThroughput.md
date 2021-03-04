---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 965e7b3d1f0775f3842e423e47c1a4cc60021408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934474"
---
# <span data-ttu-id="8ad69-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="8ad69-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="8ad69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad69-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad69-103">A Mintára billentyűtér átviteli sebességét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ad69-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="8ad69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ad69-104">SYNTAX</span></span>

### <span data-ttu-id="8ad69-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ad69-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ad69-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ad69-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ad69-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ad69-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad69-108">A **Get-AzCosmosDBCassandraKeyspaceThroughput** parancsmag az adott Keyspace-nek megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8ad69-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="8ad69-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ad69-109">EXAMPLES</span></span>

### <span data-ttu-id="8ad69-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8ad69-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="8ad69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ad69-111">PARAMETERS</span></span>

### <span data-ttu-id="8ad69-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ad69-112">-AccountName</span></span>
<span data-ttu-id="8ad69-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="8ad69-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8ad69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad69-114">-DefaultProfile</span></span>
<span data-ttu-id="8ad69-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8ad69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad69-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ad69-116">-InputObject</span></span>
<span data-ttu-id="8ad69-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="8ad69-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8ad69-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad69-118">-Name</span></span>
<span data-ttu-id="8ad69-119">Yandra Keyspace Name.</span><span class="sxs-lookup"><span data-stu-id="8ad69-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="8ad69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad69-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ad69-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8ad69-121">Name of resource group.</span></span>

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

### <span data-ttu-id="8ad69-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad69-122">CommonParameters</span></span>
<span data-ttu-id="8ad69-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad69-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad69-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ad69-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad69-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad69-125">INPUTS</span></span>

### <span data-ttu-id="8ad69-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8ad69-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8ad69-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ad69-127">OUTPUTS</span></span>

### <span data-ttu-id="8ad69-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8ad69-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8ad69-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ad69-129">NOTES</span></span>

## <span data-ttu-id="8ad69-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ad69-130">RELATED LINKS</span></span>
