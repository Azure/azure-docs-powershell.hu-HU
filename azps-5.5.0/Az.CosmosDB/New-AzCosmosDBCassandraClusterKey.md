---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144531"
---
# <span data-ttu-id="181ae-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="181ae-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="181ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="181ae-102">SYNOPSIS</span></span>
<span data-ttu-id="181ae-103">Létrehoz egy új FogasDB fürtkulcsot.</span><span class="sxs-lookup"><span data-stu-id="181ae-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="181ae-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="181ae-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="181ae-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="181ae-105">DESCRIPTION</span></span>
<span data-ttu-id="181ae-106">A **New-AzCosmosDBCassandraClusterKey létrehoz** egy új Tárolódátlag-fürtkulcsot.</span><span class="sxs-lookup"><span data-stu-id="181ae-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="181ae-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="181ae-107">EXAMPLES</span></span>

### <span data-ttu-id="181ae-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="181ae-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="181ae-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="181ae-109">PARAMETERS</span></span>

### <span data-ttu-id="181ae-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181ae-110">-DefaultProfile</span></span>
<span data-ttu-id="181ae-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="181ae-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181ae-112">-Name</span><span class="sxs-lookup"><span data-stu-id="181ae-112">-Name</span></span>
<span data-ttu-id="181ae-113">A Fürtandra-fürtkulcs neve.</span><span class="sxs-lookup"><span data-stu-id="181ae-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="181ae-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="181ae-114">-OrderBy</span></span>
<span data-ttu-id="181ae-115">A Fürtandra-fürtkulcs megrendelése.</span><span class="sxs-lookup"><span data-stu-id="181ae-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="181ae-116">Lehetséges értékek: "Asc", "Desc"</span><span class="sxs-lookup"><span data-stu-id="181ae-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="181ae-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181ae-117">CommonParameters</span></span>
<span data-ttu-id="181ae-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="181ae-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181ae-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="181ae-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181ae-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="181ae-120">INPUTS</span></span>

### <span data-ttu-id="181ae-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="181ae-121">None</span></span>

## <span data-ttu-id="181ae-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="181ae-122">OUTPUTS</span></span>

### <span data-ttu-id="181ae-123">Microsoft.Azure.Commands.CossDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="181ae-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="181ae-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="181ae-124">NOTES</span></span>

## <span data-ttu-id="181ae-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="181ae-125">RELATED LINKS</span></span>
