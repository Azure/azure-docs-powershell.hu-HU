---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480516"
---
# <span data-ttu-id="18af7-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="18af7-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="18af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18af7-102">SYNOPSIS</span></span>
<span data-ttu-id="18af7-103">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="18af7-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="18af7-104">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="18af7-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="18af7-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="18af7-105">SYNTAX</span></span>

### <span data-ttu-id="18af7-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="18af7-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18af7-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18af7-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="18af7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18af7-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18af7-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="18af7-109">DESCRIPTION</span></span>
<span data-ttu-id="18af7-110">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="18af7-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="18af7-111">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="18af7-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="18af7-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="18af7-112">EXAMPLES</span></span>

### <span data-ttu-id="18af7-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="18af7-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="18af7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18af7-114">PARAMETERS</span></span>

### <span data-ttu-id="18af7-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="18af7-115">-AccountName</span></span>
<span data-ttu-id="18af7-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="18af7-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="18af7-117">-Body</span><span class="sxs-lookup"><span data-stu-id="18af7-117">-Body</span></span>
<span data-ttu-id="18af7-118">A Felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="18af7-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="18af7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18af7-119">-Confirm</span></span>
<span data-ttu-id="18af7-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="18af7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18af7-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="18af7-121">-ContainerName</span></span>
<span data-ttu-id="18af7-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="18af7-122">Container name.</span></span>

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

### <span data-ttu-id="18af7-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="18af7-123">-DatabaseName</span></span>
<span data-ttu-id="18af7-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="18af7-124">Database name.</span></span>

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

### <span data-ttu-id="18af7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18af7-125">-DefaultProfile</span></span>
<span data-ttu-id="18af7-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="18af7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18af7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18af7-127">-InputObject</span></span>
<span data-ttu-id="18af7-128">Sql felhasználó által definiált függvényobjektum</span><span class="sxs-lookup"><span data-stu-id="18af7-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="18af7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="18af7-129">-Name</span></span>
<span data-ttu-id="18af7-130">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="18af7-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="18af7-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="18af7-131">-ParentObject</span></span>
<span data-ttu-id="18af7-132">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="18af7-132">Sql Container object.</span></span>

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

### <span data-ttu-id="18af7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18af7-133">-ResourceGroupName</span></span>
<span data-ttu-id="18af7-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="18af7-134">Name of resource group.</span></span>

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

### <span data-ttu-id="18af7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18af7-135">-WhatIf</span></span>
<span data-ttu-id="18af7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="18af7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18af7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="18af7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18af7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18af7-138">CommonParameters</span></span>
<span data-ttu-id="18af7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18af7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18af7-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18af7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18af7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18af7-141">INPUTS</span></span>

### <span data-ttu-id="18af7-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="18af7-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="18af7-143">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="18af7-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="18af7-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="18af7-144">OUTPUTS</span></span>

### <span data-ttu-id="18af7-145">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="18af7-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="18af7-146">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="18af7-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="18af7-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="18af7-147">NOTES</span></span>

## <span data-ttu-id="18af7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="18af7-148">RELATED LINKS</span></span>
