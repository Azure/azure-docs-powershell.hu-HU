---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163962"
---
# <span data-ttu-id="6d339-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="6d339-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="6d339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d339-102">SYNOPSIS</span></span>
<span data-ttu-id="6d339-103">Frissíti a MintakDB táblázat átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="6d339-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="6d339-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d339-104">SYNTAX</span></span>

### <span data-ttu-id="6d339-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d339-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d339-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d339-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d339-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d339-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d339-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d339-108">DESCRIPTION</span></span>
<span data-ttu-id="6d339-109">Frissíti egy 2010-es tábla átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="6d339-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="6d339-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d339-110">EXAMPLES</span></span>

### <span data-ttu-id="6d339-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d339-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="6d339-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d339-112">PARAMETERS</span></span>

### <span data-ttu-id="6d339-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6d339-113">-AccountName</span></span>
<span data-ttu-id="6d339-114">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="6d339-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6d339-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="6d339-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="6d339-116">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="6d339-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="6d339-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d339-117">-Confirm</span></span>
<span data-ttu-id="6d339-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d339-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d339-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d339-119">-DefaultProfile</span></span>
<span data-ttu-id="6d339-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d339-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d339-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d339-121">-InputObject</span></span>
<span data-ttu-id="6d339-122">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="6d339-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6d339-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6d339-123">-Name</span></span>
<span data-ttu-id="6d339-124">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="6d339-124">Name of the Table.</span></span>

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

### <span data-ttu-id="6d339-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6d339-125">-ParentObject</span></span>
<span data-ttu-id="6d339-126">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="6d339-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="6d339-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d339-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d339-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d339-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6d339-129">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="6d339-129">-Throughput</span></span>
<span data-ttu-id="6d339-130">A táblázat átviteli sebességét (RU/s).</span><span class="sxs-lookup"><span data-stu-id="6d339-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="6d339-131">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="6d339-131">Default value is 400.</span></span>

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

### <span data-ttu-id="6d339-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d339-132">-WhatIf</span></span>
<span data-ttu-id="6d339-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d339-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d339-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d339-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d339-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d339-135">CommonParameters</span></span>
<span data-ttu-id="6d339-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d339-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d339-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d339-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d339-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d339-138">INPUTS</span></span>

### <span data-ttu-id="6d339-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="6d339-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="6d339-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d339-140">OUTPUTS</span></span>

### <span data-ttu-id="6d339-141">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="6d339-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="6d339-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d339-142">NOTES</span></span>

## <span data-ttu-id="6d339-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d339-143">RELATED LINKS</span></span>
