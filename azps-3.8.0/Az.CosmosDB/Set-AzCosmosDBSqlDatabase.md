---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010554"
---
# <span data-ttu-id="18393-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="18393-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="18393-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="18393-102">SYNOPSIS</span></span>
<span data-ttu-id="18393-103">Új CosmosDB hoz létre, vagy frissít egy meglévő SQL-adatbázist.</span><span class="sxs-lookup"><span data-stu-id="18393-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="18393-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="18393-104">SYNTAX</span></span>

### <span data-ttu-id="18393-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18393-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18393-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18393-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18393-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="18393-107">DESCRIPTION</span></span>
<span data-ttu-id="18393-108">A **set-AzCosmosDBSqlDatabase** parancsmag új, meglévő CosmosDB SQL-adatbázist hoz létre, vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="18393-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="18393-109">Példák</span><span class="sxs-lookup"><span data-stu-id="18393-109">EXAMPLES</span></span>

### <span data-ttu-id="18393-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="18393-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="18393-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="18393-111">PARAMETERS</span></span>

### <span data-ttu-id="18393-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18393-112">-AccountName</span></span>
<span data-ttu-id="18393-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="18393-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="18393-114">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="18393-114">-Confirm</span></span>
<span data-ttu-id="18393-115">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="18393-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18393-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18393-116">-DefaultProfile</span></span>
<span data-ttu-id="18393-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18393-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18393-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18393-118">-InputObject</span></span>
<span data-ttu-id="18393-119">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="18393-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18393-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="18393-120">-Name</span></span>
<span data-ttu-id="18393-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="18393-121">Database name.</span></span>

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

### <span data-ttu-id="18393-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18393-122">-ResourceGroupName</span></span>
<span data-ttu-id="18393-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18393-123">Name of resource group.</span></span>

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

### <span data-ttu-id="18393-124">-Forgalom</span><span class="sxs-lookup"><span data-stu-id="18393-124">-Throughput</span></span>
<span data-ttu-id="18393-125">Az SQL-adatbázis (RU/s) átviteli sebessége.</span><span class="sxs-lookup"><span data-stu-id="18393-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="18393-126">Az alapértelmezett érték a 400.</span><span class="sxs-lookup"><span data-stu-id="18393-126">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18393-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18393-127">-WhatIf</span></span>
<span data-ttu-id="18393-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="18393-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18393-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18393-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18393-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18393-130">CommonParameters</span></span>
<span data-ttu-id="18393-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="18393-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18393-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="18393-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18393-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="18393-133">INPUTS</span></span>

### <span data-ttu-id="18393-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="18393-134">None</span></span>

## <span data-ttu-id="18393-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18393-135">OUTPUTS</span></span>

### <span data-ttu-id="18393-136">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="18393-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="18393-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="18393-137">NOTES</span></span>

## <span data-ttu-id="18393-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18393-138">RELATED LINKS</span></span>
