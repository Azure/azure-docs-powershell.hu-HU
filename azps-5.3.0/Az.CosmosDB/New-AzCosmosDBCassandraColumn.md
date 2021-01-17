---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477466"
---
# <span data-ttu-id="9fa65-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="9fa65-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="9fa65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa65-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa65-103">Létrehoz egy új MellőDB oszlopot.</span><span class="sxs-lookup"><span data-stu-id="9fa65-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="9fa65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fa65-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa65-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fa65-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa65-106">Az **Új-AzCosmosDBCassandraColumn létrehoz** egy új Tárolódátum oszlopot.</span><span class="sxs-lookup"><span data-stu-id="9fa65-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="9fa65-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fa65-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa65-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9fa65-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="9fa65-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fa65-109">PARAMETERS</span></span>

### <span data-ttu-id="9fa65-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa65-110">-DefaultProfile</span></span>
<span data-ttu-id="9fa65-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fa65-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fa65-112">-Name</span><span class="sxs-lookup"><span data-stu-id="9fa65-112">-Name</span></span>
<span data-ttu-id="9fa65-113">A Mintára oszlop neve.</span><span class="sxs-lookup"><span data-stu-id="9fa65-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="9fa65-114">-Type</span><span class="sxs-lookup"><span data-stu-id="9fa65-114">-Type</span></span>
<span data-ttu-id="9fa65-115">A Mintás oszlop típusa.</span><span class="sxs-lookup"><span data-stu-id="9fa65-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="9fa65-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa65-116">CommonParameters</span></span>
<span data-ttu-id="9fa65-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fa65-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa65-118">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fa65-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa65-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fa65-119">INPUTS</span></span>

### <span data-ttu-id="9fa65-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="9fa65-120">None</span></span>

## <span data-ttu-id="9fa65-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fa65-121">OUTPUTS</span></span>

### <span data-ttu-id="9fa65-122">Microsoft.Azure.Commands.EzresDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="9fa65-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="9fa65-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fa65-123">NOTES</span></span>

## <span data-ttu-id="9fa65-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fa65-124">RELATED LINKS</span></span>
