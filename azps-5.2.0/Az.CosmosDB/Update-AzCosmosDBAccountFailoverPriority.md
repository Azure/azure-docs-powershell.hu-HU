---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352770"
---
# <span data-ttu-id="64d77-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="64d77-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="64d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d77-102">SYNOPSIS</span></span>
<span data-ttu-id="64d77-103">{{ Fill in the Synopsis }}</span><span class="sxs-lookup"><span data-stu-id="64d77-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="64d77-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64d77-104">SYNTAX</span></span>

### <span data-ttu-id="64d77-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64d77-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d77-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d77-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d77-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64d77-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d77-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64d77-108">DESCRIPTION</span></span>
<span data-ttu-id="64d77-109">{{ Töltse ki a leírás }}</span><span class="sxs-lookup"><span data-stu-id="64d77-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="64d77-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64d77-110">EXAMPLES</span></span>

### <span data-ttu-id="64d77-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="64d77-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="64d77-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="64d77-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="64d77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64d77-113">PARAMETERS</span></span>

### <span data-ttu-id="64d77-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64d77-114">-AsJob</span></span>
<span data-ttu-id="64d77-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="64d77-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64d77-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64d77-116">-Confirm</span></span>
<span data-ttu-id="64d77-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64d77-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d77-118">-DefaultProfile</span></span>
<span data-ttu-id="64d77-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64d77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d77-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="64d77-120">-FailoverPolicy</span></span>
<span data-ttu-id="64d77-121">A feladatátvételi prioritás szerint rendezett, régióneveket tartalmazó karakterláncok tömbje.</span><span class="sxs-lookup"><span data-stu-id="64d77-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="64d77-122">Például: eastus, westus</span><span class="sxs-lookup"><span data-stu-id="64d77-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d77-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d77-123">-InputObject</span></span>
<span data-ttu-id="64d77-124">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="64d77-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64d77-125">-Name</span><span class="sxs-lookup"><span data-stu-id="64d77-125">-Name</span></span>
<span data-ttu-id="64d77-126">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="64d77-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="64d77-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d77-127">-ResourceGroupName</span></span>
<span data-ttu-id="64d77-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="64d77-128">Name of resource group.</span></span>

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

### <span data-ttu-id="64d77-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64d77-129">-ResourceId</span></span>
<span data-ttu-id="64d77-130">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="64d77-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d77-131">-WhatIf</span></span>
<span data-ttu-id="64d77-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64d77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d77-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64d77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d77-134">CommonParameters</span></span>
<span data-ttu-id="64d77-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d77-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64d77-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d77-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64d77-137">INPUTS</span></span>

### <span data-ttu-id="64d77-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="64d77-138">None</span></span>

## <span data-ttu-id="64d77-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64d77-139">OUTPUTS</span></span>

### <span data-ttu-id="64d77-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="64d77-140">System.Void</span></span>

## <span data-ttu-id="64d77-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64d77-141">NOTES</span></span>

## <span data-ttu-id="64d77-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64d77-142">RELATED LINKS</span></span>
