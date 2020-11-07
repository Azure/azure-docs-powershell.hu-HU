---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 0d813f6d0834a40708cc828d5b508cc6452dffc1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847773"
---
# <span data-ttu-id="78da0-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="78da0-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="78da0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="78da0-102">SYNOPSIS</span></span>
<span data-ttu-id="78da0-103">Lekérdezés eredményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="78da0-103">Returns the results from a query.</span></span>

## <span data-ttu-id="78da0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="78da0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78da0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="78da0-105">DESCRIPTION</span></span>
<span data-ttu-id="78da0-106">A **Get-AzOperationalInsightsSavedSearchResult** parancsmag a keresési azonosító által megadott lekérdezés eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="78da0-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="78da0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="78da0-107">EXAMPLES</span></span>

### <span data-ttu-id="78da0-108">Példa 1: a mentett keresés összes keresési eredményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="78da0-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="78da0-109">Ez a parancs a mentett keresés minden találatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="78da0-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="78da0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="78da0-110">PARAMETERS</span></span>

### <span data-ttu-id="78da0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78da0-111">-DefaultProfile</span></span>
<span data-ttu-id="78da0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="78da0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78da0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78da0-113">-ResourceGroupName</span></span>
<span data-ttu-id="78da0-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="78da0-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="78da0-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="78da0-115">-SavedSearchId</span></span>
<span data-ttu-id="78da0-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="78da0-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="78da0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="78da0-117">-WorkspaceName</span></span>
<span data-ttu-id="78da0-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="78da0-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="78da0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78da0-119">CommonParameters</span></span>
<span data-ttu-id="78da0-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="78da0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78da0-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78da0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78da0-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="78da0-122">INPUTS</span></span>

### <span data-ttu-id="78da0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="78da0-123">System.String</span></span>

## <span data-ttu-id="78da0-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="78da0-124">OUTPUTS</span></span>

### <span data-ttu-id="78da0-125">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="78da0-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="78da0-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="78da0-126">NOTES</span></span>

## <span data-ttu-id="78da0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="78da0-127">RELATED LINKS</span></span>

[<span data-ttu-id="78da0-128">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="78da0-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


