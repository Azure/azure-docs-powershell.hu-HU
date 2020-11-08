---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: ba1f6b1ca309226433120ea6a68ec330cabd034c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025479"
---
# <span data-ttu-id="af31d-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="af31d-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="af31d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af31d-102">SYNOPSIS</span></span>
<span data-ttu-id="af31d-103">Megkapja a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="af31d-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="af31d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af31d-104">SYNTAX</span></span>

### <span data-ttu-id="af31d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af31d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af31d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af31d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af31d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af31d-107">DESCRIPTION</span></span>
<span data-ttu-id="af31d-108">A **Get-AzCosmosDBGremlinDatabase** parancsmag a CosmosDB Gremlin adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="af31d-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="af31d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af31d-109">EXAMPLES</span></span>

### <span data-ttu-id="af31d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="af31d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="af31d-111">Az erőforrás-objektum _ridt, _tst _etag tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="af31d-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="af31d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af31d-112">PARAMETERS</span></span>

### <span data-ttu-id="af31d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="af31d-113">-AccountName</span></span>
<span data-ttu-id="af31d-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="af31d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="af31d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af31d-115">-DefaultProfile</span></span>
<span data-ttu-id="af31d-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af31d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af31d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af31d-117">-Name</span></span>
<span data-ttu-id="af31d-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="af31d-118">Database name.</span></span>

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

### <span data-ttu-id="af31d-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="af31d-119">-ParentObject</span></span>
<span data-ttu-id="af31d-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="af31d-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="af31d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af31d-121">-ResourceGroupName</span></span>
<span data-ttu-id="af31d-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="af31d-122">Name of resource group.</span></span>

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

### <span data-ttu-id="af31d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af31d-123">CommonParameters</span></span>
<span data-ttu-id="af31d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af31d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af31d-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="af31d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af31d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af31d-126">INPUTS</span></span>

### <span data-ttu-id="af31d-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="af31d-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="af31d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af31d-128">OUTPUTS</span></span>

### <span data-ttu-id="af31d-129">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="af31d-129">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="af31d-130">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="af31d-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="af31d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af31d-131">NOTES</span></span>

## <span data-ttu-id="af31d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af31d-132">RELATED LINKS</span></span>
