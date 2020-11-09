---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298979"
---
# <span data-ttu-id="92803-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="92803-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="92803-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92803-102">SYNOPSIS</span></span>
<span data-ttu-id="92803-103">Frissíti a CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="92803-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="92803-104">Ügyféloldali javítás műveletet hajt végre a meglévő UserDefinedFunction elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="92803-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="92803-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92803-105">SYNTAX</span></span>

### <span data-ttu-id="92803-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92803-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92803-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92803-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92803-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92803-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92803-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="92803-109">DESCRIPTION</span></span>
<span data-ttu-id="92803-110">Frissíti a CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="92803-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="92803-111">Ügyféloldali javítás műveletet hajt végre a meglévő UserDefinedFunction elolvasásával.</span><span class="sxs-lookup"><span data-stu-id="92803-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="92803-112">Példák</span><span class="sxs-lookup"><span data-stu-id="92803-112">EXAMPLES</span></span>

### <span data-ttu-id="92803-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92803-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="92803-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92803-114">PARAMETERS</span></span>

### <span data-ttu-id="92803-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="92803-115">-AccountName</span></span>
<span data-ttu-id="92803-116">A Cosmos DB adatbázis-fiók neve.</span><span class="sxs-lookup"><span data-stu-id="92803-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="92803-117">-Body</span><span class="sxs-lookup"><span data-stu-id="92803-117">-Body</span></span>
<span data-ttu-id="92803-118">A felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="92803-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="92803-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="92803-119">-Confirm</span></span>
<span data-ttu-id="92803-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="92803-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92803-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="92803-121">-ContainerName</span></span>
<span data-ttu-id="92803-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="92803-122">Container name.</span></span>

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

### <span data-ttu-id="92803-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="92803-123">-DatabaseName</span></span>
<span data-ttu-id="92803-124">Az adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="92803-124">Database name.</span></span>

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

### <span data-ttu-id="92803-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92803-125">-DefaultProfile</span></span>
<span data-ttu-id="92803-126">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92803-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92803-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92803-127">-InputObject</span></span>
<span data-ttu-id="92803-128">SQL-felhasználó által definiált függvény objektum</span><span class="sxs-lookup"><span data-stu-id="92803-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92803-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92803-129">-Name</span></span>
<span data-ttu-id="92803-130">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="92803-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="92803-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="92803-131">-ParentObject</span></span>
<span data-ttu-id="92803-132">SQL-tároló objektum.</span><span class="sxs-lookup"><span data-stu-id="92803-132">Sql Container object.</span></span>

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

### <span data-ttu-id="92803-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92803-133">-ResourceGroupName</span></span>
<span data-ttu-id="92803-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="92803-134">Name of resource group.</span></span>

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

### <span data-ttu-id="92803-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92803-135">-WhatIf</span></span>
<span data-ttu-id="92803-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="92803-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92803-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="92803-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92803-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92803-138">CommonParameters</span></span>
<span data-ttu-id="92803-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92803-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92803-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="92803-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92803-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92803-141">INPUTS</span></span>

### <span data-ttu-id="92803-142">Microsoft. Azure. Command. CosmosDB. models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="92803-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="92803-143">Microsoft. Azure. Command. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="92803-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="92803-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92803-144">OUTPUTS</span></span>

### <span data-ttu-id="92803-145">Microsoft. Azure. Command. CosmosDB. models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="92803-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="92803-146">Microsoft. Azure. Command. CosmosDB. kivétellel. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="92803-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="92803-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92803-147">NOTES</span></span>

## <span data-ttu-id="92803-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92803-148">RELATED LINKS</span></span>
