---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d473d87971b0fcc1b8457a7d2e362c334d480ec4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933041"
---
# <span data-ttu-id="456d4-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="456d4-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="456d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456d4-102">SYNOPSIS</span></span>
<span data-ttu-id="456d4-103">Beveszi a MongoDB-adatbázis 2010.010.000 átviteli sebességét.</b0></span><span class="sxs-lookup"><span data-stu-id="456d4-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="456d4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="456d4-104">SYNTAX</span></span>

### <span data-ttu-id="456d4-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="456d4-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="456d4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="456d4-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="456d4-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="456d4-107">DESCRIPTION</span></span>
<span data-ttu-id="456d4-108">A **Get-AzCosmosDBMongoDBDatabaseThroughput** parancsmag a MongoDB-adatbázis átviteli tulajdonságokkal rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="456d4-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="456d4-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="456d4-109">EXAMPLES</span></span>

### <span data-ttu-id="456d4-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="456d4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="456d4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="456d4-111">PARAMETERS</span></span>

### <span data-ttu-id="456d4-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="456d4-112">-AccountName</span></span>
<span data-ttu-id="456d4-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="456d4-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="456d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456d4-114">-DefaultProfile</span></span>
<span data-ttu-id="456d4-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="456d4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="456d4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="456d4-116">-InputObject</span></span>
<span data-ttu-id="456d4-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="456d4-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="456d4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="456d4-118">-Name</span></span>
<span data-ttu-id="456d4-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="456d4-119">Database name.</span></span>

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

### <span data-ttu-id="456d4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456d4-120">-ResourceGroupName</span></span>
<span data-ttu-id="456d4-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="456d4-121">Name of resource group.</span></span>

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

### <span data-ttu-id="456d4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456d4-122">CommonParameters</span></span>
<span data-ttu-id="456d4-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456d4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456d4-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="456d4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456d4-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="456d4-125">INPUTS</span></span>

### <span data-ttu-id="456d4-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="456d4-126">None</span></span>

## <span data-ttu-id="456d4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="456d4-127">OUTPUTS</span></span>

### <span data-ttu-id="456d4-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="456d4-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="456d4-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="456d4-129">NOTES</span></span>

## <span data-ttu-id="456d4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="456d4-130">RELATED LINKS</span></span>
