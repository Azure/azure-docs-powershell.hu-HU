---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: f1fb191a235cdf1c98768d3201cab49278f4403c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922041"
---
# <span data-ttu-id="2ab7a-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="2ab7a-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="2ab7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab7a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab7a-103">A 2016-os Sql StoredProcedure-t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="2ab7a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ab7a-104">SYNTAX</span></span>

### <span data-ttu-id="2ab7a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ab7a-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab7a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ab7a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab7a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ab7a-107">DESCRIPTION</span></span>
<span data-ttu-id="2ab7a-108">A **Get-AzCosmosDBSqlStoredProcedure** parancsmag az adott ResourceGroupName, AccountName, DatabaseName és ContainerName esetén az összes meglévő, Már létező Sql StoredProcedure-rekordot megkapja, és egy adott ResourceGroupName, AccountName, ContainerName és StoredProcedureName fájlhoz egyetlen, aTárTárNeve és a StoredProcedureName fájlhoz kap egy adott SqlGroupName, AccountName, ContainerName és StoredProcedureName rekordot.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="2ab7a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ab7a-109">EXAMPLES</span></span>

### <span data-ttu-id="2ab7a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="2ab7a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="2ab7a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ab7a-111">PARAMETERS</span></span>

### <span data-ttu-id="2ab7a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ab7a-112">-AccountName</span></span>
<span data-ttu-id="2ab7a-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2ab7a-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2ab7a-114">-ContainerName</span></span>
<span data-ttu-id="2ab7a-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-115">Container name.</span></span>

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

### <span data-ttu-id="2ab7a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2ab7a-116">-DatabaseName</span></span>
<span data-ttu-id="2ab7a-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-117">Database name.</span></span>

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

### <span data-ttu-id="2ab7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab7a-118">-DefaultProfile</span></span>
<span data-ttu-id="2ab7a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab7a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2ab7a-120">-Name</span></span>
<span data-ttu-id="2ab7a-121">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="2ab7a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2ab7a-122">-ParentObject</span></span>
<span data-ttu-id="2ab7a-123">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-123">Sql Container object.</span></span>

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

### <span data-ttu-id="2ab7a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab7a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ab7a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="2ab7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab7a-126">CommonParameters</span></span>
<span data-ttu-id="2ab7a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab7a-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ab7a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab7a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ab7a-129">INPUTS</span></span>

### <span data-ttu-id="2ab7a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="2ab7a-130">None</span></span>

## <span data-ttu-id="2ab7a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ab7a-131">OUTPUTS</span></span>

### <span data-ttu-id="2ab7a-132">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="2ab7a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="2ab7a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ab7a-133">NOTES</span></span>

## <span data-ttu-id="2ab7a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ab7a-134">RELATED LINKS</span></span>
