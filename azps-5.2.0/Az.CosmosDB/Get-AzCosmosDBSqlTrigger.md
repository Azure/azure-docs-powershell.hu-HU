---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372397"
---
# <span data-ttu-id="33b1a-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="33b1a-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="33b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="33b1a-103">Lejátsa a 2016-os Sql Triggert.</span><span class="sxs-lookup"><span data-stu-id="33b1a-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="33b1a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33b1a-104">SYNTAX</span></span>

### <span data-ttu-id="33b1a-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b1a-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33b1a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33b1a-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b1a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33b1a-107">DESCRIPTION</span></span>
<span data-ttu-id="33b1a-108">A **Get-AzCosmosDBSqlTrigger** parancsmag egy adott ResourceGroupName, AccountName, DatabaseName és ContainerName típusú erőforráshoz az összes meglévő, AbDB Sql Trigger listáját tartalmazza, és egy adott ResourceGroupName, AccountName, ContainerName és TriggerName esetén egyetlen.</span><span class="sxs-lookup"><span data-stu-id="33b1a-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="33b1a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33b1a-109">EXAMPLES</span></span>

### <span data-ttu-id="33b1a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="33b1a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="33b1a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33b1a-111">PARAMETERS</span></span>

### <span data-ttu-id="33b1a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33b1a-112">-AccountName</span></span>
<span data-ttu-id="33b1a-113">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="33b1a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="33b1a-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="33b1a-114">-ContainerName</span></span>
<span data-ttu-id="33b1a-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="33b1a-115">Container name.</span></span>

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

### <span data-ttu-id="33b1a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33b1a-116">-DatabaseName</span></span>
<span data-ttu-id="33b1a-117">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="33b1a-117">Database name.</span></span>

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

### <span data-ttu-id="33b1a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b1a-118">-DefaultProfile</span></span>
<span data-ttu-id="33b1a-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33b1a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b1a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="33b1a-120">-Name</span></span>
<span data-ttu-id="33b1a-121">Eseményindító neve.</span><span class="sxs-lookup"><span data-stu-id="33b1a-121">Trigger name.</span></span>

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

### <span data-ttu-id="33b1a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="33b1a-122">-ParentObject</span></span>
<span data-ttu-id="33b1a-123">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="33b1a-123">Sql Container object.</span></span>

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

### <span data-ttu-id="33b1a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b1a-124">-ResourceGroupName</span></span>
<span data-ttu-id="33b1a-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="33b1a-125">Name of resource group.</span></span>

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

### <span data-ttu-id="33b1a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b1a-126">CommonParameters</span></span>
<span data-ttu-id="33b1a-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b1a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b1a-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33b1a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b1a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33b1a-129">INPUTS</span></span>

### <span data-ttu-id="33b1a-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="33b1a-130">None</span></span>

## <span data-ttu-id="33b1a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33b1a-131">OUTPUTS</span></span>

### <span data-ttu-id="33b1a-132">Microsoft.Azure.Commands.CossDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="33b1a-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="33b1a-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33b1a-133">NOTES</span></span>

## <span data-ttu-id="33b1a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33b1a-134">RELATED LINKS</span></span>
