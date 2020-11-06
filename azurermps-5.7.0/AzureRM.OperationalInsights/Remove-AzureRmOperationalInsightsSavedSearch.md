---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: e66ca332d2fd59faa64e4360d00af714cfa28475
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492254"
---
# <span data-ttu-id="025e1-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="025e1-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="025e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="025e1-102">SYNOPSIS</span></span>
<span data-ttu-id="025e1-103">Mentett keresés eltávolítása a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="025e1-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="025e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="025e1-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025e1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="025e1-105">DESCRIPTION</span></span>
<span data-ttu-id="025e1-106">A **Remove-AzureRmOperationalInsightsSavedSearch** parancsmag eltávolítja a mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="025e1-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="025e1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="025e1-107">EXAMPLES</span></span>

### <span data-ttu-id="025e1-108">1. példa: mentett keresés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="025e1-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="025e1-109">Ez a parancs eltávolítja a mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="025e1-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="025e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="025e1-110">PARAMETERS</span></span>

### <span data-ttu-id="025e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025e1-111">-DefaultProfile</span></span>
<span data-ttu-id="025e1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="025e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="025e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="025e1-114">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="025e1-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="025e1-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="025e1-115">-SavedSearchId</span></span>
<span data-ttu-id="025e1-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="025e1-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="025e1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="025e1-117">-WorkspaceName</span></span>
<span data-ttu-id="025e1-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="025e1-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="025e1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="025e1-119">-Confirm</span></span>
<span data-ttu-id="025e1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="025e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025e1-121">-WhatIf</span></span>
<span data-ttu-id="025e1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="025e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025e1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="025e1-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025e1-124">CommonParameters</span></span>
<span data-ttu-id="025e1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="025e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025e1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025e1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025e1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="025e1-127">INPUTS</span></span>

### <span data-ttu-id="025e1-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="025e1-128">None</span></span>
<span data-ttu-id="025e1-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="025e1-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="025e1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="025e1-130">OUTPUTS</span></span>

## <span data-ttu-id="025e1-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="025e1-131">NOTES</span></span>

## <span data-ttu-id="025e1-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="025e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="025e1-133">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="025e1-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


