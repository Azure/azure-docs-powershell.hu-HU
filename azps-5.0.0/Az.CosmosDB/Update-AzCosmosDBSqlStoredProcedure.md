---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298991"
---
# <span data-ttu-id="3960d-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="3960d-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="3960d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3960d-102">SYNOPSIS</span></span>
<span data-ttu-id="3960d-103">Frissíti a CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="3960d-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="3960d-104">Ügyféloldali javítás műveletet hajt végre a meglévő StoredProcedure elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="3960d-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="3960d-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3960d-105">SYNTAX</span></span>

### <span data-ttu-id="3960d-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3960d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3960d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3960d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3960d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3960d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3960d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3960d-109">DESCRIPTION</span></span>
<span data-ttu-id="3960d-110">Frissíti a CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="3960d-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="3960d-111">Ügyféloldali javítás műveletet hajt végre a meglévő StoredProcedure elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="3960d-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="3960d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3960d-112">EXAMPLES</span></span>

### <span data-ttu-id="3960d-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3960d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="3960d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3960d-114">PARAMETERS</span></span>

### <span data-ttu-id="3960d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3960d-115">-AccountName</span></span>
<span data-ttu-id="3960d-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="3960d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3960d-117">-Body</span><span class="sxs-lookup"><span data-stu-id="3960d-117">-Body</span></span>
<span data-ttu-id="3960d-118">A tárolt eljárás törzse</span><span class="sxs-lookup"><span data-stu-id="3960d-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="3960d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3960d-119">-Confirm</span></span>
<span data-ttu-id="3960d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3960d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3960d-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3960d-121">-ContainerName</span></span>
<span data-ttu-id="3960d-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="3960d-122">Container name.</span></span>

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

### <span data-ttu-id="3960d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3960d-123">-DatabaseName</span></span>
<span data-ttu-id="3960d-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="3960d-124">Database name.</span></span>

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

### <span data-ttu-id="3960d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3960d-125">-DefaultProfile</span></span>
<span data-ttu-id="3960d-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3960d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3960d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3960d-127">-InputObject</span></span>
<span data-ttu-id="3960d-128">SQL tárolt eljárás objektum</span><span class="sxs-lookup"><span data-stu-id="3960d-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3960d-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3960d-129">-Name</span></span>
<span data-ttu-id="3960d-130">A Prcodecure tárolt név.</span><span class="sxs-lookup"><span data-stu-id="3960d-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="3960d-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3960d-131">-ParentObject</span></span>
<span data-ttu-id="3960d-132">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="3960d-132">Sql Container object.</span></span>

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

### <span data-ttu-id="3960d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3960d-133">-ResourceGroupName</span></span>
<span data-ttu-id="3960d-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="3960d-134">Name of resource group.</span></span>

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

### <span data-ttu-id="3960d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3960d-135">-WhatIf</span></span>
<span data-ttu-id="3960d-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3960d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3960d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3960d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3960d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3960d-138">CommonParameters</span></span>
<span data-ttu-id="3960d-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3960d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3960d-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3960d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3960d-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3960d-141">INPUTS</span></span>

### <span data-ttu-id="3960d-142">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="3960d-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="3960d-143">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="3960d-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="3960d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3960d-144">OUTPUTS</span></span>

### <span data-ttu-id="3960d-145">Microsoft. Azure. Command. CosmosDB. models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="3960d-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="3960d-146">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="3960d-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="3960d-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3960d-147">NOTES</span></span>

## <span data-ttu-id="3960d-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3960d-148">RELATED LINKS</span></span>
