---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480541"
---
# <span data-ttu-id="3a80a-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="3a80a-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="3a80a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a80a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a80a-103">Törli aTansDB sql triggert.</span><span class="sxs-lookup"><span data-stu-id="3a80a-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="3a80a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3a80a-104">SYNTAX</span></span>

### <span data-ttu-id="3a80a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a80a-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a80a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a80a-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a80a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3a80a-107">DESCRIPTION</span></span>
<span data-ttu-id="3a80a-108">A **Remove-AzCosmosDBSqlTrigger** parancsmag törli a Adott ResourceGroupName, AccountName és DatabaseName fájlhoz tartozó indítófájlt.</span><span class="sxs-lookup"><span data-stu-id="3a80a-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="3a80a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3a80a-109">EXAMPLES</span></span>

### <span data-ttu-id="3a80a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3a80a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="3a80a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a80a-111">PARAMETERS</span></span>

### <span data-ttu-id="3a80a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a80a-112">-AccountName</span></span>
<span data-ttu-id="3a80a-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3a80a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3a80a-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a80a-114">-Confirm</span></span>
<span data-ttu-id="3a80a-115">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3a80a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a80a-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3a80a-116">-ContainerName</span></span>
<span data-ttu-id="3a80a-117">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3a80a-117">Container name.</span></span>

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

### <span data-ttu-id="3a80a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3a80a-118">-DatabaseName</span></span>
<span data-ttu-id="3a80a-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3a80a-119">Database name.</span></span>

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

### <span data-ttu-id="3a80a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a80a-120">-DefaultProfile</span></span>
<span data-ttu-id="3a80a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3a80a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a80a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a80a-122">-InputObject</span></span>
<span data-ttu-id="3a80a-123">Sql trigger objektum</span><span class="sxs-lookup"><span data-stu-id="3a80a-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3a80a-124">-Name</span></span>
<span data-ttu-id="3a80a-125">Eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="3a80a-125">Trigger name.</span></span>

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

### <span data-ttu-id="3a80a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a80a-126">-PassThru</span></span>
<span data-ttu-id="3a80a-127">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="3a80a-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3a80a-128">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="3a80a-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3a80a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a80a-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a80a-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3a80a-130">Name of resource group.</span></span>

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

### <span data-ttu-id="3a80a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a80a-131">-WhatIf</span></span>
<span data-ttu-id="3a80a-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3a80a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a80a-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3a80a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a80a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a80a-134">CommonParameters</span></span>
<span data-ttu-id="3a80a-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a80a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a80a-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a80a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a80a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a80a-137">INPUTS</span></span>

### <span data-ttu-id="3a80a-138">Nincs</span><span class="sxs-lookup"><span data-stu-id="3a80a-138">None</span></span>

## <span data-ttu-id="3a80a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3a80a-139">OUTPUTS</span></span>

### <span data-ttu-id="3a80a-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="3a80a-140">System.Void</span></span>

### <span data-ttu-id="3a80a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a80a-141">System.Boolean</span></span>

## <span data-ttu-id="3a80a-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3a80a-142">NOTES</span></span>

## <span data-ttu-id="3a80a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3a80a-143">RELATED LINKS</span></span>
