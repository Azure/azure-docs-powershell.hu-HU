---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 2511ddc7174d4b76ec6d5df5bcbcd334f423a882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941930"
---
# <span data-ttu-id="adfcf-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="adfcf-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="adfcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adfcf-102">SYNOPSIS</span></span>
<span data-ttu-id="adfcf-103">Ezzel a funkcióval az automatikus skálás átviteli sebességet manuális átviteli sebességre, illetve fordítva.</span><span class="sxs-lookup"><span data-stu-id="adfcf-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="adfcf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="adfcf-104">SYNTAX</span></span>

### <span data-ttu-id="adfcf-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="adfcf-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adfcf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adfcf-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adfcf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adfcf-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adfcf-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="adfcf-108">DESCRIPTION</span></span>
<span data-ttu-id="adfcf-109">Az ThroughpyteType paraméter azt az átviteli sebességet határozza meg, amelybe át szeretne áttérni.</span><span class="sxs-lookup"><span data-stu-id="adfcf-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="adfcf-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="adfcf-110">EXAMPLES</span></span>

### <span data-ttu-id="adfcf-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="adfcf-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="adfcf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adfcf-112">PARAMETERS</span></span>

### <span data-ttu-id="adfcf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="adfcf-113">-AccountName</span></span>
<span data-ttu-id="adfcf-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="adfcf-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="adfcf-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adfcf-115">-Confirm</span></span>
<span data-ttu-id="adfcf-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="adfcf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adfcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfcf-117">-DefaultProfile</span></span>
<span data-ttu-id="adfcf-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="adfcf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adfcf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adfcf-119">-InputObject</span></span>
<span data-ttu-id="adfcf-120">Table objektum.</span><span class="sxs-lookup"><span data-stu-id="adfcf-120">Table Object.</span></span>

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

### <span data-ttu-id="adfcf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="adfcf-121">-Name</span></span>
<span data-ttu-id="adfcf-122">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="adfcf-122">Name of the Table.</span></span>

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

### <span data-ttu-id="adfcf-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="adfcf-123">-ParentObject</span></span>
<span data-ttu-id="adfcf-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="adfcf-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="adfcf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfcf-125">-ResourceGroupName</span></span>
<span data-ttu-id="adfcf-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="adfcf-126">Name of resource group.</span></span>

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

### <span data-ttu-id="adfcf-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="adfcf-127">-ThroughputType</span></span>
<span data-ttu-id="adfcf-128">Az áttűnni megfelelő átviteli sebesség típusa.</span><span class="sxs-lookup"><span data-stu-id="adfcf-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="adfcf-129">Lehetséges értékek: Automatikus méretezés, Kézi.</span><span class="sxs-lookup"><span data-stu-id="adfcf-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="adfcf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adfcf-130">-WhatIf</span></span>
<span data-ttu-id="adfcf-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="adfcf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adfcf-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="adfcf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adfcf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfcf-133">CommonParameters</span></span>
<span data-ttu-id="adfcf-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adfcf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfcf-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adfcf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfcf-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adfcf-136">INPUTS</span></span>

### <span data-ttu-id="adfcf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="adfcf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="adfcf-138">Microsoft.Azure.Commands.IssDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="adfcf-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="adfcf-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="adfcf-139">OUTPUTS</span></span>

### <span data-ttu-id="adfcf-140">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="adfcf-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="adfcf-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="adfcf-141">NOTES</span></span>

## <span data-ttu-id="adfcf-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="adfcf-142">RELATED LINKS</span></span>
