---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480551"
---
# <span data-ttu-id="212d5-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="212d5-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="212d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="212d5-102">SYNOPSIS</span></span>
<span data-ttu-id="212d5-103">Távolítsa el a 2010.01.012-es fiókot.</span><span class="sxs-lookup"><span data-stu-id="212d5-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="212d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="212d5-104">SYNTAX</span></span>

### <span data-ttu-id="212d5-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="212d5-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212d5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="212d5-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212d5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="212d5-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="212d5-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="212d5-108">DESCRIPTION</span></span>
<span data-ttu-id="212d5-109">Távolítson el egy Olyan Fiókot, amely az adott ResourceGroup-csoportban egy adott névvel van megadva.</span><span class="sxs-lookup"><span data-stu-id="212d5-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="212d5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="212d5-110">EXAMPLES</span></span>

### <span data-ttu-id="212d5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="212d5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="212d5-112">Az ResourceGroup rg-ban a fióknévvel egy fióknév törlődik.</span><span class="sxs-lookup"><span data-stu-id="212d5-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="212d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="212d5-113">PARAMETERS</span></span>

### <span data-ttu-id="212d5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="212d5-114">-AsJob</span></span>
<span data-ttu-id="212d5-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="212d5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="212d5-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="212d5-116">-Confirm</span></span>
<span data-ttu-id="212d5-117">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="212d5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="212d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212d5-118">-DefaultProfile</span></span>
<span data-ttu-id="212d5-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="212d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="212d5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="212d5-120">-InputObject</span></span>
<span data-ttu-id="212d5-121">Az Adatbázisfiók objektum</span><span class="sxs-lookup"><span data-stu-id="212d5-121">The Database Account object</span></span>

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

### <span data-ttu-id="212d5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="212d5-122">-Name</span></span>
<span data-ttu-id="212d5-123">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="212d5-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="212d5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="212d5-124">-PassThru</span></span>
<span data-ttu-id="212d5-125">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="212d5-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="212d5-126">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="212d5-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="212d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="212d5-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="212d5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="212d5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="212d5-129">-ResourceId</span></span>
<span data-ttu-id="212d5-130">Az erőforrás Erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="212d5-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="212d5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212d5-131">-WhatIf</span></span>
<span data-ttu-id="212d5-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="212d5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="212d5-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="212d5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="212d5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212d5-134">CommonParameters</span></span>
<span data-ttu-id="212d5-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="212d5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212d5-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="212d5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212d5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="212d5-137">INPUTS</span></span>

### <span data-ttu-id="212d5-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="212d5-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="212d5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="212d5-139">OUTPUTS</span></span>

### <span data-ttu-id="212d5-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="212d5-140">System.Void</span></span>

## <span data-ttu-id="212d5-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="212d5-141">NOTES</span></span>

## <span data-ttu-id="212d5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="212d5-142">RELATED LINKS</span></span>
