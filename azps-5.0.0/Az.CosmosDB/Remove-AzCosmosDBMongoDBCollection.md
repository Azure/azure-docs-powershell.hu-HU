---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299153"
---
# <span data-ttu-id="41ac9-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="41ac9-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="41ac9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="41ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="41ac9-103">Töröl egy CosmosDB-MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="41ac9-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41ac9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="41ac9-104">SYNTAX</span></span>

### <span data-ttu-id="41ac9-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="41ac9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41ac9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41ac9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41ac9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="41ac9-107">DESCRIPTION</span></span>
<span data-ttu-id="41ac9-108">A **Remove-AzCosmosDBMongoDBCollection** parancsmag töröl egy CosmosDB MongoDB gyűjteményt.</span><span class="sxs-lookup"><span data-stu-id="41ac9-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="41ac9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="41ac9-109">EXAMPLES</span></span>

### <span data-ttu-id="41ac9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="41ac9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="41ac9-111">A parancsmag olyan objektumot ad eredményül, amely a bool (amikor a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="41ac9-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="41ac9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="41ac9-112">PARAMETERS</span></span>

### <span data-ttu-id="41ac9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="41ac9-113">-AccountName</span></span>
<span data-ttu-id="41ac9-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="41ac9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="41ac9-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="41ac9-115">-Confirm</span></span>
<span data-ttu-id="41ac9-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="41ac9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41ac9-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41ac9-117">-DatabaseName</span></span>
<span data-ttu-id="41ac9-118">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="41ac9-118">Database name.</span></span>

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

### <span data-ttu-id="41ac9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ac9-119">-DefaultProfile</span></span>
<span data-ttu-id="41ac9-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="41ac9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41ac9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41ac9-121">-InputObject</span></span>
<span data-ttu-id="41ac9-122">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="41ac9-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41ac9-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="41ac9-123">-Name</span></span>
<span data-ttu-id="41ac9-124">Gyűjtemény neve</span><span class="sxs-lookup"><span data-stu-id="41ac9-124">Collection name.</span></span>

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

### <span data-ttu-id="41ac9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41ac9-125">-PassThru</span></span>
<span data-ttu-id="41ac9-126">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="41ac9-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="41ac9-127">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="41ac9-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="41ac9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ac9-128">-ResourceGroupName</span></span>
<span data-ttu-id="41ac9-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="41ac9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="41ac9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41ac9-130">-WhatIf</span></span>
<span data-ttu-id="41ac9-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="41ac9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41ac9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="41ac9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41ac9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ac9-133">CommonParameters</span></span>
<span data-ttu-id="41ac9-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="41ac9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ac9-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="41ac9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ac9-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ac9-136">INPUTS</span></span>

### <span data-ttu-id="41ac9-137">Microsoft. Azure. Command. CosmosDB. models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="41ac9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="41ac9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="41ac9-138">OUTPUTS</span></span>

### <span data-ttu-id="41ac9-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="41ac9-139">System.Void</span></span>

### <span data-ttu-id="41ac9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41ac9-140">System.Boolean</span></span>

## <span data-ttu-id="41ac9-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="41ac9-141">NOTES</span></span>

## <span data-ttu-id="41ac9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="41ac9-142">RELATED LINKS</span></span>
