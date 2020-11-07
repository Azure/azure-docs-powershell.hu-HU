---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836133"
---
# <span data-ttu-id="98c52-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="98c52-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="98c52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="98c52-102">SYNOPSIS</span></span>
<span data-ttu-id="98c52-103">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="98c52-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="98c52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="98c52-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98c52-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="98c52-105">DESCRIPTION</span></span>
<span data-ttu-id="98c52-106">RuleGroupOverride objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="98c52-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="98c52-107">Példák</span><span class="sxs-lookup"><span data-stu-id="98c52-107">EXAMPLES</span></span>

### <span data-ttu-id="98c52-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="98c52-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="98c52-109">RuleGroupOverride objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="98c52-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="98c52-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="98c52-110">PARAMETERS</span></span>

### <span data-ttu-id="98c52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c52-111">-DefaultProfile</span></span>
<span data-ttu-id="98c52-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98c52-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c52-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="98c52-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="98c52-114">Szabály-felülírási lista</span><span class="sxs-lookup"><span data-stu-id="98c52-114">Rule override list</span></span>

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

### <span data-ttu-id="98c52-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="98c52-115">-RuleGroupName</span></span>
<span data-ttu-id="98c52-116">A szabály csoportjának neve, amelyre ezek a felülírások érvényesek</span><span class="sxs-lookup"><span data-stu-id="98c52-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="98c52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c52-117">CommonParameters</span></span>
<span data-ttu-id="98c52-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="98c52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c52-119">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="98c52-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c52-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="98c52-120">INPUTS</span></span>

### <span data-ttu-id="98c52-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="98c52-121">None</span></span>

## <span data-ttu-id="98c52-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98c52-122">OUTPUTS</span></span>

### <span data-ttu-id="98c52-123">Microsoft. Azure. Command. FrontDoor. models. PSAzureRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="98c52-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="98c52-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="98c52-124">NOTES</span></span>

## <span data-ttu-id="98c52-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98c52-125">RELATED LINKS</span></span>

[<span data-ttu-id="98c52-126">Új – AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="98c52-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
