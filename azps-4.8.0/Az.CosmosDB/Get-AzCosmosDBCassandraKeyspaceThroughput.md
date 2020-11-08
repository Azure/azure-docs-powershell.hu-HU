---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182394"
---
# <span data-ttu-id="d814f-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="d814f-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="d814f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d814f-102">SYNOPSIS</span></span>
<span data-ttu-id="d814f-103">Beolvassa a Cassandra szóköz átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="d814f-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="d814f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d814f-104">SYNTAX</span></span>

### <span data-ttu-id="d814f-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d814f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d814f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d814f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d814f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d814f-107">DESCRIPTION</span></span>
<span data-ttu-id="d814f-108">A **Get-AzCosmosDBCassandraKeyspaceThroughput** parancsmag az adott térköznek megfelelő átviteli objektumot kapja.</span><span class="sxs-lookup"><span data-stu-id="d814f-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="d814f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d814f-109">EXAMPLES</span></span>

### <span data-ttu-id="d814f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d814f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="d814f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d814f-111">PARAMETERS</span></span>

### <span data-ttu-id="d814f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d814f-112">-AccountName</span></span>
<span data-ttu-id="d814f-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d814f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d814f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d814f-114">-DefaultProfile</span></span>
<span data-ttu-id="d814f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d814f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d814f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d814f-116">-InputObject</span></span>
<span data-ttu-id="d814f-117">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d814f-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d814f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d814f-118">-Name</span></span>
<span data-ttu-id="d814f-119">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="d814f-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="d814f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d814f-120">-ResourceGroupName</span></span>
<span data-ttu-id="d814f-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d814f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="d814f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d814f-122">CommonParameters</span></span>
<span data-ttu-id="d814f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d814f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d814f-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d814f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d814f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d814f-125">INPUTS</span></span>

### <span data-ttu-id="d814f-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d814f-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d814f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d814f-127">OUTPUTS</span></span>

### <span data-ttu-id="d814f-128">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d814f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d814f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d814f-129">NOTES</span></span>

## <span data-ttu-id="d814f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d814f-130">RELATED LINKS</span></span>
