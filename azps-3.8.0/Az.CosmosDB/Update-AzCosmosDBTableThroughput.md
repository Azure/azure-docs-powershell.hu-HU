---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 56c99a1e3cf21f38544e97ee84ba10efb51bc983
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012175"
---
# <span data-ttu-id="11e20-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="11e20-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="11e20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11e20-102">SYNOPSIS</span></span>
<span data-ttu-id="11e20-103">Frissíti egy CosmosDB-táblázat átviteli értékét.</span><span class="sxs-lookup"><span data-stu-id="11e20-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="11e20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11e20-104">SYNTAX</span></span>

### <span data-ttu-id="11e20-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11e20-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e20-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e20-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -ParentObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e20-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11e20-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -Throughput <Int32> -InputObject <PSTableGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e20-108">Példák</span><span class="sxs-lookup"><span data-stu-id="11e20-108">EXAMPLES</span></span>

### <span data-ttu-id="11e20-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="11e20-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="11e20-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11e20-110">PARAMETERS</span></span>

### <span data-ttu-id="11e20-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11e20-111">-AccountName</span></span>
<span data-ttu-id="11e20-112">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="11e20-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="11e20-113">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="11e20-113">-Confirm</span></span>
<span data-ttu-id="11e20-114">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="11e20-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e20-115">-DefaultProfile</span></span>
<span data-ttu-id="11e20-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11e20-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e20-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e20-117">-InputObject</span></span>
<span data-ttu-id="11e20-118">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="11e20-118">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11e20-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11e20-119">-Name</span></span>
<span data-ttu-id="11e20-120">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="11e20-120">Name of the Table.</span></span>

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

### <span data-ttu-id="11e20-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="11e20-121">-ParentObject</span></span>
<span data-ttu-id="11e20-122">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="11e20-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="11e20-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e20-123">-ResourceGroupName</span></span>
<span data-ttu-id="11e20-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="11e20-124">Name of resource group.</span></span>

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

### <span data-ttu-id="11e20-125">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="11e20-125">-Throughput</span></span>
<span data-ttu-id="11e20-126">A táblázat (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="11e20-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="11e20-127">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="11e20-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e20-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e20-128">-WhatIf</span></span>
<span data-ttu-id="11e20-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="11e20-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e20-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="11e20-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e20-131">CommonParameters</span></span>
<span data-ttu-id="11e20-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11e20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e20-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11e20-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e20-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e20-134">INPUTS</span></span>

### <span data-ttu-id="11e20-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="11e20-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="11e20-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11e20-136">OUTPUTS</span></span>

### <span data-ttu-id="11e20-137">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="11e20-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="11e20-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11e20-138">NOTES</span></span>

## <span data-ttu-id="11e20-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11e20-139">RELATED LINKS</span></span>
