---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbgremlindatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBGremlinDatabaseThroughput.md
ms.openlocfilehash: 8905f4e4ffc4268b74ce57bfaf1bcb14565f70fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341190"
---
# <span data-ttu-id="ac10e-101">Get-AzCosmosDBGremlinDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="ac10e-101">Get-AzCosmosDBGremlinDatabaseThroughput</span></span>

## <span data-ttu-id="ac10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac10e-102">SYNOPSIS</span></span>
<span data-ttu-id="ac10e-103">Egy TárolóDB Gremlin-adatbázis átviteli sebességét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ac10e-103">Gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ac10e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac10e-104">SYNTAX</span></span>

### <span data-ttu-id="ac10e-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ac10e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac10e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac10e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBGremlinDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac10e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac10e-107">DESCRIPTION</span></span>
<span data-ttu-id="ac10e-108">A **Get-AzCosmosDBGremlinDatabaseThroughput** parancsmag kapja meg egy AbDB Gremlin-adatbázis átviteli sebességét.</span><span class="sxs-lookup"><span data-stu-id="ac10e-108">The **Get-AzCosmosDBGremlinDatabaseThroughput** cmdlet gets the throughput of a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="ac10e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac10e-109">EXAMPLES</span></span>

### <span data-ttu-id="ac10e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ac10e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBGremlinDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}
Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ac10e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac10e-111">PARAMETERS</span></span>

### <span data-ttu-id="ac10e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac10e-112">-AccountName</span></span>
<span data-ttu-id="ac10e-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="ac10e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ac10e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac10e-114">-DefaultProfile</span></span>
<span data-ttu-id="ac10e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac10e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac10e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac10e-116">-InputObject</span></span>
<span data-ttu-id="ac10e-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="ac10e-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="ac10e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ac10e-118">-Name</span></span>
<span data-ttu-id="ac10e-119">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="ac10e-119">Database name.</span></span>

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

### <span data-ttu-id="ac10e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac10e-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac10e-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ac10e-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ac10e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac10e-122">CommonParameters</span></span>
<span data-ttu-id="ac10e-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac10e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac10e-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac10e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac10e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac10e-125">INPUTS</span></span>

### <span data-ttu-id="ac10e-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ac10e-126">None</span></span>

## <span data-ttu-id="ac10e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac10e-127">OUTPUTS</span></span>

### <span data-ttu-id="ac10e-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ac10e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ac10e-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac10e-129">NOTES</span></span>

## <span data-ttu-id="ac10e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac10e-130">RELATED LINKS</span></span>
