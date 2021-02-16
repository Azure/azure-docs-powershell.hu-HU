---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148603"
---
# <span data-ttu-id="6ba21-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="6ba21-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="6ba21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba21-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba21-103">2010-es táblát kap.</span><span class="sxs-lookup"><span data-stu-id="6ba21-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="6ba21-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6ba21-104">SYNTAX</span></span>

### <span data-ttu-id="6ba21-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ba21-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ba21-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba21-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ba21-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6ba21-107">DESCRIPTION</span></span>
<span data-ttu-id="6ba21-108">A **Get-AzCosmosDBTable** parancsmag egy meglévő táblát kap.</span><span class="sxs-lookup"><span data-stu-id="6ba21-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="6ba21-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6ba21-109">EXAMPLES</span></span>

### <span data-ttu-id="6ba21-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="6ba21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="6ba21-111">Az erőforrásobjektum _rid, _ts_ etag tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6ba21-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="6ba21-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ba21-112">PARAMETERS</span></span>

### <span data-ttu-id="6ba21-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ba21-113">-AccountName</span></span>
<span data-ttu-id="6ba21-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="6ba21-114">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba21-115">-DefaultProfile</span></span>
<span data-ttu-id="6ba21-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ba21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba21-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6ba21-117">-Name</span></span>
<span data-ttu-id="6ba21-118">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="6ba21-118">Name of the Table.</span></span>

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

### <span data-ttu-id="6ba21-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ba21-119">-ParentObject</span></span>
<span data-ttu-id="6ba21-120">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="6ba21-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba21-121">-ResourceGroupName</span></span>
<span data-ttu-id="6ba21-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ba21-122">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba21-123">CommonParameters</span></span>
<span data-ttu-id="6ba21-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ba21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba21-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ba21-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba21-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ba21-126">INPUTS</span></span>

### <span data-ttu-id="6ba21-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="6ba21-127">None</span></span>

## <span data-ttu-id="6ba21-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ba21-128">OUTPUTS</span></span>

### <span data-ttu-id="6ba21-129">Microsoft.Azure.Commands.IssDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="6ba21-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="6ba21-130">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6ba21-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6ba21-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6ba21-131">NOTES</span></span>

## <span data-ttu-id="6ba21-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ba21-132">RELATED LINKS</span></span>
