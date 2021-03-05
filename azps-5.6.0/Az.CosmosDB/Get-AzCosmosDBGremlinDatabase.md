---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 7268eff2163e408975b1711dcac4fbf8454f0b76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004373"
---
# <span data-ttu-id="0deee-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="0deee-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="0deee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0deee-102">SYNOPSIS</span></span>
<span data-ttu-id="0deee-103">Ez a rendszer beveszi a 2016-os Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0deee-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="0deee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0deee-104">SYNTAX</span></span>

### <span data-ttu-id="0deee-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0deee-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0deee-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0deee-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0deee-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0deee-107">DESCRIPTION</span></span>
<span data-ttu-id="0deee-108">A **Get-AzCosmosDBGremlinDatabase** parancsmag beveszi a TárolóDB Gremlin-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="0deee-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="0deee-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0deee-109">EXAMPLES</span></span>

### <span data-ttu-id="0deee-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0deee-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="0deee-111">Az Erőforrásobjektum _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="0deee-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="0deee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0deee-112">PARAMETERS</span></span>

### <span data-ttu-id="0deee-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0deee-113">-AccountName</span></span>
<span data-ttu-id="0deee-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0deee-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0deee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0deee-115">-DefaultProfile</span></span>
<span data-ttu-id="0deee-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0deee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0deee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0deee-117">-Name</span></span>
<span data-ttu-id="0deee-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0deee-118">Database name.</span></span>

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

### <span data-ttu-id="0deee-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0deee-119">-ParentObject</span></span>
<span data-ttu-id="0deee-120">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="0deee-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0deee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0deee-121">-ResourceGroupName</span></span>
<span data-ttu-id="0deee-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0deee-122">Name of resource group.</span></span>

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

### <span data-ttu-id="0deee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0deee-123">CommonParameters</span></span>
<span data-ttu-id="0deee-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0deee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0deee-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0deee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0deee-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0deee-126">INPUTS</span></span>

### <span data-ttu-id="0deee-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0deee-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0deee-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0deee-128">OUTPUTS</span></span>

### <span data-ttu-id="0deee-129">Microsoft.Azure.Commands.EzresDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="0deee-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="0deee-130">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0deee-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0deee-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0deee-131">NOTES</span></span>

## <span data-ttu-id="0deee-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0deee-132">RELATED LINKS</span></span>
