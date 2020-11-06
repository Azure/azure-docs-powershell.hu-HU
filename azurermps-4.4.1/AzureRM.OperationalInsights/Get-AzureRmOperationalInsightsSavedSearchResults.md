---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501695"
---
# <span data-ttu-id="71975-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="71975-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="71975-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71975-102">SYNOPSIS</span></span>
<span data-ttu-id="71975-103">Lekérdezés eredményét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="71975-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71975-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71975-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71975-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="71975-105">DESCRIPTION</span></span>
<span data-ttu-id="71975-106">A **Get-AzureRmOperationalInsightsSavedSearchResults** parancsmag a keresési azonosító által megadott lekérdezés eredményét adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="71975-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="71975-107">Példák</span><span class="sxs-lookup"><span data-stu-id="71975-107">EXAMPLES</span></span>

### <span data-ttu-id="71975-108">Példa 1: a mentett keresés összes keresési eredményének beolvasása</span><span class="sxs-lookup"><span data-stu-id="71975-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="71975-109">Ez a parancs a mentett keresés minden találatát beilleszti.</span><span class="sxs-lookup"><span data-stu-id="71975-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="71975-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71975-110">PARAMETERS</span></span>

### <span data-ttu-id="71975-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71975-111">-ResourceGroupName</span></span>
<span data-ttu-id="71975-112">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="71975-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="71975-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="71975-113">-SavedSearchId</span></span>
<span data-ttu-id="71975-114">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="71975-114">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="71975-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71975-115">-WorkspaceName</span></span>
<span data-ttu-id="71975-116">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71975-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="71975-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71975-117">-DefaultProfile</span></span>
<span data-ttu-id="71975-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71975-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71975-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71975-119">CommonParameters</span></span>
<span data-ttu-id="71975-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71975-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71975-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71975-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71975-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71975-122">INPUTS</span></span>

## <span data-ttu-id="71975-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71975-123">OUTPUTS</span></span>

### <span data-ttu-id="71975-124">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSearchResultsResponse</span><span class="sxs-lookup"><span data-stu-id="71975-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="71975-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71975-125">NOTES</span></span>

## <span data-ttu-id="71975-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71975-126">RELATED LINKS</span></span>

[<span data-ttu-id="71975-127">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="71975-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


