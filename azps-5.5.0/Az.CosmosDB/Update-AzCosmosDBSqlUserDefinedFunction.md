---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148450"
---
# <span data-ttu-id="d01d2-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="d01d2-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="d01d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d01d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d01d2-103">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="d01d2-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="d01d2-104">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="d01d2-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="d01d2-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d01d2-105">SYNTAX</span></span>

### <span data-ttu-id="d01d2-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d01d2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d01d2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d01d2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d01d2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d01d2-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d01d2-109">DESCRIPTION</span></span>
<span data-ttu-id="d01d2-110">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="d01d2-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="d01d2-111">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="d01d2-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="d01d2-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d01d2-112">EXAMPLES</span></span>

### <span data-ttu-id="d01d2-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="d01d2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="d01d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d01d2-114">PARAMETERS</span></span>

### <span data-ttu-id="d01d2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d01d2-115">-AccountName</span></span>
<span data-ttu-id="d01d2-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="d01d2-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d01d2-117">-Body</span><span class="sxs-lookup"><span data-stu-id="d01d2-117">-Body</span></span>
<span data-ttu-id="d01d2-118">A Felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="d01d2-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="d01d2-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d01d2-119">-Confirm</span></span>
<span data-ttu-id="d01d2-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d01d2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01d2-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d01d2-121">-ContainerName</span></span>
<span data-ttu-id="d01d2-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="d01d2-122">Container name.</span></span>

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

### <span data-ttu-id="d01d2-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d01d2-123">-DatabaseName</span></span>
<span data-ttu-id="d01d2-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="d01d2-124">Database name.</span></span>

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

### <span data-ttu-id="d01d2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01d2-125">-DefaultProfile</span></span>
<span data-ttu-id="d01d2-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d01d2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01d2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d01d2-127">-InputObject</span></span>
<span data-ttu-id="d01d2-128">Sql felhasználó által definiált függvényobjektum</span><span class="sxs-lookup"><span data-stu-id="d01d2-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="d01d2-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d01d2-129">-Name</span></span>
<span data-ttu-id="d01d2-130">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="d01d2-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="d01d2-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d01d2-131">-ParentObject</span></span>
<span data-ttu-id="d01d2-132">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="d01d2-132">Sql Container object.</span></span>

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

### <span data-ttu-id="d01d2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01d2-133">-ResourceGroupName</span></span>
<span data-ttu-id="d01d2-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d01d2-134">Name of resource group.</span></span>

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

### <span data-ttu-id="d01d2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d01d2-135">-WhatIf</span></span>
<span data-ttu-id="d01d2-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d01d2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d01d2-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d01d2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01d2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01d2-138">CommonParameters</span></span>
<span data-ttu-id="d01d2-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d01d2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01d2-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d01d2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01d2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d01d2-141">INPUTS</span></span>

### <span data-ttu-id="d01d2-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d01d2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d01d2-143">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="d01d2-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="d01d2-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d01d2-144">OUTPUTS</span></span>

### <span data-ttu-id="d01d2-145">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="d01d2-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="d01d2-146">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d01d2-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d01d2-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d01d2-147">NOTES</span></span>

## <span data-ttu-id="d01d2-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d01d2-148">RELATED LINKS</span></span>
