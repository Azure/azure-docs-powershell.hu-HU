---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: f31b7c995c66e2b187038c45d9955a31f904764b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928050"
---
# <span data-ttu-id="d4d3f-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="d4d3f-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="d4d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d3f-103">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d4d3f-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d4d3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d4d3f-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d3f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d4d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d3f-106">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="d4d3f-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="d4d3f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d4d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="d4d3f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d4d3f-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log
PS C:\> $ruleOverride2 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942251" -Action Log
PS C:\> $override1 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

PS C:\> $ruleOverride3 = New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "941280" -Action Log
PS C:\> $override2 = New-AzFrontDoorWafRuleGroupOverrideObject -RuleGroupName XSS -ManagedRuleOverride $ruleOverride3

PS C:\> New-AzFrontDoorWafManagedRuleObject -Type DefaultRuleSet -Version "preview-0.1" -RuleGroupOverride $override1,$override2

RuleGroupOverrides RuleSetType    RuleSetVersion
------------------ -----------    --------------
{SQLI, XSS}        DefaultRuleSet preview-0.1
```

<span data-ttu-id="d4d3f-109">ManagedRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="d4d3f-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="d4d3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="d4d3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d3f-111">-DefaultProfile</span></span>
<span data-ttu-id="d4d3f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4d3f-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="d4d3f-113">-Exclusion</span></span>
<span data-ttu-id="d4d3f-114">Kivétel</span><span class="sxs-lookup"><span data-stu-id="d4d3f-114">Exclusion</span></span>

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

### <span data-ttu-id="d4d3f-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="d4d3f-115">-RuleGroupOverride</span></span>
<span data-ttu-id="d4d3f-116">Az Azure felügyelt szolgáltató felülbírálási konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="d4d3f-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="d4d3f-117">-Type</span><span class="sxs-lookup"><span data-stu-id="d4d3f-117">-Type</span></span>
<span data-ttu-id="d4d3f-118">A szabálykészlet típusa</span><span class="sxs-lookup"><span data-stu-id="d4d3f-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="d4d3f-119">-Version</span><span class="sxs-lookup"><span data-stu-id="d4d3f-119">-Version</span></span>
<span data-ttu-id="d4d3f-120">A szabálykészlet verziója</span><span class="sxs-lookup"><span data-stu-id="d4d3f-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="d4d3f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d3f-121">CommonParameters</span></span>
<span data-ttu-id="d4d3f-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d3f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d3f-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4d3f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d3f-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4d3f-124">INPUTS</span></span>

### <span data-ttu-id="d4d3f-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="d4d3f-125">None</span></span>

## <span data-ttu-id="d4d3f-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4d3f-126">OUTPUTS</span></span>

### <span data-ttu-id="d4d3f-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="d4d3f-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="d4d3f-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d4d3f-128">NOTES</span></span>

## <span data-ttu-id="d4d3f-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4d3f-129">RELATED LINKS</span></span>

<span data-ttu-id="d4d3f-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="d4d3f-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
