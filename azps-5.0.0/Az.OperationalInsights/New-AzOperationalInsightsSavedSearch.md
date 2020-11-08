---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186038"
---
# <span data-ttu-id="22d02-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="22d02-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="22d02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="22d02-102">SYNOPSIS</span></span>
<span data-ttu-id="22d02-103">Új mentett keresést hoz létre a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="22d02-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="22d02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="22d02-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="22d02-105">DESCRIPTION</span></span>
<span data-ttu-id="22d02-106">A **New-AzOperationalInsightsSavedSearch** parancsmag új mentett keresést hoz létre a munkaterülethez megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="22d02-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="22d02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="22d02-107">EXAMPLES</span></span>

### <span data-ttu-id="22d02-108">1. példa: új mentett keresés létrehozása</span><span class="sxs-lookup"><span data-stu-id="22d02-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="22d02-109">Ezzel a paranccsal új mentett keresést hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="22d02-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="22d02-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="22d02-110">PARAMETERS</span></span>

### <span data-ttu-id="22d02-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="22d02-111">-Category</span></span>
<span data-ttu-id="22d02-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="22d02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d02-113">-DefaultProfile</span></span>
<span data-ttu-id="22d02-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22d02-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22d02-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22d02-115">-DisplayName</span></span>
<span data-ttu-id="22d02-116">A mentett keresés megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="22d02-117">-Force</span><span class="sxs-lookup"><span data-stu-id="22d02-117">-Force</span></span>
<span data-ttu-id="22d02-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="22d02-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22d02-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="22d02-119">-FunctionAlias</span></span>
<span data-ttu-id="22d02-120">A függvény aliasa, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="22d02-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="22d02-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="22d02-121">-FunctionParameter</span></span>
<span data-ttu-id="22d02-122">A választható függvény paraméterei, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="22d02-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="22d02-123">Az értéknek a következő formátumban kell lennie: "param-fájlnév1: Type1 = default_value1, param-fájlnév2: Type2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="22d02-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="22d02-124">További példákért és a megfelelő szintaxisért lásd: https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="22d02-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="22d02-125">-Query</span><span class="sxs-lookup"><span data-stu-id="22d02-125">-Query</span></span>
<span data-ttu-id="22d02-126">A mentett keresés lekérdezési kifejezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="22d02-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d02-127">-ResourceGroupName</span></span>
<span data-ttu-id="22d02-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="22d02-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="22d02-129">-SavedSearchId</span></span>
<span data-ttu-id="22d02-130">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="22d02-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="22d02-131">-Tag</span></span>
<span data-ttu-id="22d02-132">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="22d02-132">The saved search tags.</span></span>

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

### <span data-ttu-id="22d02-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="22d02-133">-Version</span></span>
<span data-ttu-id="22d02-134">A verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-134">Specifies the version.</span></span>

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

### <span data-ttu-id="22d02-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22d02-135">-WorkspaceName</span></span>
<span data-ttu-id="22d02-136">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22d02-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="22d02-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="22d02-137">-Confirm</span></span>
<span data-ttu-id="22d02-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="22d02-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d02-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d02-139">-WhatIf</span></span>
<span data-ttu-id="22d02-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="22d02-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d02-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22d02-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d02-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d02-142">CommonParameters</span></span>
<span data-ttu-id="22d02-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="22d02-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d02-144">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="22d02-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d02-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d02-145">INPUTS</span></span>

### <span data-ttu-id="22d02-146">System. String</span><span class="sxs-lookup"><span data-stu-id="22d02-146">System.String</span></span>

### <span data-ttu-id="22d02-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22d02-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="22d02-148">System. Int64</span><span class="sxs-lookup"><span data-stu-id="22d02-148">System.Int64</span></span>

## <span data-ttu-id="22d02-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22d02-149">OUTPUTS</span></span>

### <span data-ttu-id="22d02-150">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="22d02-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="22d02-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="22d02-151">NOTES</span></span>

## <span data-ttu-id="22d02-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22d02-152">RELATED LINKS</span></span>

[<span data-ttu-id="22d02-153">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="22d02-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

