---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 10faa4b020633fdf46122c4864d50f00ef3ba54c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299486"
---
# <span data-ttu-id="de002-101">Get-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="de002-101">Get-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="de002-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de002-102">SYNOPSIS</span></span>
<span data-ttu-id="de002-103">Megkapja a CosmosDB SQL-triggert.</span><span class="sxs-lookup"><span data-stu-id="de002-103">Gets the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="de002-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de002-104">SYNTAX</span></span>

### <span data-ttu-id="de002-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="de002-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de002-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de002-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlTrigger [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de002-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="de002-107">DESCRIPTION</span></span>
<span data-ttu-id="de002-108">A **Get-AzCosmosDBSqlTrigger** parancsmag az adott ResourceGroupName, accountname, databasename és ContainerName minden meglévő CosmosDB SQL-eseményindítójának listáját kapja meg, és egy adott CosmosDB, ResourceGroupName, accountname, databasename, ContainerName, TriggerName,,,, és.</span><span class="sxs-lookup"><span data-stu-id="de002-108">The **Get-AzCosmosDBSqlTrigger** cmdlet gets the list of all existing CosmosDB Sql Triggers for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql Trigger for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and TriggerName.</span></span>

## <span data-ttu-id="de002-109">Példák</span><span class="sxs-lookup"><span data-stu-id="de002-109">EXAMPLES</span></span>

### <span data-ttu-id="de002-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de002-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} 

Name                   : {triggerName}
Id                     : {triggerId}
Resource               : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="de002-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de002-111">PARAMETERS</span></span>

### <span data-ttu-id="de002-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de002-112">-AccountName</span></span>
<span data-ttu-id="de002-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="de002-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="de002-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="de002-114">-ContainerName</span></span>
<span data-ttu-id="de002-115">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="de002-115">Container name.</span></span>

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

### <span data-ttu-id="de002-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de002-116">-DatabaseName</span></span>
<span data-ttu-id="de002-117">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="de002-117">Database name.</span></span>

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

### <span data-ttu-id="de002-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de002-118">-DefaultProfile</span></span>
<span data-ttu-id="de002-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de002-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de002-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de002-120">-Name</span></span>
<span data-ttu-id="de002-121">Trigger neve.</span><span class="sxs-lookup"><span data-stu-id="de002-121">Trigger name.</span></span>

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

### <span data-ttu-id="de002-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="de002-122">-ParentObject</span></span>
<span data-ttu-id="de002-123">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="de002-123">Sql Container object.</span></span>

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

### <span data-ttu-id="de002-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de002-124">-ResourceGroupName</span></span>
<span data-ttu-id="de002-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de002-125">Name of resource group.</span></span>

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

### <span data-ttu-id="de002-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de002-126">CommonParameters</span></span>
<span data-ttu-id="de002-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de002-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de002-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="de002-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de002-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de002-129">INPUTS</span></span>

### <span data-ttu-id="de002-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="de002-130">None</span></span>

## <span data-ttu-id="de002-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de002-131">OUTPUTS</span></span>

### <span data-ttu-id="de002-132">Microsoft. Azure. Command. CosmosDB. models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="de002-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="de002-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de002-133">NOTES</span></span>

## <span data-ttu-id="de002-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de002-134">RELATED LINKS</span></span>
