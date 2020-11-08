---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 23717dfbdfd4b0504f4e1c13378ccac2b77d91d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186882"
---
# <span data-ttu-id="da637-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="da637-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="da637-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da637-102">SYNOPSIS</span></span>
<span data-ttu-id="da637-103">A megadott munkaterület összes mentett keresését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="da637-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="da637-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da637-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da637-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da637-105">DESCRIPTION</span></span>
<span data-ttu-id="da637-106">A **Get-AzOperationalInsightsSavedSearch** parancsmag megadott munkaterület összes mentett keresését visszaadja az erőforráscsoport számára, ha nem ad meg mentett keresési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="da637-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="da637-107">Ha megadhatja a mentett keresési azonosítót, a program az AZONOSÍTÓnak megfelelő mentett keresést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="da637-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="da637-108">Példák</span><span class="sxs-lookup"><span data-stu-id="da637-108">EXAMPLES</span></span>

### <span data-ttu-id="da637-109">Példa 1: az összes mentett keresés beolvasása egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="da637-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="da637-110">Ez a parancs a munkaterülethez társított összes mentett erőforrást kinyeri.</span><span class="sxs-lookup"><span data-stu-id="da637-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="da637-111">2. példa: konkrét mentett keresés kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="da637-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="da637-112">Ez a parancs az azonosító alapján adott mentett keresést kap.</span><span class="sxs-lookup"><span data-stu-id="da637-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="da637-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da637-113">PARAMETERS</span></span>

### <span data-ttu-id="da637-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da637-114">-DefaultProfile</span></span>
<span data-ttu-id="da637-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="da637-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da637-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da637-116">-ResourceGroupName</span></span>
<span data-ttu-id="da637-117">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="da637-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="da637-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="da637-118">-SavedSearchId</span></span>
<span data-ttu-id="da637-119">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="da637-119">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="da637-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da637-120">-WorkspaceName</span></span>
<span data-ttu-id="da637-121">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="da637-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="da637-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da637-122">CommonParameters</span></span>
<span data-ttu-id="da637-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da637-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da637-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da637-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da637-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da637-125">INPUTS</span></span>

### <span data-ttu-id="da637-126">System. String</span><span class="sxs-lookup"><span data-stu-id="da637-126">System.String</span></span>

## <span data-ttu-id="da637-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da637-127">OUTPUTS</span></span>

### <span data-ttu-id="da637-128">Microsoft. Azure. Command. OperationalInsights. models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="da637-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="da637-129">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="da637-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="da637-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da637-130">NOTES</span></span>

## <span data-ttu-id="da637-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da637-131">RELATED LINKS</span></span>

[<span data-ttu-id="da637-132">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="da637-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

