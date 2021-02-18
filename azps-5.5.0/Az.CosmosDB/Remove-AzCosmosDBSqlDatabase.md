---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204583"
---
# <span data-ttu-id="89638-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89638-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="89638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89638-102">SYNOPSIS</span></span>
<span data-ttu-id="89638-103">Törli aTansDB Sql-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="89638-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="89638-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="89638-104">SYNTAX</span></span>

### <span data-ttu-id="89638-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89638-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89638-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89638-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89638-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="89638-107">DESCRIPTION</span></span>
<span data-ttu-id="89638-108">A **Remove-AzCosmosDBSqlDatabase** parancsmag törli az adott ResourceGroupName, AccountName és DatabaseName fájlnak megfelelő TárolóAdatbázis sql-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="89638-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="89638-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="89638-109">EXAMPLES</span></span>

### <span data-ttu-id="89638-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="89638-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="89638-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89638-111">PARAMETERS</span></span>

### <span data-ttu-id="89638-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89638-112">-AccountName</span></span>
<span data-ttu-id="89638-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="89638-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="89638-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89638-114">-Confirm</span></span>
<span data-ttu-id="89638-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="89638-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89638-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89638-116">-DefaultProfile</span></span>
<span data-ttu-id="89638-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="89638-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89638-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89638-118">-InputObject</span></span>
<span data-ttu-id="89638-119">Sql Database-objektum.</span><span class="sxs-lookup"><span data-stu-id="89638-119">Sql Database object.</span></span>

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

### <span data-ttu-id="89638-120">-Name</span><span class="sxs-lookup"><span data-stu-id="89638-120">-Name</span></span>
<span data-ttu-id="89638-121">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="89638-121">Database name.</span></span>

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

### <span data-ttu-id="89638-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89638-122">-PassThru</span></span>
<span data-ttu-id="89638-123">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="89638-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="89638-124">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="89638-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="89638-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89638-125">-ResourceGroupName</span></span>
<span data-ttu-id="89638-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="89638-126">Name of resource group.</span></span>

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

### <span data-ttu-id="89638-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89638-127">-WhatIf</span></span>
<span data-ttu-id="89638-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="89638-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89638-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="89638-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89638-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89638-130">CommonParameters</span></span>
<span data-ttu-id="89638-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89638-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89638-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89638-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89638-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89638-133">INPUTS</span></span>

### <span data-ttu-id="89638-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="89638-134">None</span></span>

## <span data-ttu-id="89638-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="89638-135">OUTPUTS</span></span>

### <span data-ttu-id="89638-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="89638-136">System.Void</span></span>

### <span data-ttu-id="89638-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89638-137">System.Boolean</span></span>

## <span data-ttu-id="89638-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="89638-138">NOTES</span></span>

## <span data-ttu-id="89638-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="89638-139">RELATED LINKS</span></span>
