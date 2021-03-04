---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921665"
---
# <span data-ttu-id="9500a-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="9500a-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="9500a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9500a-102">SYNOPSIS</span></span>
<span data-ttu-id="9500a-103">Visszaadja egy adott munkaterület összes mentett keresését.</span><span class="sxs-lookup"><span data-stu-id="9500a-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="9500a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9500a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9500a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9500a-105">DESCRIPTION</span></span>
<span data-ttu-id="9500a-106">A **Get-AzOperationalInsightsSavedSearch** parancsmag visszaadja az erőforráscsoportban megadott munkaterület összes mentett keresését, ha nem ad meg mentett keresési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="9500a-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="9500a-107">Ha megad egy mentett keresési azonosítót, akkor a rendszer az adott azonosítónak megfelelő mentett keresést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="9500a-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="9500a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9500a-108">EXAMPLES</span></span>

### <span data-ttu-id="9500a-109">1. példa: Munkaterület összes mentett keresésének bekeresése</span><span class="sxs-lookup"><span data-stu-id="9500a-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="9500a-110">Ez a parancs a munkaterülethez társított összes mentett erőforrást leküldi.</span><span class="sxs-lookup"><span data-stu-id="9500a-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="9500a-111">2. példa: Adott mentett keresés keresése azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="9500a-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="9500a-112">Ez a parancs egy adott mentett keresést kap az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="9500a-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="9500a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9500a-113">PARAMETERS</span></span>

### <span data-ttu-id="9500a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9500a-114">-DefaultProfile</span></span>
<span data-ttu-id="9500a-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9500a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9500a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9500a-116">-ResourceGroupName</span></span>
<span data-ttu-id="9500a-117">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9500a-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="9500a-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="9500a-118">-SavedSearchId</span></span>
<span data-ttu-id="9500a-119">Egy mentett keresési azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="9500a-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9500a-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9500a-120">-WorkspaceName</span></span>
<span data-ttu-id="9500a-121">Munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9500a-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="9500a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9500a-122">CommonParameters</span></span>
<span data-ttu-id="9500a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9500a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9500a-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9500a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9500a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9500a-125">INPUTS</span></span>

### <span data-ttu-id="9500a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9500a-126">System.String</span></span>

## <span data-ttu-id="9500a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9500a-127">OUTPUTS</span></span>

### <span data-ttu-id="9500a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="9500a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="9500a-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="9500a-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="9500a-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9500a-130">NOTES</span></span>

## <span data-ttu-id="9500a-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9500a-131">RELATED LINKS</span></span>

[<span data-ttu-id="9500a-132">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9500a-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


