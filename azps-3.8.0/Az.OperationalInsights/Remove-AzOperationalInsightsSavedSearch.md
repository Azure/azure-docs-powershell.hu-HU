---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 931c85b649393d33f03e778d0e34cf6644e4c2d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94017289"
---
# <span data-ttu-id="fb3f4-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="fb3f4-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="fb3f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3f4-103">Mentett keresés eltávolítása a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="fb3f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb3f4-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3f4-106">A **Remove-AzOperationalInsightsSavedSearch** parancsmag eltávolítja a mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="fb3f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fb3f4-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3f4-108">1. példa: mentett keresés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="fb3f4-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="fb3f4-109">Ez a parancs eltávolítja a mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="fb3f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb3f4-110">PARAMETERS</span></span>

### <span data-ttu-id="fb3f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3f4-111">-DefaultProfile</span></span>
<span data-ttu-id="fb3f4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb3f4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb3f4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb3f4-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb3f4-114">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fb3f4-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="fb3f4-115">-SavedSearchId</span></span>
<span data-ttu-id="fb3f4-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="fb3f4-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb3f4-117">-WorkspaceName</span></span>
<span data-ttu-id="fb3f4-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="fb3f4-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb3f4-119">-Confirm</span></span>
<span data-ttu-id="fb3f4-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3f4-121">-WhatIf</span></span>
<span data-ttu-id="fb3f4-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3f4-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb3f4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3f4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3f4-124">CommonParameters</span></span>
<span data-ttu-id="fb3f4-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb3f4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3f4-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3f4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3f4-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb3f4-127">INPUTS</span></span>

### <span data-ttu-id="fb3f4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fb3f4-128">System.String</span></span>

## <span data-ttu-id="fb3f4-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb3f4-129">OUTPUTS</span></span>

### <span data-ttu-id="fb3f4-130">System. Void</span><span class="sxs-lookup"><span data-stu-id="fb3f4-130">System.Void</span></span>

## <span data-ttu-id="fb3f4-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb3f4-131">NOTES</span></span>

## <span data-ttu-id="fb3f4-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb3f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb3f4-133">Azure hadműveleti parancsmagok</span><span class="sxs-lookup"><span data-stu-id="fb3f4-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


