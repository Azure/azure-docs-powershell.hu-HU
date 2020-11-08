---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182376"
---
# <span data-ttu-id="f744b-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="f744b-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="f744b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f744b-102">SYNOPSIS</span></span>
<span data-ttu-id="f744b-103">Törli a CosmosDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f744b-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="f744b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f744b-104">SYNTAX</span></span>

### <span data-ttu-id="f744b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f744b-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f744b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f744b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f744b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f744b-107">DESCRIPTION</span></span>
<span data-ttu-id="f744b-108">A **Remove-AzCosmosDBTable** parancsmag törli a CosmosDB táblát.</span><span class="sxs-lookup"><span data-stu-id="f744b-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="f744b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f744b-109">EXAMPLES</span></span>

### <span data-ttu-id="f744b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f744b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="f744b-111">A parancsmag olyan objektumot ad eredményül, amely a bool (amikor a-PassThru áthalad), amely igaz, ha a törlés sikeres volt.</span><span class="sxs-lookup"><span data-stu-id="f744b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="f744b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f744b-112">PARAMETERS</span></span>

### <span data-ttu-id="f744b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f744b-113">-AccountName</span></span>
<span data-ttu-id="f744b-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="f744b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f744b-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f744b-115">-Confirm</span></span>
<span data-ttu-id="f744b-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f744b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f744b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f744b-117">-DefaultProfile</span></span>
<span data-ttu-id="f744b-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f744b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f744b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f744b-119">-InputObject</span></span>
<span data-ttu-id="f744b-120">SQL adatbázis-objektum.</span><span class="sxs-lookup"><span data-stu-id="f744b-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f744b-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f744b-121">-Name</span></span>
<span data-ttu-id="f744b-122">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="f744b-122">Name of the Table.</span></span>

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

### <span data-ttu-id="f744b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f744b-123">-PassThru</span></span>
<span data-ttu-id="f744b-124">True (igaz) értékre van állítva, ha a felhasználó kimenetet szeretne fogadni.</span><span class="sxs-lookup"><span data-stu-id="f744b-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f744b-125">A kimenet akkor igaz, ha a művelet sikeres volt, és ha nem, a program hibát jelez.</span><span class="sxs-lookup"><span data-stu-id="f744b-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="f744b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f744b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f744b-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f744b-127">Name of resource group.</span></span>

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

### <span data-ttu-id="f744b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f744b-128">-WhatIf</span></span>
<span data-ttu-id="f744b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f744b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f744b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f744b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f744b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f744b-131">CommonParameters</span></span>
<span data-ttu-id="f744b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f744b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f744b-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f744b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f744b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f744b-134">INPUTS</span></span>

### <span data-ttu-id="f744b-135">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f744b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="f744b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f744b-136">OUTPUTS</span></span>

### <span data-ttu-id="f744b-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="f744b-137">System.Void</span></span>

### <span data-ttu-id="f744b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f744b-138">System.Boolean</span></span>

## <span data-ttu-id="f744b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f744b-139">NOTES</span></span>

## <span data-ttu-id="f744b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f744b-140">RELATED LINKS</span></span>
