---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195429"
---
# <span data-ttu-id="ccdf6-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ccdf6-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="ccdf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccdf6-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdf6-103">A törölt alkalmazások törlése hivatkozással</span><span class="sxs-lookup"><span data-stu-id="ccdf6-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="ccdf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccdf6-104">SYNTAX</span></span>

### <span data-ttu-id="ccdf6-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ccdf6-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdf6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccdf6-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdf6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccdf6-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdf6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccdf6-108">DESCRIPTION</span></span>
<span data-ttu-id="ccdf6-109">A törölt alkalmazások törlése hivatkozással</span><span class="sxs-lookup"><span data-stu-id="ccdf6-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="ccdf6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ccdf6-110">EXAMPLES</span></span>

### <span data-ttu-id="ccdf6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccdf6-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="ccdf6-112">Az alkalmazás-betekintéshez társított kapcsolódó tárolási fiók törlése "componentName"</span><span class="sxs-lookup"><span data-stu-id="ccdf6-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="ccdf6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccdf6-113">PARAMETERS</span></span>

### <span data-ttu-id="ccdf6-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="ccdf6-114">-ComponentName</span></span>
<span data-ttu-id="ccdf6-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="ccdf6-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdf6-116">-DefaultProfile</span></span>
<span data-ttu-id="ccdf6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccdf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccdf6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccdf6-118">-InputObject</span></span>
<span data-ttu-id="ccdf6-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ccdf6-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdf6-120">-ResourceGroupName</span></span>
<span data-ttu-id="ccdf6-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ccdf6-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccdf6-122">-ResourceId</span></span>
<span data-ttu-id="ccdf6-123">Összetevő-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccdf6-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccdf6-124">-Confirm</span></span>
<span data-ttu-id="ccdf6-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccdf6-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdf6-126">-WhatIf</span></span>
<span data-ttu-id="ccdf6-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccdf6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdf6-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccdf6-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdf6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdf6-129">CommonParameters</span></span>
<span data-ttu-id="ccdf6-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccdf6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdf6-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ccdf6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdf6-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccdf6-132">INPUTS</span></span>

### <span data-ttu-id="ccdf6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ccdf6-133">System.String</span></span>

### <span data-ttu-id="ccdf6-134">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="ccdf6-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="ccdf6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccdf6-135">OUTPUTS</span></span>

### <span data-ttu-id="ccdf6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ccdf6-136">System.Boolean</span></span>

## <span data-ttu-id="ccdf6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccdf6-137">NOTES</span></span>

## <span data-ttu-id="ccdf6-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccdf6-138">RELATED LINKS</span></span>
