---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182396"
---
# <span data-ttu-id="acfe3-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="acfe3-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="acfe3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="acfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="acfe3-103">Beolvassa a CosmosDB-táblázat átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="acfe3-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="acfe3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="acfe3-104">SYNTAX</span></span>

### <span data-ttu-id="acfe3-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acfe3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acfe3-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acfe3-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acfe3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="acfe3-107">DESCRIPTION</span></span>
<span data-ttu-id="acfe3-108">A **Get-AzCosmosDBTableThroughput** parancsmag a CosmosDB-táblázat átviteli sebességét kapja.</span><span class="sxs-lookup"><span data-stu-id="acfe3-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="acfe3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="acfe3-109">EXAMPLES</span></span>

### <span data-ttu-id="acfe3-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="acfe3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="acfe3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="acfe3-111">PARAMETERS</span></span>

### <span data-ttu-id="acfe3-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acfe3-112">-AccountName</span></span>
<span data-ttu-id="acfe3-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="acfe3-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="acfe3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acfe3-114">-DefaultProfile</span></span>
<span data-ttu-id="acfe3-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acfe3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acfe3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acfe3-116">-InputObject</span></span>
<span data-ttu-id="acfe3-117">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="acfe3-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="acfe3-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="acfe3-118">-Name</span></span>
<span data-ttu-id="acfe3-119">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="acfe3-119">Name of the Table.</span></span>

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

### <span data-ttu-id="acfe3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acfe3-120">-ResourceGroupName</span></span>
<span data-ttu-id="acfe3-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="acfe3-121">Name of resource group.</span></span>

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

### <span data-ttu-id="acfe3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acfe3-122">CommonParameters</span></span>
<span data-ttu-id="acfe3-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="acfe3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acfe3-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="acfe3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acfe3-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="acfe3-125">INPUTS</span></span>

### <span data-ttu-id="acfe3-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="acfe3-126">None</span></span>

## <span data-ttu-id="acfe3-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acfe3-127">OUTPUTS</span></span>

### <span data-ttu-id="acfe3-128">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="acfe3-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="acfe3-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="acfe3-129">NOTES</span></span>

## <span data-ttu-id="acfe3-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acfe3-130">RELATED LINKS</span></span>
