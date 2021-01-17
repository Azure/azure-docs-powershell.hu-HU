---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336354"
---
# <span data-ttu-id="7a6a8-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="7a6a8-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="7a6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6a8-103">Törli a FogsDB Sql StoredProcedure rekordot.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="7a6a8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a6a8-104">SYNTAX</span></span>

### <span data-ttu-id="7a6a8-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6a8-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a6a8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a6a8-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a6a8-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a6a8-107">DESCRIPTION</span></span>
<span data-ttu-id="7a6a8-108">A **Remove-AzCosmosDBSqlStoredProcedure** parancsmag törli aFogsDB Sql StoredProcedure értékeket, amelyek a megadott ResourceGroupName, AccountName és DatabaseName értéknek oszlnak meg.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="7a6a8-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a6a8-109">EXAMPLES</span></span>

### <span data-ttu-id="7a6a8-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7a6a8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="7a6a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a6a8-111">PARAMETERS</span></span>

### <span data-ttu-id="7a6a8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7a6a8-112">-AccountName</span></span>
<span data-ttu-id="7a6a8-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7a6a8-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a6a8-114">-Confirm</span></span>
<span data-ttu-id="7a6a8-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6a8-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7a6a8-116">-ContainerName</span></span>
<span data-ttu-id="7a6a8-117">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-117">Container name.</span></span>

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

### <span data-ttu-id="7a6a8-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a6a8-118">-DatabaseName</span></span>
<span data-ttu-id="7a6a8-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-119">Database name.</span></span>

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

### <span data-ttu-id="7a6a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6a8-120">-DefaultProfile</span></span>
<span data-ttu-id="7a6a8-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a6a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a6a8-122">-InputObject</span></span>
<span data-ttu-id="7a6a8-123">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-123">Sql Database object.</span></span>

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

### <span data-ttu-id="7a6a8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7a6a8-124">-Name</span></span>
<span data-ttu-id="7a6a8-125">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="7a6a8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a6a8-126">-PassThru</span></span>
<span data-ttu-id="7a6a8-127">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="7a6a8-128">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="7a6a8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6a8-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a6a8-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7a6a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6a8-131">-WhatIf</span></span>
<span data-ttu-id="7a6a8-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6a8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6a8-134">CommonParameters</span></span>
<span data-ttu-id="7a6a8-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6a8-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a6a8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6a8-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a6a8-137">INPUTS</span></span>

### <span data-ttu-id="7a6a8-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="7a6a8-138">None</span></span>

## <span data-ttu-id="7a6a8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a6a8-139">OUTPUTS</span></span>

### <span data-ttu-id="7a6a8-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="7a6a8-140">System.Void</span></span>

### <span data-ttu-id="7a6a8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a6a8-141">System.Boolean</span></span>

## <span data-ttu-id="7a6a8-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a6a8-142">NOTES</span></span>

## <span data-ttu-id="7a6a8-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a6a8-143">RELATED LINKS</span></span>
