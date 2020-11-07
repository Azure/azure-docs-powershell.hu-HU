---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 2b29b0f7976f8abba8c2f1d664a40d9a67c03c5a
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847741"
---
# <span data-ttu-id="7dfb2-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="7dfb2-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="7dfb2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7dfb2-102">SYNOPSIS</span></span>
<span data-ttu-id="7dfb2-103">Már létezik mentett keresés frissítése.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="7dfb2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7dfb2-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dfb2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7dfb2-105">DESCRIPTION</span></span>
<span data-ttu-id="7dfb2-106">A **set-AzOperationalInsightsSavedSearch** parancsmag a már létező mentett keresést frissíti.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="7dfb2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7dfb2-107">EXAMPLES</span></span>

### <span data-ttu-id="7dfb2-108">1. példa: mentett keresés megadása frissített tulajdonságokkal</span><span class="sxs-lookup"><span data-stu-id="7dfb2-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="7dfb2-109">Ezzel a paranccsal a mentett keresések frissített tulajdonságokkal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="7dfb2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7dfb2-110">PARAMETERS</span></span>

### <span data-ttu-id="7dfb2-111">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="7dfb2-111">-Category</span></span>
<span data-ttu-id="7dfb2-112">A kategória nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="7dfb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dfb2-113">-DefaultProfile</span></span>
<span data-ttu-id="7dfb2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7dfb2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7dfb2-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7dfb2-115">-DisplayName</span></span>
<span data-ttu-id="7dfb2-116">A megjelenítendő nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-116">Specifies the display name.</span></span>

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

### <span data-ttu-id="7dfb2-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="7dfb2-117">-ETag</span></span>
<span data-ttu-id="7dfb2-118">A ETag nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-118">Specifies the ETag name.</span></span>

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

### <span data-ttu-id="7dfb2-119">-Query</span><span class="sxs-lookup"><span data-stu-id="7dfb2-119">-Query</span></span>
<span data-ttu-id="7dfb2-120">A lekérdezés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="7dfb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dfb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="7dfb2-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="7dfb2-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="7dfb2-123">-SavedSearchId</span></span>
<span data-ttu-id="7dfb2-124">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="7dfb2-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="7dfb2-125">-Tag</span></span>
<span data-ttu-id="7dfb2-126">A mentett keresési címkék.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-126">The saved search tags.</span></span>

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

### <span data-ttu-id="7dfb2-127">-Verzió</span><span class="sxs-lookup"><span data-stu-id="7dfb2-127">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dfb2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7dfb2-128">-WorkspaceName</span></span>
<span data-ttu-id="7dfb2-129">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7dfb2-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="7dfb2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dfb2-130">CommonParameters</span></span>
<span data-ttu-id="7dfb2-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7dfb2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dfb2-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dfb2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dfb2-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dfb2-133">INPUTS</span></span>

### <span data-ttu-id="7dfb2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7dfb2-134">System.String</span></span>

### <span data-ttu-id="7dfb2-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7dfb2-135">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7dfb2-136">System. Int64</span><span class="sxs-lookup"><span data-stu-id="7dfb2-136">System.Int64</span></span>

## <span data-ttu-id="7dfb2-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7dfb2-137">OUTPUTS</span></span>

### <span data-ttu-id="7dfb2-138">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="7dfb2-138">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="7dfb2-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7dfb2-139">NOTES</span></span>

## <span data-ttu-id="7dfb2-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7dfb2-140">RELATED LINKS</span></span>

[<span data-ttu-id="7dfb2-141">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="7dfb2-141">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


