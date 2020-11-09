---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298970"
---
# <span data-ttu-id="d324e-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="d324e-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="d324e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d324e-102">SYNOPSIS</span></span>
<span data-ttu-id="d324e-103">Frissíti egy CosmosDB-táblázat átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="d324e-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="d324e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d324e-104">SYNTAX</span></span>

### <span data-ttu-id="d324e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d324e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d324e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d324e-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d324e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d324e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d324e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d324e-108">DESCRIPTION</span></span>
<span data-ttu-id="d324e-109">Frissíti egy CosmosDB-táblázat átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="d324e-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="d324e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d324e-110">EXAMPLES</span></span>

### <span data-ttu-id="d324e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d324e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="d324e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d324e-112">PARAMETERS</span></span>

### <span data-ttu-id="d324e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d324e-113">-AccountName</span></span>
<span data-ttu-id="d324e-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d324e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d324e-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="d324e-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="d324e-116">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="d324e-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="d324e-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d324e-117">-Confirm</span></span>
<span data-ttu-id="d324e-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d324e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d324e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d324e-119">-DefaultProfile</span></span>
<span data-ttu-id="d324e-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d324e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d324e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d324e-121">-InputObject</span></span>
<span data-ttu-id="d324e-122">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d324e-122">CosmosDB Account object</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d324e-123">-Name</span></span>
<span data-ttu-id="d324e-124">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="d324e-124">Name of the Table.</span></span>

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

### <span data-ttu-id="d324e-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d324e-125">-ParentObject</span></span>
<span data-ttu-id="d324e-126">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d324e-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d324e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d324e-127">-ResourceGroupName</span></span>
<span data-ttu-id="d324e-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d324e-128">Name of resource group.</span></span>

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

### <span data-ttu-id="d324e-129">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="d324e-129">-Throughput</span></span>
<span data-ttu-id="d324e-130">A táblázat (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="d324e-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="d324e-131">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="d324e-131">Default value is 400.</span></span>

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

### <span data-ttu-id="d324e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d324e-132">-WhatIf</span></span>
<span data-ttu-id="d324e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d324e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d324e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d324e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d324e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d324e-135">CommonParameters</span></span>
<span data-ttu-id="d324e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d324e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d324e-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d324e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d324e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d324e-138">INPUTS</span></span>

### <span data-ttu-id="d324e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d324e-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d324e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d324e-140">OUTPUTS</span></span>

### <span data-ttu-id="d324e-141">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d324e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d324e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d324e-142">NOTES</span></span>

## <span data-ttu-id="d324e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d324e-143">RELATED LINKS</span></span>
