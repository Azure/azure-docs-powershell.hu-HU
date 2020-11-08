---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 4a6c93c0946780420cffb8b5cb6d2e9331d55bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010548"
---
# <span data-ttu-id="6595a-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="6595a-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="6595a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6595a-102">SYNOPSIS</span></span>
<span data-ttu-id="6595a-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="6595a-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="6595a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6595a-104">SYNTAX</span></span>

### <span data-ttu-id="6595a-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6595a-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6595a-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6595a-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6595a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6595a-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6595a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6595a-108">DESCRIPTION</span></span>
<span data-ttu-id="6595a-109">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="6595a-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="6595a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6595a-110">EXAMPLES</span></span>

### <span data-ttu-id="6595a-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6595a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="6595a-112">A FailoverPolicies a lévő régió1-as FailoverPriority 1, region2 as FailoverPriority 2 és region3 as FailoverPriority</span><span class="sxs-lookup"><span data-stu-id="6595a-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="6595a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6595a-113">PARAMETERS</span></span>

### <span data-ttu-id="6595a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6595a-114">-AsJob</span></span>
<span data-ttu-id="6595a-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="6595a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6595a-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6595a-116">-Confirm</span></span>
<span data-ttu-id="6595a-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6595a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6595a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6595a-118">-DefaultProfile</span></span>
<span data-ttu-id="6595a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6595a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6595a-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="6595a-120">-FailoverPolicy</span></span>
<span data-ttu-id="6595a-121">A területi neveket tartalmazó karakterláncok tömbje, a feladatátvételi prioritás szerint rendezve.</span><span class="sxs-lookup"><span data-stu-id="6595a-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="6595a-122">Például eastus, westus</span><span class="sxs-lookup"><span data-stu-id="6595a-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="6595a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6595a-123">-InputObject</span></span>
<span data-ttu-id="6595a-124">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="6595a-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6595a-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6595a-125">-Name</span></span>
<span data-ttu-id="6595a-126">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="6595a-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6595a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6595a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6595a-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6595a-128">Name of resource group.</span></span>

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

### <span data-ttu-id="6595a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6595a-129">-ResourceId</span></span>
<span data-ttu-id="6595a-130">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6595a-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="6595a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6595a-131">-WhatIf</span></span>
<span data-ttu-id="6595a-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6595a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6595a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6595a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6595a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6595a-134">CommonParameters</span></span>
<span data-ttu-id="6595a-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6595a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6595a-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6595a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6595a-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6595a-137">INPUTS</span></span>

### <span data-ttu-id="6595a-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="6595a-138">None</span></span>

## <span data-ttu-id="6595a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6595a-139">OUTPUTS</span></span>

### <span data-ttu-id="6595a-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="6595a-140">System.Void</span></span>

## <span data-ttu-id="6595a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6595a-141">NOTES</span></span>

## <span data-ttu-id="6595a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6595a-142">RELATED LINKS</span></span>
