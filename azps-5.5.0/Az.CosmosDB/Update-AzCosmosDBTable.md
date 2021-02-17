---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163955"
---
# <span data-ttu-id="21910-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="21910-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="21910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21910-102">SYNOPSIS</span></span>
<span data-ttu-id="21910-103">Frissíti aFrissítésekDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="21910-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="21910-104">Ügyféloldali javítást hajt végre a meglévő táblázat elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="21910-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="21910-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="21910-105">SYNTAX</span></span>

### <span data-ttu-id="21910-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21910-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21910-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21910-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21910-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21910-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21910-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="21910-109">DESCRIPTION</span></span>
<span data-ttu-id="21910-110">Frissíti aFrissítésekDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="21910-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="21910-111">Ügyféloldali javítást hajt végre a meglévő táblázat elolvasása alapján.</span><span class="sxs-lookup"><span data-stu-id="21910-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="21910-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="21910-112">EXAMPLES</span></span>

### <span data-ttu-id="21910-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="21910-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="21910-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21910-114">PARAMETERS</span></span>

### <span data-ttu-id="21910-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21910-115">-AccountName</span></span>
<span data-ttu-id="21910-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="21910-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21910-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="21910-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="21910-118">Az automatikus skálázás engedélyezése esetén a maximális átviteli sebesség.</span><span class="sxs-lookup"><span data-stu-id="21910-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="21910-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21910-119">-Confirm</span></span>
<span data-ttu-id="21910-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="21910-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21910-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21910-121">-DefaultProfile</span></span>
<span data-ttu-id="21910-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21910-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21910-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21910-123">-InputObject</span></span>
<span data-ttu-id="21910-124">Table objektum.</span><span class="sxs-lookup"><span data-stu-id="21910-124">Table Object.</span></span>

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

### <span data-ttu-id="21910-125">-Name</span><span class="sxs-lookup"><span data-stu-id="21910-125">-Name</span></span>
<span data-ttu-id="21910-126">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="21910-126">Name of the Table.</span></span>

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

### <span data-ttu-id="21910-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="21910-127">-ParentObject</span></span>
<span data-ttu-id="21910-128">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="21910-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="21910-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21910-129">-ResourceGroupName</span></span>
<span data-ttu-id="21910-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="21910-130">Name of resource group.</span></span>

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

### <span data-ttu-id="21910-131">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="21910-131">-Throughput</span></span>
<span data-ttu-id="21910-132">A táblázat átviteli sebességét (RU/s).</span><span class="sxs-lookup"><span data-stu-id="21910-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="21910-133">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="21910-133">Default value is 400.</span></span>

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

### <span data-ttu-id="21910-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21910-134">-WhatIf</span></span>
<span data-ttu-id="21910-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="21910-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21910-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="21910-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21910-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21910-137">CommonParameters</span></span>
<span data-ttu-id="21910-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21910-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21910-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21910-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21910-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21910-140">INPUTS</span></span>

### <span data-ttu-id="21910-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="21910-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="21910-142">Microsoft.Azure.Commands.EzresDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="21910-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="21910-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21910-143">OUTPUTS</span></span>

### <span data-ttu-id="21910-144">Microsoft.Azure.Commands.IssDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="21910-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="21910-145">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="21910-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="21910-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="21910-146">NOTES</span></span>

## <span data-ttu-id="21910-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21910-147">RELATED LINKS</span></span>
