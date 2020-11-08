---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014436"
---
# <span data-ttu-id="3bb20-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="3bb20-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="3bb20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bb20-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb20-103">A CosmosDB Gremlin-adatbázisát állítja be.</span><span class="sxs-lookup"><span data-stu-id="3bb20-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3bb20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bb20-104">SYNTAX</span></span>

### <span data-ttu-id="3bb20-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bb20-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb20-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bb20-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb20-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bb20-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb20-108">A **set-AzCosmosDBGremlinDatabase** parancsmag a CosmosDB Gremlin adatbázist állítja be.</span><span class="sxs-lookup"><span data-stu-id="3bb20-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="3bb20-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3bb20-109">EXAMPLES</span></span>

### <span data-ttu-id="3bb20-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3bb20-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="3bb20-111">Az erőforrás-objektum _ridt, _tst _etag tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="3bb20-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="3bb20-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bb20-112">PARAMETERS</span></span>

### <span data-ttu-id="3bb20-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3bb20-113">-AccountName</span></span>
<span data-ttu-id="3bb20-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="3bb20-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3bb20-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bb20-115">-Confirm</span></span>
<span data-ttu-id="3bb20-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bb20-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb20-117">-DefaultProfile</span></span>
<span data-ttu-id="3bb20-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bb20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb20-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb20-119">-InputObject</span></span>
<span data-ttu-id="3bb20-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="3bb20-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3bb20-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3bb20-121">-Name</span></span>
<span data-ttu-id="3bb20-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3bb20-122">Database name.</span></span>

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

### <span data-ttu-id="3bb20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb20-123">-ResourceGroupName</span></span>
<span data-ttu-id="3bb20-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3bb20-124">Name of resource group.</span></span>

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

### <span data-ttu-id="3bb20-125">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="3bb20-125">-Throughput</span></span>
<span data-ttu-id="3bb20-126">Az Gremlin-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="3bb20-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="3bb20-127">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="3bb20-127">Default value is 400.</span></span>

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

### <span data-ttu-id="3bb20-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb20-128">-WhatIf</span></span>
<span data-ttu-id="3bb20-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bb20-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb20-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bb20-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb20-131">CommonParameters</span></span>
<span data-ttu-id="3bb20-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bb20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb20-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3bb20-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb20-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bb20-134">INPUTS</span></span>

### <span data-ttu-id="3bb20-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3bb20-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3bb20-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bb20-136">OUTPUTS</span></span>

### <span data-ttu-id="3bb20-137">Microsoft. Azure. Command. CosmosDB. models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3bb20-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="3bb20-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bb20-138">NOTES</span></span>

## <span data-ttu-id="3bb20-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bb20-139">RELATED LINKS</span></span>
