---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480545"
---
# <span data-ttu-id="7642d-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="7642d-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="7642d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7642d-102">SYNOPSIS</span></span>
<span data-ttu-id="7642d-103">A 2016.012.012.0122-es adatbázis törlése.</span><span class="sxs-lookup"><span data-stu-id="7642d-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="7642d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7642d-104">SYNTAX</span></span>

### <span data-ttu-id="7642d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7642d-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7642d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7642d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7642d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7642d-107">DESCRIPTION</span></span>
<span data-ttu-id="7642d-108">A **Remove-AzCosmosDBMongoDBDatabase** parancsmag töröl egy TárolóDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="7642d-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="7642d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7642d-109">EXAMPLES</span></span>

### <span data-ttu-id="7642d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7642d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="7642d-111">A parancsmag egy bool (ha -PassThru sikeres) típusú objektumot ad vissza, amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="7642d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="7642d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7642d-112">PARAMETERS</span></span>

### <span data-ttu-id="7642d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7642d-113">-AccountName</span></span>
<span data-ttu-id="7642d-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="7642d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7642d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7642d-115">-Confirm</span></span>
<span data-ttu-id="7642d-116">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7642d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7642d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7642d-117">-DefaultProfile</span></span>
<span data-ttu-id="7642d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7642d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7642d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7642d-119">-InputObject</span></span>
<span data-ttu-id="7642d-120">Mongo Adatbázis objektum.</span><span class="sxs-lookup"><span data-stu-id="7642d-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7642d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7642d-121">-Name</span></span>
<span data-ttu-id="7642d-122">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="7642d-122">Database name.</span></span>

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

### <span data-ttu-id="7642d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7642d-123">-PassThru</span></span>
<span data-ttu-id="7642d-124">Igaz érték beállítása, ha a felhasználó kimenetet szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="7642d-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="7642d-125">A kimenet akkor igaz, ha a művelet sikeres volt, és hiba történik, ha nem.</span><span class="sxs-lookup"><span data-stu-id="7642d-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="7642d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7642d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7642d-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7642d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="7642d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7642d-128">-WhatIf</span></span>
<span data-ttu-id="7642d-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7642d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7642d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7642d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7642d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7642d-131">CommonParameters</span></span>
<span data-ttu-id="7642d-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7642d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7642d-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7642d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7642d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7642d-134">INPUTS</span></span>

### <span data-ttu-id="7642d-135">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="7642d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="7642d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7642d-136">OUTPUTS</span></span>

### <span data-ttu-id="7642d-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="7642d-137">System.Void</span></span>

### <span data-ttu-id="7642d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7642d-138">System.Boolean</span></span>

## <span data-ttu-id="7642d-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7642d-139">NOTES</span></span>

## <span data-ttu-id="7642d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7642d-140">RELATED LINKS</span></span>
