---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 98de834cebd158cc61247881305f40f84760ae2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299516"
---
# <span data-ttu-id="8582b-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="8582b-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="8582b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8582b-102">SYNOPSIS</span></span>
<span data-ttu-id="8582b-103">A CosmosDB MongoDB-adatbázis beolvasása</span><span class="sxs-lookup"><span data-stu-id="8582b-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="8582b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8582b-104">SYNTAX</span></span>

### <span data-ttu-id="8582b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8582b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8582b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8582b-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8582b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8582b-107">DESCRIPTION</span></span>
<span data-ttu-id="8582b-108">A **Get-AzCosmosDBMongoDBDatabase** parancsmag a CosmosDB MongoDB adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="8582b-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="8582b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8582b-109">EXAMPLES</span></span>

### <span data-ttu-id="8582b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8582b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="8582b-111">Az erőforrás-objektum _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8582b-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="8582b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8582b-112">PARAMETERS</span></span>

### <span data-ttu-id="8582b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8582b-113">-AccountName</span></span>
<span data-ttu-id="8582b-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="8582b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8582b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8582b-115">-DefaultProfile</span></span>
<span data-ttu-id="8582b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8582b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8582b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8582b-117">-Name</span></span>
<span data-ttu-id="8582b-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="8582b-118">Database name.</span></span>

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

### <span data-ttu-id="8582b-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8582b-119">-ParentObject</span></span>
<span data-ttu-id="8582b-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="8582b-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8582b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8582b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8582b-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8582b-122">Name of resource group.</span></span>

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

### <span data-ttu-id="8582b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8582b-123">CommonParameters</span></span>
<span data-ttu-id="8582b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8582b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8582b-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8582b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8582b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8582b-126">INPUTS</span></span>

### <span data-ttu-id="8582b-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8582b-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8582b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8582b-128">OUTPUTS</span></span>

### <span data-ttu-id="8582b-129">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8582b-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="8582b-130">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="8582b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="8582b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8582b-131">NOTES</span></span>

## <span data-ttu-id="8582b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8582b-132">RELATED LINKS</span></span>
