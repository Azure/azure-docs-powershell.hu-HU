---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 4daf2a86515522c3843d5d0225c133f0ff3686ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500792"
---
# <span data-ttu-id="05da7-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="05da7-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="05da7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05da7-102">SYNOPSIS</span></span>
<span data-ttu-id="05da7-103">A megadott munkaterület összes mentett keresését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="05da7-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05da7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05da7-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05da7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05da7-105">DESCRIPTION</span></span>
<span data-ttu-id="05da7-106">A **Get-AzureRmOperationalInsightsSavedSearch** parancsmag megadott munkaterület összes mentett keresését visszaadja az erőforráscsoport számára, ha nem ad meg mentett keresési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="05da7-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="05da7-107">Ha megadhatja a mentett keresési azonosítót, a program az AZONOSÍTÓnak megfelelő mentett keresést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="05da7-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="05da7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="05da7-108">EXAMPLES</span></span>

### <span data-ttu-id="05da7-109">Példa 1: az összes mentett keresés beolvasása egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="05da7-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="05da7-110">Ez a parancs a munkaterülethez társított összes mentett erőforrást kinyeri.</span><span class="sxs-lookup"><span data-stu-id="05da7-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="05da7-111">2. példa: konkrét mentett keresés kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="05da7-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="05da7-112">Ez a parancs az azonosító alapján adott mentett keresést kap.</span><span class="sxs-lookup"><span data-stu-id="05da7-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="05da7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05da7-113">PARAMETERS</span></span>

### <span data-ttu-id="05da7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05da7-114">-ResourceGroupName</span></span>
<span data-ttu-id="05da7-115">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="05da7-115">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="05da7-116">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="05da7-116">-SavedSearchId</span></span>
<span data-ttu-id="05da7-117">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="05da7-117">Specifies a saved search ID.</span></span>

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

### <span data-ttu-id="05da7-118">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05da7-118">-WorkspaceName</span></span>
<span data-ttu-id="05da7-119">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05da7-119">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="05da7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05da7-120">-DefaultProfile</span></span>
<span data-ttu-id="05da7-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05da7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05da7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05da7-122">CommonParameters</span></span>
<span data-ttu-id="05da7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05da7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05da7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05da7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05da7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05da7-125">INPUTS</span></span>

## <span data-ttu-id="05da7-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05da7-126">OUTPUTS</span></span>

### <span data-ttu-id="05da7-127">Microsoft. Azure. Command. OperationalInsights. models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="05da7-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="05da7-128">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="05da7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="05da7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05da7-129">NOTES</span></span>

## <span data-ttu-id="05da7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05da7-130">RELATED LINKS</span></span>

[<span data-ttu-id="05da7-131">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="05da7-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


