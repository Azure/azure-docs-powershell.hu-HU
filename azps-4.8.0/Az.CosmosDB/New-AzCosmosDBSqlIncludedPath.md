---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlincludedpath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlIncludedPath.md
ms.openlocfilehash: 0def7fc552563f9b859fd6af7d07be5cd14cd001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024080"
---
# <span data-ttu-id="a7f94-101">New-AzCosmosDBSqlIncludedPath</span><span class="sxs-lookup"><span data-stu-id="a7f94-101">New-AzCosmosDBSqlIncludedPath</span></span>

## <span data-ttu-id="a7f94-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7f94-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f94-103">Új PSIncludedPath típusú objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="a7f94-103">Creates a new object of type PSIncludedPath.</span></span> <span data-ttu-id="a7f94-104">A set-AzCosmosDBSqlContainer paraméter értéke lehet.</span><span class="sxs-lookup"><span data-stu-id="a7f94-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="a7f94-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7f94-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlIncludedPath [-Path <String>] [-Index <PSIndexes[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7f94-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7f94-106">DESCRIPTION</span></span>
<span data-ttu-id="a7f94-107">Az SQL API IncludedPath megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="a7f94-107">Object corresponding to Sql API's IncludedPath.</span></span>

## <span data-ttu-id="a7f94-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a7f94-108">EXAMPLES</span></span>

### <span data-ttu-id="a7f94-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a7f94-109">Example 1</span></span>
```powershell
PS C:\> $index1 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash
$index2 = New-AzCosmosDBSqlIncludedPathIndex -DataType String -Precision -1 -Kind Hash

New-AzCosmosDBSqlIncludedPath -Path "/*" -Index $index1,$index2

Path Indexes
---- -------
/*   {Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes,Microsoft.Azure.Commands.CosmosDB.Models.PSIndexes}
```

## <span data-ttu-id="a7f94-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7f94-110">PARAMETERS</span></span>

### <span data-ttu-id="a7f94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f94-111">-DefaultProfile</span></span>
<span data-ttu-id="a7f94-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a7f94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f94-113">– Index</span><span class="sxs-lookup"><span data-stu-id="a7f94-113">-Index</span></span>
<span data-ttu-id="a7f94-114">Az útvonal indexelésének listája</span><span class="sxs-lookup"><span data-stu-id="a7f94-114">List of indexes for this path</span></span>

```yaml
Type: PSIndexes[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f94-115">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="a7f94-115">-Path</span></span>
<span data-ttu-id="a7f94-116">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="a7f94-116">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="a7f94-117">Az index elérési útja általában a root karakterrel kezdődik és a végződés a helyettesítő karakterrel (/Path/\*)</span><span class="sxs-lookup"><span data-stu-id="a7f94-117">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f94-118">CommonParameters</span></span>
<span data-ttu-id="a7f94-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7f94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f94-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a7f94-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f94-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f94-121">INPUTS</span></span>

### <span data-ttu-id="a7f94-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a7f94-122">None</span></span>

## <span data-ttu-id="a7f94-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7f94-123">OUTPUTS</span></span>

### <span data-ttu-id="a7f94-124">Microsoft. Azure. Command. CosmosDB. models. PSIncludedPath</span><span class="sxs-lookup"><span data-stu-id="a7f94-124">Microsoft.Azure.Commands.CosmosDB.Models.PSIncludedPath</span></span>

## <span data-ttu-id="a7f94-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7f94-125">NOTES</span></span>

## <span data-ttu-id="a7f94-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7f94-126">RELATED LINKS</span></span>
