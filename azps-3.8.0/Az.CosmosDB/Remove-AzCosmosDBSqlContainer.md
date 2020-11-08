---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 2d8d136385470267ee88b139cc3dc23e134b5b88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013618"
---
# <span data-ttu-id="39d7b-101">Remove-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="39d7b-101">Remove-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="39d7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39d7b-102">SYNOPSIS</span></span>
<span data-ttu-id="39d7b-103">Törli a CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="39d7b-103">Deletes the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="39d7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39d7b-104">SYNTAX</span></span>

### <span data-ttu-id="39d7b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39d7b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBSqlContainer -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39d7b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d7b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlContainer -InputObject <PSSqlContainerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39d7b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="39d7b-107">DESCRIPTION</span></span>
<span data-ttu-id="39d7b-108">A **Remove-AzCosmosDBSqlContainer** parancsmag törli a megadott ResourceGroupName, accountname, databasename és ContainerName tartozó CosmosDB SQL-tárolót.</span><span class="sxs-lookup"><span data-stu-id="39d7b-108">The **Remove-AzCosmosDBSqlContainer** cmdlet deletes the CosmosDB Sql Container corresponding to the given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="39d7b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="39d7b-109">EXAMPLES</span></span>

### <span data-ttu-id="39d7b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="39d7b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlContainer -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -Name {containerName}
```

## <span data-ttu-id="39d7b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39d7b-111">PARAMETERS</span></span>

### <span data-ttu-id="39d7b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39d7b-112">-AccountName</span></span>
<span data-ttu-id="39d7b-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="39d7b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="39d7b-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="39d7b-114">-Confirm</span></span>
<span data-ttu-id="39d7b-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="39d7b-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d7b-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39d7b-116">-DatabaseName</span></span>
<span data-ttu-id="39d7b-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="39d7b-117">Database name.</span></span>

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

### <span data-ttu-id="39d7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d7b-118">-DefaultProfile</span></span>
<span data-ttu-id="39d7b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39d7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d7b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39d7b-120">-InputObject</span></span>
<span data-ttu-id="39d7b-121">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="39d7b-121">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39d7b-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39d7b-122">-Name</span></span>
<span data-ttu-id="39d7b-123">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="39d7b-123">Container name.</span></span>

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

### <span data-ttu-id="39d7b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39d7b-124">-PassThru</span></span>
<span data-ttu-id="39d7b-125">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="39d7b-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="39d7b-126">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="39d7b-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="39d7b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d7b-127">-ResourceGroupName</span></span>
<span data-ttu-id="39d7b-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="39d7b-128">Name of resource group.</span></span>

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

### <span data-ttu-id="39d7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d7b-129">-WhatIf</span></span>
<span data-ttu-id="39d7b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="39d7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39d7b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="39d7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d7b-132">CommonParameters</span></span>
<span data-ttu-id="39d7b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39d7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d7b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="39d7b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d7b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d7b-135">INPUTS</span></span>

### <span data-ttu-id="39d7b-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="39d7b-136">None</span></span>

## <span data-ttu-id="39d7b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d7b-137">OUTPUTS</span></span>

### <span data-ttu-id="39d7b-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="39d7b-138">System.Void</span></span>

### <span data-ttu-id="39d7b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39d7b-139">System.Boolean</span></span>

## <span data-ttu-id="39d7b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39d7b-140">NOTES</span></span>

## <span data-ttu-id="39d7b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39d7b-141">RELATED LINKS</span></span>
