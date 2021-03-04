---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 0dfcffe55eb3214f4be9d6ccfb34231d1c9ea50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940570"
---
# <span data-ttu-id="4984a-101">Get-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="4984a-101">Get-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="4984a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4984a-102">SYNOPSIS</span></span>
<span data-ttu-id="4984a-103">A TamakDB MongoDB adatbázist kapja</span><span class="sxs-lookup"><span data-stu-id="4984a-103">Gets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="4984a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4984a-104">SYNTAX</span></span>

### <span data-ttu-id="4984a-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4984a-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4984a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4984a-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4984a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4984a-107">DESCRIPTION</span></span>
<span data-ttu-id="4984a-108">A **Get-AzCosmosDBMongoDBDatabase** parancsmag megkapja a TamakDB MongoDB adatbázist.</span><span class="sxs-lookup"><span data-stu-id="4984a-108">The **Get-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="4984a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4984a-109">EXAMPLES</span></span>

### <span data-ttu-id="4984a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4984a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="4984a-111">Az Erőforrásobjektum _rid, _ts, _etag tulajdonságokat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="4984a-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="4984a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4984a-112">PARAMETERS</span></span>

### <span data-ttu-id="4984a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4984a-113">-AccountName</span></span>
<span data-ttu-id="4984a-114">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="4984a-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4984a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4984a-115">-DefaultProfile</span></span>
<span data-ttu-id="4984a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4984a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4984a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4984a-117">-Name</span></span>
<span data-ttu-id="4984a-118">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4984a-118">Database name.</span></span>

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

### <span data-ttu-id="4984a-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4984a-119">-ParentObject</span></span>
<span data-ttu-id="4984a-120">ABB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="4984a-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4984a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4984a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4984a-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4984a-122">Name of resource group.</span></span>

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

### <span data-ttu-id="4984a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4984a-123">CommonParameters</span></span>
<span data-ttu-id="4984a-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4984a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4984a-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4984a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4984a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4984a-126">INPUTS</span></span>

### <span data-ttu-id="4984a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4984a-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4984a-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4984a-128">OUTPUTS</span></span>

### <span data-ttu-id="4984a-129">Microsoft.Azure.Commands.EzresDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="4984a-129">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

### <span data-ttu-id="4984a-130">Microsoft.Azure.Commands.CossDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4984a-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4984a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4984a-131">NOTES</span></span>

## <span data-ttu-id="4984a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4984a-132">RELATED LINKS</span></span>
