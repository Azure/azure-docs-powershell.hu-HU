---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 7c9ace339da9639404072fd802782aee43d8ab37
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183572"
---
# <span data-ttu-id="36fb6-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="36fb6-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="36fb6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="36fb6-103">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="36fb6-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="36fb6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36fb6-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36fb6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="36fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="36fb6-106">ManagedRule objektum létrehozása a WAF házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="36fb6-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="36fb6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="36fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="36fb6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="36fb6-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log -EnabledState Enabled
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="36fb6-109">ManagedRule objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="36fb6-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="36fb6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36fb6-110">PARAMETERS</span></span>

### <span data-ttu-id="36fb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fb6-111">-DefaultProfile</span></span>
<span data-ttu-id="36fb6-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36fb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36fb6-113">– Kizárás</span><span class="sxs-lookup"><span data-stu-id="36fb6-113">-Exclusion</span></span>
<span data-ttu-id="36fb6-114">Kirekesztés</span><span class="sxs-lookup"><span data-stu-id="36fb6-114">Exclusion</span></span>

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

### <span data-ttu-id="36fb6-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="36fb6-115">-RuleGroupOverride</span></span>
<span data-ttu-id="36fb6-116">Az Azure felügyelt szolgáltatóinak listája felülbírálja a konfigurációt</span><span class="sxs-lookup"><span data-stu-id="36fb6-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fb6-117">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="36fb6-117">-Type</span></span>
<span data-ttu-id="36fb6-118">A szabályrendszert típusa</span><span class="sxs-lookup"><span data-stu-id="36fb6-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="36fb6-119">-Verzió</span><span class="sxs-lookup"><span data-stu-id="36fb6-119">-Version</span></span>
<span data-ttu-id="36fb6-120">A szabály verziószáma</span><span class="sxs-lookup"><span data-stu-id="36fb6-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="36fb6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fb6-121">CommonParameters</span></span>
<span data-ttu-id="36fb6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36fb6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fb6-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="36fb6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fb6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36fb6-124">INPUTS</span></span>

### <span data-ttu-id="36fb6-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="36fb6-125">None</span></span>

## <span data-ttu-id="36fb6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36fb6-126">OUTPUTS</span></span>

### <span data-ttu-id="36fb6-127">Microsoft. Azure. Command. FrontDoor. models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="36fb6-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="36fb6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36fb6-128">NOTES</span></span>

## <span data-ttu-id="36fb6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36fb6-129">RELATED LINKS</span></span>

<span data-ttu-id="36fb6-130">[Új – AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Új – AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="36fb6-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
