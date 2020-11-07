---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 535fbe737184b996ee0caa030c83137ea8cd1019
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847937"
---
# <span data-ttu-id="1f0aa-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="1f0aa-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="1f0aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f0aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1f0aa-103">Már létezik mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="1f0aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f0aa-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f0aa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f0aa-105">DESCRIPTION</span></span>
<span data-ttu-id="1f0aa-106">A **set-AzOperationalInsightsSavedSearch** parancsmag a már létező mentett keresést frissíti.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="1f0aa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1f0aa-107">EXAMPLES</span></span>

### <span data-ttu-id="1f0aa-108">1. példa: mentett keresés megadása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="1f0aa-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="1f0aa-109">Ezzel a paranccsal a mentett keresések frissített tulajdonságokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="1f0aa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f0aa-110">PARAMETERS</span></span>

### <span data-ttu-id="1f0aa-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="1f0aa-111">-Category</span></span>
<span data-ttu-id="1f0aa-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="1f0aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f0aa-113">-DefaultProfile</span></span>
<span data-ttu-id="1f0aa-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1f0aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f0aa-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f0aa-115">-DisplayName</span></span>
<span data-ttu-id="1f0aa-116">A megjelenítendő nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="1f0aa-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="1f0aa-117">-ETag</span></span>
<span data-ttu-id="1f0aa-118">A ETag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="1f0aa-119">-Query</span><span class="sxs-lookup"><span data-stu-id="1f0aa-119">-Query</span></span>
<span data-ttu-id="1f0aa-120">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="1f0aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f0aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="1f0aa-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="1f0aa-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1f0aa-123">-SavedSearchId</span></span>
<span data-ttu-id="1f0aa-124">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="1f0aa-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="1f0aa-125">-Tag</span></span>
<span data-ttu-id="1f0aa-126">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-126">The saved search tags.</span></span>

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

### <span data-ttu-id="1f0aa-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="1f0aa-127">-Version</span></span>
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

### <span data-ttu-id="1f0aa-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f0aa-128">-WorkspaceName</span></span>
<span data-ttu-id="1f0aa-129">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f0aa-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1f0aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f0aa-130">CommonParameters</span></span>
<span data-ttu-id="1f0aa-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f0aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f0aa-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f0aa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f0aa-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f0aa-133">INPUTS</span></span>

### <span data-ttu-id="1f0aa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f0aa-134">System.String</span></span>

### <span data-ttu-id="1f0aa-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f0aa-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f0aa-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="1f0aa-136">System.Int64</span></span>

## <span data-ttu-id="1f0aa-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f0aa-137">OUTPUTS</span></span>

### <span data-ttu-id="1f0aa-138">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="1f0aa-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="1f0aa-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f0aa-139">NOTES</span></span>

## <span data-ttu-id="1f0aa-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f0aa-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f0aa-141">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1f0aa-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


