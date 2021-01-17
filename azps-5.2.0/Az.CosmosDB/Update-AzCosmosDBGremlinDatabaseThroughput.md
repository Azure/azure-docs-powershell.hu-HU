---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 43426c97e809bf576dd6df19af108fb54c6874a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323661"
---
# <span data-ttu-id="afe86-101">Update-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="afe86-101">Update-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="afe86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afe86-102">SYNOPSIS</span></span>
<span data-ttu-id="afe86-103">Frissíti a MintakDB Gremlin-adatbázis átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="afe86-103">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="afe86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="afe86-104">SYNTAX</span></span>

### <span data-ttu-id="afe86-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="afe86-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe86-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe86-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afe86-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afe86-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBGremlinDatabaseThroughput [-Name <String>] -InputObject <PSGremlinDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afe86-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="afe86-108">DESCRIPTION</span></span>
<span data-ttu-id="afe86-109">Frissíti a MintakDB Gremlin-adatbázis átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="afe86-109">Updates the throughput value of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="afe86-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="afe86-110">EXAMPLES</span></span>

### <span data-ttu-id="afe86-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="afe86-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBGremlinDatabaseThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/gremlinDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="afe86-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afe86-112">PARAMETERS</span></span>

### <span data-ttu-id="afe86-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="afe86-113">-AccountName</span></span>
<span data-ttu-id="afe86-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="afe86-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="afe86-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="afe86-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="afe86-116">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="afe86-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="afe86-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afe86-117">-Confirm</span></span>
<span data-ttu-id="afe86-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="afe86-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afe86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afe86-119">-DefaultProfile</span></span>
<span data-ttu-id="afe86-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afe86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afe86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afe86-121">-InputObject</span></span>
<span data-ttu-id="afe86-122">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="afe86-122">CosmosDB Account object</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afe86-123">-Name</span><span class="sxs-lookup"><span data-stu-id="afe86-123">-Name</span></span>
<span data-ttu-id="afe86-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="afe86-124">Database name.</span></span>

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

### <span data-ttu-id="afe86-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="afe86-125">-ParentObject</span></span>
<span data-ttu-id="afe86-126">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="afe86-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="afe86-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afe86-127">-ResourceGroupName</span></span>
<span data-ttu-id="afe86-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="afe86-128">Name of resource group.</span></span>

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

### <span data-ttu-id="afe86-129">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="afe86-129">-Throughput</span></span>
<span data-ttu-id="afe86-130">A Gremlin-adatbázis (RU/s) átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="afe86-130">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="afe86-131">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="afe86-131">Default value is 400.</span></span>

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

### <span data-ttu-id="afe86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afe86-132">-WhatIf</span></span>
<span data-ttu-id="afe86-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="afe86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afe86-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="afe86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afe86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afe86-135">CommonParameters</span></span>
<span data-ttu-id="afe86-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afe86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afe86-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afe86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afe86-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afe86-138">INPUTS</span></span>

### <span data-ttu-id="afe86-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="afe86-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="afe86-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afe86-140">OUTPUTS</span></span>

### <span data-ttu-id="afe86-141">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="afe86-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="afe86-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="afe86-142">NOTES</span></span>

## <span data-ttu-id="afe86-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afe86-143">RELATED LINKS</span></span>
