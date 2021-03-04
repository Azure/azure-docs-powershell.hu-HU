---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 28b616315913ae70722b5a600d4b10879c7b8334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936250"
---
# <span data-ttu-id="baf49-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="baf49-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="baf49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baf49-102">SYNOPSIS</span></span>
<span data-ttu-id="baf49-103">Beveszi a 2010-es sql triggert.</span><span class="sxs-lookup"><span data-stu-id="baf49-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="baf49-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="baf49-104">SYNTAX</span></span>

### <span data-ttu-id="baf49-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf49-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baf49-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf49-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baf49-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="baf49-107">DESCRIPTION</span></span>
<span data-ttu-id="baf49-108">A **Get-AzCosmosDBSqlTrigger** parancsmag egy adott ResourceGroupName, AccountName, DatabaseName és ContainerName típusú erőforráshoz az összes meglévő, AbDB Sql Trigger listáját tartalmazza, és egy adott ResourceGroupName, AccountName, ContainerName és TriggerName típusú eseményindítót kap.</span><span class="sxs-lookup"><span data-stu-id="baf49-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="baf49-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="baf49-109">EXAMPLES</span></span>

### <span data-ttu-id="baf49-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="baf49-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="baf49-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baf49-111">PARAMETERS</span></span>

### <span data-ttu-id="baf49-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="baf49-112">-AccountName</span></span>
<span data-ttu-id="baf49-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="baf49-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="baf49-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="baf49-114">-ContainerName</span></span>
<span data-ttu-id="baf49-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="baf49-115">Container name.</span></span>

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

### <span data-ttu-id="baf49-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="baf49-116">-DatabaseName</span></span>
<span data-ttu-id="baf49-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="baf49-117">Database name.</span></span>

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

### <span data-ttu-id="baf49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf49-118">-DefaultProfile</span></span>
<span data-ttu-id="baf49-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baf49-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf49-120">-Name</span><span class="sxs-lookup"><span data-stu-id="baf49-120">-Name</span></span>
<span data-ttu-id="baf49-121">Eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="baf49-121">Trigger name.</span></span>

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

### <span data-ttu-id="baf49-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="baf49-122">-ParentObject</span></span>
<span data-ttu-id="baf49-123">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="baf49-123">Sql Container object.</span></span>

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

### <span data-ttu-id="baf49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf49-124">-ResourceGroupName</span></span>
<span data-ttu-id="baf49-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="baf49-125">Name of resource group.</span></span>

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

### <span data-ttu-id="baf49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf49-126">CommonParameters</span></span>
<span data-ttu-id="baf49-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf49-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baf49-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf49-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baf49-129">INPUTS</span></span>

### <span data-ttu-id="baf49-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="baf49-130">None</span></span>

## <span data-ttu-id="baf49-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf49-131">OUTPUTS</span></span>

### <span data-ttu-id="baf49-132">Microsoft.Azure.Commands.CossDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="baf49-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="baf49-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="baf49-133">NOTES</span></span>

## <span data-ttu-id="baf49-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baf49-134">RELATED LINKS</span></span>
