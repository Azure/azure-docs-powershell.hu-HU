---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299150"
---
# <span data-ttu-id="988fa-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="988fa-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="988fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="988fa-102">SYNOPSIS</span></span>
<span data-ttu-id="988fa-103">CosmosDB MongoDB-adatbázis törlése</span><span class="sxs-lookup"><span data-stu-id="988fa-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="988fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="988fa-104">SYNTAX</span></span>

### <span data-ttu-id="988fa-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="988fa-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="988fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="988fa-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="988fa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="988fa-107">DESCRIPTION</span></span>
<span data-ttu-id="988fa-108">A **Remove-AzCosmosDBMongoDBDatabase** parancsmag törli a CosmosDB MongoDB adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="988fa-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="988fa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="988fa-109">EXAMPLES</span></span>

### <span data-ttu-id="988fa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="988fa-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="988fa-111">A parancsmag olyan objektumot ad eredményül, amely a bool (amikor a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="988fa-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="988fa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="988fa-112">PARAMETERS</span></span>

### <span data-ttu-id="988fa-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="988fa-113">-AccountName</span></span>
<span data-ttu-id="988fa-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="988fa-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="988fa-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="988fa-115">-Confirm</span></span>
<span data-ttu-id="988fa-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="988fa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988fa-117">-DefaultProfile</span></span>
<span data-ttu-id="988fa-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="988fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="988fa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="988fa-119">-InputObject</span></span>
<span data-ttu-id="988fa-120">Mongo adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="988fa-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="988fa-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="988fa-121">-Name</span></span>
<span data-ttu-id="988fa-122">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="988fa-122">Database name.</span></span>

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

### <span data-ttu-id="988fa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="988fa-123">-PassThru</span></span>
<span data-ttu-id="988fa-124">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="988fa-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="988fa-125">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="988fa-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="988fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="988fa-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="988fa-127">Name of resource group.</span></span>

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

### <span data-ttu-id="988fa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988fa-128">-WhatIf</span></span>
<span data-ttu-id="988fa-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="988fa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988fa-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="988fa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988fa-131">CommonParameters</span></span>
<span data-ttu-id="988fa-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="988fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988fa-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="988fa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988fa-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="988fa-134">INPUTS</span></span>

### <span data-ttu-id="988fa-135">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="988fa-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="988fa-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="988fa-136">OUTPUTS</span></span>

### <span data-ttu-id="988fa-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="988fa-137">System.Void</span></span>

### <span data-ttu-id="988fa-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="988fa-138">System.Boolean</span></span>

## <span data-ttu-id="988fa-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="988fa-139">NOTES</span></span>

## <span data-ttu-id="988fa-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="988fa-140">RELATED LINKS</span></span>
