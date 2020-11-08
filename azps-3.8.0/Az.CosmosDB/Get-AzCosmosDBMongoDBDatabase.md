---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: f1cb4a45a68758dc1209b4e30d352def8e348e9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014106"
---
# <span data-ttu-id="d7f3c-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="d7f3c-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="d7f3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f3c-103">A CosmosDB MongoDB-adatbázis beolvasása</span><span class="sxs-lookup"><span data-stu-id="d7f3c-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="d7f3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7f3c-104">SYNTAX</span></span>

### <span data-ttu-id="d7f3c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d7f3c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7f3c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7f3c-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f3c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7f3c-107">DESCRIPTION</span></span>
<span data-ttu-id="d7f3c-108">A **Get-AzCosmosDBMongoDBDatabase** parancsmag a CosmosDB MongoDB adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="d7f3c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d7f3c-109">EXAMPLES</span></span>

### <span data-ttu-id="d7f3c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d7f3c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="d7f3c-111">Az erőforrás-objektum _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="d7f3c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7f3c-112">PARAMETERS</span></span>

### <span data-ttu-id="d7f3c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d7f3c-113">-AccountName</span></span>
<span data-ttu-id="d7f3c-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d7f3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f3c-115">-DefaultProfile</span></span>
<span data-ttu-id="d7f3c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f3c-117">– Részletes</span><span class="sxs-lookup"><span data-stu-id="d7f3c-117">-Detailed</span></span>
<span data-ttu-id="d7f3c-118">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező adatbázist adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-118">If provided then, the cmdlet returns the database with the corresponding throughput value.</span></span>

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

### <span data-ttu-id="d7f3c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7f3c-119">-InputObject</span></span>
<span data-ttu-id="d7f3c-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d7f3c-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f3c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d7f3c-121">-Name</span></span>
<span data-ttu-id="d7f3c-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-122">Database name.</span></span>

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

### <span data-ttu-id="d7f3c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f3c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7f3c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-124">Name of resource group.</span></span>

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

### <span data-ttu-id="d7f3c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f3c-125">CommonParameters</span></span>
<span data-ttu-id="d7f3c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7f3c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f3c-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d7f3c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f3c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f3c-128">INPUTS</span></span>

### <span data-ttu-id="d7f3c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d7f3c-129">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d7f3c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7f3c-130">OUTPUTS</span></span>

### <span data-ttu-id="d7f3c-131">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="d7f3c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="d7f3c-132">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d7f3c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d7f3c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7f3c-133">NOTES</span></span>

## <span data-ttu-id="d7f3c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7f3c-134">RELATED LINKS</span></span>
