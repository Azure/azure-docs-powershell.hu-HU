---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346049"
---
# <span data-ttu-id="3418d-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="3418d-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="3418d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3418d-102">SYNOPSIS</span></span>
<span data-ttu-id="3418d-103">Egy Olyan táblázat átviteli sebességét kapja meg, amelybe be lehet ásni.</span><span class="sxs-lookup"><span data-stu-id="3418d-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="3418d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3418d-104">SYNTAX</span></span>

### <span data-ttu-id="3418d-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3418d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3418d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3418d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3418d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3418d-107">DESCRIPTION</span></span>
<span data-ttu-id="3418d-108">A **Get-AzCosmosDBTableThroughput** parancsmag kapja meg a sebességet egy TárolóDB táblázatban.</span><span class="sxs-lookup"><span data-stu-id="3418d-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="3418d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3418d-109">EXAMPLES</span></span>

### <span data-ttu-id="3418d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3418d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="3418d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3418d-111">PARAMETERS</span></span>

### <span data-ttu-id="3418d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3418d-112">-AccountName</span></span>
<span data-ttu-id="3418d-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="3418d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3418d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3418d-114">-DefaultProfile</span></span>
<span data-ttu-id="3418d-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3418d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3418d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3418d-116">-InputObject</span></span>
<span data-ttu-id="3418d-117">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="3418d-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="3418d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3418d-118">-Name</span></span>
<span data-ttu-id="3418d-119">A tábla neve.</span><span class="sxs-lookup"><span data-stu-id="3418d-119">Name of the Table.</span></span>

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

### <span data-ttu-id="3418d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3418d-120">-ResourceGroupName</span></span>
<span data-ttu-id="3418d-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3418d-121">Name of resource group.</span></span>

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

### <span data-ttu-id="3418d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3418d-122">CommonParameters</span></span>
<span data-ttu-id="3418d-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3418d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3418d-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3418d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3418d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3418d-125">INPUTS</span></span>

### <span data-ttu-id="3418d-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="3418d-126">None</span></span>

## <span data-ttu-id="3418d-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3418d-127">OUTPUTS</span></span>

### <span data-ttu-id="3418d-128">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="3418d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="3418d-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3418d-129">NOTES</span></span>

## <span data-ttu-id="3418d-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3418d-130">RELATED LINKS</span></span>
