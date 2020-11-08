---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025462"
---
# <span data-ttu-id="f2f8b-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f2f8b-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="f2f8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f8b-103">Új CosmosDB Cassandra-séma létrehozása.</span><span class="sxs-lookup"><span data-stu-id="f2f8b-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f2f8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2f8b-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f8b-106">A **New-AzCosmosDBCassandraSchema** létrehoz egy új CosmosDB Cassandra-sémát.</span><span class="sxs-lookup"><span data-stu-id="f2f8b-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f2f8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f2f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="f2f8b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f2f8b-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="f2f8b-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2f8b-109">PARAMETERS</span></span>

### <span data-ttu-id="f2f8b-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="f2f8b-110">-ClusterKey</span></span>
<span data-ttu-id="f2f8b-111">PSClusterKey-objektumok tömbje</span><span class="sxs-lookup"><span data-stu-id="f2f8b-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f8b-112">-Oszlop</span><span class="sxs-lookup"><span data-stu-id="f2f8b-112">-Column</span></span>
<span data-ttu-id="f2f8b-113">PSColumn objektum</span><span class="sxs-lookup"><span data-stu-id="f2f8b-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f8b-114">-DefaultProfile</span></span>
<span data-ttu-id="f2f8b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f2f8b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f8b-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="f2f8b-116">-PartitionKey</span></span>
<span data-ttu-id="f2f8b-117">A particionálási kulcsokat tartalmazó karakterláncok tömbje</span><span class="sxs-lookup"><span data-stu-id="f2f8b-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f8b-118">CommonParameters</span></span>
<span data-ttu-id="f2f8b-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2f8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f8b-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f2f8b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f8b-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2f8b-121">INPUTS</span></span>

### <span data-ttu-id="f2f8b-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="f2f8b-122">None</span></span>

## <span data-ttu-id="f2f8b-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2f8b-123">OUTPUTS</span></span>

### <span data-ttu-id="f2f8b-124">Microsoft. Azure. Command. CosmosDB. models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f2f8b-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="f2f8b-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2f8b-125">NOTES</span></span>

## <span data-ttu-id="f2f8b-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2f8b-126">RELATED LINKS</span></span>
