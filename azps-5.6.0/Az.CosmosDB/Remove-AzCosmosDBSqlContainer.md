---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: ab64359e8db417c3c87a49a773fe56c3dcc5334b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921330"
---
# <span data-ttu-id="7eba3-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="7eba3-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="7eba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eba3-102">SYNOPSIS</span></span>
<span data-ttu-id="7eba3-103">Törli a FogsDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="7eba3-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="7eba3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7eba3-104">SYNTAX</span></span>

### <span data-ttu-id="7eba3-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7eba3-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eba3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eba3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eba3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7eba3-107">DESCRIPTION</span></span>
<span data-ttu-id="7eba3-108">A **Remove-AzCosmosDBSqlContainer** parancsmag törli a Megadott ResourceGroupName, AccountName, DatabaseName és ContainerName fájlnak megfelelő Tárolót.</span><span class="sxs-lookup"><span data-stu-id="7eba3-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="7eba3-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7eba3-109">EXAMPLES</span></span>

### <span data-ttu-id="7eba3-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7eba3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="7eba3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eba3-111">PARAMETERS</span></span>

### <span data-ttu-id="7eba3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7eba3-112">-AccountName</span></span>
<span data-ttu-id="7eba3-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="7eba3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7eba3-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7eba3-114">-Confirm</span></span>
<span data-ttu-id="7eba3-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7eba3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eba3-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7eba3-116">-DatabaseName</span></span>
<span data-ttu-id="7eba3-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7eba3-117">Database name.</span></span>

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

### <span data-ttu-id="7eba3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eba3-118">-DefaultProfile</span></span>
<span data-ttu-id="7eba3-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7eba3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eba3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eba3-120">-InputObject</span></span>
<span data-ttu-id="7eba3-121">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="7eba3-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eba3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7eba3-122">-Name</span></span>
<span data-ttu-id="7eba3-123">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7eba3-123">Container name.</span></span>

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

### <span data-ttu-id="7eba3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eba3-124">-PassThru</span></span>
<span data-ttu-id="7eba3-125">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7eba3-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="7eba3-126">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="7eba3-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="7eba3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eba3-127">-ResourceGroupName</span></span>
<span data-ttu-id="7eba3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7eba3-128">Name of resource group.</span></span>

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

### <span data-ttu-id="7eba3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eba3-129">-WhatIf</span></span>
<span data-ttu-id="7eba3-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7eba3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eba3-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7eba3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eba3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eba3-132">CommonParameters</span></span>
<span data-ttu-id="7eba3-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eba3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eba3-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eba3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eba3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eba3-135">INPUTS</span></span>

### <span data-ttu-id="7eba3-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="7eba3-136">None</span></span>

## <span data-ttu-id="7eba3-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7eba3-137">OUTPUTS</span></span>

### <span data-ttu-id="7eba3-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="7eba3-138">System.Void</span></span>

### <span data-ttu-id="7eba3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7eba3-139">System.Boolean</span></span>

## <span data-ttu-id="7eba3-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7eba3-140">NOTES</span></span>

## <span data-ttu-id="7eba3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7eba3-141">RELATED LINKS</span></span>
