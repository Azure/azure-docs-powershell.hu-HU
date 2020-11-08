---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 961ba3375c25098de32bf93b4559d9bfa6b8944d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014124"
---
# <span data-ttu-id="da589-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="da589-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="da589-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da589-102">SYNOPSIS</span></span>
<span data-ttu-id="da589-103">A CosmosDB Gremlin-adatbázis áthaladását kapja.</span><span class="sxs-lookup"><span data-stu-id="da589-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="da589-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da589-104">SYNTAX</span></span>

### <span data-ttu-id="da589-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da589-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da589-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da589-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da589-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="da589-107">DESCRIPTION</span></span>
<span data-ttu-id="da589-108">A **Get-AzCosmosDBGremlinDatabaseThroughput** parancsmag a CosmosDB Gremlin-adatbázis átviteli sebességét kapja.</span><span class="sxs-lookup"><span data-stu-id="da589-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="da589-109">Példák</span><span class="sxs-lookup"><span data-stu-id="da589-109">EXAMPLES</span></span>

### <span data-ttu-id="da589-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da589-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="da589-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da589-111">PARAMETERS</span></span>

### <span data-ttu-id="da589-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="da589-112">-AccountName</span></span>
<span data-ttu-id="da589-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="da589-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="da589-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da589-114">-DefaultProfile</span></span>
<span data-ttu-id="da589-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da589-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da589-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da589-116">-InputObject</span></span>
<span data-ttu-id="da589-117">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="da589-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da589-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da589-118">-Name</span></span>
<span data-ttu-id="da589-119">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="da589-119">Database name.</span></span>

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

### <span data-ttu-id="da589-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da589-120">-ResourceGroupName</span></span>
<span data-ttu-id="da589-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da589-121">Name of resource group.</span></span>

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

### <span data-ttu-id="da589-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da589-122">CommonParameters</span></span>
<span data-ttu-id="da589-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da589-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da589-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da589-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da589-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da589-125">INPUTS</span></span>

### <span data-ttu-id="da589-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="da589-126">None</span></span>

## <span data-ttu-id="da589-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da589-127">OUTPUTS</span></span>

### <span data-ttu-id="da589-128">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="da589-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="da589-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da589-129">NOTES</span></span>

## <span data-ttu-id="da589-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da589-130">RELATED LINKS</span></span>
