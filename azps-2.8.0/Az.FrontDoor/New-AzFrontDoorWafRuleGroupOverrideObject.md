---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafRuleGroupOverrideObject.md
ms.openlocfilehash: c55be8e72e3c5bb5418d3be4b74555eb20168113
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666405"
---
# <span data-ttu-id="32b55-101">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="32b55-101">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>

## <span data-ttu-id="32b55-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32b55-102">SYNOPSIS</span></span>
<span data-ttu-id="32b55-103">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="32b55-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="32b55-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32b55-104">SYNTAX</span></span>

```
New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32b55-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32b55-105">DESCRIPTION</span></span>
<span data-ttu-id="32b55-106">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="32b55-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="32b55-107">Példák</span><span class="sxs-lookup"><span data-stu-id="32b55-107">EXAMPLES</span></span>

### <span data-ttu-id="32b55-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="32b55-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="32b55-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="32b55-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="32b55-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32b55-110">PARAMETERS</span></span>

### <span data-ttu-id="32b55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b55-111">-DefaultProfile</span></span>
<span data-ttu-id="32b55-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32b55-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b55-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="32b55-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="32b55-114">Szabály-felülírási lista</span><span class="sxs-lookup"><span data-stu-id="32b55-114">Rule override list</span></span>

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

### <span data-ttu-id="32b55-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="32b55-115">-RuleGroupName</span></span>
<span data-ttu-id="32b55-116">A szabály csoportjának neve, amelyre ezek a felülírások érvényesek</span><span class="sxs-lookup"><span data-stu-id="32b55-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="32b55-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b55-117">CommonParameters</span></span>
<span data-ttu-id="32b55-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32b55-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b55-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="32b55-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b55-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32b55-120">INPUTS</span></span>

### <span data-ttu-id="32b55-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="32b55-121">None</span></span>

## <span data-ttu-id="32b55-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32b55-122">OUTPUTS</span></span>

### <span data-ttu-id="32b55-123">Microsoft. Azure. Command. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="32b55-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="32b55-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32b55-124">NOTES</span></span>

## <span data-ttu-id="32b55-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32b55-125">RELATED LINKS</span></span>

[<span data-ttu-id="32b55-126">Új – AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="32b55-126">New-AzFrontDoorWafManagedRuleObject</span></span>](./New-AzFrontDoorWafManagedRuleObject.md)
