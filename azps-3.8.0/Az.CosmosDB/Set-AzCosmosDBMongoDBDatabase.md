---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014435"
---
# <span data-ttu-id="06b99-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="06b99-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="06b99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06b99-102">SYNOPSIS</span></span>
<span data-ttu-id="06b99-103">A CosmosDB MongoDB adatbázisának visszaállítása</span><span class="sxs-lookup"><span data-stu-id="06b99-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="06b99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06b99-104">SYNTAX</span></span>

### <span data-ttu-id="06b99-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="06b99-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06b99-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06b99-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b99-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="06b99-107">DESCRIPTION</span></span>
<span data-ttu-id="06b99-108">A **set-AzCosmosDBMongoDBDatabase** parancsmag a CosmosDB MongoDB adatbázist kapja.</span><span class="sxs-lookup"><span data-stu-id="06b99-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="06b99-109">Példák</span><span class="sxs-lookup"><span data-stu-id="06b99-109">EXAMPLES</span></span>

### <span data-ttu-id="06b99-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="06b99-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="06b99-111">Az erőforrás-objektum _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="06b99-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="06b99-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06b99-112">PARAMETERS</span></span>

### <span data-ttu-id="06b99-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="06b99-113">-AccountName</span></span>
<span data-ttu-id="06b99-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="06b99-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="06b99-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06b99-115">-Confirm</span></span>
<span data-ttu-id="06b99-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06b99-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b99-117">-DefaultProfile</span></span>
<span data-ttu-id="06b99-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06b99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b99-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06b99-119">-InputObject</span></span>
<span data-ttu-id="06b99-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="06b99-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b99-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06b99-121">-Name</span></span>
<span data-ttu-id="06b99-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="06b99-122">Database name.</span></span>

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

### <span data-ttu-id="06b99-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b99-123">-ResourceGroupName</span></span>
<span data-ttu-id="06b99-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="06b99-124">Name of resource group.</span></span>

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

### <span data-ttu-id="06b99-125">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="06b99-125">-Throughput</span></span>
<span data-ttu-id="06b99-126">Az Mongo-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="06b99-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="06b99-127">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="06b99-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b99-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b99-128">-WhatIf</span></span>
<span data-ttu-id="06b99-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06b99-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b99-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06b99-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b99-131">CommonParameters</span></span>
<span data-ttu-id="06b99-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06b99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b99-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="06b99-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b99-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b99-134">INPUTS</span></span>

### <span data-ttu-id="06b99-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="06b99-135">None</span></span>

## <span data-ttu-id="06b99-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06b99-136">OUTPUTS</span></span>

### <span data-ttu-id="06b99-137">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="06b99-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="06b99-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06b99-138">NOTES</span></span>

## <span data-ttu-id="06b99-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06b99-139">RELATED LINKS</span></span>
