---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 61acd388dabcfe71c83d282d032e9d4bb688d88b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014109"
---
# <span data-ttu-id="e82dd-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="e82dd-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="e82dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e82dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e82dd-103">A CosmosDB SQL-tárolóhoz tartozó átviteli beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e82dd-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="e82dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e82dd-104">SYNTAX</span></span>

### <span data-ttu-id="e82dd-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e82dd-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e82dd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e82dd-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e82dd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e82dd-107">DESCRIPTION</span></span>
<span data-ttu-id="e82dd-108">A **Get-AzCosmosDBSqlContainerThroughput** parancsmag az CosmosDB SQL-tárolóhoz tartozó átviteli beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e82dd-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="e82dd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e82dd-109">EXAMPLES</span></span>

### <span data-ttu-id="e82dd-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e82dd-110">Example 1</span></span>
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

## <span data-ttu-id="e82dd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e82dd-111">PARAMETERS</span></span>

### <span data-ttu-id="e82dd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e82dd-112">-AccountName</span></span>
<span data-ttu-id="e82dd-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="e82dd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e82dd-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e82dd-114">-DatabaseName</span></span>
<span data-ttu-id="e82dd-115">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="e82dd-115">Database name.</span></span>

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

### <span data-ttu-id="e82dd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82dd-116">-DefaultProfile</span></span>
<span data-ttu-id="e82dd-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e82dd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e82dd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e82dd-118">-InputObject</span></span>
<span data-ttu-id="e82dd-119">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="e82dd-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e82dd-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e82dd-120">-Name</span></span>
<span data-ttu-id="e82dd-121">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="e82dd-121">Container name.</span></span>

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

### <span data-ttu-id="e82dd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82dd-122">-ResourceGroupName</span></span>
<span data-ttu-id="e82dd-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e82dd-123">Name of resource group.</span></span>

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

### <span data-ttu-id="e82dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82dd-124">CommonParameters</span></span>
<span data-ttu-id="e82dd-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e82dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82dd-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e82dd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82dd-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e82dd-127">INPUTS</span></span>

### <span data-ttu-id="e82dd-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e82dd-128">None</span></span>

## <span data-ttu-id="e82dd-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e82dd-129">OUTPUTS</span></span>

### <span data-ttu-id="e82dd-130">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="e82dd-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="e82dd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e82dd-131">NOTES</span></span>

## <span data-ttu-id="e82dd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e82dd-132">RELATED LINKS</span></span>
