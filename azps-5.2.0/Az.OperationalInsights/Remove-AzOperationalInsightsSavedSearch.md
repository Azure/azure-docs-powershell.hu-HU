---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337590"
---
# <span data-ttu-id="0341a-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="0341a-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="0341a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0341a-102">SYNOPSIS</span></span>
<span data-ttu-id="0341a-103">Eltávolít egy mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="0341a-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0341a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0341a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0341a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0341a-105">DESCRIPTION</span></span>
<span data-ttu-id="0341a-106">A **Remove-AzOperationalInsightsSavedSearch** parancsmag eltávolít egy mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="0341a-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0341a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0341a-107">EXAMPLES</span></span>

### <span data-ttu-id="0341a-108">1. példa: Mentett keresés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0341a-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="0341a-109">Ez a parancs eltávolítja a mentett keresést a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="0341a-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="0341a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0341a-110">PARAMETERS</span></span>

### <span data-ttu-id="0341a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0341a-111">-DefaultProfile</span></span>
<span data-ttu-id="0341a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0341a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0341a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0341a-113">-ResourceGroupName</span></span>
<span data-ttu-id="0341a-114">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0341a-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0341a-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="0341a-115">-SavedSearchId</span></span>
<span data-ttu-id="0341a-116">A mentett keresési azonosítót adja meg.</span><span class="sxs-lookup"><span data-stu-id="0341a-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="0341a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0341a-117">-WorkspaceName</span></span>
<span data-ttu-id="0341a-118">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0341a-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0341a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0341a-119">-Confirm</span></span>
<span data-ttu-id="0341a-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0341a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0341a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0341a-121">-WhatIf</span></span>
<span data-ttu-id="0341a-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0341a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0341a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0341a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0341a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0341a-124">CommonParameters</span></span>
<span data-ttu-id="0341a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0341a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0341a-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0341a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0341a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0341a-127">INPUTS</span></span>

### <span data-ttu-id="0341a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0341a-128">System.String</span></span>

## <span data-ttu-id="0341a-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0341a-129">OUTPUTS</span></span>

### <span data-ttu-id="0341a-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0341a-130">System.Void</span></span>

## <span data-ttu-id="0341a-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0341a-131">NOTES</span></span>

## <span data-ttu-id="0341a-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0341a-132">RELATED LINKS</span></span>

[<span data-ttu-id="0341a-133">Azure Operational Insights-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="0341a-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


