---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 6abad7d11da1ba73f1f34804c32bddeb779b0b1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184192"
---
# <span data-ttu-id="ca2c3-101">Remove-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="ca2c3-101">Remove-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="ca2c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2c3-103">Törli a CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-103">Deletes the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="ca2c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca2c3-104">SYNTAX</span></span>

### <span data-ttu-id="ca2c3-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca2c3-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca2c3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca2c3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlStoredProcedure -InputObject <PSSqlStoredProcedureGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca2c3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca2c3-107">DESCRIPTION</span></span>
<span data-ttu-id="ca2c3-108">A **Remove-AzCosmosDBSqlStoredProcedure** parancsmag törli a megadott ResourceGroupName, accountname és databasename tartozó SQL-StoredProcedure CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-108">The **Remove-AzCosmosDBSqlStoredProcedure** cmdlet deletes the CosmosDB Sql StoredProcedure corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="ca2c3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ca2c3-109">EXAMPLES</span></span>

### <span data-ttu-id="ca2c3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ca2c3-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlStoredProcedure -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {storedProcedureName}
```

## <span data-ttu-id="ca2c3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca2c3-111">PARAMETERS</span></span>

### <span data-ttu-id="ca2c3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca2c3-112">-AccountName</span></span>
<span data-ttu-id="ca2c3-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ca2c3-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ca2c3-114">-Confirm</span></span>
<span data-ttu-id="ca2c3-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca2c3-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ca2c3-116">-ContainerName</span></span>
<span data-ttu-id="ca2c3-117">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-117">Container name.</span></span>

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

### <span data-ttu-id="ca2c3-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ca2c3-118">-DatabaseName</span></span>
<span data-ttu-id="ca2c3-119">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-119">Database name.</span></span>

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

### <span data-ttu-id="ca2c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2c3-120">-DefaultProfile</span></span>
<span data-ttu-id="ca2c3-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca2c3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca2c3-122">-InputObject</span></span>
<span data-ttu-id="ca2c3-123">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-123">Sql Database object.</span></span>

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

### <span data-ttu-id="ca2c3-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca2c3-124">-Name</span></span>
<span data-ttu-id="ca2c3-125">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="ca2c3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca2c3-126">-PassThru</span></span>
<span data-ttu-id="ca2c3-127">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="ca2c3-128">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="ca2c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="ca2c3-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-130">Name of resource group.</span></span>

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

### <span data-ttu-id="ca2c3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca2c3-131">-WhatIf</span></span>
<span data-ttu-id="ca2c3-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca2c3-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca2c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2c3-134">CommonParameters</span></span>
<span data-ttu-id="ca2c3-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca2c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2c3-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ca2c3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2c3-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca2c3-137">INPUTS</span></span>

### <span data-ttu-id="ca2c3-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="ca2c3-138">None</span></span>

## <span data-ttu-id="ca2c3-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca2c3-139">OUTPUTS</span></span>

### <span data-ttu-id="ca2c3-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="ca2c3-140">System.Void</span></span>

### <span data-ttu-id="ca2c3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ca2c3-141">System.Boolean</span></span>

## <span data-ttu-id="ca2c3-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca2c3-142">NOTES</span></span>

## <span data-ttu-id="ca2c3-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca2c3-143">RELATED LINKS</span></span>
