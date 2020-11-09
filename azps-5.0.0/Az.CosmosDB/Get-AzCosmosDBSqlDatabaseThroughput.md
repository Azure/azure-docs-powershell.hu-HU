---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299495"
---
# <span data-ttu-id="42157-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="42157-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="42157-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42157-102">SYNOPSIS</span></span>
<span data-ttu-id="42157-103">A CosmosDB SQL-adatbázishoz tartozó átviteli beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42157-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="42157-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42157-104">SYNTAX</span></span>

### <span data-ttu-id="42157-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42157-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42157-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42157-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42157-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="42157-107">DESCRIPTION</span></span>
<span data-ttu-id="42157-108">A **Get-AzCosmosDBSqlDatabaseThroughput** parancsmag a CosmosDB SQL-adatbázishoz tartozó átviteli beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="42157-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="42157-109">Példák</span><span class="sxs-lookup"><span data-stu-id="42157-109">EXAMPLES</span></span>

### <span data-ttu-id="42157-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="42157-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="42157-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42157-111">PARAMETERS</span></span>

### <span data-ttu-id="42157-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42157-112">-AccountName</span></span>
<span data-ttu-id="42157-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="42157-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="42157-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42157-114">-DefaultProfile</span></span>
<span data-ttu-id="42157-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42157-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42157-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42157-116">-InputObject</span></span>
<span data-ttu-id="42157-117">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="42157-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="42157-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="42157-118">-Name</span></span>
<span data-ttu-id="42157-119">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="42157-119">Database name.</span></span>

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

### <span data-ttu-id="42157-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42157-120">-ResourceGroupName</span></span>
<span data-ttu-id="42157-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="42157-121">Name of resource group.</span></span>

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

### <span data-ttu-id="42157-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42157-122">CommonParameters</span></span>
<span data-ttu-id="42157-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42157-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42157-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="42157-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42157-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42157-125">INPUTS</span></span>

### <span data-ttu-id="42157-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="42157-126">None</span></span>

## <span data-ttu-id="42157-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42157-127">OUTPUTS</span></span>

### <span data-ttu-id="42157-128">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="42157-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="42157-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42157-129">NOTES</span></span>

## <span data-ttu-id="42157-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42157-130">RELATED LINKS</span></span>
