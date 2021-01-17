---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370241"
---
# <span data-ttu-id="62fdf-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="62fdf-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="62fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="62fdf-103">Visszaadja egy adott munkaterület összes mentett keresését.</span><span class="sxs-lookup"><span data-stu-id="62fdf-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="62fdf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="62fdf-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62fdf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="62fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="62fdf-106">A **Get-AzOperationalInsightsSavedSearch** parancsmag visszaadja a megadott munkaterületre vonatkozó összes mentett keresést a megadott erőforráscsoporton belül, ha nem ad meg mentett keresési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="62fdf-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="62fdf-107">Ha megad egy mentett keresési azonosítót, akkor a program az adott azonosítónak megfelelő mentett keresést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="62fdf-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="62fdf-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="62fdf-108">EXAMPLES</span></span>

### <span data-ttu-id="62fdf-109">1. példa: Munkaterület összes mentett keresésének bekeresése</span><span class="sxs-lookup"><span data-stu-id="62fdf-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="62fdf-110">Ez a parancs a munkaterülethez tartozó összes mentett erőforrást leküldi.</span><span class="sxs-lookup"><span data-stu-id="62fdf-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="62fdf-111">2. példa: Adott mentett keresés keresése azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="62fdf-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="62fdf-112">Ez a parancs egy adott mentett keresést kap az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="62fdf-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="62fdf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62fdf-113">PARAMETERS</span></span>

### <span data-ttu-id="62fdf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fdf-114">-DefaultProfile</span></span>
<span data-ttu-id="62fdf-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="62fdf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62fdf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62fdf-116">-ResourceGroupName</span></span>
<span data-ttu-id="62fdf-117">Egy munkaterületet tartalmazó Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62fdf-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="62fdf-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="62fdf-118">-SavedSearchId</span></span>
<span data-ttu-id="62fdf-119">Egy mentett keresési azonosítót ad meg.</span><span class="sxs-lookup"><span data-stu-id="62fdf-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="62fdf-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="62fdf-120">-WorkspaceName</span></span>
<span data-ttu-id="62fdf-121">Munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="62fdf-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="62fdf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fdf-122">CommonParameters</span></span>
<span data-ttu-id="62fdf-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62fdf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fdf-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62fdf-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fdf-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62fdf-125">INPUTS</span></span>

### <span data-ttu-id="62fdf-126">System.String</span><span class="sxs-lookup"><span data-stu-id="62fdf-126">System.String</span></span>

## <span data-ttu-id="62fdf-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62fdf-127">OUTPUTS</span></span>

### <span data-ttu-id="62fdf-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="62fdf-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="62fdf-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="62fdf-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="62fdf-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="62fdf-130">NOTES</span></span>

## <span data-ttu-id="62fdf-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62fdf-131">RELATED LINKS</span></span>

[<span data-ttu-id="62fdf-132">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="62fdf-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


