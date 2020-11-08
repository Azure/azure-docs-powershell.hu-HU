---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 46427a53a04e94fe42c20cfa2e6ab016a6b8c613
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182945"
---
# <span data-ttu-id="bf016-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="bf016-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="bf016-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf016-102">SYNOPSIS</span></span>
<span data-ttu-id="bf016-103">Már létezik mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="bf016-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="bf016-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf016-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf016-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf016-105">DESCRIPTION</span></span>
<span data-ttu-id="bf016-106">A **set-AzOperationalInsightsSavedSearch** parancsmag a már létező mentett keresést frissíti.</span><span class="sxs-lookup"><span data-stu-id="bf016-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="bf016-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf016-107">EXAMPLES</span></span>

### <span data-ttu-id="bf016-108">1. példa: mentett keresés megadása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="bf016-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="bf016-109">Ezzel a paranccsal a mentett keresések frissített tulajdonságokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="bf016-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="bf016-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf016-110">PARAMETERS</span></span>

### <span data-ttu-id="bf016-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="bf016-111">-Category</span></span>
<span data-ttu-id="bf016-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="bf016-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf016-113">-DefaultProfile</span></span>
<span data-ttu-id="bf016-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf016-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf016-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bf016-115">-DisplayName</span></span>
<span data-ttu-id="bf016-116">A megjelenítendő nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="bf016-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="bf016-117">-ETag</span></span>
<span data-ttu-id="bf016-118">A ETag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="bf016-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="bf016-119">-FunctionAlias</span></span>
<span data-ttu-id="bf016-120">A függvény aliasa, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="bf016-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="bf016-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="bf016-121">-FunctionParameter</span></span>
<span data-ttu-id="bf016-122">A választható függvény paraméterei, ha a lekérdezés függvényként szolgál.</span><span class="sxs-lookup"><span data-stu-id="bf016-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="bf016-123">Az értéknek a következő formátumban kell lennie: "param-fájlnév1: Type1 = default_value1, param-fájlnév2: Type2 = default_value2 '.</span><span class="sxs-lookup"><span data-stu-id="bf016-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="bf016-124">További példákért és a megfelelő szintaxisért lásd: https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="bf016-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="bf016-125">-Query</span><span class="sxs-lookup"><span data-stu-id="bf016-125">-Query</span></span>
<span data-ttu-id="bf016-126">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-126">Specifies the query name.</span></span>

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

### <span data-ttu-id="bf016-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf016-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf016-128">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="bf016-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="bf016-129">-SavedSearchId</span></span>
<span data-ttu-id="bf016-130">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="bf016-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="bf016-131">-Tag</span></span>
<span data-ttu-id="bf016-132">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="bf016-132">The saved search tags.</span></span>

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

### <span data-ttu-id="bf016-133">-Verzió</span><span class="sxs-lookup"><span data-stu-id="bf016-133">-Version</span></span>
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

### <span data-ttu-id="bf016-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf016-134">-WorkspaceName</span></span>
<span data-ttu-id="bf016-135">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf016-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="bf016-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf016-136">CommonParameters</span></span>
<span data-ttu-id="bf016-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf016-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf016-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf016-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf016-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf016-139">INPUTS</span></span>

### <span data-ttu-id="bf016-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf016-140">System.String</span></span>

### <span data-ttu-id="bf016-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf016-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bf016-142">System. Int64</span><span class="sxs-lookup"><span data-stu-id="bf016-142">System.Int64</span></span>

## <span data-ttu-id="bf016-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf016-143">OUTPUTS</span></span>

### <span data-ttu-id="bf016-144">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="bf016-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="bf016-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf016-145">NOTES</span></span>

## <span data-ttu-id="bf016-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf016-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf016-147">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="bf016-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


