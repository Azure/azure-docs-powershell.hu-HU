---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163531"
---
# <span data-ttu-id="e5c12-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="e5c12-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="e5c12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c12-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c12-103">RuleGroupOverride objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="e5c12-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="e5c12-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5c12-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c12-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5c12-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c12-106">RuleGroupOverride objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="e5c12-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="e5c12-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5c12-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c12-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="e5c12-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="e5c12-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="e5c12-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="e5c12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c12-110">PARAMETERS</span></span>

### <span data-ttu-id="e5c12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c12-111">-DefaultProfile</span></span>
<span data-ttu-id="e5c12-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5c12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c12-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="e5c12-113">-Exclusion</span></span>
<span data-ttu-id="e5c12-114">Kivétel</span><span class="sxs-lookup"><span data-stu-id="e5c12-114">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c12-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="e5c12-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="e5c12-116">Szabály felülbírálási listája</span><span class="sxs-lookup"><span data-stu-id="e5c12-116">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c12-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c12-117">-RuleGroupName</span></span>
<span data-ttu-id="e5c12-118">Szabálycsoport neve, amelyre ezek a felülbírálások vonatkoznak</span><span class="sxs-lookup"><span data-stu-id="e5c12-118">Rule Group Name for which these overrides apply</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c12-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c12-119">CommonParameters</span></span>
<span data-ttu-id="e5c12-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c12-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c12-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5c12-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c12-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5c12-122">INPUTS</span></span>

### <span data-ttu-id="e5c12-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e5c12-123">None</span></span>

## <span data-ttu-id="e5c12-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5c12-124">OUTPUTS</span></span>

### <span data-ttu-id="e5c12-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="e5c12-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="e5c12-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5c12-126">NOTES</span></span>

## <span data-ttu-id="e5c12-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5c12-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5c12-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="e5c12-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
