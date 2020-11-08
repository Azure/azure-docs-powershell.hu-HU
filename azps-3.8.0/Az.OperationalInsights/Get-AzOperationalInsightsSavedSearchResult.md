---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearchresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearchResult.md
ms.openlocfilehash: 020a0684d6fe3a14b61b8582d8ad8427e68d8855
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017227"
---
# <span data-ttu-id="1c4ab-101">Get-AzOperationalInsightsSavedSearchResult</span><span class="sxs-lookup"><span data-stu-id="1c4ab-101">Get-AzOperationalInsightsSavedSearchResult</span></span>

## <span data-ttu-id="1c4ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1c4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4ab-103">Lekérdezés eredményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-103">Returns the results from a query.</span></span>

## <span data-ttu-id="1c4ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1c4ab-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearchResult [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c4ab-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1c4ab-105">DESCRIPTION</span></span>
<span data-ttu-id="1c4ab-106">A **Get-AzOperationalInsightsSavedSearchResult** parancsmag a keresési azonosító által megadott lekérdezés eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-106">The **Get-AzOperationalInsightsSavedSearchResult** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="1c4ab-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1c4ab-107">EXAMPLES</span></span>

### <span data-ttu-id="1c4ab-108">Példa 1: a mentett keresés összes keresési eredményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="1c4ab-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzOperationalInsightSavedSearchResult -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="1c4ab-109">Ez a parancs a mentett keresés minden találatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="1c4ab-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1c4ab-110">PARAMETERS</span></span>

### <span data-ttu-id="1c4ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4ab-111">-DefaultProfile</span></span>
<span data-ttu-id="1c4ab-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1c4ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c4ab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c4ab-113">-ResourceGroupName</span></span>
<span data-ttu-id="1c4ab-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="1c4ab-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="1c4ab-115">-SavedSearchId</span></span>
<span data-ttu-id="1c4ab-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="1c4ab-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1c4ab-117">-WorkspaceName</span></span>
<span data-ttu-id="1c4ab-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1c4ab-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="1c4ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4ab-119">CommonParameters</span></span>
<span data-ttu-id="1c4ab-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1c4ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4ab-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4ab-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4ab-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c4ab-122">INPUTS</span></span>

### <span data-ttu-id="1c4ab-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1c4ab-123">System.String</span></span>

## <span data-ttu-id="1c4ab-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1c4ab-124">OUTPUTS</span></span>

### <span data-ttu-id="1c4ab-125">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="1c4ab-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="1c4ab-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1c4ab-126">NOTES</span></span>

## <span data-ttu-id="1c4ab-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1c4ab-127">RELATED LINKS</span></span>

[<span data-ttu-id="1c4ab-128">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1c4ab-128">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


