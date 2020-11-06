---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494426"
---
# <span data-ttu-id="55ccd-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="55ccd-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="55ccd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="55ccd-103">A megadott munkaterület összes mentett keresését adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="55ccd-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55ccd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55ccd-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ccd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55ccd-105">DESCRIPTION</span></span>
<span data-ttu-id="55ccd-106">A **Get-AzureRmOperationalInsightsSavedSearch** parancsmag megadott munkaterület összes mentett keresését visszaadja az erőforráscsoport számára, ha nem ad meg mentett keresési azonosítót.</span><span class="sxs-lookup"><span data-stu-id="55ccd-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="55ccd-107">Ha megadhatja a mentett keresési azonosítót, a program az AZONOSÍTÓnak megfelelő mentett keresést adja vissza.</span><span class="sxs-lookup"><span data-stu-id="55ccd-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="55ccd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="55ccd-108">EXAMPLES</span></span>

### <span data-ttu-id="55ccd-109">Példa 1: az összes mentett keresés beolvasása egy munkaterületre</span><span class="sxs-lookup"><span data-stu-id="55ccd-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="55ccd-110">Ez a parancs a munkaterülethez társított összes mentett erőforrást kinyeri.</span><span class="sxs-lookup"><span data-stu-id="55ccd-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="55ccd-111">2. példa: konkrét mentett keresés kérése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="55ccd-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="55ccd-112">Ez a parancs az azonosító alapján adott mentett keresést kap.</span><span class="sxs-lookup"><span data-stu-id="55ccd-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="55ccd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55ccd-113">PARAMETERS</span></span>

### <span data-ttu-id="55ccd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ccd-114">-DefaultProfile</span></span>
<span data-ttu-id="55ccd-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="55ccd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55ccd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ccd-116">-ResourceGroupName</span></span>
<span data-ttu-id="55ccd-117">Egy olyan Azure-erőforráscsoport nevét adja meg, amely egy munkaterületet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="55ccd-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="55ccd-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="55ccd-118">-SavedSearchId</span></span>
<span data-ttu-id="55ccd-119">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="55ccd-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ccd-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="55ccd-120">-WorkspaceName</span></span>
<span data-ttu-id="55ccd-121">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55ccd-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="55ccd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ccd-122">CommonParameters</span></span>
<span data-ttu-id="55ccd-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55ccd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ccd-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55ccd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ccd-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55ccd-125">INPUTS</span></span>

### <span data-ttu-id="55ccd-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="55ccd-126">None</span></span>
<span data-ttu-id="55ccd-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="55ccd-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55ccd-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55ccd-128">OUTPUTS</span></span>

### <span data-ttu-id="55ccd-129">Microsoft. Azure. Command. OperationalInsights. models. PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="55ccd-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="55ccd-130">Microsoft. Azure. Command. OperationalInsights. models. PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="55ccd-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="55ccd-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55ccd-131">NOTES</span></span>

## <span data-ttu-id="55ccd-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55ccd-132">RELATED LINKS</span></span>

[<span data-ttu-id="55ccd-133">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="55ccd-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


