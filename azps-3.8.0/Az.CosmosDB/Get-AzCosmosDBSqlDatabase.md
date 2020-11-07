---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847337"
---
# <span data-ttu-id="1112b-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1112b-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="1112b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1112b-102">SYNOPSIS</span></span>
<span data-ttu-id="1112b-103">Megkapja a CosmosDB SQL-adatbázisát.</span><span class="sxs-lookup"><span data-stu-id="1112b-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="1112b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1112b-104">SYNTAX</span></span>

### <span data-ttu-id="1112b-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1112b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1112b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1112b-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1112b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1112b-107">DESCRIPTION</span></span>
<span data-ttu-id="1112b-108">A **Get-AzCosmosDBSqlDatabase parancsmag beolvassa** az adott ResourceGroupName tartozó összes meglévő CosmosDB-SQL-adatbázis listáját, és egy adott CosmosDB, ResourceGroupName, accountname, databasename és ContainerName egyetlen SQL-adatbázist kap.</span><span class="sxs-lookup"><span data-stu-id="1112b-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="1112b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1112b-109">EXAMPLES</span></span>

### <span data-ttu-id="1112b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1112b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="1112b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1112b-111">PARAMETERS</span></span>

### <span data-ttu-id="1112b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1112b-112">-AccountName</span></span>
<span data-ttu-id="1112b-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="1112b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1112b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1112b-114">-DefaultProfile</span></span>
<span data-ttu-id="1112b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1112b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1112b-116">– Részletes</span><span class="sxs-lookup"><span data-stu-id="1112b-116">-Detailed</span></span>
<span data-ttu-id="1112b-117">Ha meg van határozva, akkor a parancsmag a megadott átviteli értékkel rendelkező tárolót adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1112b-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="1112b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1112b-118">-InputObject</span></span>
<span data-ttu-id="1112b-119">CosmosDB-fiók objektum</span><span class="sxs-lookup"><span data-stu-id="1112b-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1112b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1112b-120">-Name</span></span>
<span data-ttu-id="1112b-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="1112b-121">Database name.</span></span>

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

### <span data-ttu-id="1112b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1112b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1112b-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1112b-123">Name of resource group.</span></span>

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

### <span data-ttu-id="1112b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1112b-124">CommonParameters</span></span>
<span data-ttu-id="1112b-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1112b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1112b-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1112b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1112b-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1112b-127">INPUTS</span></span>

### <span data-ttu-id="1112b-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="1112b-128">None</span></span>

## <span data-ttu-id="1112b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1112b-129">OUTPUTS</span></span>

### <span data-ttu-id="1112b-130">Microsoft. Azure. Command. CosmosDB. models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1112b-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="1112b-131">Microsoft. Azure. Command. CosmosDB. models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1112b-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1112b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1112b-132">NOTES</span></span>

## <span data-ttu-id="1112b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1112b-133">RELATED LINKS</span></span>
