---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845146"
---
# <span data-ttu-id="efdbf-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="efdbf-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="efdbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="efdbf-103">Új CosmosDB Cassandra cluster billentyűt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="efdbf-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="efdbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efdbf-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efdbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="efdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="efdbf-106">A **New-AzCosmosDBCassandraClusterKey** létrehoz egy új CosmosDB Cassandra cluster kulcsot.</span><span class="sxs-lookup"><span data-stu-id="efdbf-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="efdbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="efdbf-107">EXAMPLES</span></span>

### <span data-ttu-id="efdbf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="efdbf-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="efdbf-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efdbf-109">PARAMETERS</span></span>

### <span data-ttu-id="efdbf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdbf-110">-DefaultProfile</span></span>
<span data-ttu-id="efdbf-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efdbf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efdbf-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="efdbf-112">-Name</span></span>
<span data-ttu-id="efdbf-113">A cluster kulcs neve.</span><span class="sxs-lookup"><span data-stu-id="efdbf-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="efdbf-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="efdbf-114">-OrderBy</span></span>
<span data-ttu-id="efdbf-115">A cluster kulcs elrendelése.</span><span class="sxs-lookup"><span data-stu-id="efdbf-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="efdbf-116">A lehetséges értékek a következők: "ASC", "desc"</span><span class="sxs-lookup"><span data-stu-id="efdbf-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="efdbf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdbf-117">CommonParameters</span></span>
<span data-ttu-id="efdbf-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efdbf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdbf-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="efdbf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdbf-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efdbf-120">INPUTS</span></span>

### <span data-ttu-id="efdbf-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="efdbf-121">None</span></span>

## <span data-ttu-id="efdbf-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efdbf-122">OUTPUTS</span></span>

### <span data-ttu-id="efdbf-123">Microsoft. Azure. Command. CosmosDB. models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="efdbf-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="efdbf-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efdbf-124">NOTES</span></span>

## <span data-ttu-id="efdbf-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efdbf-125">RELATED LINKS</span></span>
