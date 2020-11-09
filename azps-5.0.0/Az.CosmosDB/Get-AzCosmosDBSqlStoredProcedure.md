---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299489"
---
# <span data-ttu-id="4ddab-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="4ddab-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="4ddab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ddab-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddab-103">Megkapja a CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="4ddab-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="4ddab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ddab-104">SYNTAX</span></span>

### <span data-ttu-id="4ddab-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ddab-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ddab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ddab-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ddab-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ddab-107">DESCRIPTION</span></span>
<span data-ttu-id="4ddab-108">A **Get-AzCosmosDBSqlStoredProcedure** parancsmag minden létező SQL-StoredProcedures-CosmosDB megjelenik egy adott ResourceGroupName, accountname, databasename és ContainerName, és egy CosmosDB-StoredProcedure, ResourceGroupName, accountname, databasename, ContainerName, StoredProcedureName és.</span><span class="sxs-lookup"><span data-stu-id="4ddab-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="4ddab-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ddab-109">EXAMPLES</span></span>

### <span data-ttu-id="4ddab-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ddab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="4ddab-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ddab-111">PARAMETERS</span></span>

### <span data-ttu-id="4ddab-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4ddab-112">-AccountName</span></span>
<span data-ttu-id="4ddab-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="4ddab-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4ddab-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="4ddab-114">-ContainerName</span></span>
<span data-ttu-id="4ddab-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="4ddab-115">Container name.</span></span>

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

### <span data-ttu-id="4ddab-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ddab-116">-DatabaseName</span></span>
<span data-ttu-id="4ddab-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="4ddab-117">Database name.</span></span>

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

### <span data-ttu-id="4ddab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ddab-118">-DefaultProfile</span></span>
<span data-ttu-id="4ddab-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ddab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ddab-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4ddab-120">-Name</span></span>
<span data-ttu-id="4ddab-121">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="4ddab-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="4ddab-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4ddab-122">-ParentObject</span></span>
<span data-ttu-id="4ddab-123">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="4ddab-123">Sql Container object.</span></span>

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

### <span data-ttu-id="4ddab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ddab-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ddab-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ddab-125">Name of resource group.</span></span>

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

### <span data-ttu-id="4ddab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddab-126">CommonParameters</span></span>
<span data-ttu-id="4ddab-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ddab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddab-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ddab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddab-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ddab-129">INPUTS</span></span>

### <span data-ttu-id="4ddab-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="4ddab-130">None</span></span>

## <span data-ttu-id="4ddab-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ddab-131">OUTPUTS</span></span>

### <span data-ttu-id="4ddab-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="4ddab-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="4ddab-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ddab-133">NOTES</span></span>

## <span data-ttu-id="4ddab-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ddab-134">RELATED LINKS</span></span>
