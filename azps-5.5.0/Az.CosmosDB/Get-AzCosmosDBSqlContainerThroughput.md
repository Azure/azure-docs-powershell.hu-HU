---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166250"
---
# <span data-ttu-id="feb45-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="feb45-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="feb45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb45-102">SYNOPSIS</span></span>
<span data-ttu-id="feb45-103">A NaplósDB sql-tárolónak megfelelő átviteli sebességet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="feb45-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="feb45-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="feb45-104">SYNTAX</span></span>

### <span data-ttu-id="feb45-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="feb45-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="feb45-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="feb45-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb45-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="feb45-107">DESCRIPTION</span></span>
<span data-ttu-id="feb45-108">A **Get-AzCosmosDBSqlContainerThroughput** parancsmag kapja meg a FogalyDB sql-tárolónak megfelelő átviteli sebességet.</span><span class="sxs-lookup"><span data-stu-id="feb45-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="feb45-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="feb45-109">EXAMPLES</span></span>

### <span data-ttu-id="feb45-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="feb45-110">Example 1</span></span>
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

## <span data-ttu-id="feb45-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb45-111">PARAMETERS</span></span>

### <span data-ttu-id="feb45-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="feb45-112">-AccountName</span></span>
<span data-ttu-id="feb45-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="feb45-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="feb45-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="feb45-114">-DatabaseName</span></span>
<span data-ttu-id="feb45-115">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="feb45-115">Database name.</span></span>

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

### <span data-ttu-id="feb45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb45-116">-DefaultProfile</span></span>
<span data-ttu-id="feb45-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feb45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb45-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb45-118">-InputObject</span></span>
<span data-ttu-id="feb45-119">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="feb45-119">Sql Container object.</span></span>

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

### <span data-ttu-id="feb45-120">-Name</span><span class="sxs-lookup"><span data-stu-id="feb45-120">-Name</span></span>
<span data-ttu-id="feb45-121">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="feb45-121">Container name.</span></span>

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

### <span data-ttu-id="feb45-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb45-122">-ResourceGroupName</span></span>
<span data-ttu-id="feb45-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="feb45-123">Name of resource group.</span></span>

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

### <span data-ttu-id="feb45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb45-124">CommonParameters</span></span>
<span data-ttu-id="feb45-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb45-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb45-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb45-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feb45-127">INPUTS</span></span>

### <span data-ttu-id="feb45-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="feb45-128">None</span></span>

## <span data-ttu-id="feb45-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feb45-129">OUTPUTS</span></span>

### <span data-ttu-id="feb45-130">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="feb45-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="feb45-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="feb45-131">NOTES</span></span>

## <span data-ttu-id="feb45-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feb45-132">RELATED LINKS</span></span>
