---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299564"
---
# <span data-ttu-id="b2798-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="b2798-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="b2798-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2798-102">SYNOPSIS</span></span>
<span data-ttu-id="b2798-103">Beolvassa a Cassandra szóköz átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="b2798-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="b2798-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2798-104">SYNTAX</span></span>

### <span data-ttu-id="b2798-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2798-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2798-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2798-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2798-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2798-107">DESCRIPTION</span></span>
<span data-ttu-id="b2798-108">A **Get-AzCosmosDBCassandraKeyspaceThroughput** parancsmag az adott térköznek megfelelő átviteli objektumot kapja.</span><span class="sxs-lookup"><span data-stu-id="b2798-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="b2798-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2798-109">EXAMPLES</span></span>

### <span data-ttu-id="b2798-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b2798-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="b2798-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2798-111">PARAMETERS</span></span>

### <span data-ttu-id="b2798-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2798-112">-AccountName</span></span>
<span data-ttu-id="b2798-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="b2798-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b2798-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2798-114">-DefaultProfile</span></span>
<span data-ttu-id="b2798-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2798-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2798-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2798-116">-InputObject</span></span>
<span data-ttu-id="b2798-117">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="b2798-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b2798-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2798-118">-Name</span></span>
<span data-ttu-id="b2798-119">Üres hely neve.</span><span class="sxs-lookup"><span data-stu-id="b2798-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="b2798-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2798-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2798-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b2798-121">Name of resource group.</span></span>

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

### <span data-ttu-id="b2798-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2798-122">CommonParameters</span></span>
<span data-ttu-id="b2798-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2798-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2798-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2798-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2798-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2798-125">INPUTS</span></span>

### <span data-ttu-id="b2798-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b2798-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b2798-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2798-127">OUTPUTS</span></span>

### <span data-ttu-id="b2798-128">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b2798-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b2798-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2798-129">NOTES</span></span>

## <span data-ttu-id="b2798-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2798-130">RELATED LINKS</span></span>
