---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372075"
---
# <span data-ttu-id="9cbbc-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="9cbbc-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="9cbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbbc-103">Egy már létező mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="9cbbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cbbc-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cbbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="9cbbc-106">A **Set-AzOperationalInsightsSavedSearch** parancsmag egy már létező mentett keresést is frissíti.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="9cbbc-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cbbc-107">EXAMPLES</span></span>

### <span data-ttu-id="9cbbc-108">1. példa: Mentett keresés beállítása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="9cbbc-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="9cbbc-109">Ez a parancs egy mentett keresést állít be frissített tulajdonságokkal.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="9cbbc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cbbc-110">PARAMETERS</span></span>

### <span data-ttu-id="9cbbc-111">-Category</span><span class="sxs-lookup"><span data-stu-id="9cbbc-111">-Category</span></span>
<span data-ttu-id="9cbbc-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="9cbbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbbc-113">-DefaultProfile</span></span>
<span data-ttu-id="9cbbc-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9cbbc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9cbbc-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9cbbc-115">-DisplayName</span></span>
<span data-ttu-id="9cbbc-116">A megjelenítendő név megadása.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="9cbbc-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="9cbbc-117">-ETag</span></span>
<span data-ttu-id="9cbbc-118">Az ETag nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="9cbbc-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="9cbbc-119">-FunctionAlias</span></span>
<span data-ttu-id="9cbbc-120">A függvény aliasa, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="9cbbc-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="9cbbc-121">-FunctionParameter</span></span>
<span data-ttu-id="9cbbc-122">A választható függvényparaméterek, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="9cbbc-123">Az érték formátuma a következő: "paraméter-név1:típus1 = default_value1, paraméter-név2:típus2 = default_value2".</span><span class="sxs-lookup"><span data-stu-id="9cbbc-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="9cbbc-124">További példákat és helyes szintaxist a https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="9cbbc-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="9cbbc-125">-Query</span><span class="sxs-lookup"><span data-stu-id="9cbbc-125">-Query</span></span>
<span data-ttu-id="9cbbc-126">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="9cbbc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbbc-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cbbc-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="9cbbc-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="9cbbc-129">-SavedSearchId</span></span>
<span data-ttu-id="9cbbc-130">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="9cbbc-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cbbc-131">-Tag</span></span>
<span data-ttu-id="9cbbc-132">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-132">The saved search tags.</span></span>

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

### <span data-ttu-id="9cbbc-133">-Version</span><span class="sxs-lookup"><span data-stu-id="9cbbc-133">-Version</span></span>
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

### <span data-ttu-id="9cbbc-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9cbbc-134">-WorkspaceName</span></span>
<span data-ttu-id="9cbbc-135">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9cbbc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbbc-136">CommonParameters</span></span>
<span data-ttu-id="9cbbc-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbbc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbbc-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cbbc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbbc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cbbc-139">INPUTS</span></span>

### <span data-ttu-id="9cbbc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9cbbc-140">System.String</span></span>

### <span data-ttu-id="9cbbc-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9cbbc-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9cbbc-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="9cbbc-142">System.Int64</span></span>

## <span data-ttu-id="9cbbc-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cbbc-143">OUTPUTS</span></span>

### <span data-ttu-id="9cbbc-144">System.Net.httpStatusCode</span><span class="sxs-lookup"><span data-stu-id="9cbbc-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="9cbbc-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cbbc-145">NOTES</span></span>

## <span data-ttu-id="9cbbc-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cbbc-146">RELATED LINKS</span></span>

[<span data-ttu-id="9cbbc-147">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9cbbc-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


