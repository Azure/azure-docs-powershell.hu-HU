---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 3ceb7ccbb789c21fc0fdb51244260e6a54b3e900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943082"
---
# <span data-ttu-id="0d44e-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="0d44e-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="0d44e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d44e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d44e-103">A NaplósDB sql-tárolónak megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0d44e-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="0d44e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0d44e-104">SYNTAX</span></span>

### <span data-ttu-id="0d44e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d44e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d44e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d44e-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d44e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0d44e-107">DESCRIPTION</span></span>
<span data-ttu-id="0d44e-108">A **Get-AzCosmosDBSqlContainerThroughput** parancsmag megkapja a 2010-es Sql Containernek megfelelő átviteli sebességet.</span><span class="sxs-lookup"><span data-stu-id="0d44e-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="0d44e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0d44e-109">EXAMPLES</span></span>

### <span data-ttu-id="0d44e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0d44e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="0d44e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d44e-111">PARAMETERS</span></span>

### <span data-ttu-id="0d44e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0d44e-112">-AccountName</span></span>
<span data-ttu-id="0d44e-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="0d44e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0d44e-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d44e-114">-DatabaseName</span></span>
<span data-ttu-id="0d44e-115">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="0d44e-115">Database name.</span></span>

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

### <span data-ttu-id="0d44e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d44e-116">-DefaultProfile</span></span>
<span data-ttu-id="0d44e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d44e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d44e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d44e-118">-InputObject</span></span>
<span data-ttu-id="0d44e-119">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="0d44e-119">Sql Container object.</span></span>

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

### <span data-ttu-id="0d44e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0d44e-120">-Name</span></span>
<span data-ttu-id="0d44e-121">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="0d44e-121">Container name.</span></span>

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

### <span data-ttu-id="0d44e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d44e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0d44e-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d44e-123">Name of resource group.</span></span>

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

### <span data-ttu-id="0d44e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d44e-124">CommonParameters</span></span>
<span data-ttu-id="0d44e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d44e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d44e-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d44e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d44e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d44e-127">INPUTS</span></span>

### <span data-ttu-id="0d44e-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="0d44e-128">None</span></span>

## <span data-ttu-id="0d44e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d44e-129">OUTPUTS</span></span>

### <span data-ttu-id="0d44e-130">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0d44e-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0d44e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0d44e-131">NOTES</span></span>

## <span data-ttu-id="0d44e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d44e-132">RELATED LINKS</span></span>
