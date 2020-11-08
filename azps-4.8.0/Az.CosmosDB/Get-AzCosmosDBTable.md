---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182390"
---
# <span data-ttu-id="8d1a8-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="8d1a8-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="8d1a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d1a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1a8-103">Beolvassa a CosmosDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="8d1a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d1a8-104">SYNTAX</span></span>

### <span data-ttu-id="8d1a8-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d1a8-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8d1a8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d1a8-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1a8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d1a8-107">DESCRIPTION</span></span>
<span data-ttu-id="8d1a8-108">A **Get-AzCosmosDBTable** parancsmag meglévő táblát kap.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="8d1a8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8d1a8-109">EXAMPLES</span></span>

### <span data-ttu-id="8d1a8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d1a8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="8d1a8-111">Az erőforrás-objektum a táblázat _rid, _ts, _ ETAG tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="8d1a8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d1a8-112">PARAMETERS</span></span>

### <span data-ttu-id="8d1a8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d1a8-113">-AccountName</span></span>
<span data-ttu-id="8d1a8-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8d1a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1a8-115">-DefaultProfile</span></span>
<span data-ttu-id="8d1a8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d1a8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d1a8-117">-Name</span></span>
<span data-ttu-id="8d1a8-118">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-118">Name of the Table.</span></span>

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

### <span data-ttu-id="8d1a8-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d1a8-119">-ParentObject</span></span>
<span data-ttu-id="8d1a8-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="8d1a8-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8d1a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d1a8-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-122">Name of resource group.</span></span>

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

### <span data-ttu-id="8d1a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1a8-123">CommonParameters</span></span>
<span data-ttu-id="8d1a8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d1a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1a8-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d1a8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1a8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1a8-126">INPUTS</span></span>

### <span data-ttu-id="8d1a8-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d1a8-127">None</span></span>

## <span data-ttu-id="8d1a8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1a8-128">OUTPUTS</span></span>

### <span data-ttu-id="8d1a8-129">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8d1a8-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="8d1a8-130">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8d1a8-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8d1a8-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d1a8-131">NOTES</span></span>

## <span data-ttu-id="8d1a8-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d1a8-132">RELATED LINKS</span></span>
