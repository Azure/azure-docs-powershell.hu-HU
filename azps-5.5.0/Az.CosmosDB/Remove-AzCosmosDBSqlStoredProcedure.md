---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204575"
---
# <span data-ttu-id="3f877-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="3f877-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="3f877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f877-102">SYNOPSIS</span></span>
<span data-ttu-id="3f877-103">Törli a FogsDB Sql StoredProcedure rekordot.</span><span class="sxs-lookup"><span data-stu-id="3f877-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="3f877-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f877-104">SYNTAX</span></span>

### <span data-ttu-id="3f877-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f877-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f877-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f877-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f877-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f877-107">DESCRIPTION</span></span>
<span data-ttu-id="3f877-108">A **Remove-AzCosmosDBSqlStoredProcedure** parancsmag törli aFogsDB Sql StoredProcedure értékeket, amelyek a megadott ResourceGroupName, AccountName és DatabaseName fájlhoz vannak megadva.</span><span class="sxs-lookup"><span data-stu-id="3f877-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="3f877-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f877-109">EXAMPLES</span></span>

### <span data-ttu-id="3f877-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f877-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="3f877-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f877-111">PARAMETERS</span></span>

### <span data-ttu-id="3f877-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f877-112">-AccountName</span></span>
<span data-ttu-id="3f877-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3f877-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3f877-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f877-114">-Confirm</span></span>
<span data-ttu-id="3f877-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f877-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f877-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3f877-116">-ContainerName</span></span>
<span data-ttu-id="3f877-117">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3f877-117">Container name.</span></span>

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

### <span data-ttu-id="3f877-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f877-118">-DatabaseName</span></span>
<span data-ttu-id="3f877-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3f877-119">Database name.</span></span>

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

### <span data-ttu-id="3f877-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f877-120">-DefaultProfile</span></span>
<span data-ttu-id="3f877-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f877-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f877-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f877-122">-InputObject</span></span>
<span data-ttu-id="3f877-123">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="3f877-123">Sql Database object.</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f877-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3f877-124">-Name</span></span>
<span data-ttu-id="3f877-125">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="3f877-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="3f877-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f877-126">-PassThru</span></span>
<span data-ttu-id="3f877-127">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="3f877-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3f877-128">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="3f877-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3f877-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f877-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f877-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3f877-130">Name of resource group.</span></span>

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

### <span data-ttu-id="3f877-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f877-131">-WhatIf</span></span>
<span data-ttu-id="3f877-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f877-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f877-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f877-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f877-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f877-134">CommonParameters</span></span>
<span data-ttu-id="3f877-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f877-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f877-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f877-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f877-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f877-137">INPUTS</span></span>

### <span data-ttu-id="3f877-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="3f877-138">None</span></span>

## <span data-ttu-id="3f877-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f877-139">OUTPUTS</span></span>

### <span data-ttu-id="3f877-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f877-140">System.Void</span></span>

### <span data-ttu-id="3f877-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f877-141">System.Boolean</span></span>

## <span data-ttu-id="3f877-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f877-142">NOTES</span></span>

## <span data-ttu-id="3f877-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f877-143">RELATED LINKS</span></span>
