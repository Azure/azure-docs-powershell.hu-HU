---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182360"
---
# <span data-ttu-id="7641e-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="7641e-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="7641e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7641e-102">SYNOPSIS</span></span>
<span data-ttu-id="7641e-103">Frissíti a CosmosDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7641e-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="7641e-104">Ügyféloldali javítás műveletet hajt végre a meglévő tábla olvasásával.</span><span class="sxs-lookup"><span data-stu-id="7641e-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="7641e-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7641e-105">SYNTAX</span></span>

### <span data-ttu-id="7641e-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7641e-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7641e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7641e-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7641e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7641e-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7641e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="7641e-109">DESCRIPTION</span></span>
<span data-ttu-id="7641e-110">Frissíti a CosmosDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="7641e-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="7641e-111">Ügyféloldali javítás műveletet hajt végre a meglévő tábla olvasásával.</span><span class="sxs-lookup"><span data-stu-id="7641e-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="7641e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7641e-112">EXAMPLES</span></span>

### <span data-ttu-id="7641e-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7641e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="7641e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7641e-114">PARAMETERS</span></span>

### <span data-ttu-id="7641e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7641e-115">-AccountName</span></span>
<span data-ttu-id="7641e-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="7641e-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7641e-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="7641e-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="7641e-118">Maximális átviteli érték, ha az automéretarány engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="7641e-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="7641e-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7641e-119">-Confirm</span></span>
<span data-ttu-id="7641e-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7641e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7641e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7641e-121">-DefaultProfile</span></span>
<span data-ttu-id="7641e-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7641e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7641e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7641e-123">-InputObject</span></span>
<span data-ttu-id="7641e-124">Table objektum.</span><span class="sxs-lookup"><span data-stu-id="7641e-124">Table Object.</span></span>

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

### <span data-ttu-id="7641e-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7641e-125">-Name</span></span>
<span data-ttu-id="7641e-126">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="7641e-126">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7641e-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7641e-127">-ParentObject</span></span>
<span data-ttu-id="7641e-128">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="7641e-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="7641e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7641e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7641e-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="7641e-130">Name of resource group.</span></span>

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

### <span data-ttu-id="7641e-131">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="7641e-131">-Throughput</span></span>
<span data-ttu-id="7641e-132">A táblázat (RU/s) átviteli sebessége</span><span class="sxs-lookup"><span data-stu-id="7641e-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="7641e-133">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="7641e-133">Default value is 400.</span></span>

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

### <span data-ttu-id="7641e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7641e-134">-WhatIf</span></span>
<span data-ttu-id="7641e-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7641e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7641e-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7641e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7641e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7641e-137">CommonParameters</span></span>
<span data-ttu-id="7641e-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7641e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7641e-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7641e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7641e-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7641e-140">INPUTS</span></span>

### <span data-ttu-id="7641e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7641e-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="7641e-142">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="7641e-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="7641e-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7641e-143">OUTPUTS</span></span>

### <span data-ttu-id="7641e-144">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="7641e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="7641e-145">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7641e-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7641e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7641e-146">NOTES</span></span>

## <span data-ttu-id="7641e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7641e-147">RELATED LINKS</span></span>
