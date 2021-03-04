---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 5bf35b43db1f1d961f24c1aa2c75c9f17c333345
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922042"
---
# <span data-ttu-id="bef18-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="bef18-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="bef18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef18-102">SYNOPSIS</span></span>
<span data-ttu-id="bef18-103">A NaplósDB sql-adatbázisnak megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bef18-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bef18-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bef18-104">SYNTAX</span></span>

### <span data-ttu-id="bef18-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bef18-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bef18-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bef18-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef18-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bef18-107">DESCRIPTION</span></span>
<span data-ttu-id="bef18-108">A **Get-AzCosmosDBSqlDatabaseThroughput** parancsmag megkapja a 2010-es Sql-adatbázisnak megfelelő átviteli sebességet.</span><span class="sxs-lookup"><span data-stu-id="bef18-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="bef18-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bef18-109">EXAMPLES</span></span>

### <span data-ttu-id="bef18-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bef18-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="bef18-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bef18-111">PARAMETERS</span></span>

### <span data-ttu-id="bef18-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bef18-112">-AccountName</span></span>
<span data-ttu-id="bef18-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bef18-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bef18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef18-114">-DefaultProfile</span></span>
<span data-ttu-id="bef18-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bef18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef18-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bef18-116">-InputObject</span></span>
<span data-ttu-id="bef18-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="bef18-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="bef18-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bef18-118">-Name</span></span>
<span data-ttu-id="bef18-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bef18-119">Database name.</span></span>

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

### <span data-ttu-id="bef18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef18-120">-ResourceGroupName</span></span>
<span data-ttu-id="bef18-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bef18-121">Name of resource group.</span></span>

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

### <span data-ttu-id="bef18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef18-122">CommonParameters</span></span>
<span data-ttu-id="bef18-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef18-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bef18-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef18-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bef18-125">INPUTS</span></span>

### <span data-ttu-id="bef18-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="bef18-126">None</span></span>

## <span data-ttu-id="bef18-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bef18-127">OUTPUTS</span></span>

### <span data-ttu-id="bef18-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bef18-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bef18-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bef18-129">NOTES</span></span>

## <span data-ttu-id="bef18-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bef18-130">RELATED LINKS</span></span>
