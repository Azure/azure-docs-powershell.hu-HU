---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014882"
---
# <span data-ttu-id="fdf5c-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="fdf5c-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="fdf5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdf5c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf5c-103">Beolvassa a CosmosDB táblázatot.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="fdf5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdf5c-104">SYNTAX</span></span>

### <span data-ttu-id="fdf5c-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fdf5c-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf5c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdf5c-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf5c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdf5c-107">DESCRIPTION</span></span>
<span data-ttu-id="fdf5c-108">A **Get-AzCosmosDBTable** parancsmag meglévő táblát kap.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="fdf5c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fdf5c-109">EXAMPLES</span></span>

### <span data-ttu-id="fdf5c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdf5c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="fdf5c-111">Az erőforrás-objektum a táblázat _rid, _ts, _ ETAG tulajdonságait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="fdf5c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdf5c-112">PARAMETERS</span></span>

### <span data-ttu-id="fdf5c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fdf5c-113">-AccountName</span></span>
<span data-ttu-id="fdf5c-114">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fdf5c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf5c-115">-DefaultProfile</span></span>
<span data-ttu-id="fdf5c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf5c-117">– Részletes</span><span class="sxs-lookup"><span data-stu-id="fdf5c-117">-Detailed</span></span>
<span data-ttu-id="fdf5c-118">Ha meg van határozva, akkor a parancsmag a megfelelő átviteli értékkel rendelkező táblát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf5c-119">-InputObject</span></span>
<span data-ttu-id="fdf5c-120">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="fdf5c-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf5c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdf5c-121">-Name</span></span>
<span data-ttu-id="fdf5c-122">A táblázat neve.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-122">Name of the Table.</span></span>

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

### <span data-ttu-id="fdf5c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf5c-123">-ResourceGroupName</span></span>
<span data-ttu-id="fdf5c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-124">Name of resource group.</span></span>

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

### <span data-ttu-id="fdf5c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf5c-125">CommonParameters</span></span>
<span data-ttu-id="fdf5c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdf5c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf5c-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdf5c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf5c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdf5c-128">INPUTS</span></span>

### <span data-ttu-id="fdf5c-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fdf5c-129">None</span></span>

## <span data-ttu-id="fdf5c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdf5c-130">OUTPUTS</span></span>

### <span data-ttu-id="fdf5c-131">Microsoft. Azure. Command. CosmosDB. models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fdf5c-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="fdf5c-132">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="fdf5c-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="fdf5c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdf5c-133">NOTES</span></span>

## <span data-ttu-id="fdf5c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdf5c-134">RELATED LINKS</span></span>
