---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: 9d05502b518dcd10a22c9583546a2d010b424902
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94023982"
---
# <span data-ttu-id="c61d4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="c61d4-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="c61d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c61d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c61d4-103">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="c61d4-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c61d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c61d4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c61d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c61d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c61d4-106">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="c61d4-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="c61d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c61d4-107">EXAMPLES</span></span>

### <span data-ttu-id="c61d4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c61d4-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="c61d4-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="c61d4-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="c61d4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c61d4-110">PARAMETERS</span></span>

### <span data-ttu-id="c61d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61d4-111">-DefaultProfile</span></span>
<span data-ttu-id="c61d4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c61d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61d4-113">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="c61d4-113">-Exclusion</span></span>
<span data-ttu-id="c61d4-114">Kirekesztés</span><span class="sxs-lookup"><span data-stu-id="c61d4-114">Exclusion</span></span>

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

### <span data-ttu-id="c61d4-115">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="c61d4-115">-ManagedRuleOverride</span></span>
<span data-ttu-id="c61d4-116">Szabály-felülírási lista</span><span class="sxs-lookup"><span data-stu-id="c61d4-116">Rule override list</span></span>

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

### <span data-ttu-id="c61d4-117">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="c61d4-117">-RuleGroupName</span></span>
<span data-ttu-id="c61d4-118">A szabály csoportjának neve, amelyre ezek a felülírások érvényesek</span><span class="sxs-lookup"><span data-stu-id="c61d4-118">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="c61d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61d4-119">CommonParameters</span></span>
<span data-ttu-id="c61d4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c61d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61d4-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c61d4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61d4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c61d4-122">INPUTS</span></span>

### <span data-ttu-id="c61d4-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c61d4-123">None</span></span>

## <span data-ttu-id="c61d4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c61d4-124">OUTPUTS</span></span>

### <span data-ttu-id="c61d4-125">Microsoft. Azure. Command. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="c61d4-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="c61d4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c61d4-126">NOTES</span></span>

## <span data-ttu-id="c61d4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c61d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="c61d4-128">Új – AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="c61d4-128">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
