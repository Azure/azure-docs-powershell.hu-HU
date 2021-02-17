---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156627"
---
# <span data-ttu-id="4f2ac-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4f2ac-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="4f2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2ac-103">Egy már létező mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="4f2ac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f2ac-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f2ac-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2ac-106">A **Set-AzOperationalInsightsSavedSearch** parancsmag egy már létező mentett keresést is frissíti.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="4f2ac-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f2ac-107">EXAMPLES</span></span>

### <span data-ttu-id="4f2ac-108">1. példa: Mentett keresés beállítása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="4f2ac-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="4f2ac-109">Ez a parancs egy mentett keresést állít be frissített tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="4f2ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f2ac-110">PARAMETERS</span></span>

### <span data-ttu-id="4f2ac-111">-Category</span><span class="sxs-lookup"><span data-stu-id="4f2ac-111">-Category</span></span>
<span data-ttu-id="4f2ac-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="4f2ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2ac-113">-DefaultProfile</span></span>
<span data-ttu-id="4f2ac-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4f2ac-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f2ac-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4f2ac-115">-DisplayName</span></span>
<span data-ttu-id="4f2ac-116">A megjelenítendő név megadása.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="4f2ac-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="4f2ac-117">-ETag</span></span>
<span data-ttu-id="4f2ac-118">Az ETag nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f2ac-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="4f2ac-119">-FunctionAlias</span></span>
<span data-ttu-id="4f2ac-120">A függvény aliasa, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f2ac-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="4f2ac-121">-FunctionParameter</span></span>
<span data-ttu-id="4f2ac-122">A választható függvényparaméterek, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="4f2ac-123">Az érték formátuma a következő: "paraméter-név1:típus1 = default_value1, paraméter-név2:típus2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="4f2ac-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="4f2ac-124">További példákat és helyes szintaxist a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="4f2ac-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f2ac-125">-Query</span><span class="sxs-lookup"><span data-stu-id="4f2ac-125">-Query</span></span>
<span data-ttu-id="4f2ac-126">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="4f2ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f2ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f2ac-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="4f2ac-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="4f2ac-129">-SavedSearchId</span></span>
<span data-ttu-id="4f2ac-130">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="4f2ac-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f2ac-131">-Tag</span></span>
<span data-ttu-id="4f2ac-132">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-132">The saved search tags.</span></span>

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

### <span data-ttu-id="4f2ac-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="4f2ac-133">-Version</span></span>
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

### <span data-ttu-id="4f2ac-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4f2ac-134">-WorkspaceName</span></span>
<span data-ttu-id="4f2ac-135">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4f2ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2ac-136">CommonParameters</span></span>
<span data-ttu-id="4f2ac-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f2ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2ac-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f2ac-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2ac-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f2ac-139">INPUTS</span></span>

### <span data-ttu-id="4f2ac-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4f2ac-140">System.String</span></span>

### <span data-ttu-id="4f2ac-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f2ac-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4f2ac-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="4f2ac-142">System.Int64</span></span>

## <span data-ttu-id="4f2ac-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f2ac-143">OUTPUTS</span></span>

### <span data-ttu-id="4f2ac-144">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="4f2ac-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="4f2ac-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f2ac-145">NOTES</span></span>

## <span data-ttu-id="4f2ac-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f2ac-146">RELATED LINKS</span></span>

[<span data-ttu-id="4f2ac-147">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="4f2ac-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


