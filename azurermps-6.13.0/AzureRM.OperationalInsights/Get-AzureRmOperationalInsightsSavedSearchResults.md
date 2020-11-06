---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 202fafead72ec57f3f03460093791943d36a2ba3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491890"
---
# <span data-ttu-id="07f1d-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="07f1d-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="07f1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="07f1d-103">Lekérdezés eredményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="07f1d-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07f1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07f1d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f1d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="07f1d-106">A **Get-AzureRmOperationalInsightsSavedSearchResults** parancsmag a keresési azonosító által megadott lekérdezés eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="07f1d-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="07f1d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="07f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="07f1d-108">Példa 1: a mentett keresés összes keresési eredményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="07f1d-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="07f1d-109">Ez a parancs a mentett keresés minden találatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="07f1d-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="07f1d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07f1d-110">PARAMETERS</span></span>

### <span data-ttu-id="07f1d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f1d-111">-DefaultProfile</span></span>
<span data-ttu-id="07f1d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="07f1d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f1d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f1d-113">-ResourceGroupName</span></span>
<span data-ttu-id="07f1d-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="07f1d-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="07f1d-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="07f1d-115">-SavedSearchId</span></span>
<span data-ttu-id="07f1d-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="07f1d-116">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="07f1d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07f1d-117">-WorkspaceName</span></span>
<span data-ttu-id="07f1d-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07f1d-118">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="07f1d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f1d-119">CommonParameters</span></span>
<span data-ttu-id="07f1d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07f1d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f1d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f1d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f1d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07f1d-122">INPUTS</span></span>

### <span data-ttu-id="07f1d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="07f1d-123">System.String</span></span>

## <span data-ttu-id="07f1d-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07f1d-124">OUTPUTS</span></span>

### <span data-ttu-id="07f1d-125">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="07f1d-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="07f1d-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07f1d-126">NOTES</span></span>

## <span data-ttu-id="07f1d-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07f1d-127">RELATED LINKS</span></span>

[<span data-ttu-id="07f1d-128">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="07f1d-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


