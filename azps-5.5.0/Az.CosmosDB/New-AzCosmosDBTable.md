---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204607"
---
# <span data-ttu-id="8d537-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="8d537-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="8d537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d537-102">SYNOPSIS</span></span>
<span data-ttu-id="8d537-103">Létrehoz egy új Táblát.</span><span class="sxs-lookup"><span data-stu-id="8d537-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="8d537-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d537-104">SYNTAX</span></span>

### <span data-ttu-id="8d537-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d537-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d537-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d537-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d537-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d537-107">DESCRIPTION</span></span>
<span data-ttu-id="8d537-108">Létrehoz egy új Táblát.</span><span class="sxs-lookup"><span data-stu-id="8d537-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="8d537-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d537-109">EXAMPLES</span></span>

### <span data-ttu-id="8d537-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d537-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="8d537-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d537-111">PARAMETERS</span></span>

### <span data-ttu-id="8d537-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d537-112">-AccountName</span></span>
<span data-ttu-id="8d537-113">A Külön db-adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="8d537-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8d537-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8d537-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8d537-115">Maximális átviteli sebesség, ha engedélyezve van az automatikus méretezés.</span><span class="sxs-lookup"><span data-stu-id="8d537-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8d537-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d537-116">-Confirm</span></span>
<span data-ttu-id="8d537-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d537-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d537-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d537-118">-DefaultProfile</span></span>
<span data-ttu-id="8d537-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d537-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d537-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8d537-120">-Name</span></span>
<span data-ttu-id="8d537-121">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="8d537-121">Name of the Table.</span></span>

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

### <span data-ttu-id="8d537-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8d537-122">-ParentObject</span></span>
<span data-ttu-id="8d537-123">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="8d537-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8d537-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d537-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d537-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d537-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8d537-126">-Átviteli sebesség</span><span class="sxs-lookup"><span data-stu-id="8d537-126">-Throughput</span></span>
<span data-ttu-id="8d537-127">A táblázat átviteli sebességét (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8d537-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="8d537-128">Az alapértelmezett érték 400.</span><span class="sxs-lookup"><span data-stu-id="8d537-128">Default value is 400.</span></span>

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

### <span data-ttu-id="8d537-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d537-129">-WhatIf</span></span>
<span data-ttu-id="8d537-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d537-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d537-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d537-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d537-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d537-132">CommonParameters</span></span>
<span data-ttu-id="8d537-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d537-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d537-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d537-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d537-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d537-135">INPUTS</span></span>

### <span data-ttu-id="8d537-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8d537-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8d537-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d537-137">OUTPUTS</span></span>

### <span data-ttu-id="8d537-138">Microsoft.Azure.Commands.IssDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="8d537-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="8d537-139">Microsoft.Azure.Commands.CossDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="8d537-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="8d537-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d537-140">NOTES</span></span>

## <span data-ttu-id="8d537-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d537-141">RELATED LINKS</span></span>
