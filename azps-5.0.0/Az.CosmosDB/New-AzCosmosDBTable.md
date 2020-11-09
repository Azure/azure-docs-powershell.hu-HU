---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299201"
---
# <span data-ttu-id="edcbc-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="edcbc-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="edcbc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="edcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="edcbc-103">Új CosmosDB-táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="edcbc-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="edcbc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="edcbc-104">SYNTAX</span></span>

### <span data-ttu-id="edcbc-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edcbc-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edcbc-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edcbc-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edcbc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="edcbc-107">DESCRIPTION</span></span>
<span data-ttu-id="edcbc-108">Új CosmosDB-táblát hoz létre.</span><span class="sxs-lookup"><span data-stu-id="edcbc-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="edcbc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="edcbc-109">EXAMPLES</span></span>

### <span data-ttu-id="edcbc-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="edcbc-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="edcbc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="edcbc-111">PARAMETERS</span></span>

### <span data-ttu-id="edcbc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="edcbc-112">-AccountName</span></span>
<span data-ttu-id="edcbc-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="edcbc-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="edcbc-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="edcbc-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="edcbc-115">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="edcbc-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcbc-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="edcbc-116">-Confirm</span></span>
<span data-ttu-id="edcbc-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="edcbc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edcbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcbc-118">-DefaultProfile</span></span>
<span data-ttu-id="edcbc-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edcbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edcbc-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="edcbc-120">-Name</span></span>
<span data-ttu-id="edcbc-121">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="edcbc-121">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcbc-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="edcbc-122">-ParentObject</span></span>
<span data-ttu-id="edcbc-123">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="edcbc-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edcbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edcbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="edcbc-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="edcbc-125">Name of resource group.</span></span>

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

### <span data-ttu-id="edcbc-126">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="edcbc-126">-Throughput</span></span>
<span data-ttu-id="edcbc-127">A táblázat (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="edcbc-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="edcbc-128">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="edcbc-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcbc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcbc-129">-WhatIf</span></span>
<span data-ttu-id="edcbc-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="edcbc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcbc-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edcbc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edcbc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcbc-132">CommonParameters</span></span>
<span data-ttu-id="edcbc-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="edcbc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcbc-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="edcbc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcbc-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="edcbc-135">INPUTS</span></span>

### <span data-ttu-id="edcbc-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="edcbc-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="edcbc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edcbc-137">OUTPUTS</span></span>

### <span data-ttu-id="edcbc-138">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="edcbc-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="edcbc-139">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="edcbc-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="edcbc-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="edcbc-140">NOTES</span></span>

## <span data-ttu-id="edcbc-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edcbc-141">RELATED LINKS</span></span>
