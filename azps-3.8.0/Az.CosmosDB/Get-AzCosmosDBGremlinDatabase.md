---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 52a889ea454b5752be25ecd216f9a20e4b830b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014125"
---
# <span data-ttu-id="5d673-101">Get-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="5d673-101">Get-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="5d673-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d673-102">SYNOPSIS</span></span>
<span data-ttu-id="5d673-103">Megkapja a CosmosDB Gremlin-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="5d673-103">Gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5d673-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d673-104">SYNTAX</span></span>

### <span data-ttu-id="5d673-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5d673-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d673-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d673-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d673-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d673-107">DESCRIPTION</span></span>
<span data-ttu-id="5d673-108">A **Get-AzCosmosDBGremlinDatabase** parancsmag a CosmosDB Gremlin adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="5d673-108">The **Get-AzCosmosDBGremlinDatabase** cmdlet gets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5d673-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5d673-109">EXAMPLES</span></span>

### <span data-ttu-id="5d673-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5d673-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="5d673-111">Az erőforrás-objektum _ridt, _tst _etag tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="5d673-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="5d673-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d673-112">PARAMETERS</span></span>

### <span data-ttu-id="5d673-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d673-113">-AccountName</span></span>
<span data-ttu-id="5d673-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="5d673-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5d673-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d673-115">-DefaultProfile</span></span>
<span data-ttu-id="5d673-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d673-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d673-117">– Részletes</span><span class="sxs-lookup"><span data-stu-id="5d673-117">-Detailed</span></span>
<span data-ttu-id="5d673-118">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező adatbázist adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="5d673-118">If provided then, the cmdlet returns the Database with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d673-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d673-119">-InputObject</span></span>
<span data-ttu-id="5d673-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="5d673-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d673-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d673-121">-Name</span></span>
<span data-ttu-id="5d673-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="5d673-122">Database name.</span></span>

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

### <span data-ttu-id="5d673-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d673-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d673-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5d673-124">Name of resource group.</span></span>

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

### <span data-ttu-id="5d673-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d673-125">CommonParameters</span></span>
<span data-ttu-id="5d673-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d673-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d673-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5d673-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d673-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d673-128">INPUTS</span></span>

### <span data-ttu-id="5d673-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5d673-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5d673-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d673-130">OUTPUTS</span></span>

### <span data-ttu-id="5d673-131">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5d673-131">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="5d673-132">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="5d673-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="5d673-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d673-133">NOTES</span></span>

## <span data-ttu-id="5d673-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d673-134">RELATED LINKS</span></span>
