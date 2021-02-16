---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162506"
---
# <span data-ttu-id="a2bbd-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a2bbd-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a2bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="a2bbd-103">Alkalmazásstatikációk csatolt tárfiók törlése</span><span class="sxs-lookup"><span data-stu-id="a2bbd-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="a2bbd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a2bbd-104">SYNTAX</span></span>

### <span data-ttu-id="a2bbd-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2bbd-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2bbd-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2bbd-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2bbd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2bbd-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2bbd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a2bbd-108">DESCRIPTION</span></span>
<span data-ttu-id="a2bbd-109">Alkalmazásstatikációk csatolt tárfiók törlése</span><span class="sxs-lookup"><span data-stu-id="a2bbd-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="a2bbd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a2bbd-110">EXAMPLES</span></span>

### <span data-ttu-id="a2bbd-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a2bbd-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="a2bbd-112">Az "componentName" application insights összetevővel társított csatolt tárfiók törlése</span><span class="sxs-lookup"><span data-stu-id="a2bbd-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="a2bbd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2bbd-113">PARAMETERS</span></span>

### <span data-ttu-id="a2bbd-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a2bbd-114">-ComponentName</span></span>
<span data-ttu-id="a2bbd-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="a2bbd-115">Component Name</span></span>

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

### <span data-ttu-id="a2bbd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2bbd-116">-DefaultProfile</span></span>
<span data-ttu-id="a2bbd-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2bbd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2bbd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2bbd-118">-InputObject</span></span>
<span data-ttu-id="a2bbd-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a2bbd-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a2bbd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2bbd-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2bbd-121">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="a2bbd-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a2bbd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2bbd-122">-ResourceId</span></span>
<span data-ttu-id="a2bbd-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2bbd-123">Component ResourceId</span></span>

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

### <span data-ttu-id="a2bbd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2bbd-124">-Confirm</span></span>
<span data-ttu-id="a2bbd-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a2bbd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2bbd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2bbd-126">-WhatIf</span></span>
<span data-ttu-id="a2bbd-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a2bbd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2bbd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a2bbd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2bbd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2bbd-129">CommonParameters</span></span>
<span data-ttu-id="a2bbd-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2bbd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2bbd-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2bbd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2bbd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2bbd-132">INPUTS</span></span>

### <span data-ttu-id="a2bbd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a2bbd-133">System.String</span></span>

### <span data-ttu-id="a2bbd-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a2bbd-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a2bbd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2bbd-135">OUTPUTS</span></span>

### <span data-ttu-id="a2bbd-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2bbd-136">System.Boolean</span></span>

## <span data-ttu-id="a2bbd-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a2bbd-137">NOTES</span></span>

## <span data-ttu-id="a2bbd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2bbd-138">RELATED LINKS</span></span>
