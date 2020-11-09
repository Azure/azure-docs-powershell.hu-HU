---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299222"
---
# <span data-ttu-id="74376-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="74376-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="74376-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="74376-102">SYNOPSIS</span></span>
<span data-ttu-id="74376-103">Új CosmosDB SQL-StoredProcedure hoz létre.</span><span class="sxs-lookup"><span data-stu-id="74376-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="74376-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="74376-104">SYNTAX</span></span>

### <span data-ttu-id="74376-105">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="74376-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74376-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74376-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74376-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="74376-107">DESCRIPTION</span></span>
<span data-ttu-id="74376-108">Új CosmosDB SQL-StoredProcedure hoz létre.</span><span class="sxs-lookup"><span data-stu-id="74376-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="74376-109">Példák</span><span class="sxs-lookup"><span data-stu-id="74376-109">EXAMPLES</span></span>

### <span data-ttu-id="74376-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="74376-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="74376-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="74376-111">PARAMETERS</span></span>

### <span data-ttu-id="74376-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74376-112">-AccountName</span></span>
<span data-ttu-id="74376-113">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="74376-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="74376-114">-Body</span><span class="sxs-lookup"><span data-stu-id="74376-114">-Body</span></span>
<span data-ttu-id="74376-115">A tárolt eljárás törzse</span><span class="sxs-lookup"><span data-stu-id="74376-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="74376-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="74376-116">-Confirm</span></span>
<span data-ttu-id="74376-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="74376-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74376-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="74376-118">-ContainerName</span></span>
<span data-ttu-id="74376-119">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="74376-119">Container name.</span></span>

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

### <span data-ttu-id="74376-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74376-120">-DatabaseName</span></span>
<span data-ttu-id="74376-121">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="74376-121">Database name.</span></span>

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

### <span data-ttu-id="74376-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74376-122">-DefaultProfile</span></span>
<span data-ttu-id="74376-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="74376-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74376-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="74376-124">-Name</span></span>
<span data-ttu-id="74376-125">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="74376-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="74376-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="74376-126">-ParentObject</span></span>
<span data-ttu-id="74376-127">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="74376-127">Sql Container object.</span></span>

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

### <span data-ttu-id="74376-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74376-128">-ResourceGroupName</span></span>
<span data-ttu-id="74376-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="74376-129">Name of resource group.</span></span>

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

### <span data-ttu-id="74376-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74376-130">-WhatIf</span></span>
<span data-ttu-id="74376-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="74376-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74376-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="74376-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74376-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74376-133">CommonParameters</span></span>
<span data-ttu-id="74376-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="74376-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74376-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="74376-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74376-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="74376-136">INPUTS</span></span>

### <span data-ttu-id="74376-137">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="74376-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="74376-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="74376-138">OUTPUTS</span></span>

### <span data-ttu-id="74376-139">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="74376-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="74376-140">Microsoft. Azure. Command. CosmosDB. kivétellel. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="74376-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="74376-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="74376-141">NOTES</span></span>

## <span data-ttu-id="74376-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="74376-142">RELATED LINKS</span></span>
