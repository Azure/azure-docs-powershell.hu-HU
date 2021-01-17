---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480543"
---
# <span data-ttu-id="f567e-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f567e-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f567e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f567e-102">SYNOPSIS</span></span>
<span data-ttu-id="f567e-103">Törli a TárolóDB Sql-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f567e-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f567e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f567e-104">SYNTAX</span></span>

### <span data-ttu-id="f567e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f567e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f567e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f567e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f567e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f567e-107">DESCRIPTION</span></span>
<span data-ttu-id="f567e-108">A **Remove-AzCosmosDBSqlDatabase** parancsmag törli az adott ResourceGroupName, AccountName és DatabaseName fájlnak megfelelő TárolóAdatbázis sql-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="f567e-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="f567e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f567e-109">EXAMPLES</span></span>

### <span data-ttu-id="f567e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="f567e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="f567e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f567e-111">PARAMETERS</span></span>

### <span data-ttu-id="f567e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f567e-112">-AccountName</span></span>
<span data-ttu-id="f567e-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="f567e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f567e-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f567e-114">-Confirm</span></span>
<span data-ttu-id="f567e-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f567e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f567e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f567e-116">-DefaultProfile</span></span>
<span data-ttu-id="f567e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f567e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f567e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f567e-118">-InputObject</span></span>
<span data-ttu-id="f567e-119">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="f567e-119">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f567e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f567e-120">-Name</span></span>
<span data-ttu-id="f567e-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="f567e-121">Database name.</span></span>

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

### <span data-ttu-id="f567e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f567e-122">-PassThru</span></span>
<span data-ttu-id="f567e-123">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="f567e-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f567e-124">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="f567e-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f567e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f567e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f567e-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f567e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="f567e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f567e-127">-WhatIf</span></span>
<span data-ttu-id="f567e-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f567e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f567e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f567e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f567e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f567e-130">CommonParameters</span></span>
<span data-ttu-id="f567e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f567e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f567e-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f567e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f567e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f567e-133">INPUTS</span></span>

### <span data-ttu-id="f567e-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="f567e-134">None</span></span>

## <span data-ttu-id="f567e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f567e-135">OUTPUTS</span></span>

### <span data-ttu-id="f567e-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="f567e-136">System.Void</span></span>

### <span data-ttu-id="f567e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f567e-137">System.Boolean</span></span>

## <span data-ttu-id="f567e-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f567e-138">NOTES</span></span>

## <span data-ttu-id="f567e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f567e-139">RELATED LINKS</span></span>
