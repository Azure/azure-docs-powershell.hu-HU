---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6631cad83260a935f2849391941ec0cf6514b188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010560"
---
# <span data-ttu-id="fb775-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="fb775-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="fb775-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb775-102">SYNOPSIS</span></span>
<span data-ttu-id="fb775-103">Megkapja a CosmosDB SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="fb775-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="fb775-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb775-104">SYNTAX</span></span>

### <span data-ttu-id="fb775-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb775-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb775-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb775-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb775-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb775-107">DESCRIPTION</span></span>
<span data-ttu-id="fb775-108">A **Get-AzCosmosDBSqlTrigger** parancsmag az adott ResourceGroupName, accountname, databasename és ContainerName minden meglévő CosmosDB SQL-eseményindítójának listáját kapja meg, és egy adott CosmosDB, ResourceGroupName, accountname, databasename, ContainerName, TriggerName,,,, és.</span><span class="sxs-lookup"><span data-stu-id="fb775-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="fb775-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb775-109">EXAMPLES</span></span>

### <span data-ttu-id="fb775-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fb775-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="fb775-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb775-111">PARAMETERS</span></span>

### <span data-ttu-id="fb775-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb775-112">-AccountName</span></span>
<span data-ttu-id="fb775-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="fb775-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fb775-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fb775-114">-ContainerName</span></span>
<span data-ttu-id="fb775-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="fb775-115">Container name.</span></span>

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

### <span data-ttu-id="fb775-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb775-116">-DatabaseName</span></span>
<span data-ttu-id="fb775-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="fb775-117">Database name.</span></span>

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

### <span data-ttu-id="fb775-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb775-118">-DefaultProfile</span></span>
<span data-ttu-id="fb775-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb775-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb775-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb775-120">-InputObject</span></span>
<span data-ttu-id="fb775-121">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="fb775-121">Sql Container object.</span></span>

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

### <span data-ttu-id="fb775-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fb775-122">-Name</span></span>
<span data-ttu-id="fb775-123">Trigger neve.</span><span class="sxs-lookup"><span data-stu-id="fb775-123">Trigger name.</span></span>

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

### <span data-ttu-id="fb775-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb775-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb775-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="fb775-125">Name of resource group.</span></span>

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

### <span data-ttu-id="fb775-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb775-126">CommonParameters</span></span>
<span data-ttu-id="fb775-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb775-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb775-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb775-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb775-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb775-129">INPUTS</span></span>

### <span data-ttu-id="fb775-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="fb775-130">None</span></span>

## <span data-ttu-id="fb775-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb775-131">OUTPUTS</span></span>

### <span data-ttu-id="fb775-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="fb775-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="fb775-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb775-133">NOTES</span></span>

## <span data-ttu-id="fb775-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb775-134">RELATED LINKS</span></span>
