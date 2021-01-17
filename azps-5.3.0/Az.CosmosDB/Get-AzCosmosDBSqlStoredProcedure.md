---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480603"
---
# <span data-ttu-id="eb1aa-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="eb1aa-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="eb1aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1aa-103">A 2016-os Sql StoredProcedure-t kapja meg.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="eb1aa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb1aa-104">SYNTAX</span></span>

### <span data-ttu-id="eb1aa-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb1aa-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb1aa-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb1aa-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb1aa-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb1aa-107">DESCRIPTION</span></span>
<span data-ttu-id="eb1aa-108">A **Get-AzCosmosDBSqlStoredProcedure** parancsmag lekérte az adott ResourceGroupName, AccountName, DatabaseName és ContainerName rendszerekhez meglévő Összes meglévő, AzOsmosDB Sql StoredProcedure parancsmagot, és egy adott ResourceGroupName, AccountName, ContainerName és StoredProcedureName fájlhoz kap egy adott Sql StoredProcedure-t.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="eb1aa-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb1aa-109">EXAMPLES</span></span>

### <span data-ttu-id="eb1aa-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="eb1aa-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="eb1aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb1aa-111">PARAMETERS</span></span>

### <span data-ttu-id="eb1aa-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eb1aa-112">-AccountName</span></span>
<span data-ttu-id="eb1aa-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="eb1aa-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="eb1aa-114">-ContainerName</span></span>
<span data-ttu-id="eb1aa-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-115">Container name.</span></span>

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

### <span data-ttu-id="eb1aa-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb1aa-116">-DatabaseName</span></span>
<span data-ttu-id="eb1aa-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-117">Database name.</span></span>

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

### <span data-ttu-id="eb1aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1aa-118">-DefaultProfile</span></span>
<span data-ttu-id="eb1aa-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1aa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eb1aa-120">-Name</span></span>
<span data-ttu-id="eb1aa-121">Tárolt Prcodecure-név.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="eb1aa-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="eb1aa-122">-ParentObject</span></span>
<span data-ttu-id="eb1aa-123">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-123">Sql Container object.</span></span>

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

### <span data-ttu-id="eb1aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb1aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb1aa-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-125">Name of resource group.</span></span>

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

### <span data-ttu-id="eb1aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1aa-126">CommonParameters</span></span>
<span data-ttu-id="eb1aa-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1aa-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb1aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1aa-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb1aa-129">INPUTS</span></span>

### <span data-ttu-id="eb1aa-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb1aa-130">None</span></span>

## <span data-ttu-id="eb1aa-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb1aa-131">OUTPUTS</span></span>

### <span data-ttu-id="eb1aa-132">Microsoft.Azure.Commands.CossDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="eb1aa-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="eb1aa-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb1aa-133">NOTES</span></span>

## <span data-ttu-id="eb1aa-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb1aa-134">RELATED LINKS</span></span>
