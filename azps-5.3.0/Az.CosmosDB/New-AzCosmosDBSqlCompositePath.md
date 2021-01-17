---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477425"
---
# <span data-ttu-id="158fa-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="158fa-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="158fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158fa-102">SYNOPSIS</span></span>
<span data-ttu-id="158fa-103">Létrehoz egy új, PSCompositePath típusú objektumot.</span><span class="sxs-lookup"><span data-stu-id="158fa-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="158fa-104">A Set-AzCosmosDBSqlContainer paraméterértékeként is át lehetadva.</span><span class="sxs-lookup"><span data-stu-id="158fa-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="158fa-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="158fa-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="158fa-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="158fa-106">DESCRIPTION</span></span>
<span data-ttu-id="158fa-107">Az Sql API CompositePath-jának megfelelő objektum.</span><span class="sxs-lookup"><span data-stu-id="158fa-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="158fa-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="158fa-108">EXAMPLES</span></span>

### <span data-ttu-id="158fa-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="158fa-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="158fa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="158fa-110">PARAMETERS</span></span>

### <span data-ttu-id="158fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158fa-111">-DefaultProfile</span></span>
<span data-ttu-id="158fa-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="158fa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158fa-113">-Order</span><span class="sxs-lookup"><span data-stu-id="158fa-113">-Order</span></span>
<span data-ttu-id="158fa-114">Összetett elérési utak rendezési sorrendjét állítja be vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="158fa-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="158fa-115">Lehetséges értékek: "Növekvő", "Csökkenő"</span><span class="sxs-lookup"><span data-stu-id="158fa-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="158fa-116">-Path</span><span class="sxs-lookup"><span data-stu-id="158fa-116">-Path</span></span>
<span data-ttu-id="158fa-117">Az az elérési út, amelyre az indexelési viselkedés vonatkozik.</span><span class="sxs-lookup"><span data-stu-id="158fa-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="158fa-118">Az index elérési utak általában a gyökértől kezdődnek, és helyettesítő karakterekkel (/elérési út/\*) végződnek.</span><span class="sxs-lookup"><span data-stu-id="158fa-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="158fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158fa-119">CommonParameters</span></span>
<span data-ttu-id="158fa-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158fa-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="158fa-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158fa-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="158fa-122">INPUTS</span></span>

### <span data-ttu-id="158fa-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="158fa-123">None</span></span>

## <span data-ttu-id="158fa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="158fa-124">OUTPUTS</span></span>

### <span data-ttu-id="158fa-125">Microsoft.Azure.Commands.EzresDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="158fa-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="158fa-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="158fa-126">NOTES</span></span>

## <span data-ttu-id="158fa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="158fa-127">RELATED LINKS</span></span>
