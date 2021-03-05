---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 5d8e872ea2ca47169c727a29c1847a83b5a6542b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015285"
---
# <span data-ttu-id="1132b-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="1132b-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="1132b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1132b-102">SYNOPSIS</span></span>
<span data-ttu-id="1132b-103">RuleGroupOverride objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="1132b-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1132b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1132b-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1132b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1132b-105">DESCRIPTION</span></span>
<span data-ttu-id="1132b-106">RuleGroupOverride objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="1132b-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="1132b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1132b-107">EXAMPLES</span></span>

### <span data-ttu-id="1132b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1132b-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="1132b-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="1132b-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="1132b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1132b-110">PARAMETERS</span></span>

### <span data-ttu-id="1132b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1132b-111">-DefaultProfile</span></span>
<span data-ttu-id="1132b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1132b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1132b-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="1132b-113">-Exclusion</span></span>
<span data-ttu-id="1132b-114">Kivétel</span><span class="sxs-lookup"><span data-stu-id="1132b-114">Exclusion</span></span>

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

### <span data-ttu-id="1132b-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="1132b-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="1132b-116">Szabály felülbírálási listája</span><span class="sxs-lookup"><span data-stu-id="1132b-116">Rule override list</span></span>

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

### <span data-ttu-id="1132b-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="1132b-117">-RuleGroupName</span></span>
<span data-ttu-id="1132b-118">Szabálycsoport neve, amelyre ezek a felülbírálások vonatkoznak</span><span class="sxs-lookup"><span data-stu-id="1132b-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="1132b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1132b-119">CommonParameters</span></span>
<span data-ttu-id="1132b-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1132b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1132b-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1132b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1132b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1132b-122">INPUTS</span></span>

### <span data-ttu-id="1132b-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="1132b-123">None</span></span>

## <span data-ttu-id="1132b-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1132b-124">OUTPUTS</span></span>

### <span data-ttu-id="1132b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1132b-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="1132b-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1132b-126">NOTES</span></span>

## <span data-ttu-id="1132b-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1132b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1132b-128">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1132b-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
