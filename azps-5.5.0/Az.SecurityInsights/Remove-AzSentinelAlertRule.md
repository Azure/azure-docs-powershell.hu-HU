---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRule.md
ms.openlocfilehash: 415a4156831d00672aba5709d3f915625adac106
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168946"
---
# <span data-ttu-id="d685f-101">Remove-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d685f-101">Remove-AzSentinelAlertRule</span></span>

## <span data-ttu-id="d685f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d685f-102">SYNOPSIS</span></span>
<span data-ttu-id="d685f-103">Analytic törlése</span><span class="sxs-lookup"><span data-stu-id="d685f-103">Delete an Analytic.</span></span>

## <span data-ttu-id="d685f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d685f-104">SYNTAX</span></span>

### <span data-ttu-id="d685f-105">AlertRuleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d685f-105">AlertRuleId (Default)</span></span>
```
Remove-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d685f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d685f-106">InputObject</span></span>
```
Remove-AzSentinelAlertRule -InputObject <PSSentinelAlertRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d685f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d685f-107">DESCRIPTION</span></span>
<span data-ttu-id="d685f-108">A **Remove-AzSentinelAlertRule** parancsmag véglegesen töröl egy riasztási szabályt egy adott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d685f-108">The **Remove-AzSentinelAlertRule** cmdlet permanently deletes an Alert Rule from a specified workspace.</span></span>
<span data-ttu-id="d685f-109">A **AlertRule-objektumokat** átadhatja a folyamat műveleti jelével, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="d685f-109">You can pass an **AlertRule** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d685f-110">A Confirm paraméter és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="d685f-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d685f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d685f-111">EXAMPLES</span></span>

### <span data-ttu-id="d685f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="d685f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="d685f-113">Ez a parancs eltávolítja a riasztási szabályt a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="d685f-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="d685f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d685f-114">PARAMETERS</span></span>

### <span data-ttu-id="d685f-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d685f-115">-AlertRuleId</span></span>
<span data-ttu-id="d685f-116">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d685f-116">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d685f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d685f-117">-DefaultProfile</span></span>
<span data-ttu-id="d685f-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d685f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d685f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d685f-119">-InputObject</span></span>
<span data-ttu-id="d685f-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="d685f-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d685f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d685f-121">-PassThru</span></span>
<span data-ttu-id="d685f-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="d685f-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d685f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d685f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d685f-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d685f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d685f-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d685f-125">-WorkspaceName</span></span>
<span data-ttu-id="d685f-126">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="d685f-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d685f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d685f-127">-Confirm</span></span>
<span data-ttu-id="d685f-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d685f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d685f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d685f-129">-WhatIf</span></span>
<span data-ttu-id="d685f-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d685f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d685f-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d685f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d685f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d685f-132">CommonParameters</span></span>
<span data-ttu-id="d685f-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d685f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d685f-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d685f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d685f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d685f-135">INPUTS</span></span>

### <span data-ttu-id="d685f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d685f-136">System.String</span></span>
### <span data-ttu-id="d685f-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d685f-137">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="d685f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d685f-138">OUTPUTS</span></span>

### <span data-ttu-id="d685f-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="d685f-139">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="d685f-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d685f-140">NOTES</span></span>

## <span data-ttu-id="d685f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d685f-141">RELATED LINKS</span></span>
