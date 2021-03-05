---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: d1f4e4c5c48e33a1b3c2ac882b0c561bb50f9bed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009701"
---
# <span data-ttu-id="bba2a-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="bba2a-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="bba2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba2a-102">SYNOPSIS</span></span>
<span data-ttu-id="bba2a-103">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bba2a-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bba2a-104">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="bba2a-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bba2a-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bba2a-105">SYNTAX</span></span>

### <span data-ttu-id="bba2a-106">ByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bba2a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bba2a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bba2a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bba2a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bba2a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba2a-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bba2a-109">DESCRIPTION</span></span>
<span data-ttu-id="bba2a-110">Frissíti a TárolóDB Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="bba2a-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="bba2a-111">Ügyféloldali javítást hajt végre a meglévő UserDefinedFunction olvasva.</span><span class="sxs-lookup"><span data-stu-id="bba2a-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="bba2a-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bba2a-112">EXAMPLES</span></span>

### <span data-ttu-id="bba2a-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="bba2a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="bba2a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bba2a-114">PARAMETERS</span></span>

### <span data-ttu-id="bba2a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bba2a-115">-AccountName</span></span>
<span data-ttu-id="bba2a-116">A Coss DB adatbázisfiók neve.</span><span class="sxs-lookup"><span data-stu-id="bba2a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bba2a-117">-Body</span><span class="sxs-lookup"><span data-stu-id="bba2a-117">-Body</span></span>
<span data-ttu-id="bba2a-118">A Felhasználó által definiált függvény törzse.</span><span class="sxs-lookup"><span data-stu-id="bba2a-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="bba2a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bba2a-119">-Confirm</span></span>
<span data-ttu-id="bba2a-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bba2a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba2a-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bba2a-121">-ContainerName</span></span>
<span data-ttu-id="bba2a-122">Tároló neve.</span><span class="sxs-lookup"><span data-stu-id="bba2a-122">Container name.</span></span>

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

### <span data-ttu-id="bba2a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bba2a-123">-DatabaseName</span></span>
<span data-ttu-id="bba2a-124">Adatbázis neve.</span><span class="sxs-lookup"><span data-stu-id="bba2a-124">Database name.</span></span>

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

### <span data-ttu-id="bba2a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba2a-125">-DefaultProfile</span></span>
<span data-ttu-id="bba2a-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bba2a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba2a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bba2a-127">-InputObject</span></span>
<span data-ttu-id="bba2a-128">Sql felhasználó által definiált függvényobjektum</span><span class="sxs-lookup"><span data-stu-id="bba2a-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="bba2a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="bba2a-129">-Name</span></span>
<span data-ttu-id="bba2a-130">Felhasználó által definiált függvény neve.</span><span class="sxs-lookup"><span data-stu-id="bba2a-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="bba2a-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bba2a-131">-ParentObject</span></span>
<span data-ttu-id="bba2a-132">Sql Container objektum.</span><span class="sxs-lookup"><span data-stu-id="bba2a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="bba2a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba2a-133">-ResourceGroupName</span></span>
<span data-ttu-id="bba2a-134">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bba2a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="bba2a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba2a-135">-WhatIf</span></span>
<span data-ttu-id="bba2a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bba2a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba2a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bba2a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba2a-138">CommonParameters</span></span>
<span data-ttu-id="bba2a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bba2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba2a-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bba2a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba2a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bba2a-141">INPUTS</span></span>

### <span data-ttu-id="bba2a-142">Microsoft.Azure.Commands.CossDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="bba2a-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="bba2a-143">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bba2a-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="bba2a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bba2a-144">OUTPUTS</span></span>

### <span data-ttu-id="bba2a-145">Microsoft.Azure.Commands.EzresDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="bba2a-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="bba2a-146">Microsoft.Azure.Commands.CossDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="bba2a-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="bba2a-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bba2a-147">NOTES</span></span>

## <span data-ttu-id="bba2a-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bba2a-148">RELATED LINKS</span></span>
