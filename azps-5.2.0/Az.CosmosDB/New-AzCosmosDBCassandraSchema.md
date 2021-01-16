---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368463"
---
# <span data-ttu-id="b3187-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="b3187-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="b3187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3187-102">SYNOPSIS</span></span>
<span data-ttu-id="b3187-103">Létrehoz egy új TárolóDB sablont.</span><span class="sxs-lookup"><span data-stu-id="b3187-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="b3187-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3187-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3187-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3187-105">DESCRIPTION</span></span>
<span data-ttu-id="b3187-106">A **New-AzCosmosDBCassandraSchema** létrehoz egy új TárolóDB-séma.</span><span class="sxs-lookup"><span data-stu-id="b3187-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="b3187-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3187-107">EXAMPLES</span></span>

### <span data-ttu-id="b3187-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3187-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="b3187-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3187-109">PARAMETERS</span></span>

### <span data-ttu-id="b3187-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="b3187-110">-ClusterKey</span></span>
<span data-ttu-id="b3187-111">PSClusterKey-objektumok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b3187-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="b3187-112">-Column</span><span class="sxs-lookup"><span data-stu-id="b3187-112">-Column</span></span>
<span data-ttu-id="b3187-113">PSColumn objektum.</span><span class="sxs-lookup"><span data-stu-id="b3187-113">PSColumn object.</span></span>

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

### <span data-ttu-id="b3187-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3187-114">-DefaultProfile</span></span>
<span data-ttu-id="b3187-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3187-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3187-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="b3187-116">-PartitionKey</span></span>
<span data-ttu-id="b3187-117">Partitionkulcsokat tartalmazó karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="b3187-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="b3187-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3187-118">CommonParameters</span></span>
<span data-ttu-id="b3187-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3187-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3187-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3187-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3187-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3187-121">INPUTS</span></span>

### <span data-ttu-id="b3187-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3187-122">None</span></span>

## <span data-ttu-id="b3187-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3187-123">OUTPUTS</span></span>

### <span data-ttu-id="b3187-124">Microsoft.Azure.Commands.IssDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="b3187-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="b3187-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3187-125">NOTES</span></span>

## <span data-ttu-id="b3187-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3187-126">RELATED LINKS</span></span>
