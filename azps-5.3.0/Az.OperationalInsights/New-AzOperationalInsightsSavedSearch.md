---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468798"
---
# <span data-ttu-id="f4425-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f4425-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="f4425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4425-102">SYNOPSIS</span></span>
<span data-ttu-id="f4425-103">Létrehoz egy új mentett keresést a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f4425-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="f4425-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f4425-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4425-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f4425-105">DESCRIPTION</span></span>
<span data-ttu-id="f4425-106">A **New-AzOperationalInsightsSavedSearch** parancsmag létrehoz egy új mentett keresést a munkaterülethez megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="f4425-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="f4425-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f4425-107">EXAMPLES</span></span>

### <span data-ttu-id="f4425-108">1. példa: Új mentett keresés létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4425-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="f4425-109">Ez a parancs új mentett keresést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4425-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="f4425-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4425-110">PARAMETERS</span></span>

### <span data-ttu-id="f4425-111">-Category</span><span class="sxs-lookup"><span data-stu-id="f4425-111">-Category</span></span>
<span data-ttu-id="f4425-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4425-113">-DefaultProfile</span></span>
<span data-ttu-id="f4425-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f4425-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f4425-115">-DisplayName</span></span>
<span data-ttu-id="f4425-116">A mentett keresés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-116">Specifies the saved search display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4425-117">-Force</span></span>
<span data-ttu-id="f4425-118">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f4425-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="f4425-119">-FunctionAlias</span></span>
<span data-ttu-id="f4425-120">A függvény aliasa, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="f4425-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="f4425-121">-FunctionParameter</span></span>
<span data-ttu-id="f4425-122">A választható függvényparaméterek, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="f4425-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="f4425-123">Az érték formátuma a következő: "paraméter-név1:típus1 = default_value1, paraméter-név2:típus2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="f4425-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="f4425-124">További példákat és helyes szintaxist a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="f4425-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-125">-Query</span><span class="sxs-lookup"><span data-stu-id="f4425-125">-Query</span></span>
<span data-ttu-id="f4425-126">A mentett keresés lekérdezési kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-126">Specifies the query expression for the saved search.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4425-127">-ResourceGroupName</span></span>
<span data-ttu-id="f4425-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-128">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f4425-129">-SavedSearchId</span></span>
<span data-ttu-id="f4425-130">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-130">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4425-131">-Tag</span></span>
<span data-ttu-id="f4425-132">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="f4425-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-133">-Version</span><span class="sxs-lookup"><span data-stu-id="f4425-133">-Version</span></span>
<span data-ttu-id="f4425-134">A verziószám megadása.</span><span class="sxs-lookup"><span data-stu-id="f4425-134">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f4425-135">-WorkspaceName</span></span>
<span data-ttu-id="f4425-136">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f4425-136">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4425-137">-Confirm</span></span>
<span data-ttu-id="f4425-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f4425-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4425-139">-WhatIf</span></span>
<span data-ttu-id="f4425-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f4425-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4425-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4425-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4425-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4425-142">CommonParameters</span></span>
<span data-ttu-id="f4425-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4425-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4425-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4425-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4425-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4425-145">INPUTS</span></span>

### <span data-ttu-id="f4425-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f4425-146">System.String</span></span>

### <span data-ttu-id="f4425-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4425-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f4425-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="f4425-148">System.Int64</span></span>

## <span data-ttu-id="f4425-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4425-149">OUTPUTS</span></span>

### <span data-ttu-id="f4425-150">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="f4425-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="f4425-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f4425-151">NOTES</span></span>

## <span data-ttu-id="f4425-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4425-152">RELATED LINKS</span></span>

[<span data-ttu-id="f4425-153">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f4425-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


