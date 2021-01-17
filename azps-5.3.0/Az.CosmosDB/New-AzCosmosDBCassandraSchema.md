---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477465"
---
# <span data-ttu-id="b540c-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="b540c-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="b540c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b540c-102">SYNOPSIS</span></span>
<span data-ttu-id="b540c-103">Létrehoz egy új TárolóDB sablont.</span><span class="sxs-lookup"><span data-stu-id="b540c-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="b540c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b540c-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b540c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b540c-105">DESCRIPTION</span></span>
<span data-ttu-id="b540c-106">A **New-AzCosmosDBCassandraSchema** létrehoz egy új TárolóDB-séma.</span><span class="sxs-lookup"><span data-stu-id="b540c-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="b540c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b540c-107">EXAMPLES</span></span>

### <span data-ttu-id="b540c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b540c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="b540c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b540c-109">PARAMETERS</span></span>

### <span data-ttu-id="b540c-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="b540c-110">-ClusterKey</span></span>
<span data-ttu-id="b540c-111">PSClusterKey-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b540c-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="b540c-112">-Column</span><span class="sxs-lookup"><span data-stu-id="b540c-112">-Column</span></span>
<span data-ttu-id="b540c-113">PSColumn objektum.</span><span class="sxs-lookup"><span data-stu-id="b540c-113">PSColumn object.</span></span>

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

### <span data-ttu-id="b540c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b540c-114">-DefaultProfile</span></span>
<span data-ttu-id="b540c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b540c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b540c-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="b540c-116">-PartitionKey</span></span>
<span data-ttu-id="b540c-117">Partitionkulcsokat tartalmazó karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b540c-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="b540c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b540c-118">CommonParameters</span></span>
<span data-ttu-id="b540c-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b540c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b540c-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b540c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b540c-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b540c-121">INPUTS</span></span>

### <span data-ttu-id="b540c-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="b540c-122">None</span></span>

## <span data-ttu-id="b540c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b540c-123">OUTPUTS</span></span>

### <span data-ttu-id="b540c-124">Microsoft.Azure.Commands.IssDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="b540c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="b540c-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b540c-125">NOTES</span></span>

## <span data-ttu-id="b540c-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b540c-126">RELATED LINKS</span></span>
