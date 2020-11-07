---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672363"
---
# <span data-ttu-id="d94f5-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="d94f5-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="d94f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d94f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d94f5-103">Lekérdezés eredményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d94f5-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d94f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d94f5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d94f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d94f5-105">DESCRIPTION</span></span>
<span data-ttu-id="d94f5-106">A **Get-AzureRmOperationalInsightsSavedSearchResults** parancsmag a keresési azonosító által megadott lekérdezés eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d94f5-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="d94f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d94f5-107">EXAMPLES</span></span>

### <span data-ttu-id="d94f5-108">Példa 1: a mentett keresés összes keresési eredményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="d94f5-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="d94f5-109">Ez a parancs a mentett keresés minden találatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="d94f5-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="d94f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d94f5-110">PARAMETERS</span></span>

### <span data-ttu-id="d94f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94f5-111">-DefaultProfile</span></span>
<span data-ttu-id="d94f5-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d94f5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d94f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d94f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="d94f5-114">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="d94f5-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f5-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="d94f5-115">-SavedSearchId</span></span>
<span data-ttu-id="d94f5-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="d94f5-116">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f5-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d94f5-117">-WorkspaceName</span></span>
<span data-ttu-id="d94f5-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d94f5-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94f5-119">CommonParameters</span></span>
<span data-ttu-id="d94f5-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d94f5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94f5-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d94f5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94f5-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d94f5-122">INPUTS</span></span>

### <span data-ttu-id="d94f5-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d94f5-123">None</span></span>
<span data-ttu-id="d94f5-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d94f5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d94f5-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d94f5-125">OUTPUTS</span></span>

### <span data-ttu-id="d94f5-126">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="d94f5-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="d94f5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d94f5-127">NOTES</span></span>

## <span data-ttu-id="d94f5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d94f5-128">RELATED LINKS</span></span>

[<span data-ttu-id="d94f5-129">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d94f5-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


