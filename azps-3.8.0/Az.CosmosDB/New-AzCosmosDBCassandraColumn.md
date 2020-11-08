---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012090"
---
# <span data-ttu-id="e4b05-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="e4b05-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="e4b05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4b05-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b05-103">Új CosmosDB Cassandra oszlopot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4b05-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="e4b05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4b05-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4b05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4b05-105">DESCRIPTION</span></span>
<span data-ttu-id="e4b05-106">A **New-AzCosmosDBCassandraColumn** létrehoz egy új CosmosDB Cassandra oszlopot.</span><span class="sxs-lookup"><span data-stu-id="e4b05-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="e4b05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4b05-107">EXAMPLES</span></span>

### <span data-ttu-id="e4b05-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e4b05-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="e4b05-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4b05-109">PARAMETERS</span></span>

### <span data-ttu-id="e4b05-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b05-110">-DefaultProfile</span></span>
<span data-ttu-id="e4b05-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4b05-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4b05-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4b05-112">-Name</span></span>
<span data-ttu-id="e4b05-113">A Cassandra oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="e4b05-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="e4b05-114">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="e4b05-114">-Type</span></span>
<span data-ttu-id="e4b05-115">A Cassandra oszlop típusa.</span><span class="sxs-lookup"><span data-stu-id="e4b05-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="e4b05-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b05-116">CommonParameters</span></span>
<span data-ttu-id="e4b05-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4b05-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b05-118">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e4b05-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b05-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b05-119">INPUTS</span></span>

### <span data-ttu-id="e4b05-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4b05-120">None</span></span>

## <span data-ttu-id="e4b05-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4b05-121">OUTPUTS</span></span>

### <span data-ttu-id="e4b05-122">Microsoft. Azure. Command. CosmosDB. models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="e4b05-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="e4b05-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4b05-123">NOTES</span></span>

## <span data-ttu-id="e4b05-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4b05-124">RELATED LINKS</span></span>
