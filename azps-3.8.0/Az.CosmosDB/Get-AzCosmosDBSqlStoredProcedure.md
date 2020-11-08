---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010561"
---
# <span data-ttu-id="a21c0-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="a21c0-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="a21c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a21c0-102">SYNOPSIS</span></span>
<span data-ttu-id="a21c0-103">Megkapja a CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a21c0-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="a21c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a21c0-104">SYNTAX</span></span>

### <span data-ttu-id="a21c0-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a21c0-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a21c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a21c0-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a21c0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a21c0-107">DESCRIPTION</span></span>
<span data-ttu-id="a21c0-108">A **Get-AzCosmosDBSqlStoredProcedure** parancsmag minden létező SQL-StoredProcedures-CosmosDB megjelenik egy adott ResourceGroupName, accountname, databasename és ContainerName, és egy CosmosDB-StoredProcedure, ResourceGroupName, accountname, databasename, ContainerName, StoredProcedureName és.</span><span class="sxs-lookup"><span data-stu-id="a21c0-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="a21c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a21c0-109">EXAMPLES</span></span>

### <span data-ttu-id="a21c0-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a21c0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="a21c0-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a21c0-111">PARAMETERS</span></span>

### <span data-ttu-id="a21c0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a21c0-112">-AccountName</span></span>
<span data-ttu-id="a21c0-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a21c0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a21c0-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a21c0-114">-ContainerName</span></span>
<span data-ttu-id="a21c0-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="a21c0-115">Container name.</span></span>

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

### <span data-ttu-id="a21c0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a21c0-116">-DatabaseName</span></span>
<span data-ttu-id="a21c0-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="a21c0-117">Database name.</span></span>

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

### <span data-ttu-id="a21c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21c0-118">-DefaultProfile</span></span>
<span data-ttu-id="a21c0-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a21c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21c0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a21c0-120">-InputObject</span></span>
<span data-ttu-id="a21c0-121">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="a21c0-121">Sql Container object.</span></span>

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

### <span data-ttu-id="a21c0-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a21c0-122">-Name</span></span>
<span data-ttu-id="a21c0-123">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="a21c0-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="a21c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a21c0-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a21c0-125">Name of resource group.</span></span>

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

### <span data-ttu-id="a21c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21c0-126">CommonParameters</span></span>
<span data-ttu-id="a21c0-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a21c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21c0-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a21c0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21c0-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a21c0-129">INPUTS</span></span>

### <span data-ttu-id="a21c0-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="a21c0-130">None</span></span>

## <span data-ttu-id="a21c0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a21c0-131">OUTPUTS</span></span>

### <span data-ttu-id="a21c0-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="a21c0-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="a21c0-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a21c0-133">NOTES</span></span>

## <span data-ttu-id="a21c0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a21c0-134">RELATED LINKS</span></span>
