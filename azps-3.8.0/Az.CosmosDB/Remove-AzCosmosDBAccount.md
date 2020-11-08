---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: e9ec1f1626a1fb4335c6e5df43a96727692538c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013715"
---
# <span data-ttu-id="81349-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="81349-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="81349-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="81349-102">SYNOPSIS</span></span>
<span data-ttu-id="81349-103">CosmosDB-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="81349-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="81349-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="81349-104">SYNTAX</span></span>

### <span data-ttu-id="81349-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="81349-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81349-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81349-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81349-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81349-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81349-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="81349-108">DESCRIPTION</span></span>
<span data-ttu-id="81349-109">CosmosDB-fiók eltávolítása az adott ResourceGroup megadott névvel</span><span class="sxs-lookup"><span data-stu-id="81349-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="81349-110">Példák</span><span class="sxs-lookup"><span data-stu-id="81349-110">EXAMPLES</span></span>

### <span data-ttu-id="81349-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="81349-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="81349-112">A ResourceGroup RG fiók névvel dbname rendelkező fiók törlődik.</span><span class="sxs-lookup"><span data-stu-id="81349-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="81349-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="81349-113">PARAMETERS</span></span>

### <span data-ttu-id="81349-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81349-114">-AsJob</span></span>
<span data-ttu-id="81349-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="81349-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81349-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="81349-116">-Confirm</span></span>
<span data-ttu-id="81349-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="81349-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81349-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81349-118">-DefaultProfile</span></span>
<span data-ttu-id="81349-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="81349-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81349-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81349-120">-InputObject</span></span>
<span data-ttu-id="81349-121">Az adatbázis-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="81349-121">The Database Account object</span></span>

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

### <span data-ttu-id="81349-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="81349-122">-Name</span></span>
<span data-ttu-id="81349-123">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="81349-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="81349-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81349-124">-PassThru</span></span>
<span data-ttu-id="81349-125">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="81349-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="81349-126">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="81349-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="81349-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81349-127">-ResourceGroupName</span></span>
<span data-ttu-id="81349-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="81349-128">Name of resource group.</span></span>

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

### <span data-ttu-id="81349-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81349-129">-ResourceId</span></span>
<span data-ttu-id="81349-130">Az erőforrás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="81349-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="81349-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81349-131">-WhatIf</span></span>
<span data-ttu-id="81349-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="81349-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81349-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="81349-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81349-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81349-134">CommonParameters</span></span>
<span data-ttu-id="81349-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="81349-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81349-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="81349-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81349-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="81349-137">INPUTS</span></span>

### <span data-ttu-id="81349-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="81349-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="81349-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="81349-139">OUTPUTS</span></span>

### <span data-ttu-id="81349-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="81349-140">System.Void</span></span>

## <span data-ttu-id="81349-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="81349-141">NOTES</span></span>

## <span data-ttu-id="81349-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="81349-142">RELATED LINKS</span></span>
