---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleObject.md
ms.openlocfilehash: 266d553f70cb5c128df1d266f95ee93cb1eb013c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469774"
---
# <span data-ttu-id="1bf15-101">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="1bf15-101">New-AzFrontDoorWafManagedRuleObject</span></span>

## <span data-ttu-id="1bf15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf15-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf15-103">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="1bf15-103">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1bf15-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1bf15-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleObject -Type <String> -Version <String>
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-Exclusion <PSManagedRuleExclusion[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf15-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1bf15-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf15-106">FelügyeltRule-objektum létrehozása a WAF-házirendek létrehozásához</span><span class="sxs-lookup"><span data-stu-id="1bf15-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="1bf15-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1bf15-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf15-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1bf15-108">Example 1</span></span>
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

<span data-ttu-id="1bf15-109">ManagedRule-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="1bf15-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="1bf15-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf15-110">PARAMETERS</span></span>

### <span data-ttu-id="1bf15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf15-111">-DefaultProfile</span></span>
<span data-ttu-id="1bf15-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1bf15-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf15-113">-Exclusion</span><span class="sxs-lookup"><span data-stu-id="1bf15-113">-Exclusion</span></span>
<span data-ttu-id="1bf15-114">Kivétel</span><span class="sxs-lookup"><span data-stu-id="1bf15-114">Exclusion</span></span>

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

### <span data-ttu-id="1bf15-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="1bf15-115">-RuleGroupOverride</span></span>
<span data-ttu-id="1bf15-116">Az Azure felügyelt szolgáltató felülbírálási konfigurációjának listája</span><span class="sxs-lookup"><span data-stu-id="1bf15-116">List of azure managed provider override configuration</span></span>

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

### <span data-ttu-id="1bf15-117">-Type</span><span class="sxs-lookup"><span data-stu-id="1bf15-117">-Type</span></span>
<span data-ttu-id="1bf15-118">A szabálykészlet típusa</span><span class="sxs-lookup"><span data-stu-id="1bf15-118">Type of the ruleset</span></span>

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

### <span data-ttu-id="1bf15-119">-Version</span><span class="sxs-lookup"><span data-stu-id="1bf15-119">-Version</span></span>
<span data-ttu-id="1bf15-120">A szabálykészlet verziója</span><span class="sxs-lookup"><span data-stu-id="1bf15-120">Version of the ruleset</span></span>

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

### <span data-ttu-id="1bf15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf15-121">CommonParameters</span></span>
<span data-ttu-id="1bf15-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf15-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bf15-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf15-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf15-124">INPUTS</span></span>

### <span data-ttu-id="1bf15-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="1bf15-125">None</span></span>

## <span data-ttu-id="1bf15-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1bf15-126">OUTPUTS</span></span>

### <span data-ttu-id="1bf15-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="1bf15-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="1bf15-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1bf15-128">NOTES</span></span>

## <span data-ttu-id="1bf15-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1bf15-129">RELATED LINKS</span></span>

<span data-ttu-id="1bf15-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="1bf15-130">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)</span></span>
