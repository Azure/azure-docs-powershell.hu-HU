---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012193"
---
# <span data-ttu-id="d6ec2-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="d6ec2-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="d6ec2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d6ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ec2-103">A CosmosDB-táblázat beállítására</span><span class="sxs-lookup"><span data-stu-id="d6ec2-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="d6ec2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d6ec2-104">SYNTAX</span></span>

### <span data-ttu-id="d6ec2-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ec2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6ec2-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ec2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d6ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ec2-108">A **set-AzCosmosDBTable** parancsmag új táblát hoz létre, vagy frissít egy meglévő táblázatot, és a meglévő táblázatot teljes egészében felülírja.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="d6ec2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d6ec2-109">EXAMPLES</span></span>

### <span data-ttu-id="d6ec2-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d6ec2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="d6ec2-111">Az erőforrás-objektum a táblázat _rid, _ts, _ ETAG tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="d6ec2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d6ec2-112">PARAMETERS</span></span>

### <span data-ttu-id="d6ec2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6ec2-113">-AccountName</span></span>
<span data-ttu-id="d6ec2-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d6ec2-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d6ec2-115">-Confirm</span></span>
<span data-ttu-id="d6ec2-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ec2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ec2-117">-DefaultProfile</span></span>
<span data-ttu-id="d6ec2-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ec2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6ec2-119">-InputObject</span></span>
<span data-ttu-id="d6ec2-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="d6ec2-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ec2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d6ec2-121">-Name</span></span>
<span data-ttu-id="d6ec2-122">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-122">Name of the Table.</span></span>

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

### <span data-ttu-id="d6ec2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ec2-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6ec2-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-124">Name of resource group.</span></span>

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

### <span data-ttu-id="d6ec2-125">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="d6ec2-125">-Throughput</span></span>
<span data-ttu-id="d6ec2-126">A táblázat (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="d6ec2-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="d6ec2-127">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-127">Default value is 400.</span></span>

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

### <span data-ttu-id="d6ec2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ec2-128">-WhatIf</span></span>
<span data-ttu-id="d6ec2-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ec2-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ec2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ec2-131">CommonParameters</span></span>
<span data-ttu-id="d6ec2-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d6ec2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ec2-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d6ec2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ec2-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ec2-134">INPUTS</span></span>

### <span data-ttu-id="d6ec2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d6ec2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d6ec2-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d6ec2-136">OUTPUTS</span></span>

### <span data-ttu-id="d6ec2-137">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d6ec2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d6ec2-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d6ec2-138">NOTES</span></span>

## <span data-ttu-id="d6ec2-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d6ec2-139">RELATED LINKS</span></span>
