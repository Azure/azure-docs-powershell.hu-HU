---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 8496df5eb29d3f3a552e5b68a5e481d5cb01efd1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299141"
---
# <span data-ttu-id="050c9-101">Remove-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="050c9-101">Remove-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="050c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="050c9-102">SYNOPSIS</span></span>
<span data-ttu-id="050c9-103">Törli a CosmosDB SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="050c9-103">Deletes the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="050c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="050c9-104">SYNTAX</span></span>

### <span data-ttu-id="050c9-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c9-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050c9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="050c9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlDatabase -InputObject <PSSqlDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050c9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="050c9-107">DESCRIPTION</span></span>
<span data-ttu-id="050c9-108">A **Remove-AzCosmosDBSqlDatabase** parancsmag a megadott ResourceGroupName, accountname és databasename megfelelő CosmosDB SQL-adatbázis törlését törli.</span><span class="sxs-lookup"><span data-stu-id="050c9-108">The **Remove-AzCosmosDBSqlDatabase** cmdlet deletes the CosmosDB Sql Database corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="050c9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="050c9-109">EXAMPLES</span></span>

### <span data-ttu-id="050c9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="050c9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {databaseName}
```

## <span data-ttu-id="050c9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="050c9-111">PARAMETERS</span></span>

### <span data-ttu-id="050c9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="050c9-112">-AccountName</span></span>
<span data-ttu-id="050c9-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="050c9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="050c9-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="050c9-114">-Confirm</span></span>
<span data-ttu-id="050c9-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="050c9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050c9-116">-DefaultProfile</span></span>
<span data-ttu-id="050c9-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="050c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050c9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="050c9-118">-InputObject</span></span>
<span data-ttu-id="050c9-119">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="050c9-119">Sql Database object.</span></span>

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

### <span data-ttu-id="050c9-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="050c9-120">-Name</span></span>
<span data-ttu-id="050c9-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="050c9-121">Database name.</span></span>

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

### <span data-ttu-id="050c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="050c9-122">-PassThru</span></span>
<span data-ttu-id="050c9-123">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="050c9-123">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="050c9-124">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="050c9-124">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="050c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="050c9-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="050c9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="050c9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050c9-127">-WhatIf</span></span>
<span data-ttu-id="050c9-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="050c9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="050c9-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="050c9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050c9-130">CommonParameters</span></span>
<span data-ttu-id="050c9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="050c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050c9-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="050c9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050c9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="050c9-133">INPUTS</span></span>

### <span data-ttu-id="050c9-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="050c9-134">None</span></span>

## <span data-ttu-id="050c9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="050c9-135">OUTPUTS</span></span>

### <span data-ttu-id="050c9-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="050c9-136">System.Void</span></span>

### <span data-ttu-id="050c9-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="050c9-137">System.Boolean</span></span>

## <span data-ttu-id="050c9-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="050c9-138">NOTES</span></span>

## <span data-ttu-id="050c9-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="050c9-139">RELATED LINKS</span></span>
