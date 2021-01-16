---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347141"
---
# <span data-ttu-id="7ed55-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="7ed55-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="7ed55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed55-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed55-103">Létrehoz egy új FogasDB fürtkulcsot.</span><span class="sxs-lookup"><span data-stu-id="7ed55-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="7ed55-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7ed55-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ed55-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7ed55-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed55-106">A **New-AzCosmosDBCassandraClusterKey létrehoz** egy új TárolóDB-fürtkulcsot.</span><span class="sxs-lookup"><span data-stu-id="7ed55-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="7ed55-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7ed55-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed55-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7ed55-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="7ed55-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ed55-109">PARAMETERS</span></span>

### <span data-ttu-id="7ed55-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed55-110">-DefaultProfile</span></span>
<span data-ttu-id="7ed55-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ed55-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed55-112">-Name</span><span class="sxs-lookup"><span data-stu-id="7ed55-112">-Name</span></span>
<span data-ttu-id="7ed55-113">A Fürtandra-fürtkulcs neve.</span><span class="sxs-lookup"><span data-stu-id="7ed55-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="7ed55-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7ed55-114">-OrderBy</span></span>
<span data-ttu-id="7ed55-115">A Fürtandra-fürtkulcs megrendelése.</span><span class="sxs-lookup"><span data-stu-id="7ed55-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="7ed55-116">Lehetséges értékek: "Asc", "Desc"</span><span class="sxs-lookup"><span data-stu-id="7ed55-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="7ed55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed55-117">CommonParameters</span></span>
<span data-ttu-id="7ed55-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed55-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed55-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed55-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed55-120">INPUTS</span></span>

### <span data-ttu-id="7ed55-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="7ed55-121">None</span></span>

## <span data-ttu-id="7ed55-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ed55-122">OUTPUTS</span></span>

### <span data-ttu-id="7ed55-123">Microsoft.Azure.Commands.CossDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="7ed55-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="7ed55-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7ed55-124">NOTES</span></span>

## <span data-ttu-id="7ed55-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ed55-125">RELATED LINKS</span></span>
